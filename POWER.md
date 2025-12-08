---
name: aws-dev-best-practices
displayName: AWS Development Best Practices
version: 1.0.0
description: Comprehensive AWS development standards, best practices, and guidelines for building secure, reliable, and performant applications
keywords:
  - aws
  - development
  - best-practices
  - infrastructure
  - terraform
  - cloudformation
  - sam
  - python
  - react
  - security
  - well-architected
  - agentcore
  - strands
  - serverless
  - cloudfront
  - s3
  - lambda
  - dynamodb
  - iac
  - automation
author: Aidin Khosrowshahi
---

# AWS Development Best Practices Power

A comprehensive collection of AWS development standards, best practices, and guidelines for building secure, reliable, and performant applications on AWS.

## Overview

This power provides curated guidance for AWS development across multiple domains:

- **Infrastructure as Code**: CloudFormation, Terraform, and SAM best practices
- **Security & Compliance**: AWS Well-Architected Framework security principles
- **Application Development**: Python, React, and agentic application standards
- **Deployment Patterns**: CloudFront/S3 hosting, serverless architectures
- **Development Workflow**: Git commit standards, automation guidelines

## What's Included

### Steering Files

- **well-architected-context.md**: AWS Well-Architected Framework principles prioritizing security, reliability, and performance
- **terraform_best_practices.md**: Terraform development and deployment standards for AWS
- **python_best_practices.md**: Python 3.13 development standards including AWS Lambda and DynamoDB integration
- **react_best_practices.md**: React development best practices with performance optimization
- **automation-notes.md**: Infrastructure as Code standards and scripting guidelines
- **architecture_diagram_rules.md**: AWS architecture diagram creation guidelines
- **approved-model-for-building-agentic.md**: Approved models and frameworks for building agentic applications
- **agentcore_strands_requirements.md**: Required modules for building with Strands and AgentCore
- **CloudFront_S3_setup_for_UI_app_website.md**: CloudFormation templates for hosting websites with CloudFront and S3
- **git_commit_rules.md**: Git commit message standards and automation
- **minimal-engineering-approach.md**: Principles for minimal, focused engineering solutions
- **aws_cli_usage.md**: AWS CLI authentication and usage guidelines

## Keywords

aws, development, best-practices, infrastructure, terraform, cloudformation, sam, python, react, security, well-architected, agentcore, strands, serverless, cloudfront, s3, lambda, dynamodb, iac, automation

## Use Cases

- Setting up new AWS projects with proper standards
- Reviewing and improving existing AWS infrastructure
- Building agentic applications with Strands and AgentCore
- Deploying serverless applications with SAM
- Creating secure CloudFront/S3 website hosting
- Following AWS Well-Architected Framework principles
- Implementing Infrastructure as Code best practices

## Getting Started

This power automatically includes all steering files in your context. The guidelines will be applied when:

- Creating new AWS infrastructure
- Writing Python or React code
- Deploying applications to AWS
- Building agentic applications
- Creating architecture diagrams
- Committing code changes

## Requirements

- AWS CLI configured with appropriate credentials
- Python 3.13 for backend development
- Node.js/npm for React frontend development
- Terraform or AWS SAM CLI for infrastructure deployment

## Best Practices Highlights

### Security First
- Always apply principle of least privilege
- Encrypt data at rest and in transit
- Use AWS security services (GuardDty, Security Hub, WAF)
- Never hardcode credentials

### Infrastructure as Code
- Use CloudFormation or Terraform for all resources
- Maintain single source of truth
- Version control all infrastructure code
- Use SAM for serverless applications

### Development Standards
- Python 3.13 with proper error handling
- React functional components with hooks
- Minimal engineering approach
- Comprehensive testing

## Support

For issues or questions about these best practices, refer to:
- AWS Well-Architected Framework documentation
- AWS service-specific best practices guides
- Community discussions and examples
