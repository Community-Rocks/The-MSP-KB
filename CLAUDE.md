# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

The **MSP Knowledge Base (MSPKB)** — a GitBook-published, Markdown-only documentation site about Managed Service Providers (their business models, operations, tooling, relationships, AI adoption, and community resources). There is no application code, no package manager, and no build/lint/test pipeline. GitBook renders the content directly from the Markdown sources on `main`; contributions are also accepted via the "Edit on GitHub" link on each rendered page.

## Repository layout

Content is organized into five top-level "spaces" plus two root files:

- `README.md` — Home page (rendered as the site's landing page).
- `SUMMARY.md` — **The GitBook navigation manifest.** See "Editing SUMMARY.md" below.
- `msp-foundations/` — Intro to MSPs, operational maturity levels (OMLs), business models.
- `msp-operations/` — Tools, challenges, departments/roles, compliance & regulations.
- `msp-relationships/` — Vendor/strategic relationships, peer & accountability groups.
- `ai-for-msps/` — AI in the MSP stack, AI security & governance.
- `resources/` — Communities, business resources, technical resources, MSP toolkit.

Within each space, every sub-section is its own directory containing:

- A `README.md` that acts as the section landing page (overview + links to sub-pages).
- One Markdown file per leaf page, named in `kebab-case.md` matching the slug in `SUMMARY.md`.
- Image assets (e.g. `sharex_screenshot.png`) colocated in the same directory as the page that references them.

## Page conventions (match these when authoring or editing)

- **Frontmatter.** Most pages start with YAML frontmatter containing a `description:` (often a multi-line `>-` block). GitBook surfaces this as the page's meta description and search snippet. Add or refine it when creating/significantly editing a page.
- **First heading.** The page's H1 (`# Title`) immediately follows the frontmatter and should match the label used in `SUMMARY.md`.
- **Internal links.** Use relative paths to sibling Markdown files (e.g. `[AI vs. Automation](ai-vs.-automation.md)`) or to section indexes via the folder with a trailing slash (e.g. `[AI Governance](ai-governance-and-acceptable-use-policies/)`). Do not link to rendered GitBook URLs.
- **Images.** Reference colocated images by a root-relative path (e.g. `![Sharex](/resources/technical-resources/msp-toolkit/screen-capture/sharex_screenshot.png)`).
- **Filenames.** Lowercase, hyphen-separated, `.md` extension. Note that some historical filenames contain periods inside the slug (`ai-vs.-automation.md`, `msps-vs.-in-house-it.md`) — preserve the existing names rather than renaming, since `SUMMARY.md` references them verbatim and renaming would break navigation.
- **Tone.** This KB is descriptive ("what MSPs are and how they work"), not prescriptive. Per the home page: it is *not* a resource for solving MSPs' problems — it's a resource for *understanding* them. Avoid jargon-heavy or overly technical phrasing.

## Editing `SUMMARY.md` (critical)

`SUMMARY.md` is the source of truth for GitBook's left-hand navigation. **Any new page must be added to `SUMMARY.md` or it will not appear in the rendered site**, even though it exists in the repo.

- Section headers in `SUMMARY.md` (e.g. `## MSP Operations`) define top-level spaces.
- Section landing pages link to the folder's `README.md` (e.g. `[Section Title](path/to/section/README.md)`).
- Leaf pages link to the specific `.md` file with nested indentation reflecting hierarchy.
- When renaming or moving a page, update every link in `SUMMARY.md` and any in-body links that reference it.

## Ignored / non-published files

`.gitignore` excludes `research.md` and `style-guide.md` — these are working drafts/internal notes that contributors keep locally. Do not check them in. If you generate scratch notes, name them so they fall under those ignores or remove them before committing.

## Commit & contribution flow

- Two patterns of commits appear in history: auto-generated `GITBOOK-NN: ...` commits (from the GitBook web editor) and human commits with descriptive subjects (e.g. *"Enhance AI governance documentation with comprehensive policy templates..."*). For repo-side edits, prefer the descriptive style.
- The community accepts edits via the "Edit on GitHub" button on each rendered page, which round-trips through standard PRs against `main`.
- There is no CI to run; verifying changes means previewing the Markdown rendering (e.g. in an editor or via GitBook's preview) and confirming `SUMMARY.md` still resolves every link.

## Notable non-Markdown asset

`resources/communities/community_list` is a JSON file (no extension) that mirrors the curated community list rendered in `resources/communities/forums-and-chat-communities.md`. If you add a community to the prose page, mirror the entry into this JSON file to keep them in sync.
