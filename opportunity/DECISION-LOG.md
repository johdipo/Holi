# Decision Log

### 2026-04-08 — Kickoff intent lock (TASK-128)
- **Decision:** Run Holi in Analyze + Decide mode.
- **Options considered:**
  1. Analyze only
  2. Analyze + decide
  3. Build directly
- **Why chosen:** Task chain already targets explicit final recommendation (TASK-135); direct build now would skip evidence discipline.
- **Evidence refs:** C-101, C-103
- **Impact on scope/timeline:** Keeps immediate work analytical; protects against premature feature build.
- **Revisit condition (if any):** If Johan explicitly asks to fast-track a POC before Gate 2 outputs.

### 2026-04-08 — Scope lock and Gate 1 criteria adopted
- **Decision:** Adopt weighted Gate 1 criteria and hard-stop conditions from `SCOPE-LOCK.md`.
- **Options considered:**
  1. Qualitative scope only
  2. Lightweight checklist
  3. Weighted rubric + hard stops
- **Why chosen:** High complexity and temptation to over-scope require objective go/no-go discipline.
- **Evidence refs:** C-101, C-104, C-108
- **Impact on scope/timeline:** Adds small upfront framing effort, reduces downstream drift risk.
- **Revisit condition (if any):** If segment definition materially shifts in TASK-129.

### 2026-04-08 — Strategic framing from inbound artifact
- **Decision:** Frame Holi around constraint-aware collaborative planning, not generic itinerary generation.
- **Options considered:**
  1. Generic AI trip writer
  2. Constraint-first planning assistant
  3. Booking-first marketplace
- **Why chosen:** Artifact demonstrates pain in prioritization/constraints orchestration more than lack of raw activity ideas.
- **Evidence refs:** C-102, C-103, C-105, C-106, C-107
- **Impact on scope/timeline:** Influences TASK-129/130 research focus and TASK-131 MVP boundary.
- **Revisit condition (if any):** If competitor analysis disproves differentiation.

### 2026-04-08 — Segment priority lock for Gate-2 continuation (TASK-129)
- **Decision:** Set S1 (families with kids) as primary segment; keep S4 (friend groups) as secondary validation segment.
- **Options considered:**
  1. Family-first
  2. General traveler-first
  3. Friend-group-first collaboration wedge
- **Why chosen:** Strongest current primary signal is family constraint density (age fit, operational caveats, reservation timing); friend-group collaboration remains meaningful but less directly evidenced.
- **Evidence refs:** C-102, C-103, C-106, C-109, C-111
- **Impact on scope/timeline:** Unblocks TASK-130 with a clear segment lens and comparison baseline.
- **Revisit condition (if any):** If TASK-130 shows weak differentiation for family constraints vs substitutes.

### 2026-04-08 — Differentiation verdict gate (TASK-130)
- **Decision:** Continue to TASK-131 only with a strict wedge: constraint-first + collaborative arbitration + operational robustness.
- **Options considered:**
  1. Generic AI itinerary planner
  2. Constraint-first collaborative planner (selected)
  3. Distribution/partnership-first without product wedge
- **Why chosen:** Competitive landscape shows strong substitute pressure for generic planning; defendability appears only in explicit family/group constraint orchestration.
- **Evidence refs:** C-113, C-114, C-115, C-116, C-117, C-118
- **Impact on scope/timeline:** TASK-131 must include a clear MVP kill-list; avoids me-too product direction.
- **Revisit condition (if any):** Revisit if monetization tests (TASK-132) fail to show willingness-to-pay for wedge capabilities.
