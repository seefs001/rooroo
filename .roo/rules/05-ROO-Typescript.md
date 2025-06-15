# 05-ROO-TypeScript: TypeScript Development Guidelines

This document outlines specific rules, conventions, and best practices for TypeScript development within Rooroo. Adherence to these guidelines ensures code quality, consistency, and maintainability across projects.

## 1. Tooling & Environment
*   **Compiler Configuration (`tsconfig.json`):** Always enable `strict` mode. This is the single most effective way to leverage TypeScript's type-checking capabilities. Key flags include `noImplicitAny`, `strictNullChecks`, `strictFunctionTypes`, and `strictPropertyInitialization`.
*   **Linter & Formatter:** Use ESLint with `@typescript-eslint/parser` and `@typescript-eslint/eslint-plugin` for static analysis. Use Prettier for consistent code formatting. Ensure these are configured to run automatically on save and before commits.

## 2. Coding Best Practices
*   **Type Inference:** Prefer type inference wherever possible. Let the compiler infer types unless the type is not obvious or needs to be explicitly defined for clarity or to create a specific contract.
    ```typescript
    // Good: Type is inferred
    let name = "Rooroo";

    // Good: Explicit type for function return values and parameters
    function greet(user: string): string {
      return `Hello, ${user}`;
    }
    ```
*   **Explicit `any`:** Avoid using the `any` type. Its use negates the benefits of TypeScript. If you must use it, provide a comment explaining why. For unknown values, prefer the `unknown` type and perform type checking before use.
*   **Interfaces vs. Types:** Use `interface` for defining the shape of objects or classes that can be implemented or extended. Use `type` for creating aliases for primitive types, unions, tuples, or more complex types that don't fit the object-oriented model of interfaces.
*   **Modularity:** Keep files focused on a single responsibility. Use ES Modules (`import`/`export`) for organizing code.

## 3. Framework & Library Specifics

### 3.1. shadcn/ui
*   **Component Installation:** The `shadcn-ui` CLI command has been deprecated. The current, correct command for adding new components is via `bunx`.
*   **Command:**
    ```bash
    bunx --bun shadcn@canary add <component_name> --all --overwrite
    ```
*   **Usage Note:** Always check the project's existing components and styles before adding new ones to maintain consistency. Use the `--overwrite` flag with caution.
*   **Editing Components:** Components installed into `components/ui` are considered foundational. **Do not edit these files directly unless absolutely necessary.** If customization is required, consider wrapping the component in your own higher-level component. This approach preserves the ability to update the base components from `shadcn/ui` in the future.

## 4. Asynchronous Code
*   **`async/await`:** Prefer `async/await` over raw Promises for cleaner, more readable asynchronous code.
*   **Error Handling:** Always wrap `await` calls in `try...catch` blocks or use promise chaining with `.catch()` to handle potential rejections gracefully. Do not let promises go unhandled.