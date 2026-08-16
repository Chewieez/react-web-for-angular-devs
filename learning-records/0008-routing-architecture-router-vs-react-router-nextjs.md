# Learning Record 0008: Routing Architecture (RouterModule vs. React Router & Next.js)

## Date: 2026-08-16

## Key Insights
1. **Layout Routes & Outlets**:
   - React Router's `<Outlet />` mirrors Angular's `<router-outlet>`. Wrapping nested child routes in parent layouts preserves parent state and scroll position across route transitions without unmounting.
2. **Protected Route Guards**:
   - Angular's class-based `CanActivate` is translated into declarative **Layout Route Guards** (`<ProtectedRoute><Outlet /></ProtectedRoute>`) using `<Navigate to="/login" replace />` or data route loaders with `redirect()`.
3. **Parameter Access**:
   - Access URL parameters synchronously with `useParams()` without requiring Observable subscriptions (`ActivatedRoute.params.subscribe`).
4. **Client-Side Links**:
   - Never use native `<a href="...">` for internal routes; always use `<Link>` or `<NavLink>` to prevent hard browser refreshes and state destruction.

## Application to Codebase
- Use `createBrowserRouter` with nested layout routes and `<Outlet />` for React SPA routing.
- Implement auth and permission protection using Layout Route Guards or route `loader` redirects.
- Use `<NavLink>` for styled active navigation menus.
