# Teaching Notes & Learner Profile

- **Background**: Senior Front-End Dev / Team Lead with extensive Angular experience.
- **Learning Style**: Fast-paced conceptual translation (Angular -> React Web), architectural comparisons, real-world patterns, minimal beginner fluff.
- **Lesson Formatting Conventions**:
  - Always use the 3-column translation matrix table: `Concept | Angular (Web) | React (Web)`.
  - Focus on direct conceptual/skill translation between Angular and React.
  - Whenever an npm package or external tool is introduced, provide a direct clickable link to its npm page (`https://www.npmjs.com/package/...`) in both the section text/spotlight and the final `Official Documentation References & NPM Packages` section.
  - Always include a top header navigation bar (`<nav class="lesson-nav">`) with `<a href="../index.html" class="nav-home">&larr; Course Homepage</a>` and previous/next lesson links matching the footer navigation.
- **Key Analogies & Bridges**:
  - `@Input()` -> Component `props`
  - `@Output() EventEmitter` -> Callback props (`onAction={handleAction}`)
  - Angular Services (`providedIn: 'root'`) -> React Context / Custom Hooks / Zustand
  - Angular Signals -> React `useState()` / `useMemo()` / Zustand stores
  - Template Directives (`*ngIf`, `*ngFor`) -> JSX expressions (`&&`, `.map()`)
  - Reactive Forms (`FormGroup`) -> React Hook Form + Zod
  - `HttpClient` + RxJS -> `fetch` / TanStack Query
  - Angular Universal / SSR -> Next.js App Router & React Server Components (RSC)
  - `TestBed` -> Vitest + React Testing Library
