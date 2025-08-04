# Commit Message Convention

This project uses automated versioning based on commit messages. Follow these conventions for automatic version bumping:

## Commit Message Format

```
<type>: <description>

[optional body]

[optional footer]
```

## Types and Version Bumps

### 🚀 **Major Version** (Breaking Changes)
- `feat!: description` - Breaking feature
- `fix!: description` - Breaking fix  
- `BREAKING CHANGE: description` - Any breaking change

### ✨ **Minor Version** (New Features)
- `feat: description` - New feature
- `feat(scope): description` - New feature with scope

### 🐛 **Patch Version** (Bug Fixes & Improvements)
- `fix: description` - Bug fix
- `patch: description` - Small improvement
- `docs: description` - Documentation changes
- `style: description` - Code style changes
- `refactor: description` - Code refactoring
- `test: description` - Adding tests
- `chore: description` - Maintenance tasks

## Examples

```bash
# Major version bump (1.0.0 → 2.0.0)
git commit -m "feat!: change ESLint config structure"

# Minor version bump (1.0.0 → 1.1.0)  
git commit -m "feat: add new React rules for hooks"

# Patch version bump (1.0.0 → 1.0.1)
git commit -m "fix: resolve TypeScript compilation issue"
git commit -m "docs: update README installation instructions"
```

## Workflow

1. **Make your changes**
2. **Commit with conventional message**
3. **Push to main branch**
4. **CI/CD automatically:**
   - Builds and tests
   - Determines version bump
   - Updates package.json
   - Creates Git tag
   - Creates GitHub release
   - Publishes to GitHub Packages

## Skip CI

To skip the CI/CD process, add `[skip ci]` to your commit message:
```bash
git commit -m "docs: update README [skip ci]"
```
