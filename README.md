# claude-skills

A centralised collection of rules for Claude Code, shareable across multiple repos via git subtree.

Rules live in `rules/` as focused markdown files. Each repo imports whichever rules it needs into its own `CLAUDE.md` using Claude Code's `@import` syntax — so the rules are always active without any manual invocation.

## Rules

- [**general.md**](rules/general.md) — General coding behaviour (scope, file creation, language)
- [**node.md**](rules/node.md) — Node.js version management with nvm
- [**code-organisation.md**](rules/code-organisation.md) — File and test structure conventions
- [**pull-requests.md**](rules/pull-requests.md) — PR creation conventions
- [**conventional-commits.md**](rules/conventional-commits.md) — Conventional Commits rules and examples
- [**conventional-branch-names.md**](rules/conventional-branch-names.md) — Branch naming rules and examples

## Using these rules in another repo

### 1. Add this repo as a subtree

Run this once in your target repo, from the repo root:

```sh
git subtree add --prefix .claude/rules https://github.com/mcalthrop/claude-skills main --squash
```

This checks out the `rules/` files from this repo into `.claude/rules/` in your target repo.

### 2. Import rules into CLAUDE.md

In your target repo's `CLAUDE.md`, import whichever rules apply:

```md
@.claude/rules/general.md
@.claude/rules/node.md
@.claude/rules/code-organisation.md
@.claude/rules/pull-requests.md
@.claude/rules/conventional-commits.md
@.claude/rules/conventional-branch-names.md
```

Claude Code reads `CLAUDE.md` automatically, so the imported rules are always active.

### 3. Update the rules

To pull in the latest changes from this repo:

```sh
git subtree pull --prefix .claude/rules https://github.com/mcalthrop/claude-skills main --squash
```
