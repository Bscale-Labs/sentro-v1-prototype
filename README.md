# Sentro Demo

A Next.js demo with Railway as its deployment target.

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

## Railway deployment

Connect this repository's `main` branch to the intended Railway service.
Railpack detects Next.js and the pinned pnpm package manager.

- Install dependencies with `pnpm install --frozen-lockfile`.
- Build with `pnpm build`.
- Start with `pnpm start`; Next.js listens on Railway's `PORT`.

After each deployment, verify the deployed commit, successful deployment status,
and the service's public URL in Railway.
