# Learning Record 0010: CSS & Component Styling Architecture

## Date: 2026-08-16

## Key Insights
1. **Component-Scoped Stylesheets vs. Utility Classes**:
   - **CSS Modules (`Card.module.css`)**: Direct 1:1 conceptual replacement for Angular's `card.component.scss` (generates hashed class names like `.card_root__x9k2p` to prevent style leakage).
   - **Tailwind CSS**: Eliminates the need for separate `.css` files per component by colocating design tokens directly in JSX (`className="p-4 rounded-lg bg-white"`).
   - **Global CSS Pitfall**: In React, plain `import './Card.css'` is **global across the entire app** (unlike Angular's automatic `ViewEncapsulation.Emulated`).
2. **Type-Safe Component Variants (CVA)**:
   - **Class Variance Authority (CVA)** replicates complex SCSS variant mixins with pure TypeScript prop inference for sizes, variants, and compound variants.
3. **Class Conflict Resolution (`twMerge`)**:
   - Standard string concatenation (`clsx`) causes specificity bugs when overriding Tailwind classes. `twMerge` deduplicates and overrides conflicting classes properly.

## Application to Codebase
- Use the standard `cn()` utility (`twMerge(clsx(...))`) for all dynamic class generation.
- Structure design-system components (buttons, badges, alerts) using CVA.
