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

