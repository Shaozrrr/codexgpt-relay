# Handoff templates

Use only fields relevant to the task. Do not send this template verbatim with empty headings. Prefer concise, reproducible evidence to a long conversation dump. Never include credentials or private information without specific authorization.

## Initial plan request

> You are the planning partner; Codex will independently review, implement and verify. Produce a complete executable plan, but distinguish facts from hypotheses and avoid claiming you inspected artifacts you have not seen.
>
> **Outcome and scope:** [user's goal, audience, explicit exclusions and accepted decisions].
> **Current verified state:** [project/runtime/version, architecture, key interfaces, relevant files or sanitized excerpts, actual existing behavior]. Mark mock/prototype/installed/production separately.
> **Evidence and history:** [exact trigger and expected vs observed behavior; meaningful measurements with units, sample sizes, collection conditions and baselines; prior attempts and why they did or did not work].
> **Benchmark and comparable projects:** [user-relevant metrics and thresholds with source; actual before baseline, cases and reference; relevant competitor/project version and primary links; observed behavior versus documented claims; missing comparisons and constraints].
> **Constraints:** [environment, performance, security/privacy, compatibility, cost, deadline, existing tools and authorization].
> **Uncertainties:** [what is missing, confidence, evidence not collected, competing hypotheses].
> **Request:** For each prioritized phase specify the exact affected modules, interfaces, inputs/outputs and relevant state, dependencies, implementation sequence, representative tests and observable pass/fail criteria. Include suitable established examples or official sources, failure handling, compatibility, costs, rollback, and explicit continue/diagnose/pivot conditions. Explain alternatives and tradeoffs. Cite primary sources for current technical claims. Specify what Codex must verify and what cannot be guaranteed. Do not change scope or weaken a target without explicitly describing the tradeoff. Codex will translate the accepted plan into a checklist with evidence for each phase.

## Plan challenge or blocker

> **Decision under review:** [specific claim/step].
> **What the plan predicted:** [expected behavior].
> **What the actual environment shows:** [reproduction, exact sanitized error or data, version, sample, source or command outcome].
> **Already attempted and cost:** [what was tried, number of calls, results; state if further testing is paid].
> **Comparability:** [same or different input, build, environment, metric definition and sample; measured baseline versus candidate; what the data can and cannot prove].
> **Iteration decision:** [prior limit, meaningful-improvement criterion, number of comparable evidence-informed iterations; whether the issue is measurement, implementation or a hard constraint; candidate alternatives].
> **Why the current plan does not fit:** [contradiction, unverified assumption, risk, incompatibility, or missing prerequisite].
> Recommend the smallest useful next action, alternatives, what each outcome would prove, and a stop condition. Preserve [user requirements]. Clearly identify any hypothesis that remains unverified. Do not repeat earlier attempts without new evidence.

## Incremental update or replanning

> **Agreed plan and constraints:** [short summary, including user corrections].
> **Completed and verified:** [what changed, where, test environment and actual result].
> **Not yet verified:** [specific gaps].
> **New observation:** [evidence and impact].
> **Decision needed:** [one or a few focused questions, with options and tradeoffs]. Keep the rest of the accepted plan unless the evidence requires a change.

## Acceptance review request

> Review this work against the original requirements, using only the evidence supplied. Do not infer that a test, deployment or feature succeeded from an implementation description.
>
> **Requirements and criteria:** [each deliverable and its intended behavior].
> **Changes:** [concrete final behavior, relevant locations/versions and scope].
> **Results:** [test cases and actual outcomes, failures, sample sizes, latency/error metrics and their definitions; real vs simulated/replay; installed vs development build; before/after comparability].
> **Benchmark comparison:** [baseline versus candidate and relevant comparator on the same cases; quality, coverage, performance, usability, reliability and cost where material; raw counts, scope, conditions, incomparability and uncertainty].
> **Gaps and caveats:** [untested scenarios, missing independent ground truth, system conditions, cost and permissions].
> For each requirement classify: proven / contradicted / incomplete / insufficient evidence. Identify material gaps or regressions, decide pass/fail/not yet determinable, and recommend the smallest useful next step with a stop condition. Do not lower standards silently or ask to rerun passing tests without a reason.

## Compact continuation handoff

Preserve: user's objective and non-negotiable constraints; accepted design and model decisions; authoritative current branch/build/deployment and artifact paths; completed changes with tests and measured evidence; in-flight process handles and checkpoints; exact unresolved issues and known blockers; next safe step. Distinguish what ChatGPT suggested from what Codex actually verified. Omit secrets and unrelated history.
