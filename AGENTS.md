# Instructions for AI agents

This repo is the Mintlify deployment target for docs.serialized.xyz. The pages
are authored in `serialized-xyz/serialized-data` under `docs/mintlify/` and
published here by `scripts/publish-mintlify.mjs`.

**Prefer editing in `serialized-data`.** If you edit here, commit your changes:
the next publish runs a 3-way sync (base = last publish commit) that imports
edits made only here, and fails loudly on a file changed on both sides. See
README.md.

`README.md`, `AGENTS.md`, `LICENSE` and `.mintignore` live only in this repo.
