# Node.js Version Management

Before executing any `pnpm`, `node`, or `npm` commands:

```sh
source ~/.zshrc && nvm install
```

This ensures the correct Node.js version is installed and active based on `.nvmrc`.

Additionally, when running `pnpm`, `node`, or `git` commands that may invoke Node (e.g. Husky hooks), wrap them with:

```sh
zsh -i -c "..."
```

This ensures the correct Node version from `.nvmrc` is active.
