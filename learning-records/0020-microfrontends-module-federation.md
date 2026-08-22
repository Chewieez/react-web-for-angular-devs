# Learning Record 0020: Microfrontends & Module Federation

## Concept Overview
- **Angular Pattern**: Microfrontends implemented using `@angular-architects/module-federation`, Web Components / Angular Elements wrappers, or dynamic remote module loading in Angular router configurations.
- **React Pattern**: Module Federation 2.0 (`@module-federation/enhanced`), declaring shared singletons (`react`, `react-dom`) to prevent broken hook dispatches, dynamically loading remotes via `React.lazy()` or `loadRemote()`, and wrapping remotes in `<ErrorBoundary>` + `<Suspense>`.

## Key Bridges & Translations
1. `withModuleFederationPlugin()` &rarr; `@module-federation/enhanced` / `ModuleFederationPlugin`.
2. `shareAll({ singleton: true })` &rarr; `shared: { react: { singleton: true }, 'react-dom': { singleton: true } }`.
3. `loadRemoteModule()` &rarr; `React.lazy(() => import('remote/Component'))`.
4. Angular global error handler &rarr; React `<ErrorBoundary fallback={<Fallback />}>` per microfrontend.

## Packages & References
- [`@module-federation/enhanced`](https://www.npmjs.com/package/@module-federation/enhanced) &bull; [Module Federation Docs](https://module-federation.io)
- [`react`](https://www.npmjs.com/package/react) &bull; [React.lazy Documentation](https://react.dev/reference/react/lazy)
