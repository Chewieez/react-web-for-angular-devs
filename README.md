# React Web for Angular Devs: Fast-Track Course

A tailored, high-density learning track designed specifically for **Angular engineers and leads** transitioning into **modern React Web development** (React 19, Next.js App Router, TypeScript, React Hook Form, TanStack Query, Zustand).

Rather than starting from zero with basic HTML/JS programming concepts, this course translates the architectural patterns you already master in Angular (Services, Signals, RxJS, Reactive Forms, Route Guards, Dependency Injection, Content Projection) into React Web equivalents.

---

## 📚 Course Curriculum & Lessons

### 🏛️ Pillar 1: Component & UI Architecture (Foundations)
| Lesson # | Module Title | Core Topics | Status |
| :--- | :--- | :--- | :--- |
| **0001** | [**Angular Lead to React Web Mental Model**](./lessons/0001-angular-to-react-web-mental-model.html) | Concept translation matrix, JSX compilation, uni-directional data flow vs 2-way binding. | ✅ Active |
| **0002** | [**Angular Templates & Directives vs. JSX**](./lessons/0002-angular-templates-directives-vs-jsx.html) | `*ngIf`, `*ngFor`, `[ngClass]`, `[ngStyle]`, pipes vs JSX expressions, `.map()`, `clsx`. | ✅ Active |
| **0003** | [**Components, Props & Content Projection**](./lessons/0003-components-props-content-projection.html) | `@Input()`, `@Output() EventEmitter`, `<ng-content>` vs `props`, callbacks, and `children` slot patterns. | ✅ Active |
| **0004** | [**CSS & Component Styling Architecture**](./lessons/0004-css-component-styling-architecture.html) | ViewEncapsulation (Emulated/ShadowDOM) & SCSS vs CSS Modules, Tailwind CSS, and CSS-in-JS. | ✅ Active |
| **0005** | [**Enterprise Design Systems & Headless UI**](./lessons/0005-design-system-architecture-headless-ui-cva.html) | Angular Material / Angular CDK vs Radix UI, `shadcn/ui`, `class-variance-authority` (CVA), and `tailwind-merge`. | ✅ Active |

### ⚡ Pillar 2: Reactivity, State & Forms
| Lesson # | Module Title | Core Topics | Status |
| :--- | :--- | :--- | :--- |
| **0006** | [**State Management Fundamentals (Signals vs. useState)**](./lessons/0006-state-management-signals-vs-use-state.html) | Angular Signals (`signal`, `computed`, `effect`) vs React `useState`, `useMemo`, `useEffect`. | ✅ Active |
| **0007** | [**Lifecycle Hooks vs. useEffect & Refs**](./lessons/0007-lifecycle-hooks-vs-use-effect-refs.html) | `ngOnInit`, `ngOnDestroy`, `ngOnChanges`, `@ViewChild` vs `useEffect` dependency arrays, cleanup, and `useRef`. | ✅ Active |
| **0008** | [**Angular Services & DI vs. React Context & Custom Hooks**](./lessons/0008-angular-services-di-vs-context-custom-hooks.html) | `@Injectable({ providedIn: 'root' })` vs `createContext`, `<Provider>`, and composable custom hooks. | ✅ Active |
| **0009** | [**Forms Masterclass (Reactive Forms vs. React Hook Form & Zod)**](./lessons/0009-forms-reactive-forms-vs-react-hook-form-zod.html) | `FormGroup`, `FormControl`, custom validators vs React Hook Form, controlled inputs, and Zod schemas. | ✅ Active |
| **0010** | [**React 19 Actions, Form State & Optimistic UI**](./lessons/0010-react-19-actions-use-action-state-optimistic.html) | `(ngSubmit)` & manual rollbacks vs `useActionState`, `useOptimistic`, `useFormStatus`, and form actions. | ✅ Active |

### 🌐 Pillar 3: Data Pipelines, Server State & Global Stores
| Lesson # | Module Title | Core Topics | Status |
| :--- | :--- | :--- | :--- |
| **0011** | [**HTTP Data Pipelines & Server State (RxJS vs. TanStack Query)**](./lessons/0011-http-data-pipelines-rxjs-vs-tanstack-query.html) | `HttpClient` Observables & `| async` pipe vs `fetch` + TanStack Query (`useQuery`, `useMutation`, caching). | ✅ Active |
| **0012** | [**Real-Time Data Pipelines & WebSockets**](./lessons/0012-real-time-streaming-websockets.html) | RxJS `webSocket()` & `| async` pipe vs `useWebSocket` streaming hooks and TanStack Query live cache updates. | ✅ Active |
| **0013** | [**Complex Global State (NgRx vs. Zustand & Redux Toolkit)**](./lessons/0013-complex-global-state-ngrx-vs-zustand-rtk.html) | Actions, Reducers, Effects, Selectors vs Zustand lightweight atomic stores and RTK slices. | ✅ Active |

### 🚀 Pillar 4: Routing, Full-Stack React & Performance
| Lesson # | Module Title | Core Topics | Status |
| :--- | :--- | :--- | :--- |
| **0014** | [**Routing Architecture (RouterModule vs. React Router & Next.js)**](./lessons/0014-routing-architecture-router-vs-react-router-nextjs.html) | Lazy loading, Route Guards (`CanActivate`), dynamic params, and layout route hierarchies. | ✅ Active |
| **0015** | [**Server-Side Rendering (SSR) & React Server Components (RSC)**](./lessons/0015-server-side-rendering-ssr-react-server-components-rsc.html) | Angular Universal / SSR Hydration vs Next.js App Router, RSC, `'use client'`, and streaming. | ✅ Active |
| **0016** | [**Performance Optimization & Reconciliation**](./lessons/0016-performance-optimization-reconciliation.html) | Zone.js vs Virtual DOM Reconciliation, `OnPush` strategy vs `React.memo`, `useMemo`, `useCallback`. | ✅ Active |

### 🛡️ Pillar 5: Testing, Monorepos & Enterprise Scale
| Lesson # | Module Title | Core Topics | Status |
| :--- | :--- | :--- | :--- |
| **0017** | [**Component & Integration Testing (TestBed vs. Vitest & RTL)**](./lessons/0017-component-integration-testing-testbed-vs-vitest-rtl.html) | `TestBed`, `By.css` vs Vitest + React Testing Library (`render`, `screen`, `userEvent`, accessibility queries). | ✅ Active |
| **0018** | [**AI-Assisted Browser Testing & Network Mocking**](./lessons/0018-browser-testing-chrome-devtools-mcp-msw.html) | Protractor / Cypress & `HttpTestingController` vs Chrome DevTools MCP (AI browser verification) and Mock Service Worker (MSW v2). | ✅ Active |
| **0019** | [**Enterprise Monorepos & Workspace Tooling**](./lessons/0019-monorepos-workspace-tooling-turborepo-nx.html) | `angular.json` multi-projects & `ng g library` vs Turborepo / Nx, internal packages, and build caching. | ✅ Active |
| **0020** | [**Microfrontends & Module Federation**](./lessons/0020-microfrontends-module-federation.html) | `@angular-architects/module-federation` vs Module Federation 2.0 (Rsbuild/Webpack), dynamic remotes, and error boundaries. | ✅ Active |

---

## 💡 Quick Concept Translation Summary

| Concept | Angular (Web) | React (Web) |
| :--- | :--- | :--- |
| **Component Template** | HTML Template (`templateUrl`) | JSX / TSX |
| **Input Property** | `@Input() name: string` | `props.name` / `{ name }: Props` |
| **Event Emission** | `@Output() changed = new EventEmitter()` | Callback Prop: `onChanged(val)` |
| **Conditionals** | `*ngIf="condition"` | `{condition && <Component />}` / Ternary |
| **Loops** | `*ngFor="let item of items; trackBy: id"` | `{items.map(item => <Component key={item.id} />)}` |
| **Content Projection** | `<ng-content>` / `<ng-content select="...">` | `props.children` / Named Slot Props |
| **Component Styling** | `ViewEncapsulation` & SCSS | Tailwind CSS + CSS Modules (`.module.css`) + CVA |
| **Design System Primitives** | Angular CDK & Angular Material | Radix UI Primitives + `class-variance-authority` + `shadcn/ui` |
| **Reactive State** | Angular Signals (`signal()`) / `BehaviorSubject` | `useState()` Hook / Zustand |
| **Computed State** | `computed(() => ...)` | `useMemo(() => ...)` |
| **Side Effects & Lifecycles** | `effect(() => ...)` / `ngOnInit` / `ngOnDestroy` | `useEffect(() => ..., [deps])` |
| **Root Service / DI** | `@Injectable({ providedIn: 'root' })` | React Context (`createContext`) / Custom Hook |
| **Forms** | `ReactiveFormsModule` (`FormGroup`) | React Hook Form (`useForm`) + Zod |
| **Form Actions & Optimistic State** | `(ngSubmit)` + manual RxJS rollbacks | React 19 Actions (`useActionState`, `useOptimistic`) |
| **HTTP Fetching** | `HttpClient` + RxJS | `fetch` + TanStack React Query |
| **Real-Time Pipelines** | RxJS `webSocket()` & `| async` | `react-use-websocket` + TanStack Query cache invalidation |
| **Global State** | NgRx Store (Actions, Reducers, Effects) | Zustand atomic stores / Redux Toolkit |
| **Routing & Guards** | `RouterModule` + `CanActivate` | React Router v6+ / Next.js App Router |
| **SSR & Hydration** | Angular Universal / `provideClientHydration` | Next.js App Router & React Server Components (RSC) |
| **Change Detection / Reconciliation** | Zone.js / Signal dirty checking / `OnPush` | Virtual DOM Reconciliation + `React.memo` |
| **Component Testing** | `TestBed` & `By.css` | Vitest + React Testing Library (`userEvent`, `getByRole`) |
| **AI Browser Testing & Mocking** | Protractor / Cypress & `HttpTestingController` | Chrome DevTools MCP & Mock Service Worker (MSW v2) |
| **Monorepo Tooling** | `angular.json` & `ng g library` | Turborepo / Nx + Internal Workspace Packages |
| **Microfrontends** | `@angular-architects/module-federation` | Module Federation 2.0 (`@module-federation/enhanced`) |

