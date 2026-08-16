# Learning Record 0005: Forms Masterclass (Reactive Forms vs. React Hook Form & Zod)

## Date: 2026-08-15

## Key Insights
1. **Uncontrolled Form Performance**:
   - Rather than creating a `useState` per input (which re-renders on every keystroke), React Hook Form uses uncontrolled inputs via native DOM `ref`s for 0-re-render typing.
2. **Schema-First Validation with Zod**:
   - Defining a single Zod schema (`z.object({...})`) provides both runtime validation and static TypeScript type inference (`z.infer<typeof schema>`).
3. **Custom Component Integration**:
   - React's `<Controller>` component completely eliminates the 20+ lines of `ControlValueAccessor` (CVA) boilerplate required in Angular to integrate 3rd-party/custom input components.
4. **Form Array Management**:
   - `useFieldArray` provides declarative methods (`append`, `remove`, `move`) using unique `field.id` keys for stable list reconciliation.

## Application to Codebase
- Standardize all web forms on `react-hook-form` + `zod` with `@hookform/resolvers/zod`.
- Use `<Controller>` for custom UI elements (custom selects, date pickers, rich editors).
- Always use `field.id` as the React `key` in dynamic field arrays.
