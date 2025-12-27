# @schplitt/starter

A minimal TypeScript starter template with ESM, Vitest, and ESLint.

## Features

- 🚀 TypeScript with strict configuration
- 📦 ESM module format
- ✅ Vitest for testing
- 🎨 ESLint for code quality
- 🔧 tsdown for building
- 📝 Automated releases with bumpp

## Getting Started

### Use this template

You can create a new project from this template using [giget](https://github.com/unjs/giget):

```sh
# Using npx
npx giget@latest gh:schplitt/starter my-project

# Using pnpm
pnpm dlx giget@latest gh:schplitt/starter my-project

# Or clone directly from GitHub
git clone https://github.com/schplitt/starter.git my-project
cd my-project
rm -rf .git
git init
```

### Development

```sh
# Install dependencies
pnpm install

# Run tests
pnpm test

# Build
pnpm build

# Lint
pnpm lint

# Type check
pnpm typecheck
```

## Usage

Start building your project in the `src/` directory. The starter includes a simple example function to get you started.

## License

MIT