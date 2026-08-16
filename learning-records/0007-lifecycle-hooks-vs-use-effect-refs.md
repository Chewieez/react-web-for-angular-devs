# Learning Record 0007: Lifecycle Hooks vs. useEffect & Refs

## Date: 2026-08-16

## Key Insights
1. **Synchronization vs. Lifecycle Checkpoints**:
   - `useEffect` is not a time-based lifecycle hook (`ngOnInit`/`ngOnDestroy`); it is a synchronization tool to keep React components aligned with external systems (timers, WebSockets, browser listeners, 3rd party non-React libs).
2. **"You Might Not Need an Effect"**:
   - Avoid using `useEffect` for derived state calculations or user event handling. Compute values inline during render or inside event callbacks.
3. **useRef Superpowers**:
   - **DOM Node Access**: Direct access to native elements (`focus()`, `scrollTop`, DOM measurements).
   - **Persistent Mutable State**: Store timers, AbortControllers, and connection handles across renders without triggering re-renders.
4. **Strict Mode & Cleanups**:
   - Always return a cleanup function from `useEffect` to guarantee zero memory leaks and handle React 18/19 Strict Mode double-mounting gracefully.

## Application to Codebase
- Use `useEffect` strictly for external synchronization and always return cleanup handlers.
- Use `useRef` for DOM references and non-visual mutable values (timers, socket instances).
- Never read or write `ref.current` during JSX render evaluation.
