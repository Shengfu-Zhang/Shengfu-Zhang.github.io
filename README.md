# Shengfu Zhang — Personal Blog

**Live site:** https://shengfu-zhang.github.io/

Writing about AI, engineering systems, and how the two are reshaping the way we build software.

---

## What this repo is

This is both a **personal site** and a **content archive**. Every post lives here in full — the long-form essay plus all platform variants (LinkedIn, X/Twitter, 小红书) — so nothing gets lost across platforms.

The site is static HTML hosted on GitHub Pages. No build step, no framework, no dependencies beyond Google Fonts.

---

## Repo structure

```
/
├── index.html                        ← Personal site homepage
├── CLAUDE.md                         ← AI agent workflow instructions (for automation)
└── posts/
    └── YYYY-MM-slug/                 ← One folder per post
        ├── blog.md                   ← Long-form version (Substack)
        ├── linkedin.md               ← LinkedIn post
        ├── twitter.md                ← X/Twitter thread
        ├── xiaohongshu.md            ← 小红书 post (Chinese)
        └── images/                   ← Cover image + diagrams
```

Each post folder is self-contained. All platform variants ship together.

---

## Posts

| Date | Title | Platforms |
|------|-------|-----------|
| Mar 2026 | [We Sped Up the Wrong Part](posts/2026-03-ai-velocity/blog.md) | Blog · LinkedIn · X · 小红书 |

---

## Where to find me

- Site: https://shengfu-zhang.github.io/
- Substack: *(coming soon)*
- LinkedIn: *(coming soon)*
- X/Twitter: *(coming soon)*
- 小红书: *(coming soon)*

---

## How new posts get made

1. Think through an idea in a conversation
2. AI agent reads `CLAUDE.md` and generates all platform variants + images
3. New folder lands in `posts/`, `index.html` gets updated
4. Push to `main` → site auto-updates via GitHub Pages
5. Manually cross-post to Substack / LinkedIn / X / 小红书 (no auto-publish)
