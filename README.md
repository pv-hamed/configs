# @jix/configs

A comprehensive ESLint configuration for CoinSigma React applications using ESLint v9 flat config.

## Features

- ✅ ESLint v9 with flat config format
- ⚛️ React and React Hooks support
- 🔷 TypeScript support
- ♿ Accessibility rules (jsx-a11y)
- 📦 Import/export organization
- 🎨 Compatible with shadcn/ui components
- 🚀 Modern JavaScript/TypeScript features

## Installation

```bash
pnpm add -D @jix/configs eslint
```

## Usage

Create an `eslint.config.js` file in your project root:

```javascript
import coinSigmaConfig from "@jix/configs";

export default coinSigmaConfig;
```

### With custom overrides

```javascript
import coinSigmaConfig from "@jix/configs";

export default [
  ...coinSigmaConfig,
  {
    // Your custom rules
    rules: {
      "no-console": "off",
    },
  },
];
```

### For specific file patterns

```javascript
import coinSigmaConfig from "@jix/configs";

export default [
  ...coinSigmaConfig,
  {
    files: ["src/components/**/*.tsx"],
    rules: {
      // Component-specific rules
    },
  },
];
```

## What's included

### Base configurations

- ESLint recommended rules
- React recommended rules
- React Hooks rules
- TypeScript recommended rules
- JSX Accessibility rules
- Import/export organization rules

### Key rules

- **React**: Modern React patterns (no React import needed)
- **TypeScript**: Strict type checking with sensible defaults
- **Accessibility**: WCAG compliance helpers
- **Import organization**: Automatic import sorting and grouping
- **Code quality**: Consistent code style and best practices

## Supported file types

- `.js`, `.jsx` - JavaScript and JSX files
- `.ts`, `.tsx` - TypeScript and TSX files
- `.mjs`, `.cjs` - ES modules and CommonJS

## VS Code integration

For the best experience, install the ESLint extension and add this to your VS Code settings:

```json
{
  "eslint.experimental.useFlatConfig": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
}
```

## Development Workflow

This package uses automated CI/CD for releases:

### 🚀 Automated Publishing
- **Push to main** → Automatic version bump & publish
- **Version bumping** based on commit message conventions
- **Automatic releases** with changelog generation

### 📝 Commit Convention
Use conventional commit messages for automatic versioning:

```bash
# Major version (breaking changes)
git commit -m "feat!: restructure config exports"

# Minor version (new features)
git commit -m "feat: add new accessibility rules"

# Patch version (fixes & improvements)
git commit -m "fix: resolve TypeScript compilation issue"
```

See [Commit Convention Guide](.github/COMMIT_CONVENTION.md) for details.

## Contributing

This package is maintained by the Jix team. For issues or feature requests, please open an issue in the repository.

## License

MIT
Reusable configs
