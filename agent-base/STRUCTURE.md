# Simplified Agent Base Structure

This document describes the simplified folder layout used in `agent-base/`.

## Folder layout

- `.agents/`
  - agent definitions for delegation and task roles
- `skills/`
  - workflow definitions and reusable task patterns
- `rules/`
  - always-follow guidance for code quality, architecture, and planning
- `hooks/`
  - automation hooks that run on tool events
- `examples/`
  - sample workflows and planning templates

## Design principles

1. planning-first: break tasks into clear milestones before writing code
2. test-driven: use TDD workflows for feature work and bug fixes
3. review-driven: include a review step after implementation
4. modular: keep agents, skills, rules, and hooks separate
5. readable: document the workflow so future agents can understand it

## Major requirements

- task decomposition
- implementation planning
- test-first development
- code review and quality checks
- documentation and examples
