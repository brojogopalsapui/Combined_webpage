# Weekly post workflow across both codebases

This is the new single-source workflow for Research Watch posts.

## What happens automatically
From one filled DOCX, the master notebook updates every site root it detects in the workspace. In your current structure that means the repo roots, and it will also update any `papers_articles` mirror that contains its own `index.html`.

For each of those site roots it will:
- copy the DOCX into `weekly-inputs/`
- update `ongoing-work.html`
- update `index.html`
- create or refresh `posts/YYYY-MM-topic-name.html`

## How to use it
1. Put the filled DOCX in `common_internal/incoming_docx/`.
2. Open `common_internal/master_update_both_codebases_from_docx.ipynb`.
3. Leave `RUN_WEEKLY_POST_SYNC = True`.
4. Keep `AUTO_PICK_LATEST_DOCX = True` unless you want to point to one exact file.
5. Run all cells.
6. Review both codebases.
7. Commit and push.

## Naming rule
Use filenames like:

```text
YYYY-MM-topic-name.docx
```

Example:

```text
2026-04-secure-agent-memory.docx
```
