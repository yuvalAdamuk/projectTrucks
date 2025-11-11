# Interview Agents - Quick Reference Guide

These custom subagents help you manage token consumption and work efficiently during your interview. Each agent has its own context window, keeping your main conversation clean.

## Available Agents

### Planning & Documentation

**1. architecture-planner** 📐
- Plan architecture, ask clarifying questions, create ARD.md
- Use before starting new features
- `"Use architecture-planner to design the authentication system"`

**2. task-manager** ✅
- Break down work, create todo lists, track progress
- Use when given complex tasks
- `"Use task-manager to break down this feature"`

**3. prd-writer** 📋
- Write Product Requirements Documents with user stories
- Use at start of new features
- `"Use prd-writer to create requirements for the dashboard"`

**4. adr-writer** 📝
- Write Architecture Decision Records for important choices
- Use after making significant technical decisions
- `"Use adr-writer to document why we chose PostgreSQL"`

---

### Code Quality & Testing

**5. error-checker** 🐛
- Find and fix code errors, bugs, and issues
- Use after writing code or when tests fail
- `"Use error-checker to analyze this code"`

**6. code-reviewer** 🔍
- Review code quality, design patterns, SOLID principles, readability
- Use after writing significant code
- `"Use code-reviewer to review the user service"`

**7. unit-testing** 🧪
- Write unit tests with real API requests (no mocks)
- Use when you need comprehensive test coverage
- `"Use unit-testing to create tests for the auth module"`

**8. e2e-api-testing** 🔄
- Write end-to-end API tests for complete workflows
- Use for testing multi-step user journeys
- `"Use e2e-api-testing to test the complete checkout flow"`

---

### Performance & Optimization

**9. performance-optimizer** ⚡
- Identify bottlenecks, optimize queries, improve algorithms
- Use when code needs to be faster or more efficient
- `"Use performance-optimizer to analyze the user dashboard"`

**10. refactoring-specialist** ♻️
- Safely refactor code while preserving functionality
- Use when code needs restructuring
- `"Use refactoring-specialist to clean up the order service"`

---

### Infrastructure & Security

**11. database-expert** 🗄️
- Database design, schema modeling, migrations, query optimization
- Use for database architecture questions
- `"Use database-expert to design the user schema"`

**12. docker-devops** 🐳
- Docker, CI/CD pipelines, Kubernetes, deployment configs
- Use when setting up containerization or deployments
- `"Use docker-devops to create a Dockerfile for this app"`

**13. security-auditor** 🔒
- Security review, vulnerability detection, OWASP Top 10
- Use before submission or with sensitive features
- `"Use security-auditor to check for vulnerabilities"`

---

## Token Management Strategy

### Why These Agents Save Tokens

Each subagent has **its own context window** separate from your main conversation. This means:
- Main conversation stays focused and clean
- Less context pollution
- More efficient token usage
- Longer overall interview session possible

### Best Practices During Interview

1. **Start with task-manager** - Break down the assignment into clear steps
2. **Use architecture-planner early** - Get requirements and design sorted first
3. **Invoke error-checker frequently** - After each major code change
4. **Run security-auditor before submission** - Final check for vulnerabilities
5. **Create documentation last** - Use adr-writer or prd-writer to document decisions

### Example Interview Workflow

```
1. Receive assignment
   → "Use task-manager to break down this task"

2. Understand requirements
   → "Use architecture-planner to design the solution"
   → "Use prd-writer if product requirements are needed"

3. Database design (if needed)
   → "Use database-expert to design the schema"

4. Implement feature
   → Write code in main conversation

5. Write tests
   → "Use unit-testing to create unit tests"
   → "Use e2e-api-testing for end-to-end tests"

6. Code review
   → "Use code-reviewer to review code quality"
   → "Use refactoring-specialist if cleanup is needed"

7. Check for errors
   → "Use error-checker to verify the implementation"

8. Performance check
   → "Use performance-optimizer to analyze bottlenecks"

9. Security review
   → "Use security-auditor to check for vulnerabilities"

10. Deployment setup (if needed)
    → "Use docker-devops to create Docker/CI configs"

11. Document decisions
    → "Use adr-writer to document important choices"

12. Final review
    → Main conversation for final touches
```

---

## Tips for Interview Success

1. **Be explicit:** Say the agent name clearly when invoking
2. **One agent at a time:** Don't try to use multiple agents simultaneously
3. **Trust the agents:** They're specialized and will do focused work
4. **Save your tokens:** Use agents for specialized tasks, keep main conversation for coordination
5. **Check your work:** After agent completes, review the output before proceeding

---

## Verifying Agents Are Available

To see all available agents:
```
/agents
```

Or just ask:
```
"What subagents are available?"
```

---

## Files Location

All agent definitions are in `.claude/agents/`:
```
.claude/agents/
├── README.md (this file)
│
├── Planning & Documentation
│   ├── architecture-planner.md
│   ├── task-manager.md
│   ├── prd-writer.md
│   └── adr-writer.md
│
├── Code Quality & Testing
│   ├── error-checker.md
│   ├── code-reviewer.md
│   ├── unit-testing.md
│   └── e2e-api-testing.md
│
├── Performance & Optimization
│   ├── performance-optimizer.md
│   └── refactoring-specialist.md
│
└── Infrastructure & Security
    ├── database-expert.md
    ├── docker-devops.md
    └── security-auditor.md

Total: 13 specialized agents
```

---

## Good Luck! 🚀

You now have **13 specialized agents** covering:
- Planning & Documentation (4 agents)
- Code Quality & Testing (4 agents)
- Performance & Optimization (2 agents)
- Infrastructure & Security (3 agents)

These agents are designed to help you work efficiently and professionally during your interview. They handle specialized tasks in isolated contexts, keeping your main conversation focused and your token usage optimized.

**Pro tip:** Interviewers love seeing candidates who:
- Write tests (unit-testing, e2e-api-testing)
- Think about performance (performance-optimizer)
- Consider security (security-auditor)
- Write clean code (code-reviewer, refactoring-specialist)
- Plan before coding (architecture-planner, task-manager)
- Document decisions (adr-writer)

Use these agents strategically to demonstrate all these skills!
