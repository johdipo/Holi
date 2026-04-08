# Holi — Structured Kickoff Brief (from inbound itinerary HTML)

Date: 2026-04-08  
Input artifact: `/home/isaak/.openclaw/media/inbound/file_23---d7441c4b-b456-4543-a03b-f3ebe9c6f36d`

## 1) What the artifact proves
- Real user planning behavior already resembles a mini-product: curation, categorization, route logic, map layer, budget framing, risk alerts, reservation reminders.
- Planning work is information-dense and brittle: closures, seasonality, opening windows, kid suitability, mobility constraints, and sequencing all interact.
- Current format (single long handcrafted HTML) is powerful but manual, hard to maintain, and likely non-reusable trip to trip.

## 2) Core user jobs-to-be-done (signal level)
1. Build a family-compatible itinerary with age-appropriate activities.
2. Balance delight + logistics (distance, weather, opening hours, injury constraints).
3. Convert idea list into execution (bookings, day-by-day flow, map and budget alignment).
4. Keep optionality (free vs paid, outdoor vs indoor fallback).

## 3) Key pain/friction signals extracted
- High curation burden across many sources and formats.
- High update burden when one condition changes (weather/closure/fatigue).
- Mental overload: many candidate activities, weak prioritization mechanics.
- Coordination burden: family preferences and constraints must be merged manually.

## 4) Opportunity hypothesis for Holi
A collaborative planning assistant can reduce planning time and improve trip confidence by turning scattered trip research into adaptive, family-aware plans.

## 5) MVP boundary proposal (for downstream validation)
In MVP, Holi should prioritize:
- profile + constraints capture (kids ages, mobility, trip style, budget);
- ranked activity shortlist per day with rationale;
- reservation and risk checklist;
- map-aware route coherence;
- lightweight collaboration (preference collection / agree-disagree mechanics).

Out of MVP for now:
- full booking engine,
- continuous geo-tracking,
- exhaustive destination coverage,
- fully autonomous travel agent execution.

## 6) Strategic risks noticed at kickoff
- Feature sprawl risk due to rich artifact expectations.
- Data freshness risk (hours/prices/closures volatility).
- Differentiation risk versus maps + generic AI itinerary generation.
- Monetization timing risk before clear repeat-use behavior.

## 7) Immediate implications for sequencing
- TASK-129 must confirm strongest paying/engaged segment and quantify pain.
- TASK-130 must test differentiation against existing planner/map/AI substitutes.
- TASK-131 should enforce narrow MVP discipline from this brief.
