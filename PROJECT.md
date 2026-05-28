# The Formation — Project Reference

## What This Is
A single-file sales landing page for **The Formation**, a 12-week 1:1 marketing coaching offer for online brands. Built in vanilla HTML/CSS/JS — no framework, no build step.

---

## File Location
```
/Users/ibrahimhelwe/Claude Code/My Business/Landing Page/index.html
```

---

## Deployment
- **GitHub repo:** https://github.com/ibbyhelwe/the-formation
- **Vercel project:** the-formation (connected to GitHub, auto-deploys on push)
- **Live URL:** https://highmotionmarketing.com
- **Vercel URL:** https://the-formation.vercel.app

To deploy any change: edit `index.html`, then run from the Landing Page directory:
```bash
git add index.html && git commit -m "your message" && git push
```
Vercel redeploys automatically in ~10 seconds.

---

## Brand System

### Fonts (Google Fonts)
- **Inter** — weights 300–800. Used for all headings, subheadings, UI, body copy, buttons, labels
- **Manrope** — weights 300–700. Used for body copy, nav, labels, captions, small text

### Colour Palette
```css
--charcoal:   #2B2D2F   /* Primary dark background */
--cream:      #F5F1E8   /* Light background + text on dark */
--gold:       #D4A574   /* Accent — highlights, borders, labels */
--forest:     #1C3A30   /* Defined but not used — removed from page */
--slate-blue: #4A5F6D   /* Defined but not used — removed from page */
--signal-red: #C4443C   /* Numbered bars, scarcity indicators */
```

### Section Background Pattern
| Section | Background |
|---------|-----------|
| Hero | Charcoal |
| Who This Is For | Cream |
| The Promise | Charcoal |
| How It Works | Cream |
| What's Included | Charcoal |
| Proof | Cream |
| The Guarantee | Charcoal |
| FAQs | Cream |
| Book a Call (CTA) | Charcoal |
| Footer | Charcoal |

---

## Page Sections

### Nav
- Sticky, transparent over hero → cream + charcoal text on scroll
- Logo: "THE FORMATION" Manrope 600 uppercase
- Links: The Offer / How It Works / What's Included / Proof / FAQs / Book a Call
- CTA button: "Book Free Audit" → gold background, links to Calendly
- Mobile: hamburger menu

### Section 1 — Hero
- Large Inter 800 headline: *"Your marketing isn't broken. Your system is."*
- "broken" is italic gold
- Subheadline: *"12-week 1:1 coaching for online brands who are tired of spending money on marketing that goes nowhere."*
- Two CTAs: Book Your Free Audit Call (gold) + See What's Included (outlined)
- Slow-drifting radial gradient glow animation (gold, 8% opacity, top right)

### Section 2 — Who This Is For
- 7 numbered insight bars (signal-red left border, bold number, regular text)
- "Not for you if —" block (red left border, red tint background)

### Section 3 — The Promise
- Gold-bordered callout block
- 3 stats: 90 / 12 / $0→$50K per month

### Section 4 — How It Works
- 4 process steps as numbered insight bars
- Comparison table: integrated into cream background (no dark block), left col muted/strikethrough, right col gold-tinted

### Section 5 — What's Included
- 3 core cards in a 3-column grid
- "Bonuses Included" divider → 2 bonus cards in a 2-column grid
- Value summary: $10,200 total → $5,000 investment

### Section 6 — Proof
- 3 video testimonials in a 3-column grid (9:16 Vimeo embeds)
  - False 9 Football — Scaled to $1.3M revenue
  - Shareefico — Rebranded & grew content & podcast
  - Train with Gaff — Increased paid ads profit by 4x
- 3 text testimonial cards below (gold left border)
- Vimeo player.js loaded once at bottom of page

### Section 7 — The Guarantee
- Gold-bordered block
- 90-day working guarantee copy

### Section 8 — FAQs
- 7 accordion items, smooth expand/collapse, gold +/− icon

### Section 9 — CTA / Book
- 5 spot indicators (2 red/taken, 3 cream/open)
- Large gold CTA button
- Instagram button linking to @ibrahim.helwe

### Footer
- Wordmark only: "The Formation"
- Legal line: © 2026 The Formation

---

## Key Links
- **Calendly:** https://calendly.com/ibrahimhelwe/discovery-call-1
- **Instagram:** https://www.instagram.com/ibrahim.helwe/
- **Email:** ibbyhelwe@gmail.com

---

## Signature Design Elements
- **Numbered insight bar** — 4px signal-red left border, bold Manrope number, Inter text
- **Gold underline** — 2px gold line, 52px wide, under all section titles via `::after`
- **Section label** — 10px Manrope 600 uppercase gold, letter-spaced (e.g. "01 — WHO THIS IS FOR")
- **Gold left border** — testimonials and callout blocks
- **FadeUp animations** — Intersection Observer, 0.72s ease, staggered with `.d1–.d5` delay classes
- **FAQ accordion** — CSS `max-height` transition, JS toggles `.open` class

---

## JavaScript Features
- Sticky nav: IntersectionObserver on `#hero`
- Mobile menu: hamburger toggles `.open` on nav + body scroll lock
- Scroll animations: IntersectionObserver on all `.fade-up` elements
- FAQ accordion: click to toggle, closes others on open
- Smooth scroll: offset 84px for fixed nav height

---

## Things To Do / Placeholders
- Nothing outstanding — Calendly link is live, domain is connected
