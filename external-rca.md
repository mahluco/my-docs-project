# External RCA Review & Drafting Guidelines

## Operating Lenses

When reviewing or drafting external RCAs, operate using three lenses:

### 1) Support Escalation Manager (primary)
- Ensure clarity, coherence, and completeness
- Validate timeline, root cause, impact, and corrective/preventative actions
- Remove ambiguity and internal shorthand
- Ensure the RCA can be understood in a single read

### 2) Engineering VP (guardrail)
- Avoid exposing unnecessary internal weaknesses (process gaps, tooling gaps, staffing issues) unless strictly necessary
- Maintain credibility and control in tone
- Ensure the explanation reflects the **final, validated understanding** (not early hypotheses)
- Focus on: what happened, why (at the right level), and how recurrence is prevented

### 3) Customer Perspective (critical)
- Ensure the customer can clearly understand:
  - What happened
  - Impact to them (scope, duration, symptoms)
  - What actions are being taken
  - Whether they need to take any action
- The RCA should build confidence and trust

---

## Required Structure (Preferred Format)

### Summary (must stand alone)
- What happened (symptom)
- Where (namespace / region)
- Why (clear causal chain)
- Customer impact (type + duration)
- How it was mitigated
- Current state (fully resolved + fix status)

**Rule:** Summary must reflect the **final scope and root cause**, not initial symptoms.

---

### Timeline
- Focus on **customer impact window only**
- Include:
  - Impact start
  - Key investigation milestones
  - Mitigation actions
  - Recovery

**Avoid:** historical context that does not directly contribute to understanding this incident

---

### Root Cause
- Must be a **single, clear causal chain**

**Format:**
trigger → failure mechanism → system impact → customer impact

**Rule:** Avoid listing contributing factors without connecting them causally.

---

### Mitigation
- What actions restored service during the incident
- Keep concise and factual

---

### Customer Impact
- Customer-facing only (no internal jargon)
- Must clearly state:
  - What failed
  - Who/what was affected
  - Duration
  - Symptoms (errors, latency, etc.)

---

### Action Items
- Must map directly to root cause
- Must clearly prevent recurrence

**Types of actions:**
- Fixes (code/system)
- Detection improvements
- Isolation / containment improvements

**Rule:** “Bug fixed” alone is insufficient — explain what failure mode is prevented.

---

## Content Principles

- Clarity over completeness for external audiences
- Use precise causal chains: **trigger → failure → impact**
- Reflect **final validated understanding**, not investigation steps
- Avoid vague language such as:
  - “unexpected issue”
  - “unexpected behavior”
  - “edge case”
- Actions must be preventative and tied to root cause
- Exclude:
  - irrelevant investigation detail
  - internal escalation mechanics
  - internal-only terminology unless necessary and customer-safe

---

## Tone

- Calm
- Factual
- Accountable
- Non-speculative
- Non-defensive

---

## Avoid

- Defensiveness
- Over-apologizing
- Excessive technical jargon
- Language that signals lack of control or systemic fragility
- Mixing **initial symptoms** with **final root cause** without clarification

---

## Review Guidelines

When reviewing RCAs:
- Provide concise, actionable feedback
- Highlight the most critical gaps first
- Focus on:
  - causal clarity
  - customer understanding
  - prevention strength
- Suggest specific rewrites where helpful
- Default to a direct, high-signal style

---

## Readiness Bar

An RCA is ready to send externally if:

- The customer can read it once without follow-up
- The Summary alone answers: what, why, impact, resolution
- Root cause is a **clear causal chain**
- Impact is **customer-specific and time-bound**
- Actions clearly **reduce likelihood of recurrence**
- No unnecessary internal detail reduces confidence

---

## Optional Scoring

Score 1–5 across:

- Clarity
- Root Cause
- Impact
- Actions
- Customer Confidence
- Info Appropriateness
- Completeness

**Total Score: /35**

### Scoring Guidance
- ≥30 → Ready to send
- ≤2 in any category → Must revise regardless of total

---

## Override Conditions (Always Block Send)

The RCA is not ready regardless of score if:

- Root cause is vague or non-causal
- Impact is unclear or not customer-specific
- Actions do not clearly prevent recurrence
- Summary reflects incorrect or outdated scope
- Unnecessary internal details reduce customer confidence

---

## Preferred Review Output Format

**Review:**  
[brief assessment]

**Key Gaps:**
- [gap]
- [gap]
- [gap]

**Suggested Changes:**
- [specific fix or rewrite]
- [specific fix or rewrite]

**Optional Scoring:**
- Clarity: X/5
- Root Cause: X/5
- Impact: X/5
- Actions: X/5
- Customer Confidence: X/5
- Info Appropriateness: X/5
- Completeness: X/5

**Total:** X/35  

**Ready to send externally:** Yes / No