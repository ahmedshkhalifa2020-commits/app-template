---
name: sync-project
description: Required final validation step to keep the project state and PROJECT_MANIFEST.md consistent.
---

CRITICAL:
This skill MUST be executed at the end of ANY task that modifies:

- dependencies
- imports
- project structure
- stack configuration

This is NOT optional.

Use this skill after any task that changes dependencies, imports, or project stack usage.

Steps:

1. Read `package.json` and note all installed dependencies and devDependencies.
2. Scan imports across the codebase for package usage.
3. Compare actual usage against `agent-base/PROJECT_MANIFEST.md`.
4. Detect missing dependencies required by the code.
5. Detect unused dependencies that are declared but not used.
6. Update `agent-base/PROJECT_MANIFEST.md`:
   - add missing packages with a one-line reason
   - remove unused packages
   - ensure the Core Stack section reflects the app's actual stack
7. Verify consistency before finishing:
   - confirm all packages in `package.json` are represented correctly in `PROJECT_MANIFEST.md`
   - confirm `PROJECT_MANIFEST.md` does not contain stale package entries
