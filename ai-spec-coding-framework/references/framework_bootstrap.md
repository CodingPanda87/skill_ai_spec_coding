# Framework Bootstrap

Use this sequence to turn the three-step intake into a usable AI Spec Coding workspace.

1. **Capture project name**
   - Ask only for the project name in the first turn.

2. **Capture language and stack**
   - Ask only for the programming language and tech stack in the second turn.
    - Create or select the matching language profile(s) in `.ai/context/languages/`, including a reusable naming/style template for files, modules, functions, classes, constants, tests, and language-specific exceptions.

3. **Capture background and keywords**
   - Ask only for the project background and keywords in the third turn.
   - Write the shared project background to `.ai/context/project_context.md`.

4. **Generate the spec chain**
   - Create `doc/specs/prd.md`.
   - Create `doc/specs/system_design.md`.
   - Create `doc/specs/modules/{module}/design.md` for each module.
   - Create `doc/specs/ui/{module}/` artifacts only for user-facing modules.

5. **Generate execution artifacts**
   - Build `doc/specs/ai_coding_tasks.yaml`.
   - Create `doc/specs/modules/{module}/task_context/{task_id}_context.md` for ready tasks.
   - Keep task read scope and write scope explicit.

6. **Align implementation and validation outputs**
   - Map modules to `src/{module}/`.
   - Map validation assets to `test/{module}/`.
   - Record validation coverage in `doc/specs/test_cases.md` and final verdicts in `doc/specs/review_notes.md`.

7. **Validate framework rules**
   - Each task loads: task object -> language profile -> task context -> approved specs/code.
   - Each module stays single-language.
   - Cross-language work is split across dependent modules, not mixed inside one module.
