# Claude Project Context

## Project Overview
This is a Python project template designed for collaborative Claude-assisted development on Windows.

## Key Principles
- Clear separation of concerns
- Modular, testable code
- Comprehensive documentation
- Developer-led decision making with Claude implementation

## Development Workflow
1. **Planning**: Define requirements in requirements.txt and README.md
2. **Development**: Implement in src/ following coding standards
3. **Testing**: Add tests to tests/ directory
4. **Review**: Check against .roo/rules/
5. **Iteration**: Refactor and improve

## Quick Start
\\\ash
# Install dependencies
pip install -r requirements.txt
pip install -r dev-requirements.txt

# Run the project
python -m src.main

# Run tests
pytest
\\\

## File Organization
- **src/**: Source code
- **tests/**: Test files
- **docs/**: Documentation
- **.roo/**: AI workflow guidelines, rules, and prompts
  - **rules/**: Coding standards and architecture guidelines
  - **prompts/**: Active prompt and archive
- **requirements.txt**: Production dependencies
- **dev-requirements.txt**: Development dependencies

## Communication with Claude
When requesting work:
- **Be specific**: Clear requirements and constraints
- **Provide context**: Link to existing code, explain the context
- **Review suggestions**: Check proposed changes before accepting
- **Keep feedback loop active**: Iterate if needed
- **Use pmt: prefix**: For significant tasks (architecture, features, major refactors)

## Using Roo Prompt Generator
When you need Claude to work on a significant task:

1. Use the `pmt:` prefix in your request
   - Example: `pmt: Implement user authentication module`

2. Roo generates a structured prompt with:
   - Project context
   - Clear task definition
   - Applicable coding standards
   - Code references
   - Success criteria

3. The prompt is written to `.roo/prompts/ACTIVE.md`

4. Claude reads from ACTIVE.md and implements according to the structure

5. Previous prompts are archived to `.roo/prompts/archive/` with timestamps

**See .roo/rules/03-prompt-generation.md for detailed workflow.**
