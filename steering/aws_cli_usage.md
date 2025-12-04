# AWS CLI Usage Guidelines

## Authentication

### AWS SSO Login

For getting AWS credentials, use the following command:

```bash
aws sso login
```

This command initiates the AWS Single Sign-On authentication flow and retrieves temporary credentials for your AWS account.

## Best Practices

- Always authenticate before running AWS CLI commands
- Use AWS SSO for centralized credential management
- Credentials are temporary and will expire after a set period
- Re-run `aws sso login` if you receive authentication errors
