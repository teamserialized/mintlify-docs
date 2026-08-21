# mintlify-docs — GENERATED, do not edit

This repo is the Mintlify deployment target for the **Serialized Data** docs
(docs.serialized.xyz). Every file here except this README, AGENTS.md, LICENSE
and .mintignore is **generated and force-synced** — any hand edit will be
erased on the next publish.

## Source of truth

`serialized-xyz/serialized-data` → `docs/public/api-reference.json`
(one JSON describing the whole API surface: REST endpoints + WS streams).

## How to change the docs

In the `serialized-data` repo:

```bash
# 1. edit docs/public/api-reference.json (or the generator)
node scripts/gen-mintlify.mjs        # regenerate docs/mintlify/ (reviewable)
node scripts/publish-mintlify.mjs    # sync into this repo + push
```

The publish script refuses to run if this repo has local changes — that is the
guard against hand edits.

## Local preview

```bash
npm i -g mint   # Mintlify CLI
mint dev        # at the root of this repo
```

Deploys to production automatically on push to `main` (Mintlify GitHub app).
