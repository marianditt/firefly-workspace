# Firefly Workspace

## Repositories

- `firefly-monorepo/` — Application code (web, API, packages). Full guidance there.
- `firefly-infra/` — Infrastructure as Code (GitOps, k8s). Full guidance there.

Each repo is an **independent git repository** with its own remote origin. The
workspace `.gitignore` excludes both to prevent cross-repo leakage.

**Working with sub-repos:**
- Code changes inside `firefly-monorepo/` or `firefly-infra/` must be committed
  and pushed from within that directory — the workspace git does not track them.
- Path-scoped `AGENTS.md` files inside each repo provide detailed guidance.
- Subagents are in `.opencode/agent/`.

## Guardrails

1. Security is the highest priority.
2. EU legal and platform compliance are mandatory (GDPR, DSA, accessibility, consent, retention, auditability).
3. Correctness against approved requirements and ADR decisions.
4. Cost efficiency in build, runtime, storage, and operations.

## AI token efficiency

Be concise.

Prefer:
- bullet lists
- short explanations
- minimal repetition
- direct answers
- concrete recommendations
- diffs over restating existing code

Avoid:
- introductions
- conclusions
- motivational text
- unnecessary examples
- repeating the prompt
- summarizing unless requested
- emojis

## Delivery

- Work test-first by default in `firefly-monorepo/`.
- Keep `main` releasable: prefer small, merge-safe increments.
- Preserve or improve quality standards; never lower the bar.
