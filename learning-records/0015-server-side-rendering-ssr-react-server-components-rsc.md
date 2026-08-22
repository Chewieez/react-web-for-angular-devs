# Learning Record 0015: Server-Side Rendering (SSR) & React Server Components (RSC)

## Date: 2026-08-16

## Key Insights
1. **React Server Components (RSC) vs. Traditional SSR**:
   - In Angular SSR / traditional React SSR, the entire component tree is executed on the server and then completely re-hydrated on the client.
   - In React Server Components, server components run **only on the server**, shipping **0 KB of client JavaScript**.
2. **Interactive Client Boundaries (`'use client'`)**:
   - Mark interactive components with `'use client'` at the file top to enable hooks (`useState`, `useEffect`) and browser event listeners (`onClick`).
   - Push `'use client'` boundaries down to leaf components to maximize server prerendering.
3. **Server Actions (`'use server'`)**:
   - Execute secure async functions directly from forms without creating separate REST API endpoints.

## Application to Codebase
- Structure Next.js App Router routes with Server Components for data fetching and small client islands for user interactions.
- Access databases, secrets, and filesystem resources directly in Server Components.
