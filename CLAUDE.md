# CLAUDE.md
> Standing instructions for AI agents (Cowork, Claude Code, etc.) working on this repo.
> Read this first before doing anything.

---

## What This Repo Is

Personal blog and content artifact store for **Shengfu Zhang**.
Live site: `https://shengfuzhang.github.io`
Hosted via: GitHub Pages (static HTML, no build step)

The repo is both a **public blog** and a **cold artifact store** — every post lives here in full, across all platform variants.

---

## Repo Structure

```
shengfuzhang.github.io/
├── CLAUDE.md                          ← You are here
├── README.md                          ← Human-facing repo description
├── index.html                         ← Personal site homepage
├── style.css                          ← (if extracted later)
├── internal/                          ← Private drafts, internal docs (not linked publicly)
│   └── YYYY-MM-slug.md
└── posts/
    └── YYYY-MM-slug/
        ├── README.md                  ← Post status tracker
        ├── blog.md                    ← Substack / long-form version
        ├── blog.html                  ← Rendered HTML version for GitHub Pages
        ├── linkedin.md                ← LinkedIn post
        ├── twitter.md                 ← X/Twitter thread
        ├── xiaohongshu.md             ← 小红书 post (Chinese)
        └── images/
            ├── cover.png              ← Cover image (1200x630px)
            ├── pyramid-diagram.png    ← Diagrams referenced in blog
            └── *.png
```

---

## How to Create a New Post

### Step 1 — Get the source material
Source is always a Claude chat transcript or a markdown draft handed off from a thinking session.
The human will provide either:
- A chat transcript link or paste
- A rough markdown file
- A bullet list of ideas to expand

### Step 2 — Create the post folder
```
posts/YYYY-MM-slug/
```
Use the current month and a 2-4 word kebab-case slug. Example: `2026-04-agent-design-patterns`

### Step 3 — Draft all platform variants
Generate these files from the source material:

| File | Format | Length | Tone |
|------|--------|--------|------|
| `blog.md` | Markdown | 600–900 words | Personal, 2/3 technical, first person |
| `linkedin.md` | Plain text | 150–250 words | Thought leadership, ends with question |
| `twitter.md` | Plain text | 5–7 tweets | Punchy, opinionated, hook in tweet 1 |
| `xiaohongshu.md` | Markdown | 300–450 words | Chinese, casual, relatable, emoji ok |

**Voice:** Shengfu writes as a practitioner-thinker. Not academic. Not hype. Grounded in real experience, with a systems-thinking lens. First person. Honest about uncertainty.

### Step 4 — Generate images
Generate these images and save to `posts/YYYY-MM-slug/images/`:

| File | Size | Notes |
|------|------|-------|
| `cover.png` | 1200×630px | Clean, dark background, title text, minimal |
| One diagram per key concept in the post | 1000×600px | Match dark editorial aesthetic of site |

**Visual style:** Dark background (#0e0e0e), accent color #c8f060 (lime) or #60c8f0 (blue), DM Serif Display or DM Mono for labels. Clean, editorial, not generic.

### Step 5 — Render blog.html
Convert `blog.md` to `blog.html` matching the site aesthetic (dark theme, same fonts as index.html).
Include: post title, date, author, tags, body, links back to index.

### Step 6 — Update index.html
Add the new post to the top of the `.posts` list in `index.html`:
```html
<a class="post" href="posts/YYYY-MM-slug/blog.html">
  <div class="post-date">Mon<br>YYYY</div>
  <div class="post-body">
    <div class="post-title">Post Title</div>
    <div class="post-summary">One sentence summary.</div>
    <div class="post-tags">
      <span class="tag">Tag1</span>
    </div>
  </div>
  <div class="post-arrow">→</div>
</a>
```

### Step 7 — Update post README.md
Mark all generated files as ✅ in the post's `README.md` status table.

### Step 8 — Commit and push
```bash
git add .
git commit -m "post: YYYY-MM-slug"
git push origin main
```

---

## How to Update an Existing Post

1. Edit the relevant `.md` file(s) in the post folder
2. Regenerate `blog.html` if `blog.md` changed
3. Commit with message: `update: YYYY-MM-slug — [what changed]`

---

## Site Design Rules

- **Theme:** Dark editorial. Never change the core aesthetic without being asked.
- **Fonts:** DM Serif Display (headings), DM Sans (body), DM Mono (labels/meta)
- **Colors:** bg `#0e0e0e`, accent `#c8f060`, accent2 `#60c8f0`, muted `#555`
- **No frameworks.** No build tools. Pure HTML + CSS + minimal JS only.
- **No external dependencies** except Google Fonts.
- GitHub Pages serves `index.html` from `main` branch root.

---

## Author Context

**Name:** Shengfu Zhang
**Bio:** Engineer exploring how AI is reshaping the way we build software. Sharing what I'm learning along the way.
**Topics:** AI coding agents, engineering systems, developer productivity, multi-agent design, software quality
**Platforms:** Substack, LinkedIn, X/Twitter, 小红书
**Language:** English for all platforms except 小红书 (Chinese)
**Do not mention:** Current employer or job title explicitly

---

## What NOT to Do

- Don't change `index.html` design without being asked
- Don't publish to Substack/LinkedIn/X automatically — drafts only, human approves before posting
- Don't put internal docs in the `posts/` folder — use `internal/` instead
- Don't invent data or metrics — use placeholders like `[X%]` if real numbers aren't provided
