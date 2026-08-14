# Learning Record 0001: Angular Lead to React Web Mental Model

## Date: 2026-08-14

## Key Insight
1. **Framework vs. Library**: Angular is an opinionated framework; React is a functional UI library.
2. **JSX Transpilation**: JSX is purely JavaScript function calls (`_jsx('div', ...)`), enabling all standard JavaScript expressions inside templates.
3. **Uni-Directional Data Flow**: Props pass data down; callback functions pass events up. There are no class instances or `this` context.

## Application to Codebase
- Structure components as pure functions taking typed Props interfaces.
- Replace `@Input()` and `@Output()` with typed function props.
