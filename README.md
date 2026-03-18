# Senthil Vel Kumaran — Portfolio

**Live site:** https://senthilvel-k.github.io  
**Stack:** Pure HTML + CSS + JavaScript · Zero dependencies · GitHub Pages hosted  
**File:** Single `index.html` file — everything lives here

---

## 📁 Repository Structure

```
senthilvel-k.github.io/
├── index.html                  ← Entire portfolio (single file)
├── Senthil_Vel_K_Resume.pdf    ← Your resume (replace when updated)
├── README.md                   ← This file
└── BLOG_GUIDE.md               ← Quick reference for adding blogs
```

---

## 🚀 Deployment

### First time setup
```bash
git init
git add .
git commit -m "Initial portfolio"
git remote add origin https://github.com/senthilvel-k/senthilvel-k.github.io.git
git push -u origin main
```

Then in GitHub:  
**Settings → Pages → Source: Deploy from branch → main → / (root) → Save**

Your site goes live at `https://senthilvel-k.github.io` in ~60 seconds.

### Every update after that
```bash
git add .
git commit -m "Update: what you changed"
git push
```
GitHub Pages redeploys automatically. Live in ~60 seconds.

---

## 📖 Page Order (Storyboard)

The portfolio follows this narrative:

| # | Section | Purpose |
|---|---|---|
| 1 | **Hero** | Name, title, CES 2026 badge, live circuit canvas + signal panels |
| 2 | **About** | Bio, story, animated stat counters |
| 3 | **Experience** | Visteon Engineer II + Intern, tabbed with full deliverables |
| 4 | **Projects** | Production ECUs + Personal — click each for architecture modal |
| 5 | **Tech Stack** | Diamond grid with all skills |
| 6 | **Achievements** | Awards, Silver Award story, certifications |
| 7 | **GitHub** | Live repos fetched via GitHub API automatically |
| 8 | **Blogs** | Your technical writing (add as you publish) |
| 9 | **Ask Me** | Hardcoded Q&A terminal with typewriter effect |
| 10 | **Contact** | Links + availability card |

---

## ✍️ How to Add a Blog Post

### Step 1 — Write it anywhere
- [Hashnode](https://hashnode.com) — best for dev blogs, free custom domain, great SEO
- [Dev.to](https://dev.to) — large developer audience
- [Medium](https://medium.com) — broad readership
- GitHub markdown file — create `blogs/can-bus.md` in your repo and link to it

Get your **published URL** ready before editing the site.

### Step 2 — Open `index.html`

Find this comment in the Blogs section (search with `Ctrl+F`):
```
<!-- ─── ADD LIVE BLOGS HERE ─── -->
```

### Step 3 — Copy this template and paste it above the comment

```html
<a href="https://YOUR_BLOG_URL_HERE" target="_blank" class="blog-card">
  <span class="blog-tag proto">Protocol</span>
  <div class="blog-date">Mar 2025</div>
  <div class="blog-title">Your Blog Title Here</div>
  <div class="blog-desc">One or two sentences describing what the post covers.</div>
  <span class="blog-arrow">↗</span>
</a>
```

### Step 4 — Choose the right tag colour

| Class | Colour | Use for |
|---|---|---|
| `blog-tag proto` | Blue | Protocol deep-dives (CAN, I²C, SPI, Ethernet, UART) |
| `blog-tag safety` | Green | Safety & standards (ISO 26262, ASIL, MISRA-C) |
| `blog-tag upcoming` | Grey | Placeholder — not yet published (pointer-events:none) |

### Step 5 — Remove one placeholder

Find a `<div class="blog-card coming-soon">` block and delete the entire div. Replace it with your new `<a>` tag.

### Step 6 — Commit and push

```bash
git add index.html
git commit -m "Add blog: Your Post Title"
git push
```

Live in ~60 seconds.

---

## 🖼️ How to Change Project Images

Each project card has an image from Unsplash. To change any of them:

### Find the image in `index.html`
Search for the project name, then look for the `<img>` tag just above the `.proj-body` div.

```html
<div class="proj-img-wrap">
  <img class="proj-img" src="https://images.unsplash.com/photo-XXXXXX?w=600&q=75" alt="..." loading="lazy">
</div>
```

### Option A — Use a different Unsplash image (free, no account needed)
1. Go to [unsplash.com](https://unsplash.com)
2. Search for what you want (e.g. "car dashboard", "automotive", "circuit board")
3. Click a photo → right-click → Copy image address
4. Replace the `src` URL, keeping `?w=600&q=75` at the end for performance

```html
<!-- Replace this -->
src="https://images.unsplash.com/photo-OLD?w=600&q=75"

<!-- With this -->
src="https://images.unsplash.com/photo-NEW?w=600&q=75"
```

### Option B — Use your own photo
1. Add your photo to the repository root (e.g. `triple-display.jpg`)
2. Reference it with a relative path:

```html
src="./triple-display.jpg"
```

### Option C — Use a photo from the web (any URL)
```html
src="https://any-website.com/your-image.jpg"
```

### Recommended image sizes
- **Project cards:** 600px wide, 155px tall display height (any image works — CSS crops it)
- **Modal images:** 800px wide works well
- **Format:** JPG or WebP for best performance

### Project image locations (quick reference)

| Project | What to search |
|---|---|
| Triple 12.5" Cockpit | `automotive dashboard`, `car interior display`, `cockpit screen` |
| Dual 10.25" Controller | `car dashboard`, `SUV interior`, `Mahindra interior` |
| Infotainment ECU | `car infotainment`, `touch screen car`, `center console` |
| Braille Toy | `arduino project`, `electronics hobby`, `microcontroller` |
| RFID Attendance | `RFID card reader`, `access control`, `security system` |

---

## 🖼️ How to Change Modal Architecture Images

Each project modal has **two images** — a card image and the same full-size image inside the modal. To update:

### Find the project data in the `<script>` block
Search for `const PROJECTS = {` then find your project (e.g. `triple:`).

```javascript
triple: {
  title: 'Triple 12.5-inch Cockpit HPC Controller',
  img: 'https://images.unsplash.com/photo-XXXX?w=800&q=80',  // ← change this
  ...
}
```

Change the `img:` URL to your desired photo. Use `?w=800&q=80` for larger modal display.

---

## 🎨 How to Update Content

### Update your job title
Search for `Embedded Software Engineer II` and replace all instances.

### Update contact email
Search for `senthil3112000@gmail.com` and replace with your new email.

### Update LinkedIn URL
Search for `senthil-vel` (in the LinkedIn URL) and update.

### Update resume PDF
1. Replace `Senthil_Vel_K_Resume.pdf` in the repo root with your new file
2. Keep the same filename — the link updates automatically
3. OR update all instances of `Senthil_Vel_K_Resume.pdf` to your new filename

### Update the "Ask Me" answers
Find `const ANSWERS = {` in the script block. Each entry has a `q` (question) and `a` (answer). Edit the answer text directly. Use `<strong>text</strong>` for bold emphasis.

---

## ⚡ Animations Reference

| Class | Effect | When triggers |
|---|---|---|
| `.s-up` | Slides up from below | On scroll into view |
| `.s-left` | Slides in from left | On scroll into view |
| `.s-right` | Slides in from right | On scroll into view |
| `.s-blur` | Blurs to clear | On scroll into view |
| `.s-scale` | Scales up from 92% | On scroll into view |
| `.stagger` | Children cascade in sequence | On scroll into view |
| `.counter` | Number counts up | On scroll into About section |

All scroll animations **re-fire** when you scroll back up and then down again.

**Always-running animations:**
- Circuit board canvas with flowing signal traces (hero)
- CAN bus waveform + packet cycling (hero right panel)
- MDIO register cycling (hero right panel)
- Rotating rings (hero background)
- Grid line movement (tech stack section)
- Diagonal stripe shift (GitHub section)
- Pulsing ring expansion (Ask Me section)
- Shimmer sweep on stat cards (About section)
- Tech pills bobbing after entrance

---

## 🔧 Suggested Blog Topics (Based on Your Expertise)

Start with these — they map directly to what you've actually built:

| Priority | Title | Why it works |
|---|---|---|
| 1 | How CAN Bus Works — A Firmware Engineer's Perspective | You've configured 200+ PDUs. Nobody writes this from real production experience |
| 2 | AUTOSAR DCM — How UDS Diagnostics Actually Work | 13 service handlers. You know this inside out |
| 3 | I²C Deep Dive — From Register Maps to Driver Code | ADC polling, SerDes init, button interfaces — you've done all three |
| 4 | ISO 26262 in Practice — What ASIL-D Means in Real Code | You have zero field escapes. This is credible |
| 5 | Writing a Clause 22 MDIO Driver from Scratch | Almost nobody blogs about this. Pure differentiation |
| 6 | Automotive Ethernet — Why 100BASE-T1 is Different | Rare topic. You bring-up the PHY and switch |
| 7 | QNX Neutrino — How MCU Data Reaches Android Automotive | Your UART IPC story. Fascinating cross-domain |
| 8 | How to Debug an ECU with Lauterbach Trace32 | Practical, searchable, exactly what junior devs need |
| 9 | MISRA-C in Practice — Common Violations and How to Fix Them | 500+ cleared. You have war stories |
| 10 | GMSL2 SerDes Bring-Up — Step by Step | MAX96705/MAX9272 is niche and valuable |

---

## 📱 Mobile Behaviour

- Custom cursor hidden automatically on touch devices
- Hero signal panel hidden on mobile (< 960px)
- Nav collapses to hamburger menu
- Sidebar social icons hidden on mobile
- Project cards stack to single column
- Modal takes full width with internal scroll
- All animations still work on mobile

---

## 🏅 Your Key Numbers (For Reference)

Use these consistently across resume, LinkedIn, and portfolio:

| Metric | Value |
|---|---|
| Production ECU programs | 3 |
| OEM brands | Mahindra · Tata Motors |
| UDS service handlers (ISO 14229) | 13 |
| CAN PDUs/signals configured | 200+ |
| MISRA-C violations cleared | 500+ |
| Quiescent current reduction | 20–40% |
| Thermal field escapes | 0 (ASIL-D) |
| Production Embedded C written | 10,000+ lines |
| Global showcase | CES 2026, Las Vegas |
| Award | Visteon Silver Award |

---

## 📧 Contact & Profiles

| Platform | URL |
|---|---|
| Email | senthil3112000@gmail.com |
| LinkedIn | linkedin.com/in/senthil-vel |
| GitHub | github.com/senthilvel-k |
| Portfolio | senthilvel-k.github.io |
| Resume | github.com/senthilvel-k/senthilvel-k.github.io/blob/main/Senthil_Vel_K_Resume.pdf |

---

## 📋 LinkedIn Content Plan (30-Day Reference)

Post daily for traction. Mix these formats:

**Week 1 — Establish authority**
- Day 1: "What is AUTOSAR and why every car ECU runs it" (explainer)
- Day 2: Your Visteon journey — intern to Engineer II (personal story)
- Day 3: "CAN vs CAN FD — what changed and why it matters"
- Day 4: What is UDS? The protocol mechanics talk to your car
- Day 5: A day in the life of an automotive embedded engineer

**Week 2 — Deep dives**
- Day 6: "How I debugged a display bring-up issue with Trace32"
- Day 7: ISO 26262 explained simply — ASIL A to ASIL D
- Day 8: Why QNX is the RTOS of choice in automotive cockpits
- Day 9: SPI vs I²C — when to use which in embedded systems
- Day 10: "What is a SerDes chip and why your car's display needs one"

**Week 3 — Career content**
- Day 11: "5 things I wish I knew before joining automotive embedded"
- Day 12: How to read a microcontroller datasheet efficiently
- Day 13: CAN bus frame structure — annotated breakdown
- Day 14: My learning roadmap to become a senior embedded engineer
- Day 15: UART vs USART — the difference with real code

**Week 4 — Projects + proof**
- Day 16: Post your first GitHub project (FreeRTOS or UDS simulator)
- Day 17: "How IPC works between MCU and SoC in modern car cockpits"
- Day 18: Automotive Ethernet 100BASE-T1 — why it's different
- Day 19: Poll — "What's harder to debug — CAN or Ethernet?"
- Day 20: Share portfolio link + resume

**Format tips:**
- Start with a hook — one striking sentence
- Use line breaks every 1–2 lines (LinkedIn readers skim)
- End with a question to drive comments
- Tag: #EmbeddedSystems #Automotive #AUTOSAR #ISO26262 #CAN

---

## 🎯 GitHub Repo Ideas to Build

Push these as personal projects to fill your GitHub profile:

| Repo name | What to build | Why |
|---|---|---|
| `uds-simulator` | Python UDS diagnostic simulator | Shows ISO 14229 depth |
| `can-bus-logger` | CAN frame logger using Python + socketcan | Shows protocol knowledge |
| `rtos-tasks-demo` | FreeRTOS task scheduling on STM32 | Shows RTOS skill |
| `uart-ipc-protocol` | MCU↔host UART framing with CRC | Your actual production technique |
| `autosar-com-demo` | Simulated AUTOSAR COM layer in C | Shows stack knowledge |
| `mdio-driver` | Bare-metal MDIO Clause 22 driver | Rare, highly specific |

Each repo should have:
- A clear `README.md` explaining what it is and why
- Embedded C or Python code with comments
- A simple diagram if possible

---

*Last updated: March 2026*
