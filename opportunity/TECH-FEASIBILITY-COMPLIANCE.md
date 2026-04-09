# Holi — Faisabilité technique & conformité (TASK-133)

Date: 2026-04-09  
Owner: Isaak  
Scope: collaboration temps réel, géoloc continue, intégrations messagerie, V2 email agent

## 1) Verdict exécutif (concis)

**Verdict:** faisable en V1.5/V2 avec un **niveau de risque maîtrisable** si on impose une architecture modulaire et une conformité “privacy-by-default”.

- **Collaboration temps réel:** faisable immédiatement (WebSocket / Realtime managé) avec faible risque technique. (C-124, C-125)
- **Géoloc continue:** faisable mais **fortement contrainte** (OS permissions + justification produit + coût batterie + RGPD). À garder optionnelle et strictement bornée en V1. (C-126, C-127, C-128, C-129)
- **Messagerie (Telegram/WhatsApp):** faisable en notifications/action loops, mais dépend des limites de plateforme et d’une stratégie d’opt-in. (C-130, C-131)
- **Email agent V2:** faisable rapidement, mais conformité opt-out/consentement et gouvernance de contenu obligatoires. (C-132, C-133)

**Décision proposée pour TASK-134/135:**
1. Garder collaboration temps réel dans le cœur V1.
2. Traiter géoloc continue comme capability progressive (opt-in explicite + mode voyage uniquement).
3. Lancer intégration Telegram d’abord, WhatsApp en second (complexité opérationnelle plus élevée).
4. Positionner email agent en “digest/alerts utiles” et jamais en push marketing agressif.

---

## 2) Faisabilité technique par module

## 2.1 Collaboration temps réel (swipe + consensus)

### Faisabilité
Élevée. Un backend temps réel managé (ex: Supabase Realtime / Firestore listeners) couvre nativement présence, événements bas-latence, sync d’état. (C-124, C-125)

### Architecture cible (V1)
- **Client mobile/web:** états locaux + events idempotents.
- **Backend API:** auth, règles métier (groupes, votes, conflits), rate limiting.
- **Realtime channel:** diffusion events de session (swipes, consensus, conflits).
- **Store persistant:** sessions, items, votes, décisions.

### Risques
- collisions d’édition et ordre des events,
- coûts si fan-out élevé,
- dérive de schéma si on mélange events et snapshots.

### Garde-fous
- event versioning + optimistic concurrency,
- snapshots périodiques + event log court,
- KPIs: latence p95, taux de conflits non résolus, taux de convergence groupe.

---

## 2.2 Géolocalisation continue (mode voyage)

### Faisabilité
Moyenne (pas bloquante, mais sensible). Les contraintes viennent plus de la gouvernance OS/policy + privacy que du code pur.

### Contraintes principales
- **Android (Play):** accès en arrière-plan accepté seulement si indispensable à la fonctionnalité cœur et bien documenté. (C-127)
- **iOS:** permissions explicites et messaging usage clair via clés de description de localisation. (C-126)
- **Protection données:** minimisation, limitation de finalité, rétention courte, retrait consentement simple. (C-128, C-129)

### Recommandation produit
- pas de tracking continu “always-on” en V1,
- activer seulement en **Travel Mode**, sur fenêtres temporelles explicites,
- granularité basse par défaut (zone/cluster), précision fine uniquement si bénéfice utilisateur direct,
- bouton “pause location” et expiration auto (ex: fin de journée).

### Risques
- rejet policy store,
- rejet utilisateur (surveillance perçue),
- coût batterie,
- exposition juridique si finalité mal cadrée.

### Garde-fous
- DPIA-lite interne avant release,
- data retention courte (ex: 24h raw, puis agrégé/anonymisé),
- journal d’audit consentement/retrait,
- mode dégradé sans géoloc continue (fallback géoloc ponctuelle).

---

## 2.3 Intégrations messagerie (Telegram / WhatsApp)

### Faisabilité
Bonne pour “assist notifications + actions rapides” (rappels, conflit groupe, changement météo/fermeture, checklists).

### Telegram
- API bot mature, HTTP, rapide à intégrer. (C-130)
- Bon candidat pour V1.5: coûts/friction faibles.

### WhatsApp
- Faisable via fournisseur (ex: Twilio/Cloud API) mais onboarding opérationnel/policy plus strict.
- Sandbox rapide possible, prod plus encadrée (templates, conformité de messagerie business selon canal choisi). (C-131)

### Recommandation
- Phase 1: Telegram uniquement.
- Phase 2: WhatsApp pour segment qui l’exige, avec volume contrôlé et templates revus conformité.

---

## 2.4 Email agent V2

### Faisabilité
Élevée techniquement. Complexité principale: qualité et conformité du contenu sortant.

### Use cases pertinents
- digest plan + deltas,
- alertes actionnables (réservations, fermetures, météo),
- récap post-voyage.

### Compliance baseline
- consentement/opt-out clair,
- identification expéditeur + adresse valide,
- pas de sujet trompeur,
- stop emailing effectif rapidement. (C-132, C-133)

### Risques
- sur-sollicitation,
- confusion transactionnel vs marketing,
- baisse trust si recommandations peu fiables.

### Garde-fous
- fréquence plafonnée,
- règles de priorité d’alerte,
- scoring qualité avant envoi,
- kill switch par utilisateur/groupe.

---

## 3) Matrice conformité (résumé actionnable)

| Domaine | Exigence clé | Impact Holi | Niveau risque | Contrôle proposé |
|---|---|---|---|---|
| Données perso | Minimisation/finalité | Ne collecter que ce qui sert la planification active | H | Data map + champs obligatoires revus |
| Consentement | Retrait aussi simple que l’accord | Géoloc + email agent | H | UI opt-in/opt-out symétrique + audit trail |
| Mobile policy | Background location justifié | Travel Mode seulement | H | Dossier policy + démonstration core feature |
| Messagerie | Cadre canal + anti-spam | Notifications groupées | M | Opt-in par canal + rate limits |
| Email | Règles anti-spam + transparence | V2 agent | M | Templates conformes + unsubscribe 1-click |

---

## 4) Plan d’implémentation recommandé (séquencé)

### Phase A (MVP renforcé)
- Collaboration temps réel + consensus board.
- Pas de géoloc continue (ponctuelle uniquement).
- Pas de WhatsApp/email agent en push automatique.

### Phase B (V1.5)
- Telegram bot notifications/action shortcuts.
- Travel Mode avec géoloc semi-continue opt-in, fenêtre temporelle bornée.

### Phase C (V2)
- Email agent (digest + alertes), gouvernance stricte contenu/conformité.
- Extension WhatsApp selon traction segment et coût opérationnel.

---

## 5) Hypothèses critiques à tester

1. Les utilisateurs acceptent un opt-in géoloc limité en échange de valeur immédiate (alerte utile + adaptation du plan).  
2. La collaboration temps réel augmente la convergence groupe vs workflow asynchrone simple.  
3. Les notifications messagerie améliorent l’exécution sans fatigue notification.  
4. L’email agent est perçu comme service (pas spam) si centré utilité/pertinence.

---

## 6) Sources et niveau de confiance

Voir `SOURCE-REGISTRY.yaml` (C-124 à C-133) et `sources-verified.md` (TASK-133).

- Claims réglementaires/plateforme: confiance **moyenne à haute** (sources officielles ou docs produit).
- Claims architecture/roadmap: confiance **moyenne** (synthèse technique orientée décision, à valider en prototypage).

---

## 7) Conclusion de tâche

TASK-133 confirme qu’il n’y a **pas de blocage fatal** pour poursuivre Holi, mais la géoloc continue et les canaux sortants doivent être traités comme **features sous gouvernance**, pas comme “defaults”.

La stratégie la plus robuste: collaboration temps réel d’abord, conformité-by-design, puis expansion progressive des canaux.
