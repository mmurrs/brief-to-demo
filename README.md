# Brief to Demo

`brief-to-demo` is an Agent Skill for turning written source material into a focused, working product demonstration.

It helps an agent:

1. separate source evidence from inference and assumptions;
2. identify the primary user, current pain, and intended outcome;
3. define a one-page Demo Contract and golden path;
4. build the smallest prototype that proves the core idea;
5. verify, reset, and rehearse the finished demonstration.

The skill is intentionally optimized for prototypes. It does not treat a demo as production software, invent unsupported requirements, or hide mocked integrations.

## Install for Claude Code

Clone the repository into your personal skills directory:

```bash
git clone https://github.com/mmurrs/brief-to-demo.git ~/.claude/skills/brief-to-demo
```

Restart Claude Code if the skill is not discovered in the current session.

You can also clone it anywhere and explicitly ask Claude Code to read its `SKILL.md` before beginning.

## Use

Attach or identify the source material, then invoke the skill:

```text
Use the brief-to-demo skill. Read product-brief.pdf, create the Demo Contract,
and build the smallest end-to-end prototype that proves the core workflow.
I have three hours. State assumptions and do not deploy anything.
```

For a rough concept rather than a file:

```text
Use brief-to-demo to turn these notes into a scoped product demo. Show me the
Demo Contract first, then continue building unless a material decision is unresolved.
```

For an existing prototype:

```text
Use brief-to-demo to compare this prototype with the source brief. Identify the
highest-value gaps in the golden path, fix the blockers, and prepare a demo runbook.
```

## What it produces

- A source-backed fact map
- A concise Demo Contract
- One complete golden path
- A functional, deterministic prototype
- A verification and reset checklist
- A short demo runbook

## Structure

```text
brief-to-demo/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── demo-contract.md
    └── demo-readiness.md
```

The required skill instructions live in `SKILL.md`. Supporting references are loaded only when the workflow reaches the relevant stage.

## Design choices

- **Traceability over brainstorm volume:** Every important demo moment should connect to source evidence or a visible assumption.
- **One complete path over broad coverage:** A reliable end-to-end workflow is more persuasive than many disconnected screens.
- **Proof over polish:** Polish is valuable after the prototype demonstrates the intended outcome.
- **Honest simulation:** Mocked systems and data are useful when clearly labeled and deterministic.

## License

MIT
