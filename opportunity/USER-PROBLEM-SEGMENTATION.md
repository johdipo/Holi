# Holi — User Problem Research & Traveler Segmentation (TASK-129)

Date: 2026-04-08
Owner: Isaak

## 1) Scope of this pass
This pass establishes a **decision-grade first segmentation** for Holi using current primary evidence and clearly tagged estimates.

Evidence base:
- Primary: C-101, C-102, C-103, C-106
- Inference/estimate: C-104, C-105, C-107, C-108
- Process note: external web evidence is currently blocked by missing `BRAVE_API_KEY`; see `sources-verified.md`.

## 2) Segment matrix (v1)

| Segment | Context | Core JTBD | Top frictions observed/inferred | Severity (1-5) | Confidence |
|---|---|---|---|---:|---|
| S1 Families with kids (primary) | Multi-constraint trips (ages, fatigue, safety, weather) | “Help us build a day plan that works for everyone without last-minute failures.” | Child-fit uncertainty, activity pacing, reservation timing, weather/closure volatility, cognitive load in arbitration | 5 | Medium-High |
| S2 Couples / adult leisure duos | Flexibility and experience quality | “Give us high-quality options and a coherent route with minimal planning overhead.” | Option overload, weak prioritization logic, inconsistent local constraints | 3 | Medium |
| S3 Solo / micro-adventure travelers | Fast independent planning | “Let me quickly convert inspiration into feasible day plans.” | Time-to-plan overhead, map-to-action gap, stale info risk | 3 | Low-Medium |
| S4 Friend groups (3+) | Coordination and preference alignment | “Help us converge on choices quickly and avoid planning arguments.” | Preference conflict, asynchronous decision loops, no shared decision memory | 4 | Medium |

### Segment priority recommendation (for Gate-2 continuity)
1. **S1 Families with kids** (best pain density + strongest signal in current evidence)
2. **S4 Friend groups** (collaboration intensity validates product wedge)
3. S2
4. S3

## 3) JTBD hierarchy (top by segment)

### S1 Families with kids (primary)
1. **Feasibility JTBD:** filter options by child age/energy/safety and operational constraints (weather/opening/reservation).
2. **Coordination JTBD:** align adult preferences while preserving kid viability.
3. **Execution JTBD:** produce a realistic day-order with fallback options.

Why this segment leads now:
- Current primary artifact explicitly encodes child suitability + warnings + reservation urgency (C-102, C-103, C-106).
- Manual orchestration burden appears high (C-104).

### S4 Friend groups
1. Converge quickly on shared shortlist.
2. Resolve preference trade-offs with transparent logic.
3. Preserve planning context between async conversations.

### S2 Couples
1. Reduce search breadth to “best-fit now”.
2. Keep itinerary quality high without over-planning.

### S3 Solo travelers
1. Speed from idea to viable plan.
2. Avoid surprises from constraints not visible in map-only flows.

## 4) Pain map (cross-segment)

| Pain | Description | Affected segments | Severity | Evidence class |
|---|---|---|---:|---|
| P1 Constraint fragmentation | Critical constraints scattered across sources/tools | S1, S4, S2 | 5 | Primary + estimate |
| P2 Planning arbitration overhead | High effort to reconcile preferences into one plan | S1, S4 | 4 | Estimate (artifact-supported) |
| P3 Volatility risk | Weather/closure/booking windows break naive plans | S1, S2, S3 | 4 | Primary |
| P4 Generic output mismatch | Generic itinerary text misses practical sequencing constraints | S1, S4, S2 | 4 | Estimate |
| P5 Collaboration loss | Context lost across chat/map/doc handoffs | S4, S1 | 4 | Estimate |

## 5) Implications for downstream tasks
- **TASK-130 (competition):** explicitly test whether competitors solve P1+P2 together (not just inspiration or mapping).
- **TASK-131 (product V1):** preserve narrow wedge = constraint-aware collaborative ranking + day-plan fallback logic.
- **TASK-132 (monetization):** test willingness-to-pay against “risk/time saved” rather than generic itinerary value.

## 6) Unresolved gaps (must stay explicit)
1. Quantified prevalence of each pain by segment is still missing.
2. No direct interview transcripts yet for non-family segments.
3. No external benchmark yet on current alternatives’ satisfaction/failure modes.

## 7) Decision statement for TASK-129
**Recommendation:** Keep S1 (families with kids) as the lead segment for Gate-2, while carrying S4 as secondary validation segment.

This is sufficient to continue the chain, but remains **conditional** on competition mapping in TASK-130 and monetization/feasibility checks in TASK-132/133.
