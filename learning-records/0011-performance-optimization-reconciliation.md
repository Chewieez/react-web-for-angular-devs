# Learning Record 0011: Performance Optimization & Reconciliation

## Date: 2026-08-16

## Key Insights
1. **Virtual DOM Fiber vs. Zone.js**:
   - Angular Zone.js performs top-down dirty checking triggered by patched asynchronous APIs.
   - React Fiber updates are explicitly scheduled via state setters, diffing the Virtual DOM tree and committing only real DOM differences.
2. **OnPush vs. React.memo**:
   - `React.memo(Component)` skips component re-renders when prop references remain unchanged (`===`).
   - To make `React.memo` effective, callback functions passed as props must be stabilized with `useCallback()`, and non-primitive objects with `useMemo()`.
3. **The React 19 Compiler**:
   - Build-time automatic memoization is reducing manual `useMemo`/`useCallback` boilerplate across modern React projects.

## Application to Codebase
- Wrap large list/grid child components in `React.memo` when rendering high-frequency streaming data.
- Stabilize function props passed to memoized children using `useCallback`.
- Avoid premature `useMemo` optimization on cheap arithmetic operations.
