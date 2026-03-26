# Static article/page sync workflow across both codebases

Use this after you manually create or edit a static page in one source site root.

## Best source for static editing
Use one source site root as the place where you edit first:
- `brojogopalsapui.github.io`
- or `AiSecurityResearch`

Then let the notebook copy the changed files to:
- the other repo root
- the `papers_articles` mirror inside each repo, if present

## What this sync mode is good for
- `research.html`
- `ai-security/*.html`
- `ai-foundations/*.html`
- diagrams in `assets/img/...`
- PDFs in `assets/docs/...`
- any extra static file needed by that article/page

## How to use it
1. Edit the source site first.
2. Open `common_internal/article_sync_manifest.txt`.
3. Add every changed relative path, one per line.
4. In the notebook, enable `RUN_ARTICLE_SYNC = True`.
5. Set `ARTICLE_SOURCE_REPO_NAME` to the repo you edited.
6. Run the notebook.
7. Review changes in both repos before pushing.

## Important note
This mode copies files. It does not rewrite the content of `research.html` for you from DOCX.
So the content/card creation still starts from your source repo, and then the notebook mirrors that result everywhere else automatically.
