# How to Publish a New Blog Post

This file explains how to add a new blog post card to your portfolio.

## Step 1 — Write your blog
Write anywhere you like:
- [Hashnode](https://hashnode.com) — recommended, gives you a custom domain
- [Dev.to](https://dev.to) — great for developer audience
- [Medium](https://medium.com) — broad readership
- GitHub markdown file — commit a `.md` file to your repo and link to it directly

## Step 2 — Add the card to index.html

Open `index.html` and find the `<!-- ─── ADD YOUR BLOGS HERE ─── -->` comment in the blogs section.

Copy this template and paste it above the comment:

```html
<a href="https://YOUR_BLOG_URL_HERE" target="_blank" class="blog-card">
  <span class="blog-tag">Protocol</span>   <!-- Tag options: Protocol, Safety, AUTOSAR, SoC, Tools, Career -->
  <div class="blog-date">Mar 2025</div>
  <div class="blog-title">Your Blog Title Here</div>
  <div class="blog-desc">A 1–2 sentence description of what the post covers.</div>
  <span class="blog-arrow">↗</span>
</a>
```

Available tag styles:
- `class="blog-tag"` → Blue (Protocol, AUTOSAR, etc.)
- `class="blog-tag cs"` → Green (Career, Personal)
- `class="blog-tag upcoming"` → Grey (Coming Soon placeholders)

## Step 3 — Remove a placeholder

Find one of the `coming-soon` cards and either:
- Delete it entirely, or
- Replace it with your new live card

## Step 4 — Commit and push

```bash
git add index.html
git commit -m "Add blog: Your Post Title"
git push origin main
```

GitHub Pages deploys in ~60 seconds. Your post card goes live automatically.

---

## Suggested blog topics (based on your expertise)

| Topic | Title idea |
|---|---|
| CAN Bus | How CAN Bus Works — A Firmware Engineer's Perspective |
| I²C | I²C Deep Dive — From Register Maps to Real Driver Code |
| UDS / DCM | How UDS Diagnostics Work in AUTOSAR |
| ISO 26262 | What ASIL-D Really Means in Production Code |
| QNX | MCU to SoC IPC — How Vehicle Data Reaches Your Display |
| Ethernet | Automotive Ethernet & Why 100BASE-T1 is Different |
| MISRA-C | MISRA-C in Practice — Common Violations and How to Fix Them |
| Debugging | How to Debug an ECU with Lauterbach Trace32 |
