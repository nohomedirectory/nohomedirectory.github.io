# Joe's Coding Journey — Blog

Built with Jekyll and hosted on GitHub Pages.

## Setup

1. Create a repo on GitHub called `nohomedirectory.github.io`
2. Push all these files to the `main` branch
3. Go to repo Settings → Pages → set Source to "Deploy from a branch" → select `main` → Save
4. Your blog will be live at `https://nohomedirectory.github.io` within a few minutes
5. If you have a custom domain, add it in Settings → Pages → Custom domain

## Writing New Posts

Create a new file in `_posts/` with the format:

```
_posts/YYYY-MM-DD-title-here.md
```

Add front matter at the top:

```yaml
---
layout: post
title: "Your Title"
date: YYYY-MM-DD
categories: [journey]
---

Your content here in markdown.
```

Push to GitHub. The site rebuilds automatically.
