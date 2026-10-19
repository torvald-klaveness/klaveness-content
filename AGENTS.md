# Klaveness Content Repository

## Project purpose

This repository holds the news articles for the Torvald Klaveness website (klaveness.com/news). The website reads them straight from GitHub: a push to `main` shows up on the site within a minute, without redeploying it.

Torvald Klaveness is an Oslo-based maritime group founded in 1946 (Klaveness Dry Bulk, Baumarine, Klaveness Combination Carriers (KCC), Klaveness Digital and Klaveness Finance). Treat klaveness.com as the source of truth for names, titles and facts; ask the user when something is unclear rather than guessing.

## Scope of work

- Work here is limited to news articles and their images.
- Only edit files. Do not create branches, commits, pull requests or other Git changes unless the user asks.
- Ask before making editorial, structural or factual decisions that the user's request does not already settle. Do not invent quotes, figures, people or outcomes.

## Files

- One article per Markdown file: `news/<year>/<slug>.md`. The year is the publishing year; the folder is only for tidiness.
- The slug is the web address: `news/2026/klaveness-dry-bulk-completes-milestone-clinker-shipment.md` is published at `/news/klaveness-dry-bulk-completes-milestone-clinker-shipment`. Lowercase words joined by hyphens.
- Images sit next to the article, named after it: `<slug>.webp` for the cover, `<slug>-2.webp`, `<slug>-3.webp`… for images in the text.
- Never rename or move a published article: its address would change and old links would break. If it has to change, the website needs a redirect (tell the user).

## Front matter

```yaml
---
slug: "klaveness-dry-bulk-completes-milestone-clinker-shipment"
title: "Klaveness Dry Bulk completes milestone clinker shipment"
description: "One or two sentences for the news cards, search results and link previews."
publishedAt: "2026-09-02"
categories:
  - "Klaveness Dry Bulk"
coverImage: "klaveness-dry-bulk-completes-milestone-clinker-shipment.webp"
coverAlt: "Deck view of a bulk carrier loading cement clinker from barges in Cam Pha, Vietnam"
coverCaption: "Image: Vessel loading in Cam Pha, Vietnam"
---
```

- `slug`, `title`, `publishedAt` (YYYY-MM-DD) are required. `slug` must match the file name.
- `description`: plain text, about 90–220 characters.
- `categories`: one to three of the Newsroom filters, spelled exactly: `Klaveness Dry Bulk`, `Baumarine`, `KCC`, `Klaveness Digital`, `Klaveness Finance`, `Company news`, `Sustainability`, `People & careers`. A new name creates a new filter, so only add one when the user asks.
- `coverImage`: file name next to the article. `coverAlt` describes the photo for people who cannot see it; `coverCaption` (optional) is shown under it.
- `draft: true` keeps an article off the live site (it still shows in a local preview).
- Newest `publishedAt` comes first on the site and the homepage shows the latest three.

## Writing the body

- Plain Markdown. The title is the page heading, so start with the text; use `##` and `###` for sub-headings.
- A single line break is kept as a line break.
- Image in the text: `![Alt text](slug-2.webp "Caption shown under the image")`.
- A link alone on its own line becomes an arrow link (a call to action), e.g. `[Read the annual report](https://…)`.
- A YouTube or Vimeo address alone on its own line becomes a video player.
- Links to other pages of the site are relative (`/news/…`, `/about/about-us`); other websites open in a new tab.
- Tables use GitHub table syntax.

## Images

- WebP, at most 2400 px wide, quality around 80. Leave final image choices to the user; do not create or edit images unless asked.
- Every image needs alt text unless it is purely decorative.

## Checks before handing over

1. Spelling, grammar and names (people, vessels, companies), consistent with the existing articles.
2. Front matter: required fields, date format, slug matches the file name, categories spelled exactly.
3. Images exist next to the article and have alt text.
4. Links point where they say and open (no SharePoint, Outlook "safelinks" or tracking parameters).

Report anything unresolved or that needs the user's decision.
