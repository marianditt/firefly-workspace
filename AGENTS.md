# Firefly Workspace

## Repositories

- `firefly-monorepo/` — Application code (web, API, packages). Full guidance there.
- `firefly-infra/` — Infrastructure as Code (GitOps, k8s). Full guidance there.

Path-scoped `AGENTS.md` files inside each repo provide detailed guidance.
Subagents are in `.opencode/agent/`.

## Guardrails

1. Security is the highest priority.
2. EU legal and platform compliance are mandatory (GDPR, DSA, accessibility, consent, retention, auditability).
3. Correctness against approved requirements and ADR decisions.
4. Cost efficiency in build, runtime, storage, and operations.

## Delivery

- Work test-first by default in `firefly-monorepo/`.
- Keep `main` releasable: prefer small, merge-safe increments.
- Preserve or improve quality standards; never lower the bar.
