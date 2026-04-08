# Holi — Cartographie concurrence & substituts (TASK-130)

Date: 2026-04-08
Owner: Isaak

## 1) Périmètre de la cartographie

Axes couverts:
- Apps de planification de voyage (itinerary builders)
- Cartes/navigation (généralistes et offline)
- Guides & contenus inspiration
- Assistants IA conversationnels travel
- Substituts non-app (assemblage manuel multi-outils)

Segment de référence (hérité TASK-129):
- **S1 prioritaire:** familles avec enfants
- **S4 secondaire:** groupes d’amis

---

## 2) Clusters concurrence/substituts

## A. Planificateurs d’itinéraires (concurrence directe la plus proche)
Exemples observés:
- Wanderlog (trip planning + map)
- Roadtrippers (roadtrip + suggestions IA)
- Sygic Travel (itinéraire jour par jour + carte)
- Visit A City (travel guide personnalisé)

Forces:
- UI de planification déjà mature
- Agrégation de points d’intérêt / activités
- Cartes et structuration par journée

Limites face à Holi (hypothèse à confirmer):
- Peu de profondeur sur **contraintes familiales fines** (âge enfants, fatigue, météo locale micro, fenêtres réservation critiques)
- Collaboration souvent centrée sur co-édition, moins sur arbitrage explicite de préférences/contraintes

## B. Maps/navigation (substitut fort, mais incomplet)
Exemples:
- Google Maps
- MAPS.ME

Forces:
- Couverture globale + découverte POI + navigation
- Habitude d’usage très forte

Limites:
- Ne résout pas seul la synthèse multi-contraintes par jour
- Ne produit pas nativement un plan “décisionnel” orienté famille (trade-offs, plan B météo, charge enfant)

## C. Guides/inspiration (substitut partiel)
Exemples:
- Lonely Planet
- AllTrails (sur la verticale outdoor)

Forces:
- Richesse éditoriale / inspiration
- Qualité de découverte thématique

Limites:
- Peu orienté orchestration opérationnelle d’un séjour multi-acteurs
- Faible personnalisation dynamique sur contraintes en temps réel

## D. Assistants IA travel (substitut émergent)
Exemples:
- ChatGPT (usage généraliste)
- GuideGeek (promesse planning/booking en conversation)

Forces:
- Rapidité de génération d’idées et d’itinéraires
- Expérience conversationnelle flexible

Limites:
- Risque d’hallucinations ou recommandations peu contextualisées
- Persistance/collaboration/traçabilité du plan souvent limitée sans couche produit dédiée

## E. Substitut réel dominant aujourd’hui
- Workflow manuel multi-outils: chat IA + Maps + blogs/guides + notes + apps réservation

Force:
- Flexible, déjà possible immédiatement

Faiblesse:
- Coût cognitif élevé, faible robustesse aux changements, charge mentale forte pour le “trip owner”

---

## 3) Matrice “capacité vs manque” (lecture rapide)

| Capacité clé | Planificateurs | Maps | Guides | IA chat | Holi wedge visé |
|---|---|---|---|---|---|
| Idées de destinations/activités | fort | moyen | fort | fort | non différenciant |
| Itinéraire jour/jour | moyen-fort | faible | faible | moyen | améliorer avec contraintes |
| Collaboration multi-personnes | moyen | faible | faible | faible-moyen | **élevé (objectif)** |
| Arbitrage contraintes famille | faible-moyen | faible | faible | moyen (ad hoc) | **élevé (objectif)** |
| Robustesse opérationnelle (météo/fermetures/réservations) | faible-moyen | moyen | faible | faible-moyen | **élevé (objectif)** |
| Réduction charge mentale “organisateur” | moyen | faible | faible | moyen | **élevé (objectif)** |

Note: cette matrice combine signaux vérifiés (positionnement public) + estimation analytique (marquée dans SOURCE-REGISTRY).

---

## 4) Verdict de différenciation (Gate TASK-130)

## Verdict
**Différenciation possible mais conditionnelle.**
Holi n’a pas d’avantage défendable s’il reste un “itinerary AI” générique. La fenêtre existe uniquement si Holi devient:
1) **constraint-first** (enfants, énergie, météo, réservations, logistique),
2) **collaboratif by design** (arbitrage explicite des préférences, pas juste co-édition),
3) **opérationnel** (plans alternatifs, checklist risque/réservation, adaptation en cours de voyage).

## Menace majeure
Les suites existantes peuvent absorber rapidement les features superficielles (chat, suggestions, carte).

## Wedge défendable proposé (formulation courte)
> “Holi transforme un groupe/famille avec contraintes réelles en plan quotidien exécutable, robuste aux aléas, avec arbitrage collaboratif explicite.”

## Implication stratégique
- Si ce wedge est retenu: TASK-131 doit verrouiller un MVP centré arbitrage + contraintes + mode planning/voyage.
- Sinon: risque élevé de produit “me-too” à faible pouvoir de pricing (cf. A-102).

---

## 5) Red flags et points à tester ensuite

1. **Risque de commoditisation IA**
   - Test à prévoir: pourquoi un couple/famille paierait Holi plutôt que ChatGPT + Maps.
2. **Risque d’onboarding trop lourd**
   - Test à prévoir: quantité minimale de questions (QCM) pour générer un plan supérieur.
3. **Risque data temps réel**
   - Test à prévoir: quel niveau de données live est nécessaire en MVP pour créer une différence perceptible.

---

## 6) Conclusion opérationnelle TASK-130

- Cartographie concurrence/substituts: **faite**.
- Verdict différenciation: **positif sous condition stricte de wedge**.
- Recommandation pour la suite immédiate: **continuer vers TASK-131**, avec kill-list explicite de toutes les features “génériques non wedge”.