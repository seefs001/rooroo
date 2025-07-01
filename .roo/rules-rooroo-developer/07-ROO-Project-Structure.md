# 07-ROO-Project-Structure: Project Structure Guidelines

This document outlines standard project structure and file organization guidelines.

## 1. Core Structure
- **Workspace Manager:** We use Turborepo with bun workspaces.
- **Application Directory:** The main application(s) should reside in the `apps/` directory.
- **Shared Packages:** Reusable packages and modules should be placed in the `packages/` directory.

An example structure might look like this:
```tree
.
├── apps
│   ├── web/             # Main Next.js application
│   │   ├── app/         # Next.js App Router
│   │   │   ├── (app)/   # Main application pages
│   │   │   │   ├── assistant/     # AI assistant feature
│   │   │   │   ├── reply-zero/     # Reply Zero feature
│   │   │   │   ├── settings/       # User settings
│   │   │   │   ├── setup/          # Main onboarding
│   │   │   │   ├── clean/          # Bulk email cleanup
│   │   │   │   ├── smart-categories/ # Smart sender categorization
│   │   │   │   ├── bulk-unsubscribe/ # Bulk unsubscribe
│   │   │   │   ├── stats/          # Email analytics
│   │   │   │   ├── mail/           # Email client (in beta)
│   │   │   │   └── ... (other app routes)
│   │   │   ├── api/    # API Routes
│   │   │   │   ├── knowledge/      # Knowledge base API
│   │   │   │   ├── reply-tracker/  # Reply tracking
│   │   │   │   ├── clean/          # Cleanup API
│   │   │   │   ├── ai/            # AI features API
│   │   │   │   ├── user/          # User management
│   │   │   │   ├── google/        # Google integration
│   │   │   │   ├── auth/          # Authentication
│   │   │   │   └── ... (other APIs)
│   │   │   ├── (landing)/  # Marketing/landing pages
│   │   │   ├── blog/       # Blog pages
│   │   │   ├── layout.tsx  # Root layout
│   │   │   └── ... (other app files)
│   │   ├── utils/       # Utility functions and helpers
│   │   │   ├── actions/    # Server actions
│   │   │   ├── ai/         # AI-related utilities
│   │   │   ├── llms/       # Language model utilities
│   │   │   ├── gmail/      # Gmail integration utilities
│   │   │   ├── redis/      # Redis utilities
│   │   │   ├── user/       # User-related utilities
│   │   │   ├── parse/      # Parsing utilities
│   │   │   ├── queue/      # Queue management
│   │   │   ├── error-messages/  # Error handling
│   │   │   └── *.ts        # Other utility files (auth, email, etc.)
│   │   ├── public/      # Static assets (images, fonts)
│   │   ├── prisma/      # Prisma schema and client
│   │   ├── styles/      # Global CSS styles
│   │   ├── providers/   # React Context providers
│   │   ├── hooks/       # Custom React hooks
│   │   ├── sanity/      # Sanity CMS integration
│   │   ├── __tests__/   # AI test files (Vitest)
│   │   ├── scripts/     # Utility scripts
│   │   ├── store/       # State management
│   │   ├── types/       # TypeScript type definitions
│   │   ├── next.config.mjs
│   │   ├── package.json
│   │   └── ... (config files)
│   └── unsubscriber/    # Automates unsubscribes using browser automation. Not currently in use
├── packages
    ├── tinybird/
    ├── eslint-config/
    ├── loops/
    ├── resend/
    ├── tinybird-ai-analytics/
    └── tsconfig/
```

## 2. File Naming and Organization
- **Route Directories:** Use kebab-case for route directories (e.g. `api/hello-world/route`).
- **Component Files:** Use PascalCase for component files (e.g. `components/Button.tsx`).
- **UI Components:**
    - Foundational UI components (like shadcn/ui) are located in `components/ui`.
    - All other general-purpose components are in the root `components/` folder.
- **Colocation:** Co-locate files within the feature or component folder where they are exclusively used. If a component or utility can be used across the application, place it in a shared directory like `components/` or `utils/`.

## 3. Utility Functions
- **Location:** Reusable logic should be extracted into utility functions and placed in a `utils/` directory.
- **Third-Party Libraries:** For common operations (e.g., on arrays, objects, strings), use established utility libraries like `lodash`.
- **Bundle Size:** To minimize the final bundle size, import specific functions from libraries rather than the entire library.
  ```ts
  // Good: Imports a single function
  import groupBy from "lodash/groupBy";

  // Bad: Imports the entire library
  import _ from "lodash";