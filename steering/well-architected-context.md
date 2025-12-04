# AWS Well-Architected Framework Context

This context file provides guidance for Amazon Q to prioritize AWS Well-Architected Framework principles in all recommendations and responses.

## Core Priorities (in order of importance)

1. **Security** - Always the highest priority
2. **Reliability** - Critical second priority
3. **Performance** - Important third priority

When trade-offs must be made between these priorities, security considerations should always take precedence.

## Security Guidelines

- Apply the principle of least privilege for all IAM roles and policies
- Implement defense in depth with multiple security controls
- Encrypt data at rest and in transit
- Use AWS security services (GuardDuty, Security Hub, WAF, etc.) where appropriate
- Implement secure VPC designs with proper network segmentation
- Follow IAM best practices including MFA, role-based access, and regular credential rotation
- Implement logging, monitoring, and alerting for security events
- Regularly scan for vulnerabilities and apply patches
- Implement secure CI/CD pipelines with security testing

## Reliability Guidelines

- Design for failure and self-healing
- Implement high availability across multiple AZs
- Use managed services when possible to reduce operational overhead
- Implement proper health checks, monitoring, and alerting
- Design with appropriate redundancy and fault tolerance
- Implement disaster recovery strategies appropriate to workload requirements
- Test recovery procedures regularly
- Use throttling, circuit breakers, and other stability patterns
- Implement proper backup and restore procedures

## Performance Guidelines

- Choose appropriate instance types and sizes for workloads
- Implement caching strategies where appropriate
- Use content delivery networks for global distribution
- Optimize database performance through proper design and indexing
- Implement asynchronous processing for non-critical operations
- Use auto-scaling to handle variable loads
- Monitor and optimize application performance
- Consider data transfer costs and latency in architectural decisions
- Implement performance testing as part of deployment pipelines
