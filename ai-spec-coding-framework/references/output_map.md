# Output Map

Use this after the three-step intake.

- Project name -> `.ai/context/project_context.md`
- Programming language and tech stack -> `.ai/context/languages/{language}.md`
- Project background and keywords -> `.ai/context/project_context.md`, `doc/specs/prd.md`, `doc/specs/use_cases/`
- Module list and boundaries -> `doc/specs/system_design.md`
- Per-module responsibilities -> `doc/specs/modules/{module}/design.md`
- UI requirements -> `doc/specs/ui/{module}/`
- Execution plan -> `doc/specs/ai_coding_tasks.yaml`, `doc/specs/modules/{module}/task_context/{task_id}_context.md`
- Code output -> `src/{module}/`
- Validation output -> `doc/specs/test_cases.md`, `test/{module}/`, `doc/specs/review_notes.md`
