# Temporal Terminology for External RCAs

For full definitions, see:
https://docs.temporal.io/glossary

This document provides **minimal guardrails** to ensure correct and consistent use of Temporal concepts in external RCAs.

---

## Core Concepts

- **Workflow**  
  Deterministic orchestration logic that defines the execution flow.

- **Activity**  
  Side-effecting work executed outside the workflow.

- **Worker**  
  Process that polls and executes workflows and activities.

- **Task Queue**  
  Routing and load-balancing mechanism for distributing work to workers.

---

## Common Misuse to Avoid

- Treating **Task Queues** as simple queues  
- Treating **Workflows** as stateless jobs  
- Mixing **Workflow** and **Activity** responsibilities  
- Using internal shorthand instead of canonical terms  

---

## RCA Usage Guidelines

- Use canonical Temporal terminology when describing system behavior  
- Prefer **clear, simplified explanations** over internal implementation detail  
- Translate:
  > system behavior → customer-visible impact  

- If unsure about a term, reference the official glossary before finalizing  

---

## Practical Examples

| Internal Description            | External RCA Language                  |
|--------------------------------|---------------------------------------|
| Task queue backlog             | Delays in processing                  |
| Worker starvation              | Work not being processed in time      |
| Retry amplification            | Increased load due to retries         |

---

## Final Check

Before sending an external RCA:

- [ ] Terminology aligns with Temporal concepts  
- [ ] No incorrect abstractions (e.g. “job”, “queue”)  
- [ ] Language is understandable without internal knowledge  
