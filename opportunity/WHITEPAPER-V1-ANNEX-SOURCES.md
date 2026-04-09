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
