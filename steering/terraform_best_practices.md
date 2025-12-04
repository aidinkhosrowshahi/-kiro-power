# Terraform AWS Development and Deployment Best Practices

## General Rules
1. Always run `terraform fmt` before committing code
2. Always run `terraform validate` before applying changes
3. Use remote state with S3 backend and DynamoDB for state locking
4. Use workspaces for managing multiple environments (dev, staging, prod)
5. Set default region to "us-east-1" for all AWS providers

## Security Rules
1. Never hardcode AWS credentials in Terraform files
2. Use IAM roles with least privilege principle
3. Enable versioning on S3 buckets
4. Encrypt sensitive data at rest and in transit
5. Use security groups with minimal required access

## Resource Management
1. Always tag resources with "Environment", "Project", and "ManagedBy: Terraform"
2. Use modules for reusable infrastructure components
3. Pin module versions to specific releases
4. Use variables for all configurable values
5. Set explicit dependencies between resources when needed

## State Management
1. Never manually modify the Terraform state
2. Use state locking to prevent concurrent modifications
3. Backup state files before major changes
4. Use partial state operations for targeted changes
5. Regularly run `terraform plan` to verify state matches reality

## CI/CD Integration
1. Use Terraform in CI/CD pipelines for automated deployments
2. Run `terraform plan` in pull requests to preview changes
3. Apply changes only after approval in production environments
4. Store Terraform logs for auditing purposes
5. Use separate service accounts for CI/CD Terraform operations

## Cost Management
1. Use cost estimation tools before applying changes
2. Set up budget alerts for AWS resources
3. Regularly review and clean up unused resources
4. Use spot instances for non-critical workloads
5. Implement auto-scaling for variable workloads

## Documentation
1. Document all modules with README files
2. Include usage examples for custom modules
3. Document input and output variables
4. Maintain a changelog for infrastructure changes
5. Document architectural decisions and trade-offs
