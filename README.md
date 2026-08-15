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
| **0005** | **Forms Masterclass (Reactive Forms vs. React Hook Form & Zod)** | `FormGroup`, `FormControl`, custom validators vs React Hook Form, controlled inputs, and Zod schemas. | ⏳ Pending |
| **0006** | **Angular Services & DI vs. React Context & Custom Hooks** | `@Injectable({ providedIn: 'root' })` vs `createContext`, `<Provider>`, and composable custom hooks. | ⏳ Pending |
| **0007** | **Lifecycle Hooks vs. useEffect & Refs** | `ngOnInit`, `ngOnDestroy`, `ngOnChanges`, `@ViewChild` vs `useEffect` dependency arrays, cleanup, and `useRef`. | ⏳ Pending |
| **0008** | **Routing Architecture (RouterModule vs. React Router & Next.js)** | Lazy loading, Route Guards (`CanActivate`), dynamic params, and layout route hierarchies. | ⏳ Pending |
| **0009** | **HTTP Data Pipelines & Server State (RxJS vs. TanStack Query)** | `HttpClient` Observables & `| async` pipe vs `fetch` + TanStack Query (`useQuery`, `useMutation`, caching). | ⏳ Pending |
| **0010** | **CSS & Component Styling Architecture** | ViewEncapsulation (Emulated/ShadowDOM) & SCSS vs CSS Modules, Tailwind CSS, and CSS-in-JS. | ⏳ Pending |
| **0011** | **Performance Optimization & Reconciliation** | Zone.js vs Virtual DOM Reconciliation, `OnPush` strategy vs `React.memo`, `useMemo`, `useCallback`. | ⏳ Pending |
| **0012** | **Complex Global State (NgRx vs. Zustand & Redux Toolkit)** | Actions, Reducers, Effects, Selectors vs Zustand lightweight atomic stores and RTK slices. | ⏳ Pending |
| **0013** | **Server-Side Rendering (SSR) & React Server Components (RSC)** | Angular Universal / SSR Hydration vs Next.js App Router, RSC, `'use client'`, and streaming. | ⏳ Pending |
| **0014** | **Component & Integration Testing (TestBed vs. Vitest & RTL)** | `TestBed`, `By.css` vs Vitest + React Testing Library (`render`, `screen`, `userEvent`, accessibility queries). | ⏳ Pending |

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
