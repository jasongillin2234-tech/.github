# Codex Agent Instructions

These instructions apply to all tasks performed by Codex on this GitHub account. Follow them for every task, regardless of repository or language.

## General Principles

- Always produce the highest quality, production-ready code.
- Prefer clarity and maintainability over cleverness.
- Follow the principle of least surprise — code should behave exactly as a reader would expect.
- Favour simplicity: do the simplest thing that correctly solves the problem.
- Never leave dead code, commented-out blocks, or TODO stubs in committed code unless explicitly asked.
- Ensure all changes are backwards-compatible unless a breaking change is explicitly required.

## Code Quality

- Write clean, readable, self-documenting code with meaningful variable and function names.
- Keep functions small and focused on a single responsibility.
- Avoid deeply nested logic; prefer early returns and guard clauses.
- Remove all unused imports, variables, and dependencies.
- Follow the existing code style and conventions of the repository.
- If no style guide exists, default to the most widely adopted standard for the language (e.g. PEP 8 for Python, Prettier defaults for JS/TS).
- Use consistent formatting — run the project's linter/formatter before committing.

## Testing

- Write tests for every new feature and bug fix — no exceptions.
- Aim for high coverage of critical paths and edge cases.
- Use the testing framework already present in the project.
- Tests must be deterministic and not rely on external services unless mocked.
- Ensure all existing tests pass before committing.
- Write both unit tests and integration tests where appropriate.
- Test names should clearly describe what they are testing and what the expected outcome is.

## Documentation

- Add or update docstrings/comments for all public functions, classes, and modules.
- Keep the README up to date with any setup, usage, or configuration changes.
- Document non-obvious decisions with inline comments explaining the "why", not the "what".
- Update changelogs or release notes if present in the repository.

## Security

- Never hardcode secrets, API keys, tokens, or passwords — use environment variables.
- Validate and sanitise all user inputs.
- Avoid introducing known vulnerable dependencies; use the latest stable versions.
- Follow OWASP best practices for web-facing code.
- Never log sensitive data (passwords, tokens, PII).
- Use parameterised queries — never build SQL/query strings via string concatenation.

## Performance

- Avoid unnecessary computation, memory allocation, or I/O in hot paths.
- Use efficient data structures appropriate for the use case.
- Prefer lazy evaluation and streaming over loading everything into memory where possible.
- Profile before optimising — don't prematurely optimise without evidence of a bottleneck.

## Git & Pull Requests

- Write clear, descriptive commit messages in the imperative mood (e.g. "Add user authentication endpoint").
- Keep commits atomic — one logical change per commit.
- PRs should be small and focused; avoid mixing unrelated changes.
- PR descriptions should explain what changed, why, and how to test it.
- Reference related issues in commits and PR descriptions (e.g. "Closes #42").

## Dependencies

- Only add dependencies that are truly necessary.
- Prefer well-maintained, widely-used libraries with active communities.
- Pin dependency versions to avoid unexpected breakages.
- Document why a dependency was added if it is not obvious.

## Error Handling

- Handle errors explicitly — never silently swallow exceptions.
- Provide clear, actionable error messages.
- Use structured logging with appropriate log levels (debug, info, warning, error).
- Fail fast and loud in development; fail gracefully in production.

## Accessibility & Internationalisation (for UI work)

- Ensure UI components meet WCAG 2.1 AA accessibility standards.
- Use semantic HTML elements appropriately.
- Support keyboard navigation and screen readers.
- Externalise all user-facing strings for i18n where the project supports it.

## Code Review Standards

- When opening a PR, ensure it is ready for review — no WIP code unless labelled as a draft.
- Respond to all review comments before requesting re-review.
- Do not merge without at least one approval (if collaborators exist).
