# common_internal

This folder is the shared control room for both website codebases.

## What is inside
- `master_update_both_codebases_from_docx.ipynb` — the main notebook
- `site_sync_tools.py` — helper functions used by the notebook
- `incoming_docx/` — drop filled weekly DOCX files here
- `article_sync_manifest.txt` — list changed static files here when mirroring article/page edits
- `01_weekly_post_workflow.md` — weekly post workflow
- `02_article_sync_workflow.md` — static article/page sync workflow
- `03_docx_field_reference.md` — DOCX format reference
- `reference_assets/` — copied template and guide files for convenience

## Recommended usage
- For weekly Research Watch posts: use the DOCX workflow.
- For static research articles/pages: edit one source repo first, then mirror the changed files using the article sync mode.

## Why this is cleaner
You no longer need separate notebooks inside each repo for the same weekly post.
One notebook can now update both codebases and their mirrored `papers_articles` site roots together.
