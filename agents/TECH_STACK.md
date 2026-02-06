# Project Tech Stack & Constraints

## Meta-Comment for Bootstrap
- This is currently a template for TECH_STACK.md as we have not yet started the project.  If you are reading this, you should
update this to be in an initial state.  And delete this line/section, since it won't be true anymore.

## 🧱 Core Stack
- **Language:** [e.g., TypeScript / Python 3.11+]
- **Framework:** [e.g., Next.js 15 (App Router) / FastAPI]
- **Styling:** [e.g., Tailwind CSS / Shadcn UI]
- **Database:** [e.g., Prisma with PostgreSQL / Supabase]
- **State Management:** [e.g., Zustand / React Query]

## 🛠 Tooling & CLI Commands
*Common commands the agent should use to verify work.*
- **Install:** `npm install`
- **Build:** `npm run build`
- **Lint:** `npm run lint`
- **Test:** `npm run test`

## 📐 Architectural Rules (The "Vibe" Guardrails)
- **Pattern:** [e.g., Use Functional Components and Hooks; avoid Classes.]
- **Error Handling:** [e.g., Always use try/catch blocks in Server Actions with logged errors.]
- **Data Fetching:** [e.g., Prefer Server Components over Client-side fetching where possible.]
- **Naming Convention:** [e.g., PascalCase for components, camelCase for functions, kebab-case for files.]

## 🚫 Constraints & Forbidden Practices
- **NO** inline styles; use Tailwind classes only.
- **NO** adding new dependencies without asking the user first.
- **NO** using 'any' types; strictly enforce interfaces.
- **NO** "placeholder" logic (e.g., `// TODO: implement this`).
