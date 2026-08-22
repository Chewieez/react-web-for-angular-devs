# Learning Record 0005: Enterprise Design Systems & Headless UI

## Concept Overview
- **Angular Pattern**: Monolithic UI component libraries (Angular Material, PrimeNG) or custom components wrapping `@angular/cdk/a11y`, `@angular/cdk/overlay`, and `@angular/cdk/dialog`, with SCSS class unions and `::ng-deep` override challenges.
- **React Pattern**: Headless accessible primitives (Radix UI / React Aria) combined with `class-variance-authority` (CVA) for type-safe variants, `tailwind-merge` (`cn` helper) for conflict-free utility overrides, and the `asChild` polymorphic slot pattern (`@radix-ui/react-slot`).

## Key Bridges & Translations
1. `@angular/cdk` primitives &rarr; `@radix-ui/react-*` unstyled accessible components.
2. Angular SCSS BEM / enum variants &rarr; `class-variance-authority` (`cva()`) with `VariantProps<typeof ...>`.
3. String template class concatenation &rarr; `cn()` utility combining `clsx` and `tailwind-merge`.
4. `*ngComponentOutlet` / custom directives &rarr; `@radix-ui/react-slot` (`asChild` pattern).
5. Monolithic UI packages with CSS locks &rarr; Source-code owned design system architecture (`shadcn/ui`).

## Packages & References
- [`class-variance-authority`](https://www.npmjs.com/package/class-variance-authority) &bull; [CVA Docs](https://cva.style/docs)
- [`tailwind-merge`](https://www.npmjs.com/package/tailwind-merge) &bull; [tailwind-merge Repository](https://github.com/dcastil/tailwind-merge)
- [`@radix-ui/react-slot`](https://www.npmjs.com/package/@radix-ui/react-slot) &bull; [Radix Slot Documentation](https://www.radix-ui.com/primitives/docs/utilities/slot)
