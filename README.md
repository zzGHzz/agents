# Claude Code Subagents Collection

A comprehensive collection of specialized AI subagents for [Claude Code](https://docs.anthropic.com/en/docs/claude-code), designed to enhance development workflows with domain-specific expertise.

## Overview

This repository contains 28 specialized subagents that extend Claude Code's capabilities. Each subagent is an expert in a specific domain, automatically invoked based on context or explicitly called when needed.

## Available Subagents

### Development & Architecture
- **[backend-architect](backend-architect.md)** - Design RESTful APIs, microservice boundaries, and database schemas
- **[frontend-developer](frontend-developer.md)** - Build React components, implement responsive layouts, and handle client-side state management
- **[mobile-developer](mobile-developer.md)** - Develop React Native or Flutter apps with native integrations
- **[graphql-architect](graphql-architect.md)** - Design GraphQL schemas, resolvers, and federation
- **[architect-reviewer](architect-review.md)** - Reviews code changes for architectural consistency and patterns

### Language Specialists
- **[python-pro](python-pro.md)** - Write idiomatic Python code with advanced features and optimizations
- **[golang-pro](golang-pro.md)** - Write idiomatic Go code with goroutines, channels, and interfaces

### Infrastructure & Operations
- **[devops-troubleshooter](devops-troubleshooter.md)** - Debug production issues, analyze logs, and fix deployment failures
- **[deployment-engineer](deployment-engineer.md)** - Configure CI/CD pipelines, Docker containers, and cloud deployments
- **[cloud-architect](cloud-architect.md)** - Design AWS/Azure/GCP infrastructure and optimize cloud costs
- **[database-optimizer](database-optimizer.md)** - Optimize SQL queries, design efficient indexes, and handle database migrations
- **[incident-responder](incident-responder.md)** - Handles production incidents with urgency and precision
- **[dx-optimizer](dx-optimizer.md)** - Developer Experience specialist that improves tooling, setup, and workflows

### Quality & Security
- **[code-reviewer](code-reviewer.md)** - Expert code review for quality, security, and maintainability
- **[security-auditor](security-auditor.md)** - Review code for vulnerabilities and ensure OWASP compliance
- **[test-automator](test-automator.md)** - Create comprehensive test suites with unit, integration, and e2e tests
- **[performance-engineer](performance-engineer.md)** - Profile applications, optimize bottlenecks, and implement caching strategies
- **[debugger](debugger.md)** - Debugging specialist for errors, test failures, and unexpected behavior

### Data & AI
- **[data-scientist](data-scientist.md)** - Data analysis expert for SQL queries, BigQuery operations, and data insights
- **[data-engineer](data-engineer.md)** - Build ETL pipelines, data warehouses, and streaming architectures
- **[ai-engineer](ai-engineer.md)** - Build LLM applications, RAG systems, and prompt pipelines
- **[ml-engineer](ml-engineer.md)** - Implement ML pipelines, model serving, and feature engineering
- **[prompt-engineer](prompt-engineer.md)** - Optimizes prompts for LLMs and AI systems

### Specialized Domains
- **[api-documenter](api-documenter.md)** - Create OpenAPI/Swagger specs and write developer documentation
- **[payment-integration](payment-integration.md)** - Integrate Stripe, PayPal, and payment processors
- **[quant-analyst](quant-analyst.md)** - Build financial models, backtest trading strategies, and analyze market data
- **[legacy-modernizer](legacy-modernizer.md)** - Refactor legacy codebases and implement gradual modernization
- **[context-manager](context-manager.md)** - Manages context across multiple agents and long-running tasks

## Installation

These subagents are automatically available when placed in `~/.claude/agents/` directory.

## Usage

### Automatic Invocation
Claude Code will automatically delegate to the appropriate subagent based on the task context and the subagent's description.

### Explicit Invocation
Mention the subagent by name in your request:
```
"Use the code-reviewer to check my recent changes"
```

## Subagent Format

Each subagent follows this structure:
```markdown
---
name: subagent-name
description: When this subagent should be invoked
tools: tool1, tool2  # Optional - defaults to all tools
---

System prompt defining the subagent's role and capabilities
```

## Best Practices

1. **Let Claude Code delegate automatically** - The main agent knows when to use each subagent
2. **Use explicit invocation for specific needs** - When you want a particular expert's perspective
3. **Combine multiple subagents** - Complex tasks may benefit from multiple specialists

## Contributing

To add a new subagent:
1. Create a new `.md` file following the format above
2. Use lowercase, hyphen-separated names
3. Write clear descriptions for when the subagent should be used
4. Include specific instructions in the system prompt

## Learn More

- [Claude Code Documentation](https://docs.anthropic.com/en/docs/claude-code)
- [Subagents Documentation](https://docs.anthropic.com/en/docs/claude-code/sub-agents)
- [Claude Code GitHub](https://github.com/anthropics/claude-code)