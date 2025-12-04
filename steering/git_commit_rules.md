# Git Commit Rules

When committing code or changes:

## Commit Process

1. Determine which files are new, modified, or deleted using `git status`
2. Stage all relevant files using `git add` for new/modified files or `git rm` for deleted files
3. Generate a commit message following best practices
4. Execute the commit with the generated message
5. Confirm the commit was successful and show the commit hash

## Commit Message Format

Use the conventional commits format: `<type>(<scope>): <description>`

### Types
- **feat**: New feature
- **fix**: Bug fix
- **docs**: Documentation changes
- **style**: Code style changes (formatting, missing semicolons, etc.)
- **refactor**: Code refactoring
- **test**: Adding or updating tests
- **chore**: Maintenance tasks

### Best Practices
- Use the imperative mood ("Add feature" not "Added feature")
- Start with a concise summary line (50 chars or less)
- Include a more detailed explanation after a blank line if needed
- Reference any relevant issue numbers with #issue-number
- Scope is optional but helpful (component name affected)

## Example Commit Message

```
feat(auth): implement OAuth2 authentication flow

- Add OAuth2 client configuration
- Create login and callback endpoints
- Store tokens securely in user session

Closes #123
```

## Automation

Do not ask for confirmation before committing unless specifically requested. Always show the generated commit message before executing the commit.
