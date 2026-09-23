# Rubric: is this a good first issue?

This rubric answers a narrow question: is the issue a sensible first
contribution **now**, based on evidence a second reviewer can inspect? A label
such as `good first issue` is useful context, but it never overrides a required
check.

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| Repository is writable | The repo line's `archived:` value in the repo-facts block. In live mode, use the archived banner or repository metadata described in `references/evidence-guide.md`. | Pass only when `archived: no`. Fail when the repository is archived. If the archived state is absent, grade `unclear`. | required |
| Recent project activity | The bundle capture date; `last push to any branch`; latest release date; and the last 5 default-branch commit dates and authors in the repo-facts block. In live mode, inspect the repository front page, commit history, branches, and Releases. | Pass when at least one of these occurred within the 365 days before capture (or today in live mode): a push, a release, or a default-branch commit showing human work. A bot merge of a human PR counts as human work; dependency/version churn by bots alone does not. Fail when every qualifying signal is older than 365 days. Grade `unclear` only if none of the named dates is available. | required |
| Bounded and implementable | The issue title and body, its acceptance criteria or expected behavior, named files/components, and the full comment thread. Also inspect closed linked PRs when the bundle or live issue identifies them. | Pass when the issue requests one testable outcome, even if that outcome needs several related edits, and the body or a maintainer comment provides enough settled behavior, examples, or code surface to begin. A terse issue may pass when it still names the faulty or desired behavior. Fail for a support question; an umbrella/tracking issue; an open-ended codebase-wide campaign; an issue whose essential product/design choice is still unresolved; or a thread with at least two abandoned attempts and no settled current implementation direction. If the available text cannot distinguish these cases, grade `unclear`. | required |
| Work is available | `this issue: assignees` and `linked PRs` in repo facts, plus claim comments, PR links, release/abandon messages, and maintainer replies in the issue thread. In live mode, inspect the Assignees and Development sidebars and the complete thread. | Pass when there is no assignee, no open linked or thread-mentioned PR, and no unreleased claim from the last 30 days. An old claim passes only when a later maintainer/bot message releases it or explicitly invites new contributors. Any assignee or open PR fails regardless of age. Apply a scoped repository's house rule when it explicitly changes which claim comments count. Missing assignee or PR evidence is `unclear`, not a pass. | required |
| AI-assisted contribution allowed | The `contribution policy` line in repo facts. In live mode, inspect root or `.github/CONTRIBUTING.md`, linked contributor docs, dedicated AI policy files, and PR templates as described in `references/evidence-guide.md`. | Fail only for an explicit ban on AI-generated or AI-assisted code/documentation, because this course requires an AI-assisted workflow. Pass for silence and for conditions such as disclosure, testing, personal understanding, or human review. If the policy points elsewhere and that referenced policy is unavailable, grade `unclear`. | required |
| Maintainer engagement | The maintainer first-response sample, issue author's association, and Owner/Member/Collaborator comments in the issue thread. In live mode, use the same surfaces in `references/evidence-guide.md`. | Pass when at least one sampled issue received a maintainer response within 30 days, this issue was filed by a maintainer, or a maintainer gave actionable direction in this thread within 30 days. Fail when the evidence shows no qualifying response. Use `unclear` when response timing and author association are both unavailable. | preferred |
| Newcomer guidance | The issue's labels, body, and maintainer comments, especially named files/components, reproduction steps, acceptance criteria, a test command, or a `good first issue`/equivalent label. | Pass when at least one explicit newcomer signal is present: a newcomer label, named starting files/components, reproducible steps, objective acceptance criteria, or a maintainer-provided verification method. Fail when none appears; `unclear` only when the issue text is missing. | preferred |

## Verdict rule

Accept only if every `required` check passes. Reject when any required check
is `fail` or `unclear`; uncertainty at a gate means the risk has not been
cleared. Preferred checks never change `accept` or `reject`: use them only to
rank issues that already pass every required check. An `unclear` preferred
check remains `unclear` and does not affect the verdict.
