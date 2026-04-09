# Holi — Modèle business & monétisation (TASK-132)

Date: 2026-04-09  
Statut: draft review-ready  
Owner: Isaak

## 1) Résumé exécutable

**Position recommandée:**
- **V1 (0-6 mois):** freemium + affiliation contextuelle (hébergements/activités), sans sponsorisation intrusive.
- **V1.5 (6-12 mois):** premium léger (abonnement groupe/famille) + tests sponsorisation POI très encadrés.
- **V2 (>12 mois):** montée en puissance vers revenus récurrents (abonnement) ; affiliation reste complément.

**Pourquoi:**
- La différenciation Holi est sur la **résolution de contraintes collaboratives**, pas sur la simple inspiration voyage (C-117, C-118).
- Les revenus “transactionnels” (affiliation) peuvent monétiser tôt sans forcer un paywall prématuré.
- Les revenus “récurrents” (premium) protègent mieux la marge et la dépendance plateforme à moyen terme (A-109).

## 2) Mécaniques de revenu proposées

### 2.1 Affiliation (priorité V1)
**Principe:** proposer des liens/action cards au moment de décision (ex: hébergement, activité), avec tracking affilié.

**Sources marché/feasibility:**
- Existence d’un programme affilié travel explicite côté GetYourGuide (C-134).
- Les comparateurs travel basés sur renvoi partenaire restent un modèle visible du marché (C-138).

**Règles produit recommandées:**
- Affiliation uniquement après score de “fit contraintes” (pas avant).
- Transparence UX: badge “lien affilié” + explication valeur utilisateur.
- Limite de densité commerciale par étape du plan (anti-spam).

### 2.2 Freemium + abonnement (priorité V1.5)
**Free (acquisition):**
- 1 voyage actif
- collaboration limitée (ex: 2 participants)
- chatbot borné en quota

**Premium (conversion):**
- voyages illimités
- collaboration groupe/famille étendue
- exports intelligents + checklistes avancées + modes anti-imprévus

**Contrainte plateforme:**
- Les biens/services digitaux in-app doivent suivre les règles de billing stores (C-135, C-136).
- Implication: architecture pricing dès V1 pensée “store-safe”.

### 2.3 Sponsorisation POI (option contrôlée, pas core V1)
**Principe:** visibilité sponsorisée d’un POI/activité **uniquement** si pertinence contraintes élevée.

**Conditions minimales:**
- séparation claire “sponsorisé” vs “recommandé algorithmique”
- pas d’impact négatif sur le classement sécurité/enfants/logistique
- fréquence plafonnée

**Risque majeur:** destruction de confiance si biais perçu (A-110).  
=> Recommandé en **expérimentation limitée** seulement après validation du PMF initial.

## 3) Unit economics simplifiés (pré-modèle)

> Tous les chiffres ci-dessous sont des **estimations de travail** à valider terrain.

- Revenu V1 attendu = **Affiliation (dominant)** + **petite poche premium**.
- Revenu V2 visé = **Premium (dominant)** + affiliation d’appoint + sponsorisation sélective.

### Hypothèses de calcul (estimates)
- Taux d’usage fonctionnalité transactionnelle: `[À VÉRIFIER — source non confirmée]`
- CTR vers partenaires affiliés: `[À VÉRIFIER — source non confirmée]`
- CVR partenaire: `[À VÉRIFIER — source non confirmée]`
- Take rate net après intermédiaires: `[À VÉRIFIER — source non confirmée]`
- Taux de conversion premium mensuel: `[À VÉRIFIER — source non confirmée]`
- Churn premium mensuel: `[À VÉRIFIER — source non confirmée]`

## 4) Risques business & mitigation

1. **Dépendance partenaires affiliés (H)**  
   - Mitigation: portefeuille multi-partenaires + fallback non-monetized links.

2. **Contrainte policy stores sur monétisation digitale (H)**  
   - Mitigation: design prix/billing compliant dès le début (C-135, C-136).

3. **Baisse de confiance via sponsorisation POI (H)**  
   - Mitigation: sponsorisation limitée, strictement contextualisée, auditée (A-110).

4. **Affiliation cannibalise la valeur premium (M)**  
   - Mitigation: réserver gains “temps/fiabilité collaborative” au premium.

5. **Anti-bot limite la veille compétitive/sourcing data (M)**  
   - Mitigation: marquer explicitement les zones d’incertitude (C-139).

## 5) Décision recommandée (TASK-132)

**Go conditionnel** vers TASK-134 avec ce mix:
- **Adopter**: Freemium + Affiliation contextuelle en core business model.
- **Différer**: sponsorisation POI comme expérimentation encadrée post-signal confiance.
- **Préparer**: architecture premium + billing compliance dès la conception UX/paywall.

## 6) Evidences / metadata refs
- Produit/différenciation: C-117, C-118, C-120, C-121, C-122, C-123
- Monétisation marché/politiques: C-134, C-135, C-136, C-137, C-138, C-139, C-140
- Hypothèses clés: A-102, A-105, A-109, A-110
- Questions ouvertes: Q-117, Q-118
