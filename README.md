# @coinsigma/eslint-config-react

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
pnpm add -D @coinsigma/eslint-config-react eslint
```

## Usage

Create an `eslint.config.js` file in your project root:

```javascript
import coinSigmaConfig from '@coinsigma/eslint-config-react';

export default coinSigmaConfig;
```

### With custom overrides

```javascript
import coinSigmaConfig from '@coinsigma/eslint-config-react';

export default [
  ...coinSigmaConfig,
  {
    // Your custom rules
    rules: {
      'no-console': 'off'
    }
  }
];
```

### For specific file patterns

```javascript
import coinSigmaConfig from '@coinsigma/eslint-config-react';

export default [
  ...coinSigmaConfig,
  {
    files: ['src/components/**/*.tsx'],
    rules: {
      // Component-specific rules
    }
  }
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

## Contributing

This package is maintained by the CoinSigma team. For issues or feature requests, please open an issue in the repository.

## License

MIT
Reusable configs
