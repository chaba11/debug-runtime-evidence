---
description: Debug with runtime evidence and hypothesis-driven instrumentation
argument-hint: [describe the bug]
---

Debug the following issue using the `debug-runtime-evidence` skill:

**Bug report:** $ARGUMENTS

Follow the full 8-step workflow — no shortcuts:

1. **Intake** — Understand the bug and reproduction steps.
2. **Codebase Exploration** — Read relevant code paths before hypothesizing.
3. **Generate Hypotheses** — Produce 3-5 testable hypotheses with predicted log output.
4. **Add Instrumentation** — MANDATORY. Add `[DEBUG-H<N>]` logging to test each hypothesis.
5. **Reproduce** — Ask the user to reproduce and share log output.
6. **Analyze Evidence** — Classify each hypothesis as CONFIRMED / REJECTED / INCONCLUSIVE.
7. **Fix and Verify** — Fix only confirmed root causes, re-verify with logs still active.
8. **Clean Up** — Remove instrumentation after user confirms the fix.

Do NOT skip Step 4 (instrumentation). Do NOT propose a fix before Step 6 (evidence analysis).
