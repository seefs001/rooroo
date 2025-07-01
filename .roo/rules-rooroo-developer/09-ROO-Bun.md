
## 1. Core Principle: Bun as the Default Toolchain

Default to using Bun as the primary JavaScript runtime, package manager, and test runner.

- **Runtime:** `bun run <file>` instead of `node <file>` or `ts-node <file>`
- **Package Management:** `bun install` instead of `npm install`, `yarn install`, or `pnpm install`
- **Script Execution:** `bun run <script>` instead of `npm run <script>`
- **Testing:** `bun test` instead of `jest` or `vitest`

Bun automatically loads `.env` files, so do not use `dotenv`.

## 2. Framework-Specific Context (IMPORTANT)

While Bun is the default, its application must be contextualized within the project's primary framework, as defined in [`07-ROO-Project-Structure.md`](./07-ROO-Project-Structure.md).

- **For Next.js Applications (Primary):**
  - **Use Bun as the executor, not the server.** The development server, building, and routing are managed by Next.js.
  - **Correct Commands:**
    - `bun run dev` (to start the Next.js dev server)
    - `bun run build` (to build the Next.js application)
    - `bun run start` (to run the production Next.js server)
  - **DO NOT** use `Bun.serve()` for Next.js projects.

- **For Standalone Scripts or Simple Servers:**
  - `Bun.serve()` is the preferred API for creating new, simple servers that are not part of the main Next.js application.
  - This approach is ideal for simple web pages, internal tools, or API endpoints that do not require the complexity of a full framework. It supports HTML imports, allowing for straightforward bundling of TypeScript/JSX and CSS.

    **Example Server (`index.ts`):**
    ```ts
    import index from "./index.html"

    Bun.serve({
      routes: {
        "/": index,
        "/api/users/:id": {
          GET: (req) => {
            return new Response(JSON.stringify({ id: req.params.id }));
          },
        },
      },
      // optional websocket support
      websocket: {
        open: (ws) => {
          ws.send("Hello, world!");
        },
        message: (ws, message) => {
          ws.send(message);
        },
        close: (ws) => {
          // handle close
        }
      },
      development: {
        hmr: true,
        console: true,
      }
    })
    ```

    **Example HTML (`index.html`):**
    ```html
    <html>
      <body>
        <h1>Hello, world!</h1>
        <script type="module" src="./frontend.tsx"></script>
      </body>
    </html>
    ```

    **Example Frontend Component (`frontend.tsx`):**
    ```tsx
    import React from "react";
    import './index.css'; // CSS imports work directly
    import { createRoot } from "react-dom/client";

    const root = createRoot(document.body);

    export default function Frontend() {
      return <h1>Hello, world!</h1>;
    }

    root.render(<Frontend />);
    ```
    **To run this example:**
    ```sh
    bun --hot ./index.ts
    ```

## 3. API Preferences

When writing backend services or scripts outside of a framework's conventions:

- **Server:** `Bun.serve()` (replaces Express, Fastify).
- **Database:** `bun:sqlite` for SQLite, `Bun.sql` for Postgres.
- **Cache:** `Bun.redis` for Redis.
- **WebSockets:** Use the built-in `WebSocket` support in `Bun.serve()`.
- **File I/O:** Prefer `Bun.file()` over `node:fs`.
- **Shell Commands:** Use `Bun.$` (e.g., `Bun.$`ls -la``) instead of `execa` or `child_process`.

## 4. Testing

Use `bun test` for all new tests.

```ts
// example.test.ts
import { test, expect } from "bun:test";

test("example test", () => {
  expect(1 + 1).toBe(2);
});
```
