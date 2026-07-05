# Updating the Website

Most updates can be made directly on GitHub by editing a Markdown or YAML file.

## Add a New Paper

Edit `data/papers.yaml` and add a new entry:

```yaml
- title: "Paper Title"
  coauthors:
    - "Coauthor Name"
  status: "working paper"
  status_detail: "Optional discussion paper or journal status"
  pdf: "/files/paper-file.pdf"
  link: "https://example.com"
  description: "One sentence about the paper."
  job_market_paper: false
```

If you have a PDF, upload it to `static/files/` and point `pdf` to `/files/filename.pdf`.

## Update the Bio

Edit `content/_index.md`. The paragraphs below the front matter are the homepage bio. The lists at the top control research interests, education, awards, and affiliations.

## Add a Teaching Entry

Edit `data/teaching.yaml` and add another item with the same fields as the existing entries.

## Add a Blog Post

Create a folder such as `content/blog/post-title/index.md` with:

```yaml
---
title: "Post Title"
date: 2026-07-05
description: "One-sentence summary."
tags: ["topic"]
---

Write the post here.
```

## Update the CV

Upload the new PDF to `static/files/cv.pdf`. Add a CV menu item in `hugo.yaml` once the file exists.

## Change the Photo

Replace `static/images/photo.jpg` with a new web-sized headshot using the same filename.

## Add a News Item

Edit `data/news.yaml` if you decide to add a news section later. Use dates in `YYYY-MM-DD` format.

## Mark a Paper as Published

In `data/papers.yaml`, change:

```yaml
status: "working paper"
```

to:

```yaml
status: "published"
venue: "Journal or venue name"
```

## Add a Job Market Paper

Set `job_market_paper: true` on the relevant entry in `data/papers.yaml`. The homepage will highlight it automatically.
