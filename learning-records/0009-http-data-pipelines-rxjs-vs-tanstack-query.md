# Learning Record 0009: HTTP Data Pipelines & Server State (RxJS vs. TanStack Query)

## Date: 2026-08-16

## Key Insights
1. **Server State vs. Client State**:
   - In React, server responses are not treated as global client state (avoiding complex NgRx stores or manual `BehaviorSubject` cache layers). TanStack Query manages caching, deduplication, and background synchronization out-of-the-box.
2. **Query Keys as Reactive Dependencies**:
   - The `queryKey` array functions like RxJS `switchMap`: whenever dynamic parameters in the key change (e.g. `['users', { role, page }]`), TanStack Query automatically fetches fresh data and cancels stale in-flight requests.
3. **Mutations & Invalidation**:
   - `useMutation` pairs with `queryClient.invalidateQueries({ queryKey: ['users'] })` to declaratively refresh data across the application upon successful writes.
4. **`staleTime` vs `gcTime`**:
   - `staleTime` dictates when background refetching occurs; `gcTime` dictates how long unused cache memory is retained.

## Application to Codebase
- Install and wrap the application root in `<QueryClientProvider client={queryClient}>`.
- Standardize all REST/GraphQL fetching on `useQuery` and mutations on `useMutation`.
- Use `@tanstack/react-query-devtools` during development for visual cache inspection.
