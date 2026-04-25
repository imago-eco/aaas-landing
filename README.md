# aaas.imago.eco

Static landing for **Imago AAAS** — invite-only alpha for the five-friend cohort.

A persistent AI orchestrator and a small specialist team, running 24/7 on Even's home server. This page is the public-facing front door; the actual onboarding flow runs through Discord by invite.

## What's here

- `index.html` — single-file landing, zero JS, ~16KB
- `fonts/dawo.otf` — display face for the wordmark and section headings
- `favicon.svg` — ink-square favicon
- `vercel.json` — long cache headers for fonts/favicon

## DNA

- **Type:** Dawo (display) · Space Grotesk (UI) · JetBrains Mono (mono — Google Fonts)
- **Palette:** ink `#0F0F0F` · paper `#FFFFFF` · off-white `#FAFAF8`
- **Geometry:** square corners (`border-radius: 0 !important` on `*`), no gradients, no shadows

Spec: `shared/aaas-imago-eco-landing-prd.md` (in the orchestrator workspace, not this repo).
Copy: `shared/aaas-imago-eco-landing-copy.md`.

## Deploy

**Option A — Vercel dashboard (recommended for first deploy):**

1. <https://vercel.com/new> → Import Git Repository → `imago-eco/aaas-landing`
2. Framework preset: **Other** (no build step needed; static).
3. Output directory: leave blank (root).
4. Deploy — gets a `*.vercel.app` URL immediately.

**Option B — Vercel CLI:**

```bash
vercel --prod
```

## DNS

Target: `aaas.imago.eco` → Vercel (CNAME or A record per Vercel's domain dashboard).
DNS flip is manual (HITL) — done once the `*.vercel.app` deploy is verified.
