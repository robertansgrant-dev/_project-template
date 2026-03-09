# Project Template

A comprehensive Python project template designed for collaborative development with Claude.

## Quick Start

### Installation
\\\ash
# Clone the repository
git clone https://github.com/robertansgrant-dev/_project-template.git
cd _project-template

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
pip install -r dev-requirements.txt
\\\

### Running the Project
\\\ash
python -m src.main
\\\

## Workflow Explanation

### 6-Phase Development Cycle

#### Phase 1: Requirements & Planning
- Define project objectives
- List dependencies in requirements.txt
- Update README.md with goals
- Create skeleton code structure

#### Phase 2: Architecture & Design
- Review .roo/rules/ (AI Roles, Coding Standards, Architecture)
- Plan module organization
- Define data structures and interfaces
- Identify external dependencies

#### Phase 3: Implementation
- Implement core functionality in src/
- Follow coding standards (see .roo/rules/01-coding-standards.md)
- Write docstrings and comments
- Keep code modular and testable

#### Phase 4: Testing
- Write unit tests in tests/
- Aim for 80%+ code coverage
- Test edge cases and error handling
- Document test scenarios

#### Phase 5: Refinement
- Code review against standards
- Optimize performance
- Refactor duplicated code
- Update documentation

#### Phase 6: Integration & Deployment
- Verify all tests passing
- Final validation
- Prepare deployment
- Create release notes

## Project Structure

\\\
_project-template/
├── .roo/                          # AI workflow and rules
│   ├── rules/
│   │   ├── 00-ai-roles.md         # Claude/Developer responsibilities
│   │   ├── 01-coding-standards.md # Code style guidelines
│   │   └── 02-architecture.md     # Project structure
│   ├── prompts/
│   │   └── README.md
│   └── results/
│       └── README.md
├── src/                           # Source code
│   ├── __init__.py                # Package initialization
│   └── main.py                    # Entry point
├── tests/                         # Test files
├── docs/                          # Documentation
├── CLAUDE.md                      # AI context and preferences
├── README.md                      # This file
├── requirements.txt               # Production dependencies
├── dev-requirements.txt           # Development dependencies
└── .gitignore                     # Git ignore rules
\\\

## Roo Prompt Generator

The Roo prompt generator creates structured, context-rich prompts for Claude to implement tasks efficiently.

### When to Use
Use the `pmt:` prefix for significant tasks:
- Implementing features
- Debugging complex issues
- Refactoring modules
- Generating tests
- Major documentation updates

**Example:**
```
pmt: Implement user authentication module with JWT tokens
```

### Workflow
1. Developer provides task with `pmt:` prefix
2. Roo gathers context and generates structured prompt
3. Prompt is written to `.roo/prompts/ACTIVE.md`
4. Claude reads ACTIVE.md and implements task
5. Previous prompts are archived with timestamps

**See .roo/rules/03-prompt-generation.md for full documentation.**

## Testing

### Running Tests
\\\ash
# Run all tests
pytest

# Run with coverage
pytest --cov=src

# Run specific test file
pytest tests/test_main.py

# Run with verbose output
pytest -v
\\\

### Test Structure
- Place tests in tests/ directory
- Use test_*.py naming convention
- Use pytest framework
- Aim for 80%+ code coverage

## Dependencies

### Production (requirements.txt)
Core packages needed to run the project.

### Development (dev-requirements.txt)
Additional packages for development, testing, and documentation:
- pytest: Testing framework
- black: Code formatter
- flake8: Linter
- mypy: Type checker

## Workflow Rules

See .roo/rules/ for detailed guidelines:

1. **00-ai-roles.md**: Defines role boundaries between Claude and Developer
2. **01-coding-standards.md**: Code style and organization standards
3. **02-architecture.md**: Project structure and module guidelines
4. **03-prompt-generation.md**: Roo prompt generator workflow

## Contributing

### Code Review Checklist
- [ ] Follows coding standards
- [ ] Tests written and passing
- [ ] Documentation updated
- [ ] No unnecessary dependencies
- [ ] Code is modular and maintainable

## License

MIT License - See LICENSE file for details

## Support

For issues or questions, create an issue on the GitHub repository.
