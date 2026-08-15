# Learning Record 0002: Angular Templates & Directives vs. JSX

## Date: 2026-08-15

## Key Insights
1. **No Micro-Syntax in React**: React has no special template language or DSL; conditionals (`&&`, ternary) and loops (`.map()`) are standard JavaScript expressions.
2. **Virtual DOM Keys**: The `key` prop in React serves the same reconciliation role as `trackBy` / `@for (...; track id)` in Angular. Keys must be unique and stable.
3. **Dynamic Styling**: Class toggling is handled with standard utilities like `clsx` rather than `[ngClass]`.
4. **Pipes vs Pure JS Functions**: Angular Pipes are replaced by standard JavaScript helper functions or standard Web APIs (e.g. `Intl.DateTimeFormat`).

## Application to Codebase
- Use `clsx` for conditional CSS classes.
- Use explicit boolean casting (`count > 0 && <Badge />`) to avoid rendering literal `0`.
