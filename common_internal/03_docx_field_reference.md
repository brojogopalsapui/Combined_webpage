# DOCX fields expected by the master notebook

The notebook uses the same weekly Research Watch DOCX structure as your earlier updater.

## Metadata table
Use the first table in the DOCX with these keys in column 1:

- `Post ID`
- `Title`
- `Meta Line`
- `Preview`
- `Full Post Link (optional)`
- `Related Static Page (optional)`
- `Related Static Page Label (optional)`
- `External Link 1 URL (optional)`
- `External Link 1 Label (optional)`
- `External Link 2 URL (optional)`
- `External Link 2 Label (optional)`

The master notebook will automatically normalize two fields for consistency:
- `Post ID` becomes the DOCX filename stem.
- `Full Post Link (optional)` becomes `posts/<filename-stem>.html`.

## Required headings in normal paragraphs
These paragraph headings should appear exactly as written:

- `Preview`
- `Full Note Paragraph 1`
- `Full Note Paragraph 2`
- `What Is Changing Technically`
- `What Reviewers Should Notice`
- `Current Research Tension`

## File naming rule
Save the DOCX as:

```text
YYYY-MM-topic-name.docx
```

Example:

```text
2026-04-secure-agent-memory.docx
```

That stem becomes:
- the weekly post ID
- the generated full post page name
- the anchor used inside `ongoing-work.html`
