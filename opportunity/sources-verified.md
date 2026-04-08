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

## Usage discipline
- Any precise quantitative market/product claim not directly verifiable from above is tagged as estimate in `SOURCE-REGISTRY.yaml`.
- TASK-130 verdict relies on:
  - verified public positioning statements (website headlines/features), and
  - explicit strategic estimates with medium confidence.