# mintlify-docs: deployment target for docs.serialized.xyz

Mintlify deploys this repo (a push to `main` goes to production). The content is
authored in `serialized-xyz/serialized-data` under `docs/mintlify/` (hand-written
MDX) and published here by `scripts/publish-mintlify.mjs`.

## Editing here is allowed, with one rule

You can edit pages in this repo (Mintlify web editor, a quick fix on GitHub), as
long as the edits are **committed** (the publish refuses a dirty working tree).
The next publish from `serialized-data` runs a 3-way sync, using the last publish
commit as the base:

- changed only here: imported back into `serialized-data`, then kept;
- changed only in `serialized-data`: published over this repo;
- changed on both sides, differently: the publish **fails** and lists the files.
  Someone reconciles them in `serialized-data` and publishes again. Nothing is
  silently lost either way.

Prefer editing in `serialized-data` when you can: the API code, the contract
and the docs live and get reviewed together there.

## How to publish

In the `serialized-data` repo:

```bash
node scripts/publish-mintlify.mjs    # 3-way sync, overlay, commit, push
```

## Files owned by this repo only

`README.md`, `AGENTS.md`, `LICENSE`, `.mintignore`: never touched by the
publish, edit them here.

## Local preview

```bash
npm i -g mint   # Mintlify CLI
mint dev        # at the root of this repo
```
