# Agent Base Reference

This folder contains a simplified Claude Code-inspired workspace for planning coding tasks, organizing agents, skills, rules, and hooks.

It is intended as a local reference that future chat and agent sessions can use as a base for how to think about coding tasks and planning.

## Purpose

- capture the major requirements of an agent-driven coding workflow
- keep the structure small and easy to follow
- make it easy to extend with more agents, skills, or rules later

## How to use this reference

- `agent-base/STRUCTURE.md` explains the folder layout
- `.agents/` contains simple agent role definitions
- `skills/` contains workflow definitions for planning and TDD
- `rules/` contains always-follow development guidance
- `hooks/` shows a minimal hook example for automation
- `examples/` shows a sample workflow for task planning and execution

## What I learned from Everything Claude Code

- separate agents, skills, commands, rules, hooks, and examples into distinct folders
- make skills the primary workflow surface, with agents delegating to skills for repeatable work
- keep rules small and language-agnostic at the top level, then add stack-specific guidance only as needed
- build a planning-first workflow: define the task, break it into milestones, then implement with tests and review
- provide accessible documentation so the system can inspect the structure and make consistent choices

## Next steps

Use this folder as the base for future agent workflows in this repository.
If you want, I can also wire these files into a more formal `.claude` or `.opencode` structure later.
