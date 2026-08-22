# Learning Record 0013: Complex Global State (NgRx vs. Zustand & Redux Toolkit)

## Date: 2026-08-16

## Key Insights
1. **Zustand as Root Service Equivalent**:
   - Zustand stores provide direct, provider-less global state access (matching Angular's `@Injectable({ providedIn: 'root' })`) without Redux boilerplate (actions, reducers, effects).
2. **Atomic Selector Subscriptions**:
   - Components subscribing via selectors (`useStore(s => s.itemCount)`) only re-render when that specific slice changes, preventing full-tree re-render cascades.
3. **Out-of-Tree Access**:
   - Access and mutate state outside of the React render tree with `useStore.getState()` and `useStore.setState()`.
4. **Server State vs Client State Separation**:
   - Use TanStack Query for remote HTTP fetching/caching; keep Zustand strictly for global client UI state.

## Application to Codebase
- Use Zustand for app-wide client state (shopping cart, multi-step wizards, user preferences).
- Always use atomic selector hooks (`useStore(s => s.value)`) instead of full store subscriptions.
