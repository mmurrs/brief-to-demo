---
name: brief-to-demo
description: Turn a written brief, specification, requirements document, or rough concept into a tightly scoped, working product demo. Use when starting from source material and needing to identify users and motivation, separate evidence from assumptions, choose a golden path, build the smallest convincing prototype, and prepare it for a reliable demonstration. Do not use for ordinary feature work with an already-defined implementation plan.
---

# Brief to Demo

Convert source material into a demonstrable product argument, then into a working prototype. Preserve a visible chain:

`source evidence -> product decision -> demo moment -> observable proof`

The goal is not maximum feature coverage. The goal is the smallest end-to-end experience that proves the important idea.

## Operating principles

- Treat the source's stated direction and constraints as the mandate. Do not reopen them without evidence of a contradiction or material risk.
- Separate `Evidence`, `Inference`, `Assumption`, and `Unknown`. Never present one as another.
- Answer first, then support the answer with evidence.
- Ask no more than three questions, and only when different answers would materially change the product or build.
- Prefer one complete golden path over several partial workflows.
- Make each major screen or interaction prove a requirement, remove a pain, or test an assumption.
- Simulate unavailable integrations with deterministic fixtures and label the simulation. Never imply that a mocked integration is live.
- Keep the prototype easy to start, reset, and demonstrate.
- Do not deploy, publish, purchase, or mutate external resources without explicit authorization.

## 1. Intake the source

Read all supplied material before designing. If files are provided, inspect the authoritative files rather than relying on summaries when practical.

Determine:

- the requested outcome and deliverable;
- explicit users, workflows, requirements, constraints, and exclusions;
- the available build time and environment;
- whether a codebase exists or the prototype starts from a blank workspace;
- any required technology, data source, or deployment target.

When no timebox is given, state a reasonable working assumption. Use it to constrain scope, not to invent urgency.

## 2. Build the fact map

Extract only decision-relevant information. Classify every important statement:

| Class | Meaning | Treatment |
|---|---|---|
| Evidence | Directly supported by the source | Cite or point to its location |
| Inference | Reasonable conclusion from evidence | Explain the reasoning briefly |
| Assumption | Needed to proceed but unverified | Make it visible and reversible |
| Unknown | Could materially change the solution | Ask, test, or isolate it |

Do not turn generic benefits such as efficiency, consistency, revenue, or satisfaction into stated goals unless the source supports them.

## 3. Produce the Demo Contract

Before substantial implementation, create a concise Demo Contract using [references/demo-contract.md](references/demo-contract.md). Keep it to roughly one page.

It must establish:

1. **Mandate:** What outcome and constraints are fixed by the source?
2. **Primary user and job:** Who experiences the chosen workflow, and what are they trying to complete?
3. **Current pain:** Where does the present workflow create meaningful friction or risk?
4. **Solution thesis:** How will the proposed capability create value while respecting the mandate?
5. **Prototype hypothesis:** What must the demo make believable?
6. **Golden path:** What single end-to-end journey will the audience watch?
7. **Proof map:** What does each demo moment prove, and which evidence supports it?
8. **Boundaries:** What is intentionally excluded, assumed, mocked, or deferred?
9. **Success signal:** What observable outcome would indicate improvement?

Surface the contract before building. If the user has already authorized implementation and no material fork remains, continue without creating a ceremonial approval pause. Otherwise, ask for the one decision that unlocks the build.

## 4. Convert the contract into a build slice

Define the smallest functional spine that supports the golden path:

- a credible starting state;
- the minimum user inputs and decisions;
- the system response that demonstrates the core value;
- a clear end state or recorded outcome;
- realistic seed data sufficient to make the scenario understandable.

Prioritize in this order:

1. Complete golden path
2. Visible proof of the solution thesis
3. Reliable data and state transitions
4. Clear information hierarchy and interaction cues
5. Only then, secondary polish or edge cases

Default to excluding authentication, account management, generalized administration, exhaustive settings, production infrastructure, and peripheral workflows unless they are central to the hypothesis.

## 5. Build for demonstration

If a codebase exists, inspect its structure, conventions, and available commands before editing. If starting from scratch, choose a familiar, low-dependency stack that fits the environment and timebox.

During implementation:

- establish a runnable shell and one happy path first;
- use realistic names, dates, statuses, and content rather than lorem ipsum;
- keep data deterministic so the same actions produce the same result;
- provide an obvious reset or repeatable starting condition;
- make loading, empty, success, and error states explicit where they affect the golden path;
- use plain language and visible system feedback;
- keep simulated capabilities honest and visually distinguishable when necessary;
- preserve existing user work and unrelated files.

Do not add a feature merely because it is easy. Add it only if it strengthens the proof map.

## 6. Verify the experience

Use [references/demo-readiness.md](references/demo-readiness.md) for the final pass.

At minimum:

- run the application in the actual environment;
- execute the golden path from a clean state;
- verify every proof moment in the Demo Contract;
- test the reset path;
- remove broken controls and misleading affordances from the visible route;
- record assumptions, simulations, and known limitations;
- confirm startup instructions work.

Fix blockers to the golden path before cosmetic defects outside it.

## 7. Prepare the demonstration

Create a short runbook with:

- a one-sentence problem and outcome;
- the primary user and scenario;
- the sequence of actions to perform;
- the proof point attached to each action;
- a closing statement connecting the demonstrated outcome to the mandate;
- a fallback route if a nonessential element fails.

Do not narrate interface mechanics alone. Explain the user problem, the action, and why the resulting change matters.

## Final handoff

Report:

- what was built;
- where to start the demo;
- how to run and reset it;
- what the golden path proves;
- what is simulated, assumed, or deliberately excluded;
- the most valuable next improvement if more time becomes available.

Keep the handoff short enough to use immediately.
