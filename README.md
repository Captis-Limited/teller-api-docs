# teller-api-docs

Public **docs-only mirror** for the (private) `teller-api` proof-of-concept.

This repo exists solely so Mintlify's free tier can host the documentation —
the free tier only connects to **public** repos, and the real source lives in
the private `Captis-Limited/teller-api`. Only the docs artifacts are mirrored
here; no application source, SDKs, or secrets.

## Contents

| File | Purpose |
| ---- | ------- |
| `docs.json` | Mintlify site config (navigation + theme). |
| `index.mdx` | Guides landing page. |
| `openapi/teller-api.yaml` | OpenAPI spec — the API Reference is generated from this. |
| `favicon.svg` | Site favicon. |

## How it's updated

These files are generated in the private `teller-api` repo. After changing the
API there, run `scripts/sync_docs.sh` from that repo to copy the latest spec +
config here and push — Mintlify then redeploys automatically.

> Everything documented here is backed by a **mocked** data layer. It is a
> tooling proof-of-concept, not a live banking API.
