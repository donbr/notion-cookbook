# Notion MCP Claude Skills

A collection of Claude skills that enable powerful workflows with Notion using the Model Context Protocol (MCP).

## Skills Overview

### 1. Research & Documentation

Search workspace, fetch pages, synthesize findings, and write structured output to Notion.

**Triggers:** "research X and document it", "gather information about Y and create a summary"

### 2. Task Manager

Query task databases, update properties, create follow-up tasks, and manage task relationships.

**Triggers:** "update my tasks", "create task for X", "what's blocked", "move this to done"

### 3. Spec to Implementation

Fetch specs, extract requirements, create implementation plans, update status, and log progress.

**Triggers:** "implement this spec", "work on [task name]", "plan out [feature]"

### 4. Meeting Intelligence

Search context, fetch related pages, synthesize pre-reads, and create agenda pages.

**Triggers:** "prep for meeting about X", "create agenda for Y", "what do I need to know about Z"

### 5. Knowledge Capture

Take conversation context, structure into documentation, and save to Notion wiki.

**Triggers:** "save this to Notion", "document this conversation", "add this to wiki"

## Development Guidelines

This project follows the [Notion Skill Authoring Best Practices](https://dev.notion.so/notion/Skill-authoring-best-practices-6ad753e68def42eba7a64a6a4f261107):

- **Concise content**: Keep SKILL.md files under 500 lines
- **Progressive disclosure**: Use reference files for detailed information
- **Evaluation-driven**: Write evaluations before extensive documentation
- **Workflow-oriented**: Break complex operations into clear sequential steps
- **Tool bundling**: Combine related MCP tools for coherent workflows

## File Structure

```
skills/
├── research-documentation/    # Research & synthesize to Notion
├── task-manager/             # Task database management
├── spec-to-implementation/   # Spec parsing and tracking
├── meeting-intelligence/     # Meeting prep and agenda creation
└── knowledge-capture/        # Conversation to wiki documentation

evaluations/                  # Test scenarios for all skills
shared/                       # Common utilities and templates
```

## Installation

1. Ensure Notion MCP server is configured in your Claude environment
2. Place skills in your Claude skills directory
3. Skills will be automatically discovered when relevant triggers are detected

## Testing

Each skill includes evaluations in the `evaluations/` directory. Run these to validate skill effectiveness across different Claude models (Haiku, Sonnet, Opus).

## Contributing

When adding or modifying skills:

1. Start with evaluations (3+ scenarios)
2. Write minimal instructions to pass evaluations
3. Test with multiple Claude models
4. Document only validated patterns
5. Keep SKILL.md concise, use reference files for details
