# How to Set Up Your Interview Agents

The agents I created are in `.claude/agents/` as markdown files, but they need to be registered with Claude Code.

## Method 1: Use /agents Command (Easiest)

1. Run `/agents` in the chat
2. Click "Create New Agent" for each agent you want
3. Copy the content from the corresponding `.md` file:
   - Name: (e.g., "error-checker")
   - Description: (copy from the frontmatter)
   - System Prompt: (copy the entire content after the frontmatter)
   - Tools: Leave as default (all tools)

## Method 2: Use Agent Files with Proper Format

If the files aren't being detected, they might need a different format. Let me know and I can help convert them.

## Quick Test

Try running:
```
/agents
```

If it shows "no agents configured", you'll need to add them manually through the UI.

## Agent List to Set Up

1. error-checker - Find and fix code errors
2. architecture-planner - Design systems and ask clarifying questions
3. security-auditor - Security review and OWASP compliance
4. task-manager - Break down work and track progress
5. adr-writer - Write Architecture Decision Records
6. prd-writer - Write Product Requirements Documents
7. unit-testing - Write unit tests with real API requests
8. e2e-api-testing - Write end-to-end API tests
9. code-reviewer - Review code quality and design patterns
10. performance-optimizer - Identify bottlenecks and optimize
11. refactoring-specialist - Safely refactor code
12. database-expert - Database design and optimization
13. docker-devops - Docker, CI/CD, and deployment

## Need Help?

Let me know if you want me to:
- Convert these to the proper format
- Help you set them up one by one
- Create a different configuration approach
