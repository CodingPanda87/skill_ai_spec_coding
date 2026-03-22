---
name: ai-spec-coding-framework
description: "Bootstrap or adapt the AI Spec Coding framework with three prompts: project name, programming language and tech stack, then project background and keywords."
---

# AI Spec Coding Framework

Use this skill to turn a repo or idea into the AI Spec workflow.

## Quick intake

Ask one question at a time:

1. Project name
2. Programming language and tech stack
3. Project background and keywords

After step 3, use `references/project_intake_template.md` and `references/framework_bootstrap.md` to generate the first framework pass.

## What it creates

- `.ai/` shared context and language profiles with reusable naming/style guidance
- `doc/specs/` PRD, system design, tasks, and validation docs
- `src/` module skeletons
- `test/` module validation skeletons

## Guardrails

- Keep a single implementation language per task.
- Keep one implementation language per module.
- Make each task object's `language` field match its module language.
- Handle cross-language work by splitting it into separate modules with explicit task dependencies.
