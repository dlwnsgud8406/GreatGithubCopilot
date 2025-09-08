---
description: 'Python Coding standards'
applyTo: '**/*.py'
---

# Python Coding Standards Template

## Core Principles

* **Simplicity First**: Avoid over-engineering solutions
* **Clear Architecture**: Keep design simple and understandable  
* **User-Focused**: Build minimal solutions that meet requirements

## Type Hints

Add type hints to functions and methods for better code clarity and IDE support.

## Code Quality Guidelines

* Follow existing code patterns before creating new structures
* Clean up temporary files, scripts, and helpers after use
* Include `__init__.py` files in Python packages
* Follow project linting and formatting standards

## Quality Assurance Workflow

Before running tests or declaring work complete, ensure code passes quality checks:

### Setup Environment
```bash
# Activate virtual environment (adjust path as needed)
source .venv/bin/activate
# or
source venv/bin/activate
```

### Quality Gates
1. **Linting**: Run linter to fix code style issues
   ```bash
   ruff check .  # or flake8, pylint
   ```

2. **Type Checking**: Resolve type errors  
   ```bash
   mypy src/  # adjust path to your source directory
   ```

3. **Testing**: Run tests only after fixing lint/type errors
   ```bash
   pytest -v
   ```

## Execution Commands

* **Tests**: `pytest -v`
* **Linting**: `ruff check .` (or your preferred linter)
* **Type Checking**: `mypy src/` (adjust source path)

```
