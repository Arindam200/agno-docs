# AGENTS.md

## Cursor Cloud specific instructions

This is a **Mintlify documentation site** for the Agno AI framework. There is no application code, backend, or database — only MDX content files and a `docs.json` configuration.

### Running the dev server

```
mintlify dev --port 3000
```

The server takes ~30-60 seconds to prepare. A `TypeError: controller[kState].transformAlgorithm is not a function` may appear in the terminal — this is harmless and the preview still works correctly.

### Key notes

- The README references `mint` as the CLI command, but the current package installs as `mintlify`. Use `mintlify dev` (not `mint dev`).
- Search is unavailable in local preview — this is expected Mintlify behavior (indexing requires production build).
- If the dev server misbehaves, run `mintlify update` to refresh internal dependencies.
- There are no lint, test, or build commands for this repo. Validation is purely visual via the dev server.
- Site configuration lives in `docs.json` (navigation, theming, metadata). Content lives in `.mdx` files across ~32 directories.
