<!-- BEGIN:nextjs-agent-rules -->

# This is NOT the Next.js you know

This version has breaking changes — APIs, conventions, and file structure may all differ from your training data. Read the relevant guide in `node_modules/next/dist/docs/` before writing any code. Heed deprecation notices.

<!-- END:nextjs-agent-rules -->

---

# Custom Agent System Entry Point

**IMPORTANT:** This project uses a custom agent system to organize features, planning, and code review.

**If you are an AI agent reading this, follow the steps below. Do not skip.**

---

## Agent Quick Start (READ THIS FIRST)

This project has been structured with an explicit agent workflow system. Before you start any work:

### Step 1: Read Project Context

```
File: agent-base/PROJECT_CONTEXT.md
Time: 5 minutes
Goal: Understand what this project is and how to approach features
Required: YES - do not skip
```

### Step 2: Read the Agent System Index

```
File: agent-base/AGENT_INDEX.md
Time: 5-10 minutes
Goal: See all available agents, skills, rules, and examples
Required: YES - this is your navigation map
```

### Step 3: Find Your Skill

Based on what you need to do, read the relevant skill:

- **Planning a feature**: Read `agent-base/skills/planning/SKILL.md`
- **Implementing code**: Read `agent-base/skills/tdd-workflow/SKILL.md`
- **Reviewing code**: See `.agents/reviewer.md` in AGENT_INDEX.md

### Step 4: Follow the Workflow

Execute the skill's steps in order. Each skill has explicit success criteria.

### Step 5: Update the Index (if you added anything)

If you created a new agent, skill, rule, or example:

- Update `agent-base/AGENT_INDEX.md` with the new entry
- Follow the naming and format shown in that file
- Keep tables in alphabetical order

---

## What This System Provides

| Component      | Location                        | Purpose                                     |
| -------------- | ------------------------------- | ------------------------------------------- |
| **Agents**     | `agent-base/.agents/`           | Delegated task handlers (planner, reviewer) |
| **Skills**     | `agent-base/skills/`            | Reusable workflows (planning, TDD)          |
| **Rules**      | `agent-base/rules/`             | Always-follow guidelines                    |
| **Hooks**      | `agent-base/hooks/`             | Automation triggers                         |
| **Examples**   | `agent-base/examples/`          | Reference workflows                         |
| **Navigation** | `agent-base/AGENT_INDEX.md`     | Central map of everything                   |
| **Context**    | `agent-base/PROJECT_CONTEXT.md` | Project purpose and approach                |

---

## Key Principles

1. **Planning comes before code** - Use the planning skill first
2. **Tests come before implementation** - Use TDD workflow
3. **Review happens after implementation** - Delegate to reviewer agent
4. **Rules are ALWAYS enforced** - Check `rules/common/guidelines.md`
5. **Documentation is kept up to date** - Update AGENT_INDEX.md when adding files

---

## Important Rules for Agents

### DO

- Read `PROJECT_CONTEXT.md` before starting any task
- Read `AGENT_INDEX.md` to see what's available
- Follow the skill workflow step-by-step
- Update `AGENT_INDEX.md` when you add new files
- Document your additions clearly
- Use the maintenance rules in AGENT_INDEX.md

### DO NOT

- Skip reading the context or index files
- Create files outside the defined structure
- Leave the index stale or out of sync
- Ignore the rules in `rules/common/guidelines.md`
- Assume previous work was perfect (verify consistency)

---

## Troubleshooting for Agents

**"What should I do?"**
→ Read `AGENT_INDEX.md` → find your task type → read the skill file

**"Where does this file go?"**
→ Check `STRUCTURE.md` or use table in AGENT_INDEX.md

**"What's the naming convention?"**
→ See AGENT_INDEX.md - Maintenance Rules section

**"System feels out of sync"**
→ Check AGENT_INDEX.md against actual files in agent-base/.
Update immediately if mismatches are found.

**"I'm creating something new"**
→ Pick the right folder, name it consistently, update AGENT_INDEX.md.

---

## Navigation Map

```
This file (AGENTS.md)
    ↓
agent-base/PROJECT_CONTEXT.md    ← Start here
    ↓
agent-base/AGENT_INDEX.md        ← Navigate from here
    ↓
agent-base/skills/{skill}/SKILL.md    ← Do your work
    ↓
agent-base/.agents/{agent}.md    ← Delegate if needed
    ↓
Review → Update AGENT_INDEX.md
```

---

## For Humans Reading This

If you're a human developer:

- This structure makes it easier for AI models to understand how to work on this project
- You can follow the same workflow manually
- The skills and rules are good practices regardless
- The system self-updates through the maintenance rules
- Examples show real workflows you can follow

Start with `agent-base/PROJECT_CONTEXT.md` if you want to understand the approach.
