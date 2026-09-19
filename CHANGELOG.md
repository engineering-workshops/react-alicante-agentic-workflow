## [0.2.0] — 2026-09-19

### Features

- i18n: move to next-intl with locale-prefixed routes
- db: grant select on sessions, ship the Playwright MCP server
- db: make track a Postgres enum and derive types from the schema
- workshop: add tickets script, simplify the env var ticket
- sessions: read the schedule from a Supabase sessions table
- auth: restore /protected as the default post-signin route
- auth: restore Supabase login, gate /stats behind sign-in
- i18n: add EN/ES language context with nav toggle
- schedule: add stats page and session timeline
- sessions: add sessions pages, strip starter boilerplate

### Bug Fixes

- sessions: survive an environment whose migrations have not run
- skills: ignore NEXT_RUNTIME and drop Redis leftovers
- skills: make the release skills run in this repo
- nav: use a hamburger menu below md instead of wrapping
- sessions: add missing route layout for nav/container/spacing

### Refactoring

- components: organise by atomic design, split by purpose, drop unused ones
- ui: move every component to Chakra and drop Tailwind
- drop auth, add public /news page driven by env vars
- consolidate lib/ into a single top-level utils/
- ui: migrate shadcn primitives to Chakra UI v3
- role-based component structure

### Tests

- add component testing setup, cover nav and timeline
- add vitest with a first suite

### Maintenance

- deps: pin every version, move to the Next 16 eslint config
- ci: run lint, type-check and tests on pushes and PRs; pin pnpm
- tooling: prettier, husky, lint-staged
- claude: skills, agents and rules set up for this repo
- docs: workshop notes, tickets, README and layout updates
- workshop: add workshop:reset, baseline is the latest release tag
- scaffold from vercel/next.js with-supabase example

## Test Suite

| Suite          | Status     |
| -------------- | ---------- |
| ESLint         | ✅ passed  |
| Type-check     | ✅ passed  |
| Unit tests     | ✅ passed  |
| Build (Vercel) | ⏳ pending |

CI: https://github.com/engineering-workshops/react-alicante-agentic-workflow/actions/runs/35466566177
