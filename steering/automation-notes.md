# Development Standards

## Infrastructure as Code
- Always use Infrastructure as Code (IaC) for resource creation and management
- Maintain a single source of truth - use and update existing templates instead of creating new ones
- For serverless services: Use AWS SAM templates for deployment
- For non-serverless resources: Use AWS CloudFormation templates
- Never create or modify resources directly through console or separate scripts
- Ensure all infrastructure changes are tracked through version control
- Before creating new templates, check and extend existing infrastructure code

## Technology Stack
- Frontend: React
- Backend: Python 3.13

## Scripting Guidelines
- All scripts must be automation-friendly for Amazon Q Developer CLI execution
- Avoid interactive scripts that require manual input during execution
- Design scripts to be used in testing and validation workflows
- Include appropriate error handling and logging
- Use environment variables for configuration where appropriate

## Best Practices
- Follow the principle of least privilege for IAM roles and policies
- Implement proper error handling and logging
- Use parameter stores for sensitive information
- Include comprehensive documentation
- Write unit and integration tests
- Maintain infrastructure consistency by updating existing templates
