# Contributing Guidelines

## Code Style

- Use consistent indentation (2 spaces for JavaScript, 4 for Python)
- Follow ESLint/Pylint configurations
- Write meaningful commit messages
- Add comments for complex logic

## Pull Request Process

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Make your changes
4. Write or update tests
5. Commit with clear messages
6. Push to your fork
7. Create a Pull Request with description

## Commit Message Format

```
type(scope): subject

body

footer
```

Types: feat, fix, docs, style, refactor, test, chore

Example:
```
feat(auth): add JWT token refresh mechanism

Implement refresh token endpoint to extend user sessions
without requiring re-authentication.

Closes #123
```

## Testing

- Write tests for new features
- Maintain >80% code coverage
- Run tests before submitting PR

## Code Review

All code must be reviewed before merging. Please be respectful and constructive.
