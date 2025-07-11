Knowledge Base Links (use tools to access):

- Vercel AI SDK: https://v5.sdk.vercel.ai/llms.txt → ai@beta
- uv: https://docs.astral.sh/uv/llms.txt
- Drizzle ORM: https://orm.drizzle.team/llms-full.txt
- Better Auth: https://www.better-auth.com/llms.txt
- Supabase: https://supabase.com/llms.txt
- UX Patterns for Devs: https://uxpatterns.dev/en/llms-full.txt
- Bun: https://bun.sh/llms-full.txt
- Axiom: https://axiom.co/docs/llms-full.txt
- Raycast: https://developers.raycast.com/llms.txt
- Svelte: https://svelte.dev/llms-full.txt
- Perplexity: https://docs.perplexity.ai/llms.txt
- Resend: https://resend.com/docs/llms-full.txt
- Upstash: https://upstash.com/docs/llms.txt
- DaisyUI: https://daisyui.com/llms.txt
- Langfuse: https://langfuse.com/llms.txt
- Expo: https://docs.expo.dev/llms-full.txt
- Pydantic: https://docs.pydantic.dev/latest/llms-full.txt
- Chakra UI: https://chakra-ui.com/llms-full.txt
- ElysiaJS: https://elysiajs.com/llms.txt / https://elysiajs.com/llms-full.txt

Important Notes:
- You have the ability to read and edit multiple files simultaneously!
- Always review user input critically. Identify potential issues, point them out, and offer suggestions that go beyond the user's current thinking framework. If the user's idea is clearly unreasonable, call it out directly to help them quickly realize and correct it.
- Make full use of ast-grep/bash commands where appropriate.

## Technology-Specific Guidelines

Based on the technology used in the project, you **MUST** refer to the following additional rule files:

*   **TypeScript:** If the project uses TypeScript, you **MUST** adhere to the guidelines in:
    *   [`../other-rules/05-ROO-Typescript.md`](~/.roo/other-rules/05-ROO-Typescript.md)
*   **Bun:** If the project uses Bun as a runtime or package manager, you **MUST** adhere to the guidelines in:
    *   [`../other-rules/09-ROO-Bun.md`](~/.roo/other-rules/09-ROO-Bun.md)
*   **Bun + React:** For projects initialized with Bun and React, you **MUST** also refer to:
    *   [`../other-rules/08-ROO-Bun-React-Init.md`](~/.roo/other-rules/08-ROO-Bun-React-Init.md)
*   **Project Structure:** For general project structure, especially in a monorepo, refer to:
    *   [`../other-rules/07-ROO-Project-Structure.md`](~/.roo/other-rules/07-ROO-Project-Structure.md)
*   **Design & UI/UX:** For all design and user interface related work, you **MUST** adhere to the global principles defined in:
    *   [`../rules-rooroo-designer/00-ROO-Design-Global.md`](~/.roo/rules-rooroo-designer/00-ROO-Design-Global.md)
*   **Design & UI/UX:** For all design and user interface related work, you **MUST** adhere to the global principles defined in:
    *   [`../rules-rooroo-designer/00-ROO-Design-Global.md`](~/.roo/rules-rooroo-designer/00-ROO-Design-Global.md)

## Knowledge Base Handling

When a task requires consulting an external knowledge base from a URL:
*   First, determine a descriptive local name for the knowledge base (e.g., `vercel_ai_sdk.md` from a URL). The local path will be `.rooroo/docs/{local_name}`.
*   You **MUST** ensure a local copy exists before using it.
*   To do this, first check if the file exists. If not, you **MUST** download it using a command that also ensures the directory is created, for example: `mkdir -p .rooroo/docs && curl -L -o .rooroo/docs/{local_name} {url}`.
*   All subsequent operations **MUST** use the local copy from `.rooroo/docs/`.
*   For `rooroo-planner`, the plan itself must include these steps for the executing agent.