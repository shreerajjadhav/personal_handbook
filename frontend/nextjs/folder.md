## Next.js Project Folder Structure

The following is the recommended folder structure for a Next.js project using TypeScript, Tailwind CSS, App Router, and Motion for React.

### 1. Complete Folder Structure

```text
frontend/
│
├── public/
│   ├── images/
│   ├── icons/
│   ├── fonts/
│   └── ...
│
├── src/
│   │
│   ├── app/
│   │   ├── favicon.ico
│   │   ├── globals.css
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   └── ...
│   │
│   ├── components/
│   │   ├── ui/
│   │   ├── layout/
│   │   ├── common/
│   │   └── animations/
│   │
│   ├── features/
│   ├── hooks/
│   ├── services/
│   │   └── api/
│   │
│   ├── lib/
│   ├── types/
│   ├── constants/
│   └── utils/
│
├── .env.local
├── .gitignore
├── eslint.config.mjs
├── next.config.ts
├── package.json
├── package-lock.json
├── postcss.config.mjs
├── tsconfig.json
└── README.md
```

**Note:** `public`, `src/app`, and the configuration files are part of the standard project setup. Folders such as `components`, `features`, `hooks`, and `services` are recommended organizational folders that you create as your application grows.

### 2. Folder and File Purposes

#### Root Directory

| File / Folder | Purpose |
|---|---|
| `public/` | Stores static assets such as images, icons, and fonts. |
| `src/` | Contains the main application source code. |
| `.env.local` | Stores local environment variables, such as backend API URLs. |
| `.gitignore` | Specifies files and folders Git should ignore. |
| `eslint.config.mjs` | Configures ESLint rules for code quality. |
| `next.config.ts` | Contains Next.js configuration. |
| `package.json` | Stores project metadata, dependencies, and npm scripts. |
| `package-lock.json` | Locks dependency versions for consistent installations. |
| `postcss.config.mjs` | Configures PostCSS and Tailwind CSS processing. |
| `tsconfig.json` | Configures TypeScript compiler options and path aliases. |
| `README.md` | Contains project information and documentation. |

#### `src/app/` – Application Routing

This is the main directory for pages, layouts, and routing when using the App Router.

| File | Purpose |
|---|---|
| `page.tsx` | Defines the homepage (`/`). |
| `layout.tsx` | Defines the shared layout for application pages. |
| `globals.css` | Contains global CSS styles and Tailwind CSS imports. |
| `favicon.ico` | Defines the website favicon. |

**Example of routing:**

```text
src/app/
│
├── page.tsx
├── about/
│   └── page.tsx
├── contact/
│   └── page.tsx
└── dashboard/
    ├── page.tsx
    └── settings/
        └── page.tsx
```

This automatically creates the following routes:

| File Location | URL |
|---|---|
| `app/page.tsx` | `/` |
| `app/about/page.tsx` | `/about` |
| `app/contact/page.tsx` | `/contact` |
| `app/dashboard/page.tsx` | `/dashboard` |
| `app/dashboard/settings/page.tsx` | `/dashboard/settings` |

#### `src/components/` – Reusable UI Components

Contains components that can be reused across multiple pages.

| Folder | Purpose |
|---|---|
| `ui/` | Buttons, inputs, cards, modals, and other UI elements. |
| `layout/` | Navbar, footer, sidebar, and page layouts. |
| `common/` | Shared components used throughout the application. |
| `animations/` | Reusable animated components built with Motion. |

#### Other Source Directories

| Folder | Purpose |
|---|---|
| `features/` | Organizes application functionality into separate feature modules. |
| `hooks/` | Stores reusable React custom hooks. |
| `services/` | Contains services responsible for external communication and business-related API operations. |
| `services/api/` | Stores API client configuration and backend API functions. |
| `lib/` | Contains shared libraries, integrations, and initialized configurations. |
| `types/` | Stores reusable TypeScript interfaces and type definitions. |
| `constants/` | Stores fixed values such as application settings and configuration constants. |
| `utils/` | Contains reusable helper and utility functions. |

#### `public/` – Static Assets

Stores files that can be accessed directly through their public paths.

```text
public/
│
├── images/
├── icons/
├── fonts/
└── ...
```

For example, an image stored at:

```text
public/images/logo.png
```

Can be accessed using:

```text
/images/logo.png
```

### 3. Important Development Guidelines

1. Keep pages and routing-related files inside `src/app/`.
2. Create reusable UI components inside `src/components/`.
3. Keep API communication logic organized inside `src/services/api/`.
4. Store environment-specific values in `.env.local`.
5. Never expose secret API keys or credentials through variables prefixed with `NEXT_PUBLIC_`.
6. Avoid creating unnecessary folders. Add organizational folders as the application grows.
7. Use TypeScript for components, functions, and data models.

**Important:** This is a recommended scalable folder structure, not a mandatory Next.js requirement. You can organize your application according to its size and complexity.
