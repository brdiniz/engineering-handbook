# 02. Code review

**Purpose:** reviews exist to improve the code and spread knowledge, not to gatekeep or to prove cleverness.

## For authors

- **Keep changes small.** Aim for a change a reviewer can understand in 15 to 30 minutes. Split larger work into a series of reviewable steps.
- **Write a useful description.** What is the problem, what did you change, how did you test it, and what should the reviewer focus on?
- **Review your own change first.** Read the diff as a reviewer would, and remove debug code and unrelated edits.
- **Tests and docs are part of the change.**
- **Respond to every comment**, either with a change or a short reason. Resolve a thread only when it is addressed.
- **Do not take it personally.** Comments are about the code.

## For reviewers

- **Respond quickly.** Target a first response within one working day. Slow reviews are a major cause of slow delivery.
- **Start with the big picture.** Does the change solve the right problem? Is the design sound? Then look at details.
- **Check correctness first:** edge cases, error handling, concurrency, security, data integrity, backwards compatibility.
- **Then maintainability:** naming, structure, duplication, test quality, documentation.
- **Distinguish the weight of your comments** using prefixes:
  - `blocking:` must be fixed before merge
  - `suggestion:` worth considering, author decides
  - `question:` I need to understand this
  - `nit:` minor style point, safe to ignore
  - `praise:` something done well
- **Ask, do not command.** "What happens if this list is empty?" works better than "Handle the empty case."
- **Do not block on personal style.** If a linter or formatter can settle it, automate it.
- **Approve when the change is good enough to improve the codebase**, even if it is not how you would have written it.

## What reviewers look for (checklist)

- [ ] The change does what the description says
- [ ] Tests cover the new behaviour and the likely failure cases
- [ ] Errors are handled and logged usefully
- [ ] No secrets, credentials or personal data in code or logs
- [ ] Inputs are validated and outputs are safe (injection, authorisation checks)
- [ ] Database changes are safe to deploy and roll back, and queries are indexed
- [ ] Public interfaces remain compatible, or the break is intended and communicated
- [ ] Performance impact is understood for hot paths
- [ ] Observability: metrics, logs or traces for new behaviour where it matters
- [ ] Documentation or runbooks updated

## Escalation

If author and reviewer disagree after one round, talk synchronously for ten minutes. If still stuck, ask the tech lead to decide, and record the reasoning in the pull request.

## Using AI assistants in review

AI-generated code and AI-assisted reviews are welcome as long as the author understands and owns the change. The author is accountable for correctness, tests and security regardless of how the code was produced. Reviewers apply the same standard to all code.
