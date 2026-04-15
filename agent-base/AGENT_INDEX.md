# Agent System Index

This is the **central navigation map** for all agents, skills, rules, and examples in this project.

**DO NOT SKIP THIS FILE.** Every agent session MUST read this file first after reading `PROJECT_CONTEXT.md`.

---

## Quick Start for Agents

1. Read `PROJECT_CONTEXT.md` to understand the project
2. Scan the **Agents** section below to understand what delegated work looks like
3. Find the skill matching your task in the **Skills** section
4. Scan **Rules** to understand project constraints
5. Follow **Usage Patterns** for your workflow

---

## Agents

Available agents for task delegation. Use these when you need specialized focus on a specific workflow.

| Agent        | File                  | Purpose                               | When to Use                      |
| ------------ | --------------------- | ------------------------------------- | -------------------------------- |
| **planner**  | `.agents/planner.md`  | Break tasks into milestones and files | Starting any new feature or fix  |
| **reviewer** | `.agents/reviewer.md` | Review code for quality and alignment | After implementation is complete |

**Note:** Agents work best when delegated with a clear task scope and success criteria.

---

## Skills

Skills are reusable workflows for common development patterns. These are the PRIMARY SURFACE for your work.

| Skill            | Folder                 | Purpose                                | Usage                           |
| ---------------- | ---------------------- | -------------------------------------- | ------------------------------- |
| **planning**     | `skills/planning/`     | Plan a task into clear milestones      | `/planning "Add feature X"`     |
| **tdd-workflow** | `skills/tdd-workflow/` | Implement with tests-first methodology | `/tdd` or when writing new code |

**How to use skills:**

- Skills are self-contained workflow definitions (see `SKILL.md` in each folder)
- Each skill has explicit steps and success criteria
- Skills can invoke agents when deeper work is needed

---

## Rules

Always-follow guidelines that apply to all code and planning work in this project.

| Rule           | File                         | Topic                 | Scope    |
| -------------- | ---------------------------- | --------------------- | -------- |
| **guidelines** | `rules/common/guidelines.md` | Development practices | All work |

**How rules work:**

- Rules are ALWAYS ENFORCED
- They define constraints, not suggestions
- If a rule conflicts with your task, raise the issue explicitly

---

## Examples

Reference workflows and templates showing how to use the agent system together.

| Example             | File                          | Shows                                         |
| ------------------- | ----------------------------- | --------------------------------------------- |
| **simple-workflow** | `examples/simple-workflow.md` | How to plan, test, and review a small feature |

---

## System Structure

```
agent-base/
├── .agents/              ← agent definitions
│   ├── planner.md
│   └── reviewer.md
├── skills/               ← workflow definitions
│   ├── planning/
│   │   └── SKILL.md
│   └── tdd-workflow/
│       └── SKILL.md
├── rules/                ← always-follow guidelines
│   └── common/
│       └── guidelines.md
├── hooks/                ← automation triggers
│   └── hooks.json
├── examples/             ← reference workflows
│   └── simple-workflow.md
├── AGENT_INDEX.md        ← THIS FILE
├── PROJECT_CONTEXT.md    ← project overview
├── STRUCTURE.md          ← folder layout explanation
└── README.md             ← quick introduction
```

---

## Maintenance Rules (CRITICAL)

**Every agent session MUST follow these rules to keep the system clean and updated.**

### Rule 1: Detect New Files

When you create a new agent, skill, rule, example, or hook, you MUST:

1. Put it in the correct folder (`.agents/`, `skills/`, `rules/`, `examples/`, or `hooks/`)
2. Use the correct naming:
   - agents: `{agent-name}.md`
   - skills: `{skill-name}/SKILL.md`
   - rules: `{rule-category}/{rule-name}.md`
   - examples: `{example-name}.md`

### Rule 2: Update This Index

After creating a new file, you MUST:

1. Identify what type it is (agent, skill, rule, or example)
2. Update the corresponding section in THIS file
3. Add a row to the appropriate table with:
   - Name / File path / Purpose / When/How to use
4. Keep entries in alphabetical order within each section

### Rule 3: Document Each Addition

Every new file MUST have:

- A clear title/name at the top
- A description of its purpose
- Explicit steps or guidelines (not vague)
- At least one example of how to use it

### Rule 4: Consistency Checks

Before finishing any agent session:

1. Verify all items in this index have corresponding files
2. Verify all new files in the folders are listed here
3. If mismatch is found, update immediately
4. Never leave orphaned or undocumented files

### Rule 5: Versioning (Advanced)

If you add a MAJOR new workflow or agent family:

1. Create a summary at the top of this file
2. Note the date and who/what added it
3. Link to the new agent or skill from this index

---

## How Agents Should Use This Index

**Step 1: Read PROJECT_CONTEXT.md**

```
Read: agent-base/PROJECT_CONTEXT.md
Goal: Understand what this project is and how features should be approached.
Time: 2-3 minutes
```

**Step 2: Scan This Index**

```
Read: agent-base/AGENT_INDEX.md (you are here)
Goal: See what agents, skills, and rules exist.
Time: 3-5 minutes
```

**Step 3: Read the Relevant Skill or Agent**

```
If planning a feature: Read skills/planning/SKILL.md
If implementing code: Read skills/tdd-workflow/SKILL.md
If reviewing: Delegate to .agents/reviewer.md
Time: 5-10 minutes per skill
```

**Step 4: Read Detailed Rules**

```
Read: rules/common/guidelines.md and any language-specific rules
Goal: Understand constraints and always-follow practices
Time: 5-10 minutes
```

**Step 5: Check Examples**

```
If unsure: Read examples/simple-workflow.md
Goal: See a real workflow walkthrough
Time: 5 minutes
```

---

## Common Workflows

Use this section to quickly find what to do given a task type.

### "I need to add a new feature"

1. Use the `planning` skill: read `skills/planning/SKILL.md`
2. If unsure about structure: ask the planner agent
3. Then use `tdd-workflow` skill to implement
4. Invoke reviewer agent before submitting

### "I need to fix a bug"

1. Use the `tdd-workflow` skill: read `skills/tdd-workflow/SKILL.md`
2. Write a failing test that reproduces the bug
3. Implement the fix
4. Verify tests pass
5. Invoke reviewer agent

### "I need to review someone's code"

1. Delegate to `reviewer` agent with clear review criteria
2. Reference `rules/common/guidelines.md` for style

### "System feels disorganized or missing something"

1. Check this index for gaps
2. Create new agent/skill/rule following the naming rules above
3. Update this index immediately
4. Document the addition clearly

---

## Critical Notes for Future Agents

- **Do NOT ignore the rules.** They define project standards.
- **Do NOT create files outside the defined structure.** Keep it organized.
- **Do NOT leave this index stale.** Update it when you add anything.
- **Do NOT assume previous sessions finished perfectly.** Verify the system is consistent.
- **Do READ examples before delegating to agents.** Understand context first.

---

## Last Updated

- **Prior:** agent-base structure created with planner, reviewer, planning skill, tdd-workflow skill, guidelines rule
- **This index:** Establishes maintenance and discovery rules for all future additions

---

## Future Expansion Guide

When you find gaps in the system, create new skills or rules following this pattern:

**New Skill Example:**

```
skills/my-new-skill/
├── SKILL.md         (title, description, explicit steps)
└── example.md       (optional walkthrough)
```

**New Agent Example:**

```
.agents/my-new-agent.md   (name, description, tools, model)
```

**New Rule Example:**

```
rules/category/my-new-rule.md   (title, guidelines, examples)
```

Then update the appropriate table in THIS file.

---

## Questions?

If you are an agent reading this and something is unclear:

- Check PROJECT_CONTEXT.md for what the project is
- Check STRUCTURE.md for folder organization
- Check README.md for quick overview
- Check specific skill/agent files for implementation details

The system is intentionally flat and explicit. There should be no hidden logic or surprise files.
