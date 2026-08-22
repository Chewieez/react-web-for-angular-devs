# Learning Record 0019: Enterprise Monorepos & Workspace Tooling

## Concept Overview
- **Angular Pattern**: Monorepos managed via `angular.json` multi-project configurations or Nx for Angular, `ng generate library`, secondary entrypoints, and `tsconfig.base.json` path mappings.
- **React Pattern**: Package manager workspaces (pnpm / npm / yarn) orchestrated by Turborepo or Nx, internal workspace packages (e.g. `@repo/ui`) with modern `exports` maps, and local/remote build pipeline caching (`turbo.json`).

## Key Bridges & Translations
1. `angular.json` build/test targets &rarr; `turbo.json` task dependency graph (`dependsOn: ["^build"]`).
2. `ng g library @my-org/ui` &rarr; Workspace package `packages/ui` exporting source `.tsx` directly.
3. `tsconfig.base.json` path mapping &rarr; pnpm workspace protocol (`"workspace:*"`) + TS Project References.
4. `.angular/cache` &rarr; Turborepo / Nx remote hash-based caching in CI/CD.

## Packages & References
- [`turbo`](https://www.npmjs.com/package/turbo) &bull; [Turborepo Documentation](https://turbo.build/repo/docs)
- [`nx`](https://www.npmjs.com/package/nx) &bull; [Nx Documentation](https://nx.dev)
