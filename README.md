# Sentro Demo — Legacy UI Prototype

Older standalone Next.js prototype of Sentro's incident-response experience, retained for demo and design reference. The original UI work dates to January 2026; later maintenance updates do not turn it into the current platform.

## Purpose and scope

- Citizen incident reporting and tracking demos
- Dispatcher incident queues, maps, analytics, audit logs, and management screens
- Responder assignment, navigation, and resolution flows
- Flood/water-level monitoring and alert demos

The screens use mock data in `lib/mock-data.ts`, `lib/mock-crud-data.ts`, and related demo modules, with browser-local state for interactions. Treat this as a UI/demo reference, not a live emergency-response system.

This repository is distinct from Sentro Platform. It is a standalone prototype, not a complete copy of the current platform. See [FEATURES.md](FEATURES.md) and [USER_FLOWS.md](USER_FLOWS.md) for the original demo scope.

## Local development

Use the pnpm version pinned in `package.json`.

```bash
corepack enable
pnpm install --frozen-lockfile
pnpm dev
```

Open http://localhost:3000.

## Checks

```bash
pnpm build
pnpm exec tsc --noEmit
pnpm lint
```

## Optional Railway demo deployment

These are setup instructions, not confirmation of a live deployment for this repository.
If deploying this legacy demo, connect this repository's `main` branch to a dedicated demo service.
Railpack detects Next.js and the pinned pnpm package manager.

- Install dependencies with `pnpm install --frozen-lockfile`.
- Build with `pnpm build`.
- Start with `pnpm start`; Next.js listens on Railway's `PORT`.

After each deployment, verify the deployed commit, successful deployment status,
and the service's public URL in Railway.
