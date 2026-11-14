# Iteration, decision and stop rules

Use for substantial implementation or investigation; for a trivial task, apply the same judgments without creating a formal artifact. User-provided constraints and stop instructions take precedence. An iteration is an evidence-informed change to a candidate approach followed by the relevant comparable validation; compiling, a broken harness, waiting, changing random parameters or a failed network connection is not an efficacy result. Diagnose such infrastructure failures separately and do not misreport them as product results.

## Decisions and executable plan

- ChatGPT proposes the architecture, material dependencies, approach selection, measurable gates and fallback. Codex checks facts, feasibility, consistency, security, rights, cost and alignment with the user's objective before accepting; it owns execution and acceptance.
- Codex handles nonmaterial implementation details and clear local fixes without waiting. Escalate to ChatGPT with evidence when an architecture or benchmark assumption fails, requirements or materially consequential costs change, a major blocker persists, or iteration limits are reached. No invented approvals; user authorization and privacy constraints remain in force.
- Ask for a phase-by-phase implementation contract: objective, exact affected modules and interfaces, inputs, outputs and state, dependencies and sequencing, implementation steps, tests and observable pass/fail criteria, failure mode, rollback and stop/pivot criteria. If external APIs or facts are uncertain, identify how to verify them. Convert each accepted phase into a checklist and link evidence to each item; use a compact list for small work.

## Efficient change-and-test cycle

1. Start from the actual baseline and current authoritative source; inspect related failures and shared components in one pass. Group symptoms by likely root cause and boundary, separate symptoms from causes, and avoid editing the same place repeatedly without learning why it fails.
2. Before a meaningful experiment, record the hypothesis, candidate change, expected measurable effect, comparable baseline, validation and what both pass and fail would imply. Define a meaningful improvement in terms of the user's goal, not merely a local metric. Where competing requirements trade off, preserve coverage, quality and speed together; do not count suppressed outputs, hidden failures or relaxed targets as a win.
3. Implement a coherent change set. Batch compatible changes when they share a known cause and can be validated together; keep conflicting or independent experimental variables separate when attribution matters. Perform focused local/negative checks first, integration at the phase boundary, and the required real user-path acceptance on the resulting build. Avoid retesting unchanged, already-passed areas without a new risk; never skip checks required by the repository or user.
4. Capture the actual result, conditions and uncertainty, and update the single project decision record. Independently owned parallel work may proceed only if authorized and free from conflicting edits, shared-state races and duplicate external calls. Integrate and verify the combined result.

## When to continue, diagnose or change route

- **Continue the approach:** before the stop condition is reached, the benchmark shows a meaningful, comparable improvement toward the user goal, regressions are acceptable under agreed criteria, and a concrete next step remains; or a newly evidenced root cause has a discriminating, bounded fix. After the stop condition is reached, apply the escalation gate below before any further candidate. Do not claim improvement from noisy, non-comparable or insufficient data.
- **Diagnose before another attempt:** a required metric cannot be measured reliably, reference data or controls are missing, a test tool is broken, a single result is ambiguous, or there is an unexplained regression. Fix/verify the measurement first; do not keep changing the product or pay for repeated live requests until the result can distinguish alternatives. An ambiguous result is not evidence of no improvement.
- **Escalate and consider a different route:** a hard documented constraint prevents meeting a non-negotiable requirement; the approach breaches a relevant safety, license or budget limit; a well-controlled test shows it cannot satisfy the agreed tradeoffs; or the agreed limit on evidence-based iterations has been reached. If no limit was set, **after two comparable, evidence-informed iterations with no meaningful improvement**, stop tuning this approach and send ChatGPT the results. The default is a trigger to diagnose and decide, not proof the approach is impossible and not permission to reduce scope. One clearly infeasible or harmful result can justify earlier escalation; user-specified thresholds override this default.
- **Unavailable planner at the stop gate:** do not run another proposed solution or candidate test on the stalled approach, even as a seemingly small or obvious correction. Record and report the blocker and evidence; gather existing evidence or verify measurement integrity read-only and continue unrelated authorized work. Resume the approach after ChatGPT's evidence-based review or a clear user instruction authorizing the next attempt. User instructions and higher-priority requirements take precedence.
- **Decision after escalation:** compare continuing, using an established alternative, changing implementation/model/service or requesting a user decision on a genuine scope/cost tradeoff. Adopt a new route only if supported by evidence and it fits the authorized objective. If the same route remains defensible, record the distinct new hypothesis, measurable expected gain, capped next experiment and stop condition. Do not repeat essentially identical tests in hope of a lucky result.
- **Stop as requested:** honor an explicit pause, stop rule or spending limit. Do not claim the overall goal is complete merely because a local experiment passes or a route is abandoned.

## Evidence packet when returning to ChatGPT

Always include: expected behavior and acceptance target; actual behavior and exact reproduction; environment/version and sanitized errors; what was tried and results/cost; baseline and candidate metrics with units, sample count, identical or different inputs/conditions and start/end definitions; evidence strength and what remains unproven; likely root-cause hypotheses; constraints and the precise decision requested. Link or cite authorized source evidence, and label competitor results as measured versus documented claims. Exclude secrets and unauthorized private data.

## Durable project decision record

Maintain one discoverable, lightweight note for complex or continuing work, updated at decision or acceptance milestones rather than on every action:

- User goal, accepted constraints, benchmark and immutable acceptance targets; decisions needing user input.
- Candidate/accepted/rejected plan, reasons, source evidence and actual ChatGPT advice versus Codex judgment; current versions and affected modules.
- Milestone checklist mapping deliverables to actual implementation and acceptance evidence; before/after benchmark, failed tests, sample/measurement limitations and pending end-to-end checks.
- Attempts, root causes tested, next bounded hypothesis, remaining budget/stop condition and exact next safe action. Link authoritative artifacts; omit secrets and private content.

On context continuation, inspect the current code and process state rather than treating the note as live truth. Preserve approved decisions and avoid repeating completed tests unless new evidence warrants it.
