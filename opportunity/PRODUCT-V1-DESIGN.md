# Holi — Product Design V1 (TASK-131)

Date: 2026-04-09  
Owner: Isaak

## 1) Design goal (V1)
Build a **constraint-first collaborative planner** for S1 families (primary) and S4 friend groups (secondary), explicitly avoiding generic itinerary generation.

This V1 exists to validate one core promise:
> Holi reduces organizer mental load by turning fragmented constraints into an executable day plan with shared group alignment.

Evidence anchors: C-109, C-113..C-120.

---

## 2) MVP boundaries (what is IN / OUT)

### IN (must-have in V1)
1. **Onboarding profile + trip context**
   - Trip dates window, destination area, mobility constraints, kids ages, preferred rhythm, budget comfort.
2. **QCM (structured constraints capture)**
   - Fast questionnaire to capture hard constraints vs soft preferences.
3. **Collaborative swipe + arbitration**
   - Group members swipe shortlist options; organizer sees conflict heatmap and tie-break suggestions.
4. **Dual modes**
   - **Planning mode**: build candidate day plans.
   - **Travel mode**: execute plan with fallback suggestions when constraints change.
5. **Chatbot copilot (bounded)**
   - Uses captured constraints + current plan context only.
   - Produces alternatives, not generic long-form travel essays.
6. **Day-plan output + fallback**
   - Primary plan + 1 fallback option per critical time block.

### OUT (kill-list for V1)
- End-to-end booking engine.
- Open-ended destination inspiration feed/social layer.
- Full map/navigation replacement.
- Unlimited free-form AI conversation detached from constraints.
- Complex loyalty/rewards monetization mechanics.

Rationale: protect wedge and avoid me-too scope (C-117, C-120, A-104).

---

## 3) End-to-end user journey (V1)

## Step 0 — Trip creation
Organizer creates trip room and invites participants.

## Step 1 — Onboarding + QCM (5–7 minutes target)
Each participant answers a compact QCM:
- non-negotiables (must-have / must-avoid)
- intensity and pace
- child-specific constraints (if relevant)
- budget guardrails
- reservation sensitivity tolerance

Output: normalized constraint profile per user + group aggregate.

## Step 2 — Candidate generation (constraint-aware)
System proposes a ranked set of day blocks (morning/afternoon/evening), each with confidence and risk flags.

## Step 3 — Collaborative swipe
Participants swipe options:
- right = keep
- left = discard
- up = strong preference

Organizer gets:
- consensus score
- conflict alerts
- suggested compromise variants

## Step 4 — Plan lock (Planning mode)
Group locks day plans with explicit plan A/plan B per day.

## Step 5 — Travel mode execution
During trip, users can trigger “re-plan this block” when conditions shift (weather/closure/fatigue).
Chatbot proposes alternatives constrained by existing profile and logistics.

---

## 4) Information architecture (screens/modules)

1. **Trip Room**
   - Participants, status, readiness.
2. **Constraint Capture**
   - Onboarding + QCM forms.
3. **Option Deck**
   - Swipe cards with key metadata (family fit, effort, timing risk).
4. **Consensus Board**
   - Where disagreements are visible and resolved.
5. **Plan Timeline**
   - Day-by-day plan A/B.
6. **Travel Mode Console**
   - Live adjustments + chatbot actions.

---

## 5) Core loop definition (what must repeat)

1. Capture constraints
2. Generate constrained options
3. Collect group preference signal
4. Resolve conflicts transparently
5. Lock executable day plan + fallback
6. Adapt in travel mode without losing shared context

Success of V1 depends on loop completion speed and perceived stress reduction (estimate, to validate in TASK-132/133).

---

## 6) Chatbot scope (strict)

### Allowed
- Explain why an option is (or is not) recommended given constraints.
- Offer 2–3 alternatives for a failing day block.
- Summarize trade-offs between two candidate plans.

### Not allowed in V1
- Broad “plan my whole trip from scratch” without QCM context.
- Claims requiring live data certainty when unavailable.
- Financial/booking commitments.

---

## 7) MVP data model (minimal)

- Trip
- Participant
- ConstraintProfile
- OptionCard
- SwipeSignal
- ConsensusState
- DayPlan (A/B)
- Alert/Event (constraint change)

This model supports collaboration and adaptation without overbuilding.

---

## 8) UX principles

1. **Constraint clarity over inspiration overload**
2. **Disagreement made visible, not hidden**
3. **Every day has a fallback**
4. **AI suggestions must reference constraints explicitly**
5. **Organizer cognitive load is a first-class metric**

---

## 9) V1 success metrics (product-level)

- Time-to-first-viable-plan (target: <20 min for first full day draft) [À VALIDER]
- QCM completion rate (target: >80% invited participants) [À VALIDER]
- Consensus convergence rate (target: >70% of day blocks locked without external chat threads) [À VALIDER]
- Re-plan usefulness score in travel mode (self-report) [À VALIDER]

All numeric targets are estimates pending validation in later tasks.

---

## 10) Decision summary for TASK-131

**Go-forward design:** Keep V1 intentionally narrow around the wedge
- onboarding/QCM,
- collaborative swipe arbitration,
- planning vs travel mode,
- bounded chatbot,
- executable plan + fallback.

**Do not add** booking, social feed, or generic AI planner features in this phase.

This satisfies TASK-131 acceptance target: scoped MVP journey + kill-list + core loop definition.
