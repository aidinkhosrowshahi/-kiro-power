# Approved Models for Building Agentic Applications

## Global Claude Sonnet 4+ Models (Recommended for Agentic Development)

Use only these approved global Claude Sonnet 4+ models for building agentic applications with Strands Agents framework:

### Primary Recommended Global Models

**Global Claude Sonnet 4.5** (Latest and Most Capable)
- Model ID: `global.anthropic.claude-sonnet-4-5-20250929-v1:0`
- Description: Latest Sonnet model with enhanced reasoning capabilities
- Region: Global routing across all supported AWS regions
- Status: ✅ Tested and verified working with Strands framework

**Global Claude Sonnet 4**
- Model ID: `global.anthropic.claude-sonnet-4-20250514-v1:0`
- Description: Advanced reasoning and analysis capabilities
- Region: Global routing across all supported AWS regions
- Status: ✅ Tested and verified working with Strands framework

## Usage Guidelines

- Default to Global Claude Sonnet 4.5 for new agentic applications
- Global models provide better availability and automatic routing
- All models support text and image input modalities
- Configure temperature and other parameters as needed for your use case
- Both models are production-ready and fully compatible with Strands framework

## Benefits of Global Models

- Automatic routing to available regions
- Better fault tolerance and availability
- Simplified configuration (no region-specific setup needed)
- Consistent performance across different geographic locations

## Framework for Building Agentic Applications

When building agentic applications, use MCP tools to research and learn about best practices and how to use the Strands Agent SDK and AgentCore. You must use the following MCP tools:

- **strands-agents** - For Strands Agent SDK documentation and best practices
- **bedrock-agentcore-mcp-server** - For AgentCore implementation guidance and examples

### Development Guidelines

- Always research using these MCP tools before implementing agentic features
- Reference the latest documentation and examples from both tools
- Follow the established patterns and best practices from the official documentation
- Use the tools to understand proper integration between Strands Agents and AgentCore

This approach ensures you're building with the most current and recommended practices for agentic application development.
