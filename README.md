# Devbox + Turborepo Kitchen-Sink Starter

[![Built with Devbox](https://www.jetify.com/img/devbox/shield_galaxy.svg)](https://www.jetify.com/devbox/docs/contributor-quickstart/)

> This is a port of [vercel/turborepo/examples/kitchen-sink](https://github.com/vercel/turborepo/tree/main/examples/kitchen-sink)
> to [Devbox](https://www.jetify.com/devbox).

## Why?

_See [Why Use Devbox?](https://www.jetify.com/docs/devbox/#why-use-devbox)_

- 1 command to run the project
  - `devbox run all`
- 1 command to access the env
  - `devbox shell`
- Import `.env` into the environment
  - ❌ Replaces [dotenv](https://github.com/motdotla/dotenv)
- TUI for service management & visibility, powered by [process-compose](https://github.com/F1bonacc1/process-compose)
  - ❌ Replaces [concurrently](https://github.com/open-cli-tools/concurrently) & turborepo's TUI
- Shared, project-specific shell for all contributors
  - 🙅‍♂️ No more fighting `$PATH`
- Isolate project dependencies from other projects
  - ❌ Replaces [n](https://github.com/tj/n), [nvm](https://github.com/nvm-sh/nvm), conflicting package managers, etc.
- Unlike Docker, no slowness from virtualization
  - ⚠️ So you still need to use different ports for apps (e.g. `:3000`, `:3001`)
- Re-use of the same environment in CI
  - If `devbox run lint` works locally, it works in CI 💪

---

# Turborepo kitchen sink starter

This Turborepo starter is maintained by the Turborepo core team.

This example also shows how to use [Workspace Configurations](https://turborepo.com/docs/core-concepts/monorepos/configuring-workspaces).

## Using this example

Run the following command:

```sh
npx create-turbo@latest -e kitchen-sink
```

## What's inside?

This Turborepo includes the following packages and apps:

### Apps and Packages

- `api`: an [Express](https://expressjs.com/) server
- `storefront`: a [Next.js](https://nextjs.org/) app
- `admin`: a [Vite](https://vitejs.dev/) single page app
- `blog`: a [Remix](https://remix.run/) blog
- `@repo/eslint-config`: ESLint configurations used throughout the monorepo
- `@repo/jest-presets`: Jest configurations
- `@repo/logger`: isomorphic logger (a small wrapper around console.log)
- `@repo/ui`: a dummy React UI library (which contains `<CounterButton>` and `<Link>` components)
- `@repo/typescript-config`: tsconfig.json's used throughout the monorepo

Each package and app is 100% [TypeScript](https://www.typescriptlang.org/).

### Utilities

This Turborepo has some additional tools already setup for you:

- [TypeScript](https://www.typescriptlang.org/) for static type checking
- [ESLint](https://eslint.org/) for code linting
- [Jest](https://jestjs.io) test runner for all things JavaScript
- [Prettier](https://prettier.io) for code formatting
