# Hamza Productions — Website

A multi-page cinematic website for **Hamza Productions**, a Pakistan-based videography, tourism, and cinematography business. Built by **Muhammad Ali Eesa** (Warriordude) as a web dev project with Faraz.

Deployed on **Vercel**: [hamzepro.vercel.app](https://hamzepro.vercel.app)

---

## Pages

| File | Route | Purpose |
|---|---|---|
| `index (14).html` | `/` | Homepage |
| `work.html` | `/work` | Projects — Videos, Photos, Reels |
| `reviews.html` | `/reviews` | Client reviews with filter tabs |
| `websitecreation.html` | `/websitecreation` | Developer portfolio (Muhammad Ali Eesa) |

---

## Page Breakdown

### `index.html` — Homepage
- Full-screen hero with a background image and fade-in headline
- **Plan Your Tour** button opens a rich modal form with:
  - Province + city selector (all 8 provinces/regions)
  - Budget slider (PKR / USD)
  - Group size, duration, accommodation style, trip type chips
  - Ready to connect to EmailJS for real form submissions
- Destinations grid (Islamabad, Sindh, Swat Valley, Lahore) — each card opens a detail modal with a draggable image and a "Book This Tour" button that pre-fills the tour form
- Trailer video section (`videos/trailor0001-1904.mp4`) with mute toggle and fullscreen expand
- Services section: Tourism & Travel + Cinematic Videography
- Page transition overlay (gold slide-in/out on navigation)

### `work.html` — Projects
- **Videos section**: 4 video cards in a horizontal carousel (`v1.mp4` through `v4.mp4` + `v30001-1082.mp4`). Each has an inline mute button, a fullscreen expand modal, and a collapsible LinkedIn-style description.
- **Photos section**: 3-column grid (`p1.jpg`, `p2.jpg`, `p3.jpg`). Click any photo to open a fullscreen lightbox.
- **Reels section**: 10 short-form reels (`r1.mp4`–`r10.mp4`) in a 5-per-page carousel. Click any reel to open a TikTok-style fullscreen player with scroll/arrow navigation between reels and a mute toggle.

### `reviews.html` — Reviews
- Stats bar: 50+ Clients, 5.0★, 30+ Videos, 100% Recommend
- Featured review card (Ahmad Al-Rashidi)
- 12 review cards across 3 categories: Tourism (5), Cinematography (4), Photography (3)
- Filter tabs with animated counts — filters cards live without page reload
- Load More button (shows 6 at a time)
- Influencer Spotlight section (4 placeholder cards — fill in real influencers)
- Dynamic CTA section that changes title, subtitle, button text, and background animation based on the active filter tab (pins for tourism, film reel for cinematography, shutter rings for photography)

### `websitecreation.html` — Developer Portfolio
- Personal portfolio page for Muhammad Ali Eesa
- Hero with photo (`photos/pic1.png`), LinkedIn button, tech tags
- 3 specialty cards: AI Websites, Cybersecurity, Web Development
- Projects grid: Hamza Productions (live link) + 2 placeholder project slots
- Skills grid with "Show More" toggle (8 visible + 4 hidden)
- Scroll-triggered reveal animations on all sections

---

## File Structure

```
/
├── index.html         # Homepage
├── work.html               # Projects page
├── reviews.html            # Reviews page
├── websitecreation.html    # Developer portfolio
├── vercel.json             # Vercel deployment config
├── .gitignore
│
├── photos/
│   ├── pic1.png            # Developer photo (websitecreation page)
│   ├── pic21.jpg           # Work page photos
│   ├── pic32.jpg
│   ├── pic43.jpg
│   ├── pic5.jpg            # Islamabad card
│   ├── pic6.jpg            # Sindh card
│   ├── pic7.jpg            # Swat Valley card
│   ├── pic8.jpg            # Lahore card
│   └── pic9.png            # Homepage hero background
│
├── videos/
│   ├── v1.mp4              # Homepage trailer
│   ├── v2.mp4              # Sindh Desert Expedition reel
│   ├── v3.mp4              # Badgoi Top expedition
│   ├── v4.mp4              # Snow Expedition trailer
│   └── v5.mp4              # Color Grading Showcase
│
└── reels/
    ├── r1.mp4 — r10.mp4        # Short-form reels (work page)
```

> **Note:** `photos/`, `videos/`, and `reels/` are in `.gitignore` due to file size. Host media on a CDN (Cloudinary, Bunny CDN, etc.) and update `src` paths before production deployment.

---

## Tech Stack

- Pure **HTML / CSS / JavaScript** — no frameworks, no build tools
- **Google Fonts**: Playfair Display + Plus Jakarta Sans
- **Vercel** for deployment
- All animations are CSS keyframes + JS class toggling
- No npm, no dependencies — open any file directly in a browser

---

## To Do / Placeholders

- [ ] Replace influencer cards in `reviews.html` with real names, handles, and follower counts
- [ ] Fill in the 2 empty project cards in `websitecreation.html`
- [ ] Add EmailJS credentials to the tour form in `index (14).html` (look for the `YOUR_PUBLIC_KEY` comment)
- [ ] Upload media to a CDN and update all `src` paths in the HTML files
- [ ] Add real social media links (currently all `href="#"`)
- [ ] Rename `index (14).html` to `index.html` before final deployment

---

## Deployment

The site is deployed via **Vercel**. Push the HTML files (without media) and Vercel auto-deploys. The `vercel.json` file handles routing config.

```
git add .
git commit -m "your message"
git push
```

Vercel picks it up automatically from the connected GitHub repo.

## live demo
https://hamzepro.vercel.app/

---

*Built by Muhammad Ali Eesa · Hamza Productions · Pakistan*
