# Holi — Final Whitepaper Master

Date: 2026-04-09
Version: final-v1
Owner: Isaak

## Navigation des livrables
- `whitepaper-full.html` : version exhaustive (knowledge complète, traçabilité, risques, hypothèses, sources).
- `whitepaper-human.html` : version décisionnaire (lecture rapide, décision go/no-go, plan d’action).

## Convention de publication
- Source master unique: `whitepaper.md`
- Rendu public par défaut: `whitepaper-human.html`
- Rendu analytique: `whitepaper-full.html`
- Domaine: `https://holi.dpdp.ch`

---

## Contenu master (base analytique)

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


---

## Recommandation finale et gates POC

# Holi — Recommandation stratégique finale (TASK-135)

## Décision explicite
**GO pour un POC cadré (8 semaines), puis go/no-go strict.**

Le POC ne vise pas la scale, il vise la **preuve de traction collaborative** sur un segment précis, avec instrumentation de conversion et signal de rétention.

## Pourquoi ce choix
Sur base des livrables TASK-129 à TASK-134:
- Le problème utilisateur est réel sur la coordination de groupe (alignement, arbitrage, partage)
- La différenciation est défendable si Holi se concentre sur la **collaboration native** plutôt qu’un clone de guide/trip planner
- Le modèle économique est possible mais sensible au timing (affiliate + freemium d’abord, sponsorisation ensuite)
- Les risques conformité/complexité sont gérables avec une V1 sobre (géoloc non continue, consentement explicite)

## Scope du POC (8 semaines)
### In-scope
1. Onboarding + QCM préférences
2. Swipe collaboratif simple (petits groupes)
3. Plan de voyage partagé minimal (décisions + shortlist)
4. Canal Telegram (prioritaire), WhatsApp reporté
5. Tracking analytics minimal: activation, shortlist, action partenaire

### Out-of-scope
- Géoloc continue en arrière-plan
- Email agent V2 automatisé
- Sponsorisation POI payante
- Intégrations complexes multi-provider

## KPI de validation (gates)
Décision à 8 semaines:
- **Activation**: ≥35% des groupes créés atteignent une shortlist partagée
- **Engagement collaboratif**: ≥2 participants actifs dans ≥60% des groupes
- **Signal monétisation**: CTR affilié utile (seuil cible: 8–12%) [À VÉRIFIER — source non confirmée]
- **Satisfaction rapide**: feedback “gain de temps” positif majoritaire

Si <2 KPI sur 4 atteints: **NO-GO / pivot fort**.
Si ≥3 KPI sur 4 atteints: **GO phase 2** (durcissement produit + canaux).

## Risques principaux à surveiller
1. Produit trop large trop tôt → dilution de valeur
2. Dépendance acquisition payante prématurée
3. Dette conformité si géoloc/messagerie élargies trop vite
4. “Feature creep” hors thèse collaboration

## Recommendation opératoire
- Nommer un owner KPI hebdo
- Geler le scope (changement uniquement si impact KPI)
- Revue hebdo go/no-go avec tableau simple
- Préparer dès semaine 1 un plan de fermeture propre (si NO-GO)

## Traceability
Synthèse dérivée de:
- `USER-PROBLEM-SEGMENTATION.md`
- `COMPETITION-SUBSTITUTES-MAP.md`
- `PRODUCT-V1-DESIGN.md`
- `BUSINESS-MODEL-MONETIZATION.md`
- `TECH-FEASIBILITY-COMPLIANCE.md`
- `WHITEPAPER-V1.md`
- `WHITEPAPER-V1-ANNEX-SOURCES.md`


---

## Annexes sources

# Holi — Annexes sources & hypothèses (TASK-134)

Date: 2026-04-09

## A) Sources externes utilisées (URLs vérifiées)

### Concurrence / positionnement
- https://wanderlog.com
- https://roadtrippers.com
- https://www.sygic.com/travel
- https://www.google.com/maps
- https://maps.me
- https://www.lonelyplanet.com
- https://www.alltrails.com
- https://chatgpt.com
- https://guidegeek.com

### Faisabilité technique / conformité
- https://supabase.com/docs/guides/realtime
- https://firebase.google.com/docs/firestore/real-time_queries_at_scale
- https://developer.apple.com/documentation/corelocation/handling-location-updates-in-the-background
- https://developer.apple.com/documentation/bundleresources/information-property-list/nslocationalwaysandwheninuseusagedescription
- https://support.google.com/googleplay/android-developer/answer/9799150?hl=en
- https://commission.europa.eu/law/law-topic/data-protection/rules-business-and-organisations/legal-grounds-processing-data/grounds-processing/what-if-somebody-withdraws-their-consent_en
- https://www.eff.org/issues/location-privacy
- https://core.telegram.org/bots/api
- https://www.twilio.com/docs/whatsapp/tutorial/send-and-receive-media-messages-whatsapp-nodejs
- https://www.ftc.gov/business-guidance/resources/can-spam-act-compliance-guide-business

### Monétisation / marché
- https://partner.getyourguide.com/
- https://support.google.com/googleplay/android-developer/answer/9858738?hl=en
- https://developer.apple.com/app-store/review/guidelines/#payments
- https://www.statista.com/topics/2704/online-travel-market/
- https://www.trivago.com/advertising
- https://ads.google.com/intl/en_ch/home/resources/articles/travel-marketing/

> Vérification: voir `sources-verified.md` (statut reachable/protected).

## B) Sources non-web (primaires)
- Artefact de planification entrant: `/home/isaak/.openclaw/media/inbound/file_23---d7441c4b-b456-4543-a03b-f3ebe9c6f36d`
- Synthèses internes: `KICKOFF-BRIEF-2026-04-08.md`, `MEETING-INTEL-2026-04-08.md`, `SCOPE-LOCK.md`

## C) Claims de référence utilisés dans WHITEPAPER-V1.md
- Problème/segmentation: C-101..C-111
- Concurrence/wedge: C-113..C-120
- Produit V1: C-121..C-123
- Faisabilité/conformité: C-124..C-133
- Monétisation: C-134..C-140

## D) Hypothèses structurantes encore ouvertes
- A-105 (friction QCM acceptable)
- A-106 (acceptation géoloc bornée)
- A-107 (valeur Telegram-first)
- A-108 (email agent non perçu spam)
- A-109 (hybride monétise tôt sans dégrader confiance)
- A-110 (sponsorisation POI sans perte trust)

## E) Points d’incertitude explicitement assumés
- Benchmarks quantitatifs fins concurrents limités par anti-bot sur plusieurs domaines majeurs (C-119, C-139).
- Unit economics (CTR/CVR/churn/take-rate) non confirmés: à valider par pilote terrain.

