## [0.2.0] — 2026-09-20

### Features

- i18n: move to next-intl with locale-prefixed routes
- db: grant select on sessions, ship the Playwright MCP server
- db: make track a Postgres enum and derive types from the schema
- workshop: add tickets script and simplify the env var ticket
- sessions: read the schedule from a Supabase sessions table
- auth: restore /protected as the default post-signin route
- auth: restore Supabase login, gate /stats behind sign-in
- i18n: add EN/ES language context with nav toggle
- schedule: add stats page and session timeline; remove auth
- sessions: add sessions pages, strip starter boilerplate

### Bug Fixes

- sessions: survive an environment whose migrations have not run
- skills: ignore NEXT_RUNTIME and drop Redis leftovers
- skills: make the release skills run in this repo
- nav: use a hamburger menu below md instead of wrapping
- sessions: add missing route layout for nav/container/spacing

### Refactoring

- components: organise by atomic design
- components: split by purpose and drop the unused ones
- ui: move every component to Chakra and drop Tailwind
- drop auth, add public /news page driven by env vars
- consolidate lib/ into a single top-level utils/
- ui: migrate shadcn primitives to Chakra UI v3
- role-based component structure; copy feature-builder + release-manager

### Tests

- add component testing setup and cover nav and timeline
- add vitest with a first suite, and enum-ify the level ticket

### Maintenance

- ci: answer pnpm's build-script prompt for every package
- ci: pin the pnpm version for the runner
- ci: run lint, type-check and tests on pushes and PRs
- deps: pin every version, move to the Next 16 eslint config
- tooling: add prettier, husky and lint-staged
- claude: offer to file the release audit follow-ups as tickets
- claude: release audit blockers get fixed, one audit reported at a time
- claude: add a rule for concise breakpoint output
- claude: make the agent clean up the dev server it starts
- claude: calibrate the skills to this repo's actual conventions
- claude: strip the internal references from the remaining skills
- claude: make the release-path skills runnable here
- claude: point the agents and AGENTS.md at this repo's stack
- claude: copy the skills and rules the agents referenced but lacked
- claude: block env file reads and remote DB/force pushes
- claude: copy Chakra UI v3 skill, agent and rule updates from platform-website
- workshop: baseline is the latest release tag, not a marker
- workshop: add workshop:reset for dry-run rollbacks
- keep the production project ref out of .env.local
- add version, db scripts and production project ref
- docs: list the hooks folder in the layout table
- docs: Chakra only, Tailwind is gone
- docs: state the Chakra and Tailwind split
- docs: bring the workshop notes into the repo, organised by audience
- docs: attribute the skills and agents to Philomath Academy
- docs: prefer userEvent over fireEvent in engineering-new-test
- docs: update README for QA/Production projects and db scripts
- docs: add attendee tickets for UI, database and env var work
- docs: copy feature-planner agent, list it in AGENTS.md

### Other

- style: trim the comments in the refactored components
- Revert "chore(claude): make the agent clean up the dev server it starts"
- Revert "chore: keep the production project ref out of .env.local"

## Test Suite

| Suite          | Status     |
| -------------- | ---------- |
| ESLint         | ⏳ pending |
| Type-check     | ⏳ pending |
| Unit tests     | ⏳ pending |
| Build (Vercel) | ⏳ pending |

CI: pending (branch not pushed yet)
