# Conventional Branch Names

Always name branches following this convention.

## Format

```
<type>/<short-description>
```

Use the same types as Conventional Commits. The short description should be lowercase, hyphen-separated, and concise.

## Types

| Type | Use when |
|------|----------|
| `feat` | Implementing a new feature |
| `fix` | Fixing a bug |
| `docs` | Documentation-only changes |
| `style` | Formatting or style changes |
| `refactor` | Code restructuring without behaviour change |
| `test` | Adding or updating tests |
| `chore` | Build, dependency, or tooling updates |
| `ci` | CI/CD pipeline changes |
| `perf` | Performance improvements |
| `revert` | Reverting a previous change |

## Rules

- Use only lowercase letters, numbers, and hyphens.
- Keep the description short — ideally 2–5 words.
- Do not include ticket/issue numbers in the branch name unless the project convention requires it.
- Never use `main` or `master` as a base name.

## Examples

```
feat/user-authentication
fix/null-pointer-on-login
docs/update-api-reference
chore/upgrade-dependencies
refactor/extract-payment-service
test/add-checkout-unit-tests
ci/add-deploy-workflow
```
