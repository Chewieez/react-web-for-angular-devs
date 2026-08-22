# Learning Record 0010: React 19 Actions, Form State & Optimistic UI

## Concept Overview
- **Angular Pattern**: Form submissions using `(ngSubmit)`, manual boolean flags (`isSubmitting = true`), manual error handling, and manual array rollbacks inside RxJS `catchError`.
- **React 19 Pattern**: Async **Actions** integrated directly with `<form action={...}>`, `useActionState` managing async response/error/pending states, `useFormStatus` for decoupled button pending indicators, and `useOptimistic` for declarative provisional updates with automatic rollback.

## Key Bridges & Translations
1. `(ngSubmit)="onSubmit()"` &rarr; `<form action={formAction}>` (Receives native `FormData`).
2. Manual loading & error booleans &rarr; `const [state, formAction, isPending] = useActionState(asyncFn, initialVal)`.
3. `@Input() isSubmitting` on button &rarr; `const { pending } = useFormStatus()` inside button components.
4. Imperative rollback in RxJS `catchError` &rarr; `const [optimistic, setOptimistic] = useOptimistic(state, updateFn)` (React handles rollback if action fails).

## Packages & References
- [`react`](https://www.npmjs.com/package/react) &bull; [React useActionState Docs](https://react.dev/reference/react/useActionState)
- [`react-dom`](https://www.npmjs.com/package/react-dom) &bull; [React useFormStatus Docs](https://react.dev/reference/react-dom/hooks/useFormStatus)
