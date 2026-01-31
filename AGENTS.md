# AGENTS.md

## Project Overview

**@schplitt/starter** is a minimal TypeScript starter template designed as a lightweight foundation for building packages. It features ESM modules, Vitest for testing, ESLint for code quality, and tsdown for automated builds.

## Architecture

```
src/
└── index.ts            # Main entry point with exports
tests/
└── greet.test.ts       # Tests using Vitest
```

### Source (src/index.ts)

- Main entry point for the package
- All public exports should be defined here
- Uses ESM module format

### Tests (tests/)

- Uses Vitest for testing
- Test files follow the `*.test.ts` naming convention
- Import from `../src` to test the source code

## Development

```sh
pnpm install    # Install dependencies
pnpm test       # Run tests with Vitest (watch mode)
pnpm build      # Build with tsdown
pnpm lint       # Lint with ESLint
pnpm lint:fix   # Lint and auto-fix
pnpm typecheck  # TypeScript type checking
```

## Code Style

- ESM only (`"type": "module"`)
- TypeScript strict mode enabled
- Uses `tsdown` for building
- Uses `@schplitt/eslint-config` for linting
- Uses `vitest` for testing

## Testing

- Write tests in the `tests/` directory
- Use `*.test.ts` file naming convention
- Run `pnpm test` for watch mode during development
- Import modules from `../src`

Example test structure:

```ts
import { expect, test } from 'vitest'
import { myFunction } from '../src'

test('should do something', () => {
  expect(myFunction()).toBe(expectedValue)
})
```

## Maintaining Documentation

When making changes to the project (new APIs, architectural changes, updated conventions):

- **`AGENTS.md`** — Update with technical details, architecture, and best practices for AI agents
- **`README.md`** — Update with user-facing documentation (usage, installation, examples) for end users

## Agent Guidelines

When working on this project:

1. **Run tests** after making changes: `pnpm test`
2. **Run linting** to ensure code quality: `pnpm lint`
3. **Run type checking** before committing: `pnpm typecheck`
4. **Update this file** when adding new modules, APIs, or changing architecture
5. **Keep exports in `src/index.ts`** — all public API should be exported from the main entry point
6. **Add tests** for new functionality in the `tests/` directory
7. **Record learnings** — When the user corrects a mistake or provides context about how something should be done, add it to the "Project Context & Learnings" section below if it's a recurring pattern (not a one-time fix)
8. **Notify documentation changes** — When updating `README.md` or `AGENTS.md`, explicitly call out the changes to the user at the end of your response so they can review and don't overlook them

## Project Context & Learnings

This section captures project-specific knowledge, tool quirks, and lessons learned during development. When the user provides corrections or context about how things should be done in this project, add them here if they are recurring patterns (not a one-time fix).

> **Note:** Before adding something here, consider: Is this a one-time fix, or will it come up again? Only document patterns that are likely to recur or are notable enough to prevent future mistakes.

### Tools & Dependencies

<!-- Add tool-specific notes, required configurations, or gotchas here -->

### Patterns & Conventions

<!-- Add project-specific patterns, preferred approaches, or conventions here -->

### Common Mistakes to Avoid

<!-- Add things that have been done wrong before and should be avoided -->
