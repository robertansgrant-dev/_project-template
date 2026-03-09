# Prompt: Project Template Restructuring
Generated: 2026-03-09T12:00:00Z
Task Type: refactor

## Context
This project template is designed for developers working with Claude on Windows. The repository has been restructured to remove Copilot references and implement a formal Roo prompt generator system.

### Current State
- .roo/rules/ contains governance and coding standards
- No formal prompt generation system previously existed
- Manual copy-paste workflow was required for tasks

### Relevant Standards
- **Coding Standards**: See .roo/rules/01-coding-standards.md
- **Architecture**: See .roo/rules/02-architecture.md
- **AI Roles**: See .roo/rules/00-ai-roles.md
- **Prompt Generation**: See .roo/rules/03-prompt-generation.md

## Task
This file serves as a template showing the structure that Claude Code should expect when reading `.roo/prompts/ACTIVE.md`.

When a developer uses the `pmt:` prefix in a request, Roo generates a new prompt with:
1. **Context**: Project state, relevant code, applicable standards
2. **Task**: Clear objective and scope
3. **Requirements**: Constraints, testing requirements, standards to follow
4. **Code References**: Links to relevant files
5. **Success Criteria**: Verifiable outcomes

## Requirements
When implementing tasks with Claude:
- Follow all standards in .roo/rules/01-coding-standards.md
- Maintain architecture guidelines from .roo/rules/02-architecture.md
- Ensure 80%+ test coverage
- Document changes in code comments and docstrings
- Request clarification if requirements are ambiguous

## Code References
- **Architecture rules**: .roo/rules/02-architecture.md
- **Coding standards**: .roo/rules/01-coding-standards.md
- **AI roles**: .roo/rules/00-ai-roles.md
- **Prompt generation**: .roo/rules/03-prompt-generation.md
- **Project context**: CLAUDE.md
- **README**: README.md

## Success Criteria
- [ ] Prompt structure is clear and actionable
- [ ] All required sections are present (Context, Task, Requirements, Code References, Success Criteria)
- [ ] Claude can read ACTIVE.md directly
- [ ] Prompts are archived before being replaced
- [ ] Developer can verify task completion against success criteria

## Next Steps
When you have a task for Claude, use the format:
```
pmt: [Brief task description]
[Additional context or specifications]
```

Roo will generate a structured prompt in `.roo/prompts/ACTIVE.md` following this template format.
