---
layout: default
title: Checklist Skill for LLMs
nav_order: 5
---

# CLAIM Checklist Skill for Language Models

The CLAIM checklist skill is an [Agent Skill](https://agentskills.io) that guides a large language model (LLM), such as Claude, through the 44 items of the CLAIM 2024 checklist for a medical imaging AI manuscript. It works in two modes:

- **Author mode** — completes the checklist for your own manuscript, with page/line locations for each Yes, a reason for each No or NA, and suggested text for fixable gaps.
- **Assessor mode** — rates someone else's manuscript (peer review, meta-research), with a quote or section pointer as evidence for each answer.

The output is a checklist table, Yes/No/NA totals, and a list of borderline items for human review. The skill adds item-specific answer rules for the items that LLMs most often misjudge and refers the model to the [item elaborations](claim-items.md) on this site.

[Download skill (.zip)]({{ '/skills/claim-checklist.zip' | relative_url }}){: .btn .btn-primary } [View on GitHub](https://github.com/RSNA/claim/tree/main/skills/claim-checklist){: .btn }

## Installation

### Claude apps (claude.ai, desktop)

Download the skill archive above and upload it in the Skills section of the Claude settings.

### Claude Code

Copy the skill into your personal skills folder (or into `.claude/skills/` of a project):

```bash
mkdir -p ~/.claude/skills/claim-checklist
curl -fsSL https://raw.githubusercontent.com/RSNA/claim/main/skills/claim-checklist/SKILL.md -o ~/.claude/skills/claim-checklist/SKILL.md
```

### Other agents and language models

Tools that support the Agent Skills format load the unzipped `claim-checklist` folder from their skills directory. For any other LLM, paste the contents of [SKILL.md](https://github.com/RSNA/claim/blob/main/skills/claim-checklist/SKILL.md) (without the front matter between the `---` lines) at the start of the conversation.

## Usage

Provide the complete manuscript, including tables, figure legends and supplements, and ask, for example:

- "Fill out the CLAIM checklist for my manuscript."
- "Assess this paper's adherence to CLAIM 2024."
- "Which CLAIM items does this draft still miss?"

{: .note }
The skill is licensed under [MIT](https://github.com/RSNA/claim/blob/main/LICENSE-CODE). The CLAIM item text it contains is © RSNA and reproduced by permission; it is not covered by the MIT grant.
