# Learning Record 0003: Components, Props & Content Projection

## Date: 2026-08-15

## Key Insights
1. **Single Props Argument**: Unlike Angular's `@Input()` and `@Output() EventEmitter` class decorators, React functions receive a single typed `props` object containing both data and event callbacks.
2. **Strict Prop Immutability**: Props are read-only. Children must never mutate props; instead, invoke parent callbacks to trigger state updates.
3. **Flexible Slot Architecture**:
   - Single slot (`<ng-content>`): `children: React.ReactNode`.
   - Multi-slot (`<ng-content select="[header]">`): Named JSX slot props (`header?: React.ReactNode`).
   - Contextual projection (`*ngTemplateOutlet`): Render Props (`renderItem: (item: T) => React.ReactNode`).
4. **Composition over Prop Drilling**: Using `children` and slot props lets parent components compose UI directly, eliminating intermediate prop drilling without needing global services.

## Application to Codebase
- Use standard TypeScript interfaces for component props with destructured defaults.
- Use `React.ReactNode` for slots and children.
- Leverage component composition to simplify deep component hierarchies.
