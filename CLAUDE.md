# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is the **Claude Code Subagents Collection** - a comprehensive collection of 78 specialized AI subagents for Claude Code that provide domain-specific expertise across software development, infrastructure, and business operations.

## Architecture

### Repository Structure
- **Root directory**: Contains 78+ individual subagent definition files (`.md` format)
- **examples/**: Contains usage examples and patterns (e.g., `tdd-usage.md`)
- **.github/**: GitHub configuration including issue templates for new subagents
- **README.md**: Comprehensive documentation with agent categories and usage patterns

### Subagent Categories
The repository is organized into logical categories:

#### Architecture & System Design
- **Core Architecture**: `backend-architect`, `frontend-developer`, `cloud-architect`, `kubernetes-architect`
- **UI/UX & Mobile**: `ui-ux-designer`, `mobile-developer`, `ios-developer`, `flutter-expert`

#### Programming Languages
- **Systems & Low-Level**: `c-pro`, `cpp-pro`, `rust-pro`, `golang-pro`
- **Web & Application**: `javascript-pro`, `typescript-pro`, `python-pro`, `ruby-pro`
- **Enterprise & JVM**: `java-pro`, `scala-pro`, `csharp-pro`

#### Infrastructure & Operations
- **DevOps & Deployment**: `devops-troubleshooter`, `deployment-engineer`, `terraform-specialist`
- **Database Management**: `database-optimizer`, `database-admin`

#### Quality Assurance & Security
- **Code Quality**: `code-reviewer`, `security-auditor`, `test-automator`
- **Performance**: `performance-engineer`, `debugger`

#### Data & AI
- **Data Engineering**: `data-scientist`, `data-engineer`
- **Machine Learning**: `ai-engineer`, `ml-engineer`, `mlops-engineer`

#### Business & Operations
- **Business Analysis**: `business-analyst`, `content-marketer`, `hr-pro`
- **SEO & Content**: 10 specialized SEO agents for content optimization

### Model Configuration
Agents are assigned to specific Claude models based on complexity:
- **Haiku** (11 agents): Quick, focused tasks
- **Sonnet** (46 agents): Standard development tasks
- **Opus** (21 agents): Complex reasoning and architecture

## Subagent File Format

Each subagent follows a consistent Markdown format with YAML frontmatter:

```markdown
---
name: agent-name
description: Activation criteria and purpose
model: haiku|sonnet|opus
---

Detailed system prompt defining expertise and behavior
```

## Key Development Patterns

### Agent Coordination
- Agents automatically coordinate for complex multi-step tasks
- Common workflows: Architecture → Development → Testing → Security → Performance
- Project coordination handled by `project-owner` agent (Opus model)

### TDD Integration
- Comprehensive TDD support through `tdd-orchestrator` and enhanced `test-automator`
- Follows red-green-refactor cycle with proper agent coordination
- Language-specific TDD patterns available for all major programming languages

### Quality Gates
- Code quality enforced through `code-reviewer` (Opus model) for security and reliability
- Performance optimization via `performance-engineer` (Opus model)
- Security auditing through `security-auditor` (Opus model)

## Common Operations

### No Build System
This repository contains only documentation and configuration files. There are no build commands, test suites, or compilation steps required.

### Agent Development
- Create new agents by adding `.md` files following the established pattern
- Use lowercase, hyphen-separated naming convention
- Include clear activation criteria in description field
- Select appropriate model tier based on task complexity

### Documentation Updates
- README.md serves as the primary documentation and agent index
- Examples directory contains usage patterns and workflows
- GitHub issue templates facilitate new agent requests

## Agent Selection Strategy

### Automatic Delegation
Claude Code automatically selects appropriate agents based on:
- Task context and domain requirements
- Technical complexity level
- Available agent capabilities

### Explicit Invocation
Specify agents directly using patterns like:
- "Use code-reviewer to analyze security vulnerabilities"
- "Have performance-engineer optimize this bottleneck"
- "Get tdd-orchestrator to implement with test-first approach"

### Multi-Agent Workflows
Complex tasks automatically invoke multiple agents in sequence:
- Feature development: `backend-architect` → `frontend-developer` → `test-automator` → `security-auditor`
- Performance optimization: `performance-engineer` → `database-optimizer` → `code-reviewer`
- Infrastructure setup: `cloud-architect` → `terraform-specialist` → `security-auditor`

## Best Practices

### Agent Design
- Focus on specific domain expertise rather than general capabilities
- Include concrete examples and actionable guidance
- Specify tools and technology stacks where relevant
- Balance specificity with reusability across projects

### Usage Patterns
- Start with high-level requirements and let agents coordinate
- Use explicit agent selection for specialized tasks
- Combine agents strategically for validation (e.g., security review after implementation)
- Track multi-agent workflows for complex features

### Quality Assurance
- Always use `code-reviewer` for security-sensitive changes
- Employ `test-automator` for comprehensive test coverage
- Apply `performance-engineer` for optimization tasks
- Utilize `security-auditor` for compliance requirements

## Integration Points

### GitHub Integration
- Issue templates for new agent requests and bug reports
- Standardized contribution guidelines
- MIT license for open source usage

### Claude Code Commands
- Compatible with [Claude Code Commands](https://github.com/wshobson/commands) collection
- Supports slash commands for complex workflows
- Enables sophisticated multi-agent orchestration

This repository serves as a comprehensive toolkit for extending Claude Code's capabilities across all aspects of software development and operations.