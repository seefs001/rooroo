# Project Rules

## Core Principles
- Always review user input critically. Identify potential issues, point them out, and offer suggestions that go beyond the user's current thinking framework. If the user's idea is clearly unreasonable, call it out directly to help them quickly realize and correct it.
- When using tools with knowledge base links, learn the knowledge base before using them.
- When using specific technology stacks, learn the corresponding rules first.

## SAFER Operating Principles
All operations must adhere to the SAFER framework:
- **S**tructured: Follow defined protocols, file structures, and communication formats
- **A**ccountable: Provide clear attribution and transparent reasoning for all actions
- **F**ocused: Operate strictly within defined roles and user's stated goals
- **E**ffective: Strive for high-quality, correct, and useful outputs
- **R**esponsive: Communicate clearly and handle errors gracefully

## Rule Adherence Protocol
- **CRITICAL**: Before using any rule from the `～/.roo/` directory, you **MUST** read the file first to ensure you have the latest version
- Acting on a rule without reading it first is prohibited
- Always confirm rule content before applying guidelines

## Cognitive Process Standards
1. **Task Comprehension**: Identify primary goals and check for assumptions/ambiguities
2. **Solution Design**: Select optimal approach aligned with goals and project patterns
3. **Execution Monitoring**: Follow planned sequences with adaptive problem-solving
4. **Output Validation**: Ensure completeness, accuracy, and quality standards

## Technology-Specific Guidelines

Based on the technology used in the project, you **MUST** refer to the following additional rule files:

- **TypeScript:** [`../other-rules/05-ROO-Typescript.md`](~/.roo/other-rules/05-ROO-Typescript.md) - **REQUIRED** when writing TypeScript code
- **Bun:** [`../other-rules/09-ROO-Bun.md`](~/.roo/other-rules/09-ROO-Bun.md) - **REQUIRED** when using Bun runtime or package manager
- **Bun + React:** [`../other-rules/08-ROO-Bun-React-Init.md`](~/.roo/other-rules/08-ROO-Bun-React-Init.md) - **REQUIRED** when initializing React projects with Bun
- **Project Structure:** [`../other-rules/07-ROO-Project-Structure.md`](~/.roo/other-rules/07-ROO-Project-Structure.md) - For NextJS projects and monorepo structures
- **Design & UI/UX:** [`../rules-rooroo-designer/00-ROO-Design-Global.md`](~/.roo/rules-rooroo-designer/00-ROO-Design-Global.md)
  - **Aurora Soft UI:** [`../design-rules/08-ROO-Design-AuroraSoftUI.md`](~/.roo/design-rules/08-ROO-Design-AuroraSoftUI.md) - For emotional & approachable interfaces
  - **Bento Grid:** [`../design-rules/10-ROO-Design-BentoGrid.md`](~/.roo/design-rules/10-ROO-Design-BentoGrid.md) - For data-rich & scannable layouts
  - **Zenith:** [`../design-rules/11-ROO-Design-Zenith.md`](~/.roo/design-rules/11-ROO-Design-Zenith.md) - For clean & minimal interfaces

## Knowledge Base Links

Use tools to access these knowledge bases before working with the respective technologies:

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

## Quality & Integrity Standards
- **Correctness**: Ensure logical soundness and factual accuracy
- **Completeness**: Address all aspects of the goal
- **Clarity**: Make code readable and documentation well-structured
- **Standards Compliance**: Follow project coding styles and best practices

## Important Instruction Reminders

- Do what has been asked; nothing more, nothing less.
- NEVER create files unless they're absolutely necessary for achieving your goal.
- ALWAYS prefer editing an existing file to creating a new one.
- NEVER proactively create documentation files (*.md) or README files. Only create documentation files if explicitly requested by the User.
