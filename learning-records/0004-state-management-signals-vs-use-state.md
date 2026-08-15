# Learning Record 0004: State Management Fundamentals (Signals vs. useState & useMemo)

## Date: 2026-08-15

## Key Insights
1. **Reactivity Mental Model**:
   - **Angular Signals**: Granular push/pull dependency graph where updates selectively dirty targeted template nodes without re-executing component methods.
   - **React Hooks**: Top-to-bottom function re-execution model where state updates schedule a complete re-run of the functional component.
2. **Derived State & Anti-Patterns**:
   - In React, avoid mirroring derived or computed data into redundant `useState` hooks with `useEffect` synchronizers.
   - Compute values inline during render or wrap in `useMemo` for expensive computations / referential stability.
3. **Immutability & Reference Equality**:
   - React skips re-renders if `Object.is(oldState, newState)` is true. Direct in-place array/object mutations (`push`, `splice`) break reactivity. Always use spread syntax or `.map()` / `.filter()`.
4. **Updater Functions for Batching**:
   - Always use `setCount(prev => prev + 1)` when next state depends on current state to protect against stale closures in batched updates.

## Application to Codebase
- Use `useState` for true local component state.
- Keep derived values inline or cached with `useMemo`.
- Never mutate state objects directly.
