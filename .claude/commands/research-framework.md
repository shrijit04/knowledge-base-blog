---
description: Research an investing framework and optionally publish it as a card + one-pager to the knowledge-base blog
---

You are helping research an investing framework and optionally publish it to the knowledge-base Hugo blog.

The framework to research is: **$ARGUMENTS**

## Step 1 — Research

Use WebSearch and WebFetch to research "$ARGUMENTS" thoroughly. Look for:
- The origin and popularizers of this framework (books, investors, communities like r/IndiaGrowthStocks, Substack writers, etc.)
- The core mechanics — what exactly does this framework measure or evaluate?
- Concrete examples of companies or situations where it applies
- Common pitfalls or misapplications
- How it relates to other investing frameworks

Synthesize your research into a structured brief.

## Step 2 — Draft the content

Produce two pieces of content:

### A. Card content (for the investing-frameworks.md index page)
Format as a set of shortcode parameters:
```
name: <framework name, e.g. "The Two Engine Framework">
tagline: <one punchy sentence — the single insight>
explanation: <2–4 sentences that capture the core idea, concisely>
relevance: <when to use this — 1–2 sentences>
link: /posts/frameworks/<slug>/
```

Where `<slug>` is the framework name lowercased, spaces replaced with hyphens.

### B. One-pager detail page (Markdown, ~600–900 words)

Structure:
```markdown
---
title: "<Framework Name>"
description: "<one-line summary>"
date: <today's date in YYYY-MM-DDT00:00:00Z>
draft: false
tags:
    - investing
    - frameworks
    - <any relevant tags>
categories: ["Investing"]
---

> <Memorable one-liner that captures the framework's insight>

## The core idea
<2–3 paragraphs. What is it? Where does it come from?>

## How it works
<The mechanics. Use headers for sub-components if there are multiple parts. Include a concrete example or table if it helps.>

## How I use it
<4–6 numbered bullet points — practical checklist for applying this framework when evaluating a stock or business>

## Pitfalls to avoid
<2–4 brief bullet points on common misapplications>

## Pairs well with
<Links to related frameworks already in the blog if applicable>

---
*Back to [Investing Frameworks](/posts/investing-frameworks/).*
```

## Step 3 — Present the research

Show the user:
1. A **Research Summary** — key sources, who uses this framework, what you found
2. The **Card draft** (the shortcode parameters)
3. The **One-pager draft** (full markdown)

Then ask the user:

> "Would you like me to add this to your blog? I'll create the card on the Investing Frameworks page and the detail one-pager, then build and push to GitHub."

Use AskUserQuestion with two options: "Yes, publish it" and "No, just keep the research".

## Step 4 — Publish (only if user says yes)

If the user says yes, perform these steps in order:

### 4a. Add the card to the index page

Read `content/posts/investing-frameworks.md`. Find the last `{{< framework` block and insert a new one after it (before any trailing content) using the card draft from Step 2A. The shortcode format is:

```
{{< framework
  name="<name>"
  tagline="<tagline>"
  explanation="<explanation>"
  relevance="<relevance>"
  link="<link>"
>}}
```

### 4b. Create the detail page

Write the one-pager to `content/posts/frameworks/<slug>.md` where `<slug>` matches the link from the card.

### 4c. Build and verify

Run:
```bash
hugo --minify 2>&1 | tail -10
```

Confirm it built without errors and that `public/posts/frameworks/<slug>/index.html` exists.

### 4d. Commit and push

Stage only source files (never stage `public/`):
```bash
git add content/posts/frameworks/<slug>.md content/posts/investing-frameworks.md
git commit -m "Add <Framework Name> to investing frameworks

Research-backed one-pager and index card for <Framework Name>.

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>"
git push origin main
```

Confirm the push succeeded and tell the user the GitHub Actions deploy will be live in ~1–2 minutes at:
`https://shrijit04.github.io/knowledge-base-blog/posts/investing-frameworks/`
