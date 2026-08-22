# Learning Record 0008: Angular Services & DI vs. React Context & Custom Hooks

## Date: 2026-08-16

## Key Insights
1. **Logic Sharing vs. State Sharing**:
   - **Custom Hooks**: Encapsulate reusable stateful logic; each consumer component receives its own isolated state instance.
   - **React Context**: Used to share a single state instance down a component tree without prop drilling.
2. **Gold Standard Provider Pattern**:
   - Create a typed Context (`createContext<T | null>(null)`).
   - Wrap in a dedicated `<Provider>` component that manages internal state and memoizes the context value (`useMemo`).
   - Expose a custom hook (`useAuth()`) that validates the provider is present and throws a fail-fast error if missing.
3. **React 19 Enhancements**:
   - Render `<Context value={...}>` directly instead of `<Context.Provider>`.
   - Read context conditionally or inside async loops using the `use(Context)` hook.
4. **Context vs External Stores (Zustand)**:
   - React Context re-renders all consumer components on any state change. For high-frequency state updates, use lightweight selector-based stores like Zustand.

## Application to Codebase
- Encapsulate app-wide shared state (Auth, Theme, Workspaces) using the Context + Custom Hook pattern.
- Always wrap context values in `useMemo` to prevent unnecessary re-render cascades.
- Use Zustand for complex or high-frequency global state.
