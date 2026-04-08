# Scope Lock — Holi Kickoff

Date: 2026-04-08  
Owner: Johan / Isaak  
Status: Locked for Gate 1 (TASK-128)

## 1) Scope statement
This phase defines whether Holi is a decision-worthy opportunity, based on a concrete artifact (family trip planner HTML) showing real planning behavior and frictions.

Deliverable objective for Gate 1:
- lock intent,
- lock problem perimeter,
- lock measurable decision criteria for downstream tasks.

## 2) In scope (TASK-128)
1. Extract user/problem signal from inbound itinerary HTML.
2. Translate signals into product intent + bounded scope.
3. Define non-goals to prevent feature sprawl.
4. Define weighted decision criteria for go/no-go recommendation.
5. Align TASK-129 sequencing with discovered evidence quality.

## 3) Out of scope (TASK-128)
- Full TAM/SAM/SOM quantification.
- Competitive benchmarking depth (reserved for TASK-130).
- Technical architecture validation depth (reserved for TASK-133).
- Final monetization decision (reserved for TASK-132+135).

## 4) Opportunity framing (locked working hypothesis)
Holi is a collaborative family travel planning assistant turning high-effort manual itinerary curation into a guided, personalized and execution-ready trip plan.

Primary user context captured from artifact:
- multi-day road trip,
- mixed audience (parents + kids),
- hard constraints (weather, closures, mobility constraints, booking windows),
- heavy manual aggregation (activities, logistics, prices, maps, tips, notes).

## 5) Decision criteria (Gate 1)

| Criterion | Weight | Evidence threshold | Pass condition |
|---|---:|---|---|
| Problem intensity (time/cognitive load) | 25% | Artifact + at least 2 external validation signals in TASK-129 | Score >= 3/5 |
| Segment clarity (who suffers most) | 20% | Clear JTBD segmentation + exclusion rules | Score >= 3/5 |
| Product differentiation potential | 20% | Distinct value beyond itinerary docs/maps/chat | Score >= 3/5 |
| 90-day execution feasibility | 20% | Practical MVP scope and integration risk map | Score >= 3/5 |
| Monetization plausibility | 15% | At least 2 viable revenue hypotheses with risk notes | Score >= 2/5 |

### Scoring rule
- Per criterion: 1–5 with rationale and claim refs.
- Weighted score threshold:
  - `>= 70`: proceed toward POC recommendation
  - `55–69`: conditional progression with evidence closure plan
  - `< 55`: stop/re-scope before build intent

## 6) Hard-stop conditions
1. No tight segment definition by end of TASK-129.
2. No defensible differentiation thesis by end of TASK-130.
3. Core value proposition still depends on unsourced assumptions by end of TASK-134.

## 7) Required artifacts for TASK-128 completion
- [x] Scope lock (`SCOPE-LOCK.md`)
- [x] Structured kickoff brief (`KICKOFF-BRIEF-2026-04-08.md`)
- [x] Decision log entry updated
- [x] Source registry seeded with artifact-derived claims
- [x] Task sequencing updated (`TASK-PLAN.md`)
