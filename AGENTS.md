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
