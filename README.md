# External RCA Translation Guide

## Why this exists

Most external RCAs fail not due to lack of information, but due to poor **translation** of internal understanding into customer clarity.

This guide shows how to go from:
> **accurate internal RCA → clear, confident external RCA**

For real examples, see the RCA repository.  
This guide focuses on how to think, not exhaustive examples.

---

## When to use this

Use this **after the internal RCA is finalized and validated**.

---

## Core Principle

> **Do not rewrite the internal RCA. Distill it.**

- Remove noise  
- Preserve truth  
- Improve clarity  
- Increase customer confidence  

---

## The Transformation

Final Internal RCA  
↓  
Extract final root cause (ignore hypotheses/history)  
↓  
Identify customer impact (who, what, duration, symptoms)  
↓  
Simplify causal chain (trigger → failure → impact)  
↓  
Strip internal-only details  
↓  
Translate into customer language  
↓  
Reframe actions → prevention  
↓  
External RCA  

---

## Strip vs Keep

**Remove**
- Investigation steps / dead ends  
- Multiple hypotheses  
- Internal escalation or process detail  
- Debug-level logs and metrics  

**Simplify**
- Internal system names → general terms  
- Deep technical layers → causal chain  

**Keep (and strengthen)**
- Final root cause  
- Customer impact  
- Mitigation  
- Preventative actions  

---

## Root Cause: Compress the Chain

Internal RCAs often look like:  
A → B → C → D → E → Impact  

External RCA should be:  
**Trigger → Failure → Customer Impact**

**Rules:**
- If it doesn’t change customer understanding → remove it  
- If steps are tightly coupled → merge them  
- Translate internal terminology  

---

## Translate to Customer Language

Always convert:
> **System behavior → Customer symptom**

Examples:
- Task queue backlog → Delays in processing  
- Shard imbalance → Uneven system load  
- Retry amplification → Increased load from retries  

**Test:**  
Could a customer understand this without knowing our system?

---

## Actions Must Build Confidence

Weak:
- “Fixed bug”
- “Improved monitoring”

Strong:
- “Prevents duplicate execution under concurrent conditions”
- “Detects and mitigates delays before customer impact”

**Rule:**
> Every action must clearly map to a **prevented failure mode**

---

## Anti-Patterns

Avoid:
- “Unexpected issue occurred”  
- Mixing symptoms with root cause  
- Multiple causes without a causal chain  
- Investigation detail leaking into RCA  
- Actions that don’t reduce recurrence  

---

## Before / After Example

**Internal RCA**  
Shard rebalancing caused task queue saturation due to uneven partition ownership. Retry amplification increased load.

**External RCA**  
A system rebalancing event caused uneven load distribution, leading to delays in workflow processing. Retry behavior increased system load, extending the duration of impact.

---

## Final Check (Before Sending)

- [ ] Root cause is a clear causal chain  
- [ ] Impact is customer-specific and time-bound  
- [ ] No internal-only detail remains  
- [ ] Language is customer-safe  
- [ ] Actions clearly prevent recurrence  
- [ ] Readable in one pass  

---

## One-line Test

> If a customer reads only the summary, do they understand what happened, whether they were impacted, and whether it will happen again?

When in doubt, bias toward **clarity over completeness**.
