# Learning Record 0014: Component & Integration Testing (TestBed vs. Vitest & RTL)

## Date: 2026-08-16

## Key Insights
1. **User-Centric Accessible Testing**:
   - Rather than asserting on internal component properties or querying fragile CSS classes (`By.css`), React Testing Library encourages querying via accessible roles (`getByRole`, `getByLabelText`).
2. **Realistic User Simulation (`userEvent`)**:
   - `userEvent` simulates complete browser interaction cycles (focus, keyboard typing, clicking) asynchronously.
3. **Vitest & Jest-DOM**:
   - Vitest provides instant hot-module test execution; `@testing-library/jest-dom` supplies expressive DOM matchers (`toBeInTheDocument`, `toBeDisabled`).

## Application to Codebase
- Standardize all unit and integration testing on Vitest + React Testing Library + `@testing-library/user-event`.
- Write tests that verify user-observable behavior and accessibility roles.
