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

### 2026-04-09 — Product V1 scope lock (TASK-131)
- **Decision:** Lock V1 to five modules only: onboarding+QCM, collaborative swipe arbitration, planning mode, travel mode, bounded chatbot; enforce explicit kill-list (no booking, no generic AI planner, no social feed).
- **Options considered:**
  1. Broad “all-in-one” travel app MVP
  2. Narrow wedge MVP with collaboration + constraints (selected)
  3. Chatbot-first MVP without collaborative layer
- **Why chosen:** Preserves the only defendable differentiation path identified in TASK-130 while reducing overbuild risk.
- **Evidence refs:** C-117, C-118, C-120, C-121, C-122, C-123
- **Impact on scope/timeline:** Keeps TASK-132/133 focused on validating monetization and feasibility of one coherent loop.
- **Revisit condition (if any):** Revisit if onboarding/QCM completion or group convergence metrics fail in prototype tests.

### 2026-04-09 — Feasibility/compliance sequencing lock (TASK-133)
- **Decision:** Keep collaboration real-time in core path; treat continuous geolocation as opt-in bounded Travel Mode; sequence integrations Telegram-first, then WhatsApp; defer Email Agent to V2 with strict consent/opt-out governance.
- **Options considered:**
  1. Ship all channels + background location in V1
  2. Progressive rollout with compliance guardrails (selected)
  3. Remove location/messaging capabilities entirely
- **Why chosen:** Preserves value wedge while reducing policy/privacy rejection risk and operational complexity.
- **Evidence refs:** C-124, C-125, C-126, C-127, C-128, C-130, C-131, C-132, C-133
- **Impact on scope/timeline:** Clarifies implementation phases for TASK-134 and final recommendation in TASK-135.
- **Revisit condition (if any):** Revisit if prototype data shows low user value for Travel Mode alerts or if messaging channel adoption is weak.

### 2026-04-09 — Monetization stack lock (TASK-132)
- **Decision:** Adopt a phased model: V1 freemium + contextual affiliation; defer POI sponsorisation to controlled experiments; design premium architecture early for recurring revenue.
- **Options considered:**
  1. Subscription-first immediately
  2. Affiliation-first only
  3. Hybrid phased stack (selected)
- **Why chosen:** Hybrid model monetizes early while preserving trust and keeps long-term margin path via premium.
- **Evidence refs:** C-117, C-118, C-134, C-135, C-136, C-138, C-139, C-140
- **Impact on scope/timeline:** Unblocks TASK-134 with explicit business model assumptions and risk controls.
- **Revisit condition (if any):** Revisit after first pilot metrics on affiliate conversion, trust/NPS drift, and premium conversion baseline.

### 2026-04-09 — Whitepaper v1 assembly decision (TASK-134)
- **Decision:** Publish a consolidated decision-grade whitepaper (`WHITEPAPER-V1.md`) plus a dedicated sources/assumptions annex (`WHITEPAPER-V1-ANNEX-SOURCES.md`) as baseline for final recommendation task.
- **Options considered:**
  1. Keep fragmented docs only
  2. Build whitepaper without annex
  3. Build whitepaper + traceability annex (selected)
- **Why chosen:** TASK-135 needs a single coherent narrative with explicit traceability and uncertainty markers, not a set of disconnected files.
- **Evidence refs:** C-101..C-140, A-101..A-110
- **Impact on scope/timeline:** Moves project from analysis fragments to integrated decision package; directly unblocks TASK-135.
- **Revisit condition (if any):** Revisit if Johan requests alternate packaging (e.g., 3-format final pack in TASK-138 priority).

- 2026-04-09 (TASK-135): **Decision = GO POC cadré 8 semaines** avec gates explicites (activation, collaboration, monétisation, satisfaction) puis go/no-go strict.
