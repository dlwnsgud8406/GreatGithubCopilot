# Commit Message Format

When making changes to the codebase, please follow the **Conventional Commits** format. This helps maintain a clear and consistent commit history.

The format is as follows:

```
<type>[optional scope]: <subject>

[optional body]

[optional footer(s)]
```

* **type**: A single word that describes the kind of change (`feat`, `fix`, `docs`, `refactor`, `test`, `chore`, …).
* **scope**: The affected area (module, folder, etc.) in parentheses; optional.
* **subject**: Imperative, present tense, up to 50 characters; start with a lowercase letter; no period at the end.

## type

* **feat** — a new feature (SemVer *minor*)
* **fix** — a bug fix (SemVer *patch*)
* **docs** — documentation‑only changes
* **style** — formatting, semicolons, etc.; no logical code changes
* **refactor** — refactoring (neither adding features nor fixing bugs)
* **perf** — performance improvements
* **test** — adding or modifying tests
* **build** — changes to the build system or external dependencies
* **ci** — changes to CI configuration or scripts
* **chore** — maintenance tasks (build settings, dependency updates, etc.)
* **revert** — revert a previous commit

## Tips for Writing Good Commit Messages

1. Focus on **“what” and “why”**; let the code explain **“how.”**
2. Wrap the body at 72 characters to improve compatibility with terminals and tools.
3. Even when writing the body in Korean, separate the header and body with a blank line.
4. Commit early and often, even for small changes, to keep the history granular.