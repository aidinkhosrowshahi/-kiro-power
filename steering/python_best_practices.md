# Python Development Best Practices

## General Rules
1. Follow PEP 8 style guide for code formatting
2. Use Python 3.13 for all new development
3. Write docstrings for all functions, classes, and modules
4. Keep functions small and focused on a single responsibility
5. Use virtual environments for dependency management

## Code Structure
1. Organize code into modules and packages
2. Use meaningful names for variables, functions, and classes
3. Follow the principle of least astonishment
4. Keep module imports at the top of the file
5. Group imports in the order: standard library, third-party, local application

## Error Handling
1. Use specific exception types instead of catching all exceptions
2. Provide meaningful error messages
3. Log exceptions with appropriate context
4. Use context managers (with statements) for resource management
5. Implement proper cleanup in finally blocks when needed

## AWS Lambda Best Practices
1. Keep handler functions small and delegate to other functions
2. Reuse connections and clients across invocations
3. Use environment variables for configuration
4. Implement proper error handling and logging
5. Optimize package size by excluding unnecessary dependencies

## DynamoDB Integration
1. Use boto3 resource interface for higher-level operations
2. Implement proper error handling for DynamoDB operations
3. Use batch operations for multiple items when possible
4. Implement pagination for large result sets
5. Use consistent serialization/deserialization for DynamoDB items

## API Development
1. Implement proper input validation
2. Return consistent error responses
3. Use appropriate HTTP status codes
4. Implement CORS headers for browser access
5. Document API endpoints with examples

## Testing
1. Write unit tests for all functions and classes
2. Use pytest for test framework
3. Mock external services in tests
4. Implement integration tests for critical paths
5. Use fixtures for test setup and teardown

## Security
1. Sanitize and validate all user input
2. Don't hardcode credentials in code
3. Use AWS IAM roles with least privilege
4. Implement proper authentication and authorization
5. Keep dependencies updated to avoid security vulnerabilities

## Performance
1. Use list comprehensions and generator expressions for efficient data processing
2. Avoid unnecessary computation in loops
3. Use appropriate data structures for the task
4. Profile code to identify bottlenecks
5. Implement caching for expensive operations

## Documentation
1. Maintain a README with setup and usage instructions
2. Document API endpoints and expected request/response formats
3. Include examples for common use cases
4. Document environment variables and configuration options
5. Keep documentation updated with code changes
