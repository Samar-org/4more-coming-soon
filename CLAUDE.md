# 4more-coming-soon -- Claude Instructions

This repo follows the **Samar AI White Glove Project** -- canonical methodology at https://github.com/Samar-org/white-glove-setup
Read methodology/ from that repo before doing any work.

---

> **Stage: PRODUCTION -- Phase 2 security applies.**
> No shortcuts, no skipped validations, no unreviewed deploys.
> If you need to cut a corner, add it to PUNCH_LIST.md with severity and get explicit confirmation first.
## First-session setup

On your first session in this repo, fetch and read the methodology files from the central repo:

1. Read `methodology/00-operating-mode.md` through `methodology/07-secrets-management.md` from `Samar-org/white-glove-setup`
2. Follow all rules defined there — they are authoritative
3. Use this file for repo-specific context only

---

## Repo-specific stack

<!-- Fill in the actual stack for this project -->

- **Framework:** Static HTML
- **Hosting:** manual
- **Database:** none
- **Auth:** see repo code
- **Payments:** none
- **Other services:** see repo code

---

## Repo-specific business memory

<!-- What does this project do? Who is it for? Key business rules. -->

- **Project:** 4more Coming Soon
- **Business:** 4more Corporation
- **Users:** see project docs
- **Key business rules:**
  - see project docs
  - see project docs

---

## Repo-specific gotchas

<!-- Known quirks, legacy decisions, things that will surprise a new contributor. -->

- none documented yet
- none documented yet

---

## Project stage

Current stage: **PRODUCTION** (see [Samar-org/white-glove-setup → projects/registry.yaml](https://github.com/Samar-org/white-glove-setup/blob/master/projects/registry.yaml))

Security posture: Phase 2 -- full security. No shortcuts without explicit confirmation.

## Deployment fingerprint

<!-- Populated from registry.yaml. Update there, not here. -->

| Layer | Value |
|-------|-------|
| **Platform** | manual |
| **Prod URL** | https://4more.ca |
| **Database** | none (secret: `none`) |
| **CDN/DNS** | cloudflare |
| **Email** | none |
| **Payments** | none |
| **Monitoring** | errors: none, uptime: none, logs: none |
| **CI/CD** | none, branch protection: false |

---

## Secrets

This repo uses **Doppler** for secrets management.

- **Local dev:** Run `doppler run -- claude` to start Claude Code with all secrets injected.
- **Any process:** `doppler run -- pnpm dev`, `doppler run -- node server.js`, etc.
- **CI/CD:** Secrets are auto-synced from Doppler to GitHub Org Secrets (Samar-org).
- **Never commit secrets** to `.env` files. Doppler injects them at runtime.
- **Doppler project:** `4more-ecosystem` | **Config:** `dev` (local), `stg`, `prd`

---

## Repo-specific context

<!-- Preserved from existing repo documentation. Do not overwrite — append only. -->
