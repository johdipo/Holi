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
