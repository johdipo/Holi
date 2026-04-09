# Holi — Whitepaper v1

Date: 2026-04-09  
Version: v1 (draft review)  
Owner: Isaak

---

## 0) Executive summary

Holi vise un problème concret: transformer une planification de voyage familiale/groupe, aujourd’hui fragmentée et mentale, en plan journalier exécutable et adaptable.

Le verdict de cette V1 est **go conditionnel** sur une stratégie produit stricte:

1. **Wedge non-négociable**: planification *constraint-first* + arbitrage collaboratif (pas un simple “chatbot voyage”).
2. **MVP cadré**: onboarding/QCM, swipe collaboratif, modes Planning/Travel, chatbot borné, plan A/B.
3. **Monétisation progressive**: freemium + affiliation contextuelle en V1, premium en montée, sponsorisation POI seulement en test contrôlé.
4. **Conformité by design**: géoloc continue non-default (opt-in borné), consentement/rétractation symétriques, messagerie séquencée Telegram-first.

Sans ce cadrage, Holi tombe dans la commoditisation (ChatGPT + Maps + outils existants).

---

## 1) Problème utilisateur et segment cible

### 1.1 Problème central
Le problème principal n’est pas le manque d’idées de destinations; c’est la **fragmentation des contraintes** et la difficulté d’arbitrage en groupe/famille (C-101, C-103, C-110, C-118).

### 1.2 Segment prioritaire
- **S1 prioritaire**: familles avec enfants (signal le plus fort sur la densité de contraintes) (C-102, C-109)
- **S4 secondaire**: groupes d’amis (friction de convergence décisionnelle) (C-111)

### 1.3 Job-to-be-done (résumé)
"Aide-nous à converger vite vers un plan du jour réalisable pour tout le monde, avec plan de secours quand la réalité change."

---

## 2) Marché, concurrence et substituts

### 2.1 Paysage
- Planificateurs: Wanderlog, Roadtrippers, Sygic Travel (C-113)
- Cartes/substituts puissants: Google Maps, MAPS.ME (C-114)
- IA conversationnelle: ChatGPT, GuideGeek (C-116)
- Workflow réel dominant: stack manuelle multi-outils (C-118)

### 2.2 Implication stratégique
Les alternatives couvrent déjà l’inspiration et une partie de la planification. La différenciation Holi n’est viable que si la proposition reste:

- orientée contraintes réelles (famille/groupe),
- collaborative avec arbitrage explicite,
- robuste aux aléas opérationnels (C-117, C-120).

---

## 3) Proposition de valeur et produit V1

### 3.1 Proposition de valeur
Holi convertit des contraintes hétérogènes (enfants, fatigue, météo, timing, réservations) en un plan journalier exécutable, partagé, et replanifiable.

### 3.2 Périmètre V1 (in)
1. Onboarding + profil voyage
2. QCM contraintes (hard/soft)
3. Swipe collaboratif + résolution de conflits
4. Planning mode + Travel mode
5. Chatbot borné au contexte de contraintes
6. Sortie plan A / plan B par bloc critique

### 3.3 Kill-list V1 (out)
- Booking end-to-end
- Feed inspiration/social
- Remplacement cartographie complet
- Chat IA générique sans contexte contraintes

Références: C-121, C-122, C-123.

---

## 4) Modèle business et monétisation

### 4.1 Stack recommandée
- **V1:** freemium + affiliation contextuelle
- **V1.5:** premium léger (famille/groupe, exports, fiabilité)
- **V2:** premium dominant, affiliation complémentaire, sponsorisation POI encadrée

### 4.2 Pourquoi ce choix
- Monétisation précoce possible sans paywall prématuré (C-134, C-138)
- Préservation de la confiance si la densité commerciale est contrôlée (A-110)
- Contrainte store billing intégrée dès la conception (C-135, C-136)

### 4.3 Limites explicites
Les paramètres unit economics (CTR/CVR/take-rate/churn) restent des estimations tant qu’ils ne sont pas testés sur pilotes réels.

---

## 5) Faisabilité technique et conformité

### 5.1 Faisabilité
- Collaboration temps réel: faisable avec stack realtime managée (C-124, C-125)
- Intégrations messagerie: faisables, Telegram d’abord (C-130, C-131)
- Email agent: faisable, gouvernance de contenu/consentement obligatoire (C-132)

### 5.2 Géolocalisation continue (point sensible)
- Faisable techniquement, mais sous contraintes produit/policy/juridiques fortes (C-126, C-127, C-128, C-129)
- Décision: optionnelle, bornée, Travel Mode uniquement, opt-in explicite + pause + expiry.

---

## 6) Risques majeurs

1. **Commoditisation IA** si Holi devient un planner générique (H)
2. **Friction onboarding** si QCM trop long (H, A-105)
3. **Risque confiance** si sponsorisation POI perçue comme biaisée (H, A-110)
4. **Risque conformité/policy** sur géoloc continue (H, C-126..C-129)
5. **Dépendance partenaires** pour l’affiliation (H, A-109)

---

## 7) Hypothèses critiques à valider

- A-105: acceptation friction QCM vs valeur perçue
- A-106: opt-in géoloc bornée réellement acceptable
- A-107: Telegram-first génère une valeur exécution mesurable
- A-109: hybride freemium+affiliation monétise plus tôt sans dégrader trust
- A-110: seuil sponsorisation acceptable avant baisse confiance

Toutes les hypothèses et deadlines sont tracées dans `ASSUMPTIONS.md`.

---

## 8) Décision v1 (pré-TASK-135)

**Décision de ce whitepaper v1:** poursuivre vers la recommandation finale (TASK-135) avec un **go conditionnel**.

Conditions minimales:
1. MVP reste strictement dans le wedge défendable.
2. Monétisation commerciale reste progressive et contrôlée.
3. Conformité privacy/store est traitée comme contrainte de design, pas comme patch tardif.

Si une de ces conditions est abandonnée, la recommandation doit pivoter vers **no-go / hold**.

---

## 9) Références et traçabilité

- Sources détaillées et statuts d’accessibilité: `sources-verified.md`
- Registre claims: `SOURCE-REGISTRY.yaml` (C-101..C-140)
- Hypothèses: `ASSUMPTIONS.md`
- Questions ouvertes: `OPEN-QUESTIONS.md`
- Décisions et rationale: `DECISION-LOG.md`, `CHANGE-RATIONALE.md`

Note méthodologique: plusieurs sites travel majeurs sont partiellement bloqués en extraction automatisée dans cet environnement; les claims détaillés non robustes ont été évités ou explicitement marqués comme estimations (C-119, C-139).
