# Project Context

This document defines what this project is, what it is building toward, and how future features should be approached.

**Read this FIRST before any other agent system file.**

---

## What is This Project?

**Name:** Learn Next JS - App Template

**Type:** A Next.js application scaffold and learning environment

**Purpose:** Serve as a clean, well-architected starting point for Next.js applications with clear patterns for:

- Planning and organizing features
- Test-driven development
- Code review and quality standards
- Scalable folder structure
- Documentation and examples

**Status:** Active development with agent-guided workflow

---

## Project Principles

### 1. Planning First

Every feature or change MUST start with a plan, not code.

- Define the goal clearly
- Break into milestones
- List files to create/modify
- Define success criteria (tests, examples, docs)
- Review the plan before starting

See: `skills/planning/SKILL.md`

### 2. Test-Driven Development

Tests are the first concrete output, not an afterthought.

- Write failing tests that define behavior
- Implement minimal code to pass tests
- Refactor for clarity
- Verify no regressions

See: `skills/tdd-workflow/SKILL.md`

### 3. Code Review and Quality

All non-trivial changes get reviewed before merging.

- Verify against the plan
- Check for style and clarity
- Identify missing tests or edge cases
- Suggest improvements

See: `.agents/reviewer.md` and `rules/common/guidelines.md`

### 4. Scalability Through Structure

The folder structure and naming conventions support growth.

- Clear separation: agents, skills, rules, hooks, examples
- Consistent naming makes future additions easy
- Self-documenting file organization
- Maintenance rules prevent decay

See: `STRUCTURE.md` and `AGENT_INDEX.md`

### 5. Documentation is Code

Documentation is as important as implementation.

- Every feature has an example
- Every rule is explicit
- Every skill has clear steps
- Every agent has a defined scope

---

## Tech Stack

**Framework:** Next.js (latest, see node_modules/next/dist/docs/)

**Language:** TypeScript

**Testing:** (To be chosen during feature work - follow TDD skill)

**Build:** Biome (see biome.json)

**Important:** Always check Next.js docs in node_modules. This version may have breaking changes.

---

## Project Goals for Features

When approaching ANY new feature, follow this framework:

### Goal 1: Clarity

- The feature purpose is obvious
- Users understand what it does
- Code is readable without extensive comments
- Tests explain the intended behavior

### Goal 2: Testability

- Feature is testable before implementation
- Tests are isolated and fast
- Coverage is comprehensive (aim for 80%+)
- Edge cases are documented

### Goal 3: Maintainability

- Code follows project style rules
- Changes are small and focused
- Review process catches issues early
- Documentation explains the "why"

### Goal 4: Scalability

- Feature doesn't create technical debt
- Pattern can be repeated for similar features
- Folder structure remains clean
- Future developers can extend easily

---

## How to Approach New Features

### Phase 1: Planning

**Use:** `skills/planning/SKILL.md`

1. Define what you're building
2. Identify milestones
3. List files and components
4. Define validation (tests, examples)
5. Get agreement on the plan

### Phase 2: Implementation

**Use:** `skills/tdd-workflow/SKILL.md`

1. Write failing test(s)
2. Implement minimal code
3. Verify tests pass
4. Refactor for clarity
5. Document with examples

### Phase 3: Review

**Use:** `.agents/reviewer.md`

1. Verify plan was followed
2. Check style and clarity
3. Identify gaps (tests, docs, edge cases)
4. Suggest improvements
5. Approve or iterate

### Phase 4: Documentation

**Examples:** `examples/simple-workflow.md`

1. Add a reference example
2. Update this context if needed
3. Link from relevant skills/rules
4. Ensure future agents understand

---

## Folder Structure Rules

### DO

- Put agents in `.agents/`
- Put skills in `skills/{skill-name}/`
- Put rules in `rules/{category}/`
- Put hooks in `hooks/`
- Put examples in `examples/`
- Keep files organized and named clearly

### DO NOT

- Put random files at the root of agent-base
- Create nested agent-base/ directories
- Mix concerns (agents, skills, rules in same file)
- Leave files undocumented or hidden

### When Adding New Items

- Create in the correct location
- Update `AGENT_INDEX.md` immediately
- Document the purpose and usage
- Link from relevant sections (rules, examples, etc.)

See: `AGENT_INDEX.md` - Maintenance Rules section

---

## Scalability Pattern

This project is designed to grow cleanly.

**Current scale:** 2 agents, 2 skills, 1 rule set

**Expected future scale:** 5-10 agents, 10-20 skills, 5-10 rule sets

**Growth pattern:**

- Each new skill gets its own folder
- Related rules get grouped by category
- Examples document multi-skill workflows
- Index stays up to date (CRITICAL)

---

## Success Criteria for This Project

The project is "successful" when:

✅ New features follow the planning → TDD → review cycle  
✅ Code is clean, tested, and reviewed  
✅ Documents match actual implementation  
✅ New developers can find patterns and follow them  
✅ The agent system is self-updating  
✅ Examples exist for common workflows  
✅ No hidden logic or surprise files

---

## Key Files to Know

| File                           | Purpose                                    |
| ------------------------------ | ------------------------------------------ |
| `AGENTS.md`                    | Root entry point (links here)              |
| `AGENT_INDEX.md`               | Central navigation for agents/skills/rules |
| `PROJECT_CONTEXT.md`           | This file - explains project and approach  |
| `STRUCTURE.md`                 | Folder organization details                |
| `skills/planning/SKILL.md`     | How to plan a feature                      |
| `skills/tdd-workflow/SKILL.md` | How to implement with tests                |
| `rules/common/guidelines.md`   | Always-follow development rules            |
| `examples/simple-workflow.md`  | Reference workflow                         |

---

## Maintenance Responsibility

Every agent session is responsible for:

1. **Reading** this context before starting work
2. **Following** the planning → TDD → review process
3. **Creating** clear code and tests
4. **Documenting** what was done
5. **Updating** AGENT_INDEX.md if anything new was added
6. **Leaving** the system cleaner than found

This is not optional. It's how we scale.

---

## Questions for Future Agents

If you're reading this, ask yourself:

- **Do I understand what this project is?** (Next.js App Template)
- **Do I understand the 5 principles?** (planning, TDD, review, structure, docs)
- **Do I know where to find the planning skill?** (`skills/planning/SKILL.md`)
- **Do I know where to find the TDD skill?** (`skills/tdd-workflow/SKILL.md`)
- **Do I understand the maintenance rules?** (AGENT_INDEX.md)
- **Do I see any gaps or problems?** (Update AGENT_INDEX.md and this file)

If you answered NO to any of these, re-read relevant sections before proceeding.

---

## Next Steps

After reading this file:

1. Read `AGENT_INDEX.md` for the complete system map
2. Find the skill matching your task
3. Read the relevant skill's `SKILL.md` file
4. Check `examples/` if you want to see a walkthrough
5. Start your work following the skill's steps
6. Update `AGENT_INDEX.md` when done if anything was added

Good luck. Build something great.
