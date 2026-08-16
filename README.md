# React Web for Angular Devs: Fast-Track Course

A tailored, high-density learning track designed specifically for **Angular engineers and leads** transitioning into **modern React Web development** (React 19, Next.js App Router, TypeScript, React Hook Form, TanStack Query, Zustand).

Rather than starting from zero with basic HTML/JS programming concepts, this course translates the architectural patterns you already master in Angular (Services, Signals, RxJS, Reactive Forms, Route Guards, Dependency Injection, Content Projection) into React Web equivalents.

---

## 📚 Course Curriculum & Lessons

| Lesson # | Module Title | Core Topics | Status |
| :--- | :--- | :--- | :--- |
| **0001** | [**Angular Lead to React Web Mental Model**](./lessons/0001-angular-to-react-web-mental-model.html) | Concept translation matrix, JSX compilation, uni-directional data flow vs 2-way binding. | ✅ Active |
| **0002** | [**Angular Templates & Directives vs. JSX**](./lessons/0002-angular-templates-directives-vs-jsx.html) | `*ngIf`, `*ngFor`, `[ngClass]`, `[ngStyle]`, pipes vs JSX expressions, `.map()`, `clsx`. | ✅ Active |
| **0003** | [**Components, Props & Content Projection**](./lessons/0003-components-props-content-projection.html) | `@Input()`, `@Output() EventEmitter`, `<ng-content>` vs `props`, callbacks, and `children` slot patterns. | ✅ Active |
| **0004** | [**State Management Fundamentals (Signals vs. useState)**](./lessons/0004-state-management-signals-vs-use-state.html) | Angular Signals (`signal`, `computed`, `effect`) vs React `useState`, `useMemo`, `useEffect`. | ✅ Active |
| **0005** | [**Forms Masterclass (Reactive Forms vs. React Hook Form & Zod)**](./lessons/0005-forms-reactive-forms-vs-react-hook-form-zod.html) | `FormGroup`, `FormControl`, custom validators vs React Hook Form, controlled inputs, and Zod schemas. | ✅ Active |
| **0006** | [**Angular Services & DI vs. React Context & Custom Hooks**](./lessons/0006-angular-services-di-vs-context-custom-hooks.html) | `@Injectable({ providedIn: 'root' })` vs `createContext`, `<Provider>`, and composable custom hooks. | ✅ Active |
| **0007** | [**Lifecycle Hooks vs. useEffect & Refs**](./lessons/0007-lifecycle-hooks-vs-use-effect-refs.html) | `ngOnInit`, `ngOnDestroy`, `ngOnChanges`, `@ViewChild` vs `useEffect` dependency arrays, cleanup, and `useRef`. | ✅ Active |
| **0008** | [**Routing Architecture (RouterModule vs. React Router & Next.js)**](./lessons/0008-routing-architecture-router-vs-react-router-nextjs.html) | Lazy loading, Route Guards (`CanActivate`), dynamic params, and layout route hierarchies. | ✅ Active |
| **0009** | [**HTTP Data Pipelines & Server State (RxJS vs. TanStack Query)**](./lessons/0009-http-data-pipelines-rxjs-vs-tanstack-query.html) | `HttpClient` Observables & `| async` pipe vs `fetch` + TanStack Query (`useQuery`, `useMutation`, caching). | ✅ Active |
| **0010** | [**CSS & Component Styling Architecture**](./lessons/0010-css-component-styling-architecture.html) | ViewEncapsulation (Emulated/ShadowDOM) & SCSS vs CSS Modules, Tailwind CSS, and CSS-in-JS. | ✅ Active |
| **0011** | [**Performance Optimization & Reconciliation**](./lessons/0011-performance-optimization-reconciliation.html) | Zone.js vs Virtual DOM Reconciliation, `OnPush` strategy vs `React.memo`, `useMemo`, `useCallback`. | ✅ Active |
| **0012** | [**Complex Global State (NgRx vs. Zustand & Redux Toolkit)**](./lessons/0012-complex-global-state-ngrx-vs-zustand-rtk.html) | Actions, Reducers, Effects, Selectors vs Zustand lightweight atomic stores and RTK slices. | ✅ Active |
| **0013** | [**Server-Side Rendering (SSR) & React Server Components (RSC)**](./lessons/0013-server-side-rendering-ssr-react-server-components-rsc.html) | Angular Universal / SSR Hydration vs Next.js App Router, RSC, `'use client'`, and streaming. | ✅ Active |
| **0014** | [**Component & Integration Testing (TestBed vs. Vitest & RTL)**](./lessons/0014-component-integration-testing-testbed-vs-vitest-rtl.html) | `TestBed`, `By.css` vs Vitest + React Testing Library (`render`, `screen`, `userEvent`, accessibility queries). | ✅ Active |

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
| **Reactive State** | Angular Signals (`signal()`) / `BehaviorSubject` | `useState()` Hook / Zustand |
| **Computed State** | `computed(() => ...)` | `useMemo(() => ...)` |
| **Side Effects** | `effect(() => ...)` / `ngOnInit` | `useEffect(() => ..., [deps])` |
| **Root Service / DI** | `@Injectable({ providedIn: 'root' })` | React Context (`createContext`) / Custom Hook |
| **DOM Reference** | `@ViewChild('myInput')` | `useRef<HTMLInputElement>(null)` |
| **Forms** | `ReactiveFormsModule` (`FormGroup`) | React Hook Form (`useForm`) + Zod |
| **HTTP Fetching** | `HttpClient` + RxJS | `fetch` + TanStack React Query |
| **Change Detection** | Zone.js / Signal dirty checking | Virtual DOM Reconciliation + `React.memo` |
