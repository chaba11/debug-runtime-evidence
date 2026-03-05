# debug-runtime-evidence

A [skills.sh](https://skills.sh) skill for AI coding agents that enforces hypothesis-driven debugging with mandatory runtime instrumentation. No guessing — only log-proven fixes.

## Install

```bash
npx skills add chaba11/debug-runtime-evidence
```

## What it does

Forces your AI agent through an 8-step debugging loop:

1. **Intake** — Understand the bug and reproduction steps
2. **Codebase Exploration** — Read code paths before hypothesizing
3. **Generate Hypotheses** — 3-5 testable hypotheses with predicted log output
4. **Add Instrumentation** — Mandatory `[DEBUG-H<N>]` logging (cannot be skipped)
5. **Reproduce** — User reproduces with instrumentation active
6. **Analyze Evidence** — Classify each hypothesis: CONFIRMED / REJECTED / INCONCLUSIVE
7. **Fix and Verify** — Fix only confirmed causes, re-verify with logs
8. **Clean Up** — Remove all debug instrumentation

The key constraint: **the agent cannot propose a fix until runtime logs confirm a root cause.**

## Usage

### Slash command

```
/debug Login fails silently when email has uppercase letters
```

### Auto-triggered

The skill activates automatically when you ask the agent to debug, investigate, or add logging.

## How it differs from general debugging

Most debugging skills say "be systematic." This one **enforces a specific loop**:

- Hypotheses must predict exact log output
- Instrumentation is a mandatory gate — not optional
- Evidence is analyzed per-hypothesis before any fix is attempted
- Fixes are verified with before/after log comparison

## Supported languages

Built-in logging templates for: JavaScript/TypeScript, Python, Go, Ruby, Rust, and Shell.

Works with any language — the `[DEBUG-H<N>]` prefix convention is universal.

## License

MIT
