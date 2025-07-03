# 08-ROO-Bun-React-Init: Bun React Project Initialization

## Using `bun init --react`

When using Bun to initialize a new React project, you can use the command `bun init --react`.

### Flags
You can also use flags to initialize a project with additional tools:
```
-r, --react            Initialize a React project
    --react=tailwind   Initialize a React project with TailwindCSS
    --react=shadcn     Initialize a React project with @shadcn/ui and TailwindCSS
```

This command will scaffold a new project with the following structure:

```tree
├── src/
│   ├── index.tsx       # Server entry point with API routes
│   ├── frontend.tsx    # React app entry point with HMR
│   ├── App.tsx         # Main React component
│   ├── APITester.tsx   # Component for testing API endpoints
│   ├── index.html      # HTML template
│   ├── index.css       # Styles
│   └── *.svg           # Static assets
├── package.json        # Dependencies and scripts
├── tsconfig.json       # TypeScript configuration
├── bunfig.toml         # Bun configuration
└── bun.lock            # Lock file
```

## Notes
- The `APITester.tsx` file is provided as an example and can be safely removed once you understand its implementation.
- For multiple applications on different paths, you can create additional `index.html` and `frontend.tsx` pairs and configure the routing accordingly in `index.tsx`.
- The TailwindCSS integration is pre-configured for you. It uses TailwindCSS v4, which does not require a `tailwind.config.js` file.
- If you initialize with `--react=shadcn`, you must use `bunx shadcn@canary add [component]` to add new UI components.
- After initialization, you can modify or remove unnecessary global styles from `index.css` as needed. However, be mindful of potential impacts on font styles and layout.