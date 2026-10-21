# CLAIM checklist skill for language models

[`claim-checklist/SKILL.md`](claim-checklist/SKILL.md) is an [Agent Skill](https://agentskills.io) that guides a large language model through the 44 items of the CLAIM 2024 checklist for a medical imaging AI manuscript. It works in two modes:

- **Author mode** — completes the checklist for your own manuscript, with page/line locations for each Yes, a reason for each No or NA, and suggested text for fixable gaps.
- **Assessor mode** — rates someone else's manuscript (peer review, meta-research), with a quote or section pointer as evidence for each answer.

The output is a checklist table, Yes/No/NA totals, and a list of borderline items for human review. The skill adds item-specific answer rules for the items that language models most often misjudge (for example, answering No instead of NA for ensembling or clinical trial registration).

> **Note:** The completed checklist is a draft. Authors and reviewers remain responsible for every answer; check the flagged items in particular against the manuscript and the [item elaborations](https://rsna.github.io/claim/claim-items.html).

## Installation

### Claude Code

Copy the skill into your personal skills folder (or into `.claude/skills/` of a project):

```bash
mkdir -p ~/.claude/skills/claim-checklist
curl -fsSL https://raw.githubusercontent.com/RSNA/claim/main/skills/claim-checklist/SKILL.md -o ~/.claude/skills/claim-checklist/SKILL.md
```

### Claude apps (claude.ai, desktop)

Download the archive from the [website](https://rsna.github.io/claim/llm-skill.html) and upload it in the Skills section of Settings. To build it yourself, zip the `claim-checklist` folder:

```bash
zip -r claim-checklist.zip claim-checklist
```

### Other agents and language models

Tools that support the Agent Skills format load the `claim-checklist` folder from their skills directory. For any other language model, paste the contents of `SKILL.md` (without the front matter between the `---` lines) at the start of the conversation.

## Usage

Provide the complete manuscript, including tables, figure legends and supplements, and ask, for example:

- "Fill out the CLAIM checklist for my manuscript."
- "Assess this paper's adherence to CLAIM 2024."
- "Which CLAIM items does this draft still miss?"

## License

The skill is licensed under the [MIT License](../LICENSE-CODE). The CLAIM item text it contains is © RSNA and reproduced by permission; it is not covered by the MIT grant.
