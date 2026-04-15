# Project Manifest

This file is the single source of truth for the current project stack, installed packages, and actual project infrastructure.

## Core Stack

- **Framework:** Next.js 16.2.3
  - Verified by `package.json` dependency `next`
  - Used in `src/app/layout.tsx` and `src/app/page.tsx`
- **Language:** TypeScript
  - Verified by `package.json` dev dependency `typescript`
- **ORM:** Drizzle ORM
  - Verified by installed packages `drizzle-orm` and `drizzle-kit`
  - No direct import evidence found in current source files
- **Database:** PostgreSQL
  - Verified by installed package `pg`
- **Validation:** Zod
  - Verified by installed package `zod`
  - No direct import evidence found in current source files
- **Environment config:** `@t3-oss/env-nextjs`
  - Verified by installed package `@t3-oss/env-nextjs`
  - No direct import evidence found in current source files
- **UI / Styling:** Tailwind CSS
  - Verified by installed package `tailwindcss` and `@tailwindcss/postcss`
  - Current source uses Tailwind-style classes in `src/app/page.tsx`
- **UI library check:** `shadcn/ui` is not installed and no import evidence exists in the current source

## Installed Packages

### Dependencies
- `@prisma/client` → Prisma client runtime for database access
- `@t3-oss/env-nextjs` → environment variable handling for Next.js
- `dotenv` → loads `.env` variables in local development
- `drizzle-kit` → Drizzle CLI and schema tooling
- `drizzle-orm` → Drizzle ORM for database modeling
- `next` → Next.js framework
- `pg` → PostgreSQL driver
- `react` → React runtime for UI components
- `react-dom` → React DOM renderer
- `zod` → schema validation library

### Dev Dependencies
- `@biomejs/biome` → code formatting and linting toolchain
- `@tailwindcss/postcss` → Tailwind CSS PostCSS plugin
- `@types/node` → Node.js TypeScript definitions
- `@types/react` → React TypeScript definitions
- `@types/react-dom` → React DOM TypeScript definitions
- `tailwindcss` → Tailwind CSS framework
- `typescript` → TypeScript compiler

## Evidence Summary

- **Verified from `package.json`:** all installed dependencies and devDependencies listed above
- **Verified from source scan:** `next`, `react`, `react-dom`, and Tailwind classes are used in `src/app` files
- **No source import evidence for:** `drizzle-orm`, `drizzle-kit`, `pg`, `zod`, `@t3-oss/env-nextjs`

## Notes

- This manifest reflects the current project state as of the latest package and source scan.
- If any new package is installed or new imports are added, update this file immediately.
- If the current code begins to use Drizzle, Zod, or `@t3-oss/env-nextjs`, add the specific file references to this manifest.
