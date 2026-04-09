# Sources verified — Holi opportunity

Date: 2026-04-08

## Notes globales
- `web_search` Brave reste indisponible dans cet environnement (`missing_brave_api_key`).
- Pour TASK-130, les URLs utilisées dans le livrable ont toutes été testées via `web_fetch`.
- Certaines plateformes protègent fortement l’accès automatisé (anti-bot/JS) ; elles sont conservées uniquement comme signaux de présence marché, sans extraire de claims fins non vérifiés.

## TASK-129 evidence base
1. Inbound planning artifact (primary evidence)
   - Path: `/home/isaak/.openclaw/media/inbound/file_23---d7441c4b-b456-4543-a03b-f3ebe9c6f36d`
2. Kickoff synthesis artifacts
   - `opportunities/holi/KICKOFF-BRIEF-2026-04-08.md`
   - `opportunities/holi/MEETING-INTEL-2026-04-08.md`
   - `opportunities/holi/SCOPE-LOCK.md`

## TASK-130 URL audit (competition/substitutes)

### Reachable (used)
- https://wanderlog.com (200)
- https://roadtrippers.com (200)
- https://www.google.com/maps (200)
- https://www.lonelyplanet.com (200)
- https://chatgpt.com (200)
- https://www.alltrails.com (200)
- https://www.polarsteps.com (200)
- https://www.tripit.com (200)
- https://maps.me (200)
- https://guidegeek.com (200)
- https://www.visitacity.com (200)
- https://www.sygic.com/travel (200)
- https://www.google.com/travel (200)

### Protected / partially blocked (not used for detailed factual claims)
- https://www.tripadvisor.com (403)
- https://www.rome2rio.com (403)
- https://www.getyourguide.com (403)
- https://www.booking.com (202 + anti-bot payload)

## TASK-131 evidence base (product design)
- No new external factual URLs required; TASK-131 is a design synthesis constrained by prior verified evidence.
- Claims introduced in TASK-131 are explicitly tagged as `estimate` in `SOURCE-REGISTRY.yaml` (C-121..C-123).

## TASK-133 URL audit (faisabilité + conformité)

### Reachable (used)
- https://supabase.com/docs/guides/realtime (200)
- https://firebase.google.com/docs/firestore/real-time_queries_at_scale (200)
- https://support.google.com/googleplay/android-developer/answer/9799150?hl=en (200)
- https://commission.europa.eu/law/law-topic/data-protection/rules-business-and-organisations/legal-grounds-processing-data/grounds-processing/what-if-somebody-withdraws-their-consent_en (200)
- https://core.telegram.org/bots/api (200)
- https://www.twilio.com/docs/whatsapp/tutorial/send-and-receive-media-messages-whatsapp-nodejs (200)
- https://www.ftc.gov/business-guidance/resources/can-spam-act-compliance-guide-business (200)
- https://support.google.com/accounts/answer/3467281?hl=en (200)
- https://www.eff.org/issues/location-privacy (200)
- https://developer.apple.com/documentation/corelocation/handling-location-updates-in-the-background (200, extraction limité)
- https://developer.apple.com/documentation/bundleresources/information-property-list/nslocationalwaysandwheninuseusagedescription (200, extraction limité)

### Unreachable / blocked (not used for factual claims)
- https://developers.facebook.com/docs/whatsapp/cloud-api/overview (error payload)
- https://www.whatsapp.com/legal/business-policy/ (error payload)
- https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng (extraction failed)

## Usage discipline
- Any precise quantitative market/product claim not directly verifiable from above is tagged as estimate in `SOURCE-REGISTRY.yaml`.
- TASK-130 verdict relies on:
  - verified public positioning statements (website headlines/features), and
  - explicit strategic estimates with medium confidence.
- TASK-133 compliance synthesis uses official docs when extractable; when tooling returns title-only/partial extracts, confidence is lowered and claims are framed conservatively.