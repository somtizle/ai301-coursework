# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

**Issue link**

https://github.com/codepath/pathreview-ai301-fa26-s1/issues/73

**Verdict output**

Here is the graded result for issue #73:

**Check-by-check summary**

| Check | Grade | Evidence |
|---|---|---|
| Repository is writable | **pass** | `isArchived: false`; repo was pushed to 2026-09-16, 6 days ago |
| Recent project activity | **pass** | Andrew Burke committed to `main` on 2026-09-16 (6 days before today) — human work, not bot churn |
| Bounded and implementable | **pass** | Single testable outcome: reconcile `README.md` and `.env.example` on the `OPENROUTER_API_KEY` variable; two relevant files named; 1–2 h effort estimate; no abandoned attempts |
| Work is available | **pass** | No assignees; no open or linked PRs against this issue; no claim comments (zero comments total) |
| AI-assisted contribution allowed | **pass** | No CONTRIBUTING.md exists; PR template lists testing checklist only — silence passes |
| Maintainer engagement _(preferred)_ | **pass** | Issue author `Aburke225` has `author_association: COLLABORATOR`; rubric passes when the issue was filed by a maintainer |
| Newcomer guidance _(preferred)_ | **pass** | Labels: `good first issue`, `tier-1`, `docs`, `bug`; named files: `README.md`, `.env.example`, `core/config.py`; explicit goal stated in body |

All four required checks pass → **accept**.

**Fit note:** This is a pure documentation/config reconciliation — no Python code to write, just two text files to bring into agreement. It sits squarely inside the student's stated preference for "contained … documentation change" and can be reproduced and explained from first principles in minutes. The `good first issue` + `tier-1` labels and named files mean there is no ambiguity about where to start or what done looks like.

```json
{
  "item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/73",
  "checks": [
    {
      "name": "Repository is writable",
      "grade": "pass",
      "evidence": "isArchived: false; last push 2026-09-16, 6 days before today"
    },
    {
      "name": "Recent project activity",
      "grade": "pass",
      "evidence": "Andrew Burke committed to main on 2026-09-16 — human work within 365 days"
    },
    {
      "name": "Bounded and implementable",
      "grade": "pass",
      "evidence": "One testable outcome: reconcile README.md and .env.example on OPENROUTER_API_KEY; two files named; no prior abandoned attempts"
    },
    {
      "name": "Work is available",
      "grade": "pass",
      "evidence": "No assignees, no open linked PRs, zero claim comments"
    },
    {
      "name": "AI-assisted contribution allowed",
      "grade": "pass",
      "evidence": "No CONTRIBUTING.md; PR template lists testing checklist only — silence passes"
    },
    {
      "name": "Maintainer engagement",
      "grade": "pass",
      "evidence": "Issue author Aburke225 has author_association: COLLABORATOR — issue filed by a maintainer"
    },
    {
      "name": "Newcomer guidance",
      "grade": "pass",
      "evidence": "Labels: good first issue, tier-1, docs, bug; named files README.md, .env.example, core/config.py; explicit goal in body"
    }
  ],
  "verdict": "accept"
}
```

---

## Eval iterations

Quote source text directly in each field below. Paraphrase does not satisfy them.

**Run history**

One complete evaluation run occurred:

> agreement: 19/20 scored items  (bar: 18/20: PASS)

**Issue analysis**

The only disagreement was:

> issue-15  reject  accept   NO     graded accept

My rubric returned `accept`; the gold label was `reject`. The issue describes
one observable payload transformation, the repository is active, AI assistance
is allowed, and no current assignee or open linked PR appears in the bundle.
Those signals led the grader to pass every required check. The gold reasoning
weighs the history more heavily: the thread contains years of design questions
and `linked PRs: zulip/zulip#20840 (closed); zulip/zulip#23123 (closed)`.
Although **Bounded and implementable** names “at least two abandoned attempts
and no settled current implementation direction,” the proposed command/text
behavior looked settled enough to the grader. The miss shows that the check's
conjunction is permissive when a long-running issue has a simple-looking final
sentence.

**Check rationale**

> **Bounded and implementable** — Pass when the issue requests one testable
> outcome, even if that outcome needs several related edits, and the body or a
> maintainer comment provides enough settled behavior, examples, or code
> surface to begin. A terse issue may pass when it still names the faulty or
> desired behavior. Fail for a support question; an umbrella/tracking issue; an
> open-ended codebase-wide campaign; an issue whose essential product/design
> choice is still unresolved; or a thread with at least two abandoned attempts
> and no settled current implementation direction. If the available text
> cannot distinguish these cases, grade `unclear`.

I wrote this around readiness rather than word count. A one-sentence maintainer
bug can be perfectly actionable, while a long thread can hide an umbrella task
or years of unresolved design. The check therefore asks whether a contributor
can name the finish line and start work without inventing a product decision.

**Trade-offs**

This check gives up a stricter “two closed PRs always means reject” rule. That
choice protects valid issues where an earlier implementation merely went stale
or failed CI, but it also caused the `issue-15` false accept in this run. I am
accepting that miss because the rubric still scored 19/20 and passed every
category floor, while an automatic closed-PR rejection could discard a now
well-specified issue that a maintainer has reopened to contributors. In future
use I would treat two abandoned attempts plus unresolved maintainer questions
as stronger evidence than a concise issue body.

> issue-15  reject  accept   NO     graded accept

---

## Selection rationale

Graded on whether all three are answered, in your own words. Not on how good the
reasoning is, and not on length — a short honest answer to each earns the full marks.
This is also the basis for the claim comment you write in Unit 2.

**Selection rationale**

1. Issue #73 fits both my experience and the available week. It is a contained
   documentation/configuration consistency bug in two named files, not a broad
   feature. I can trace `Settings` in `core/config.py`, make the documented
   environment variables agree, and verify the result without first learning a
   large subsystem. Its 1–2 hour estimate leaves time for setup, tests, and CI.

2. The verdict correctly identifies the repository as active, the work as
   bounded and available, the AI policy as non-blocking, and the issue as
   newcomer-friendly. The rubric cannot measure whether the documentation's
   final wording will be genuinely clear to a first-time user, so I also
   weighed the two files side by side and checked that the inconsistency is
   visible and objectively resolvable rather than a matter of writing taste.

3. Claiming should be low difficulty. The issue is unassigned, has no comments,
   and has no open PR reference. The Path Review house rule also says classmates'
   claim comments would not block it if one appeared before Unit 2. The main
   risk is timing: another student may open a PR first, but course credit is
   attached to the PR I open rather than exclusivity on the issue.

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
