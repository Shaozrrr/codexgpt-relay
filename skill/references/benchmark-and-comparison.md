# Benchmark and comparison guidance

Use this for a substantial collaboration where a baseline, measurable quality or competitor comparison will inform the plan. Scale effort to the task: an ordinary small change may need only a short before/after check. The benchmark serves a user decision; it is not permission to create a large test program, send private information, make purchases or run unbounded paid experiments.

## Define before measuring

1. Convert user outcomes into observable criteria and separate mandatory requirements from aspirational targets. Record who set each threshold and why; proposed engineering targets are not vendor guarantees or industry standards. Clarify any missing condition that cannot reasonably be inferred.
2. Identify the actual baseline: version/commit, build, configuration and environment, data source, deployment and known limitations. Preserve original behavior only as needed for a fair comparison. If it cannot be measured, mark **no baseline**, never invent one.
3. Choose a small representative suite covering common user journeys, important edge/failure cases and relevant languages/devices/data sizes. Use public, synthetic or user-authorized fixtures as appropriate; preserve input identity/version and an independent ground truth. Do not treat a service's own output as objective truth. Note fixture licensing and storage rules.
4. Define metrics before running: exact start/end events and units; what counts as success, error or timeout; denominator, aggregation, sample independence and warm/cold conditions. For interface tasks record observable readability, interaction and accessibility states as well as timing; qualitative judgment should have explicit rubric and examples. Record cost where material.
5. Predetermine the test sequence, limits, number of paid requests, stop/rollback conditions and which decisions each test can change. Validate the harness on local/fake data first when it prevents false claims or wasted calls. Once evidence is adequate, stop; do not run more trials simply to get a passing result.

## Select comparators when useful

Choose relevant products or open-source implementations for the same user scenario and comparable platform or environment. Prefer a small set of representative alternatives, including a mature or established implementation and any user-specified competitor; include their exact version, configuration and source links. Search official documentation, project code/releases and license first, and check maintenance, platform compatibility, dependencies and security before recommending reuse. Consult other available research/design skills if they fit. When examples are unavailable, inaccessible, not authorized or expensive to test, state the limitation rather than inventing results or blocking unrelated work.

Differentiate:

- **Observed/tested**: what was actually run or inspected, by whom, on which build, under which conditions.
- **Documented/claimed**: current official capabilities, pricing or vendor benchmark claims, with source and date; not treated as independent proof.
- **Inference/unknown**: unverified implementation details, quality, speed, behavior or missing coverage.

Do not assume a competitor's UI implies a particular architecture or an outcome observed elsewhere. Assess UX/accessibility, functional coverage, quality, latency, reliability and cost as relevant; do not reduce all quality to one number. Reuse permitted implementation patterns and libraries, verify licenses and attribution, and comply with the user's intended distribution. Benchmarking is not an instruction to copy branding, proprietary assets or inaccessible source code.

## Make the comparison fair

Use the same inputs, reference answers, time anchors, scope and metrics for baseline and candidate where feasible; use a fixed seed/configuration or same event replay when valid. For live services, document that separate calls can differ; use the same source material, environment and timing protocol and do not claim a paired result unless both truly share the relevant input/events. Log failures and timeouts in the denominator; disclose missing timestamps, selection/exclusion and clock drift. Do not compare API arrival with actual visual display or raw word error with translation quality. Report raw counts, sample size, distributions only when meaningful, units, and measurement uncertainty. Distinguish a statistical signal from a one-off observation; avoid broad claims based on a few samples.

Include task-relevant quality tradeoffs: output coverage vs correctness, latency vs revision, fidelity vs conversion loss, resource use vs availability, and real user experience vs laboratory proxies. Do not treat suppressing outputs or lowering a threshold as an improvement by itself. If a fair test cannot be performed, report the two values separately, mark not directly comparable and explain the missing baseline or necessary independent evaluation.

## Review and decision with ChatGPT

Provide ChatGPT a sanitized evidence packet with benchmark purpose, fixed criteria, versions, input provenance, environment, exact methodology, baseline/candidate/competitor measurements, sample counts, errors, cost and limitations. Label official claims separately. Ask it to classify each requirement as satisfied, failed or not established, explain meaningful improvements and regressions, identify the most likely bottleneck and propose the smallest next discriminating action. Have it compare alternative plans against the user goal and stop conditions, not against a post-hoc reduced target.

Codex checks its reasoning against the source measurements and executes an accepted next step. If a benchmark fails repeatedly, determine whether the test, implementation, service capability or the target itself is responsible before further changes; present evidence and tradeoffs rather than trial-and-error. Any proposal to change the user's requirements or incur an unauthorized consequential cost requires the appropriate user decision.

## Compact project record

When the project merits a durable note, keep one discoverable record with:

- Objective, non-negotiable requirements, user decisions and current status.
- Accepted/rejected approaches with reasons and primary links; record who made a decision, not as an appeal to authority.
- Baseline and benchmark definitions, versions, fixtures/reference, environment and dated actual results including failures; distinguish prototype, installed and public builds.
- What was sent to ChatGPT, its recommendation versus Codex's independent judgment, and the next concrete step.
- Tests still due, constraints and blockers; links to result artifacts, excluding credentials and private content.

Update at meaningful milestones; avoid duplicate copies, verbose logs and repetition of checks that have already passed without a new reason.

## Minimal experiment record

For a repeated or decision-relevant measured trial, append a concise entry to the existing benchmark record. Set meaningful improvement, experiment and cost limits before testing; respect user limits. Record actual paid usage when relevant. Keep the same fixtures and metric definitions where possible; explicitly mark missing baselines and non-comparable results. Do not use this template as a requirement for ordinary small changes.

```text
Question / hypothesis and decision this test can change:
Case, reference, version, environment and metric definitions:
Baseline and target / source of target:
Change and controlled variables:
Result, failures, sample size, cost and evidence link:
Decision: continue / diagnose / pivot; reason, next bounded step and stop condition:
```

For evaluating this skill's efficiency, compare representative similar tasks with and without it using the same scope and acceptance standard. Record total input/output tokens across both tools when available, elapsed time, cost, outcome and rework; note missing usage and confounders. One task or prompt length alone does not establish a general saving. Never claim a percentage without measured comparable data.
