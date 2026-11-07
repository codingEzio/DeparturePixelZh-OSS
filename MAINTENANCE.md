# Local source maintenance

This repository owns the font recipe, notices and public source allowlist.
The pinned builder owns the maintenance commands. No publication or installation
is part of these checks.

1. Obtain the builder revision in `builder-version` in any local directory.
2. Stage reviewed source changes and update `public-source.json` if the file list changes.
3. From that builder, run `uv run --frozen python scripts/maintain.py --font-root /path/to/this/repository`.
4. Use `audit-public --root /path/to/this/repository --index --export /new/source-directory`
   through the same builder CLI to produce a source-only candidate with relative
   file hashes. The destination must be new and its parent must exist.

The builder's `docs/maintenance.md` specifies the exact checks, failure behavior,
clean dependency/build procedure and limitations. This source export has no Git
history. Existing history requires separate review and is never rewritten by
these commands. Preserve legitimate attribution and all component notices.

`Local/`, `Build/` and `dist/` are private or generated state and do not enter the
source allowlist. The allowlist does not replace the separate font archive
allowlist used by the builder's `package` command. A source check is not proof of
font rendering, full upstream reconstruction, or permission to publish.
