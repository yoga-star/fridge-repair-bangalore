# Fridge Repair Bangalore — Brand Brief & Claude Chat Instructions

> Paste this entire file as the first message of any new Claude conversation to give it full project context.

---

## 1. Business Snapshot

| Field | Value |
|---|---|
| Brand name | **Fridge Repair** |
| Category | Appliance repair service |
| Service | Same-day doorstep refrigerator repair |
| City | Bangalore, Karnataka, India |
| Hours | 24 × 7, every day of the year |
| Phone | +91 73376 31617 |
| Email | fridgerepairp@gmail.com |
| Visit fee | ₹250 (waived on repair) |
| Positioning | "Fridge Not Cooling? We Fix It Today — Or You Pay Nothing." |

**Target customer:** Bangalore homeowners / tenants whose fridge just broke and they need it fixed today. High urgency, high intent, mobile-first, likely arriving from a Google search or Google Ad.

**Primary business goal:** Generate phone calls (Google Call Ads) and online form leads (Google Search / Display Ads).

---

## 2. Brand Voice

- **Confident, warm, local.** "We reach you in 90 minutes." Not corporate-stiff.
- **Transparent & fair.** Talks about fixed-rate quotes, no upsell, written warranty.
- **Urgent but not pushy.** The CTA is "Call now — it takes 60 seconds," not "ACT FAST!"
- **Trust signals first.** 4.8★, 1,247 reviews, 12+ years, 12,000+ repairs, 1-year warranty.

Avoid: hyperbole ("world's best"), melodrama, discount-screaming, generic SEO word-salad.

---

## 3. Design System

### Colors
| Token | Value | Use |
|---|---|---|
| `--primary` | `#0B6E99` | Deep teal — trust, primary accent |
| `--primary-dark` | `#074E6E` | Darker teal — hovers, gradient stops |
| `--primary-light` | `#E6F4FA` | Soft teal tint — backgrounds |
| `--accent` | `#F97316` | Orange — every CTA button |
| `--accent-dark` | `#C2410C` | Orange hover |
| `--ink` | `#0F172A` | Near-black — body text |
| `--ink-2` | `#334155` | Secondary text |
| `--muted` | `#64748B` | Tertiary / meta text |
| `--success` | `#16A34A` | Green dot, checkmarks |

Hero background is a deep teal gradient (`#052437 → #07476B → #0B6E99`).

### Typography
- Headings: **Manrope** 700–800
- Body: **Inter** 400–600
- Both loaded from Google Fonts

### Components
- Buttons: pill-shaped (border-radius 9999px), orange primary / white outline ghost
- Cards: 14px radius, subtle teal-tinted shadow
- All sections alternate white / `--bg-soft` (#F8FAFC)
- Scroll-reveal animation via IntersectionObserver

---

## 4. Technical Stack

- **Single file:** `index.html` (~1000 lines, everything inline — HTML + CSS + JS)
- **No build step.** Open the file directly or host as static.
- **Local path:** `/Users/apple/Desktop/fridge-repair-sample/index.html`
- **Git repo:** https://github.com/yoga-star/fridge-repair-bangalore
- **Deployed on:** Vercel (auto-deploys on every push to `main`)
- **Hero image:** `hero-image.jpg` in project root (technician photo)

### Why a single file
- Loads fast on mobile (critical for Google Ads quality score)
- No dependencies to break
- Easy to hand off, easy to edit in any tool

### Editing workflow
1. Edit `index.html` (or ask Claude to)
2. `git add . && git commit -m "..." && git push`
3. Vercel auto-redeploys in ~15 seconds

---

## 5. Page Architecture (in order)

1. **Announcement bar** — ₹250 visit fee, 24/7 service, 1-year warranty
2. **Sticky header** — Logo (fridge icon + "Fridge Repair"), nav, phone CTA
3. **Hero** — dark teal gradient, technician photo on right, headline + subtitle + two CTAs (Call / Book) + trust row + form card
4. **Problem strip** — 8 common fridge issues (cooling, leak, noise, ice, light, door, power, gas)
5. **Services** — 6 service cards with placeholder pricing ("Call for best quote")
6. **Why Us** — Dark panel with 4 feature tiles + 4 stats (12K+, 12+, 4.8★, 90 min)
7. **Process** — 5-step flow (Call → Reach → Diagnose → Repair → Warranty)
8. **Brands** — 12 logo tiles via Clearbit (LG, Samsung, Whirlpool, Godrej, Haier, Bosch, Siemens, Panasonic, Hitachi, Electrolux, Voltas, IFB) with text fallback
9. **Testimonials** — 3 Google-style review cards
10. **Service areas** — 16 Bangalore localities
11. **CTA block** — teal gradient card with phone CTA
12. **FAQ** — 6 questions, accordion-style, wrapped in FAQPage schema
13. **Footer** — 4 columns (About / Services / Company / Contact) + copyright
14. **Sticky mobile bar** — Call + WhatsApp buttons (always visible on <760px)

---

## 6. Conversion Infrastructure

### Google Ads tracking (placeholder IDs — replace before launch)
- `AW-CONVERSION-ID` → your Google Ads account ID
- `CALL-LABEL` → call-conversion label (fires on phone click)
- `FORM-LABEL` → form-conversion label (fires on form submit)
- `gtag_report_call_conversion()` — attached to every `tel:` link
- `gtag_report_form_conversion()` — fires on hero form submit

### Schema.org (for SEO / rich results)
- `LocalBusiness` — with geo, openingHours (24/7), aggregateRating, areaServed
- `FAQPage` — 6 Q&A pairs eligible for Google rich snippets

### CTAs (in priority order)
1. Phone call: header pill, hero button, CTA block, sticky mobile bar, footer — **~7 touchpoints**
2. WhatsApp: sticky mobile bar, footer
3. Form: hero card ("Get Free Quote in 60 Seconds" — 4 fields)

---

## 7. What's Real vs Placeholder

### ✅ Real / confirmed
- Phone: +91 73376 31617
- Email: fridgerepairp@gmail.com
- City: Bangalore
- Hours: 24/7
- Visit fee: ₹250

### ⚠️ Placeholder — needs real values before launch
| Field | Current | Notes |
|---|---|---|
| Google Ads ID | `AW-CONVERSION-ID` / `CALL-LABEL` / `FORM-LABEL` | Create Google Ads account → get IDs |
| Canonical domain | `www.coolfix-bangalore.in` | Replace with real domain in meta + schema |
| Reviews / rating | 4.8★ · 1,247 reviews | Pull from real Google Business Profile |
| Years in business | 12+ / 12,000+ repairs | Replace with real numbers |
| Testimonials | 3 fictional (Ramya M., Arjun Krishnan, Sneha Patel) | Swap for real reviews |
| Social URLs | `#` | Add real Facebook / Instagram / WhatsApp Business |
| OG image | `/og-image.jpg` (404) | Create a 1200×630 social share image |
| Favicon | None | Add a 32×32 icon |
| Legal entity | "Fridge Repair Bangalore" | Replace with registered name + GST if applicable |

### 🚫 Pricing
- **All specific prices were removed by user request.** Every service card now says "Call for best quote." Visit fee (₹250) is the only price shown.

---

## 8. Instructions for Future Claude Chats

When you start a new chat and want Claude to work on this project, paste this brief and then state your task. Good opening prompts:

### Examples

> "Here's the brand brief. I want to add a section about commercial fridge repair (hotels / restaurants) between the services and why-us sections. Match existing style."

> "Here's the brand brief. The phone CTA feels weak on mobile — suggest 3 variants and implement the best one."

> "Here's the brand brief. Write 3 real-sounding testimonials for a Samsung double-door owner in Whitefield, a Godrej single-door owner in Electronic City, and a Voltas deep-freezer owner in HSR — and replace the existing fictional ones."

> "Here's the brand brief. Add a blog section linked from the footer with 3 starter article stubs: 'Why your fridge is not cooling', 'How to clean the condenser coils', 'When to repair vs replace your fridge'."

> "Here's the brand brief. Before launch, swap all placeholder Google Ads IDs with these real ones: [IDs]. Also update the canonical URL to fridgerepairbangalore.com."

### Claude rules for this project

1. **Edit `index.html` directly** — never introduce a build step or framework.
2. **Match the existing voice** — confident, local, transparent, not salesy.
3. **Preserve conversion hooks** — don't remove `onclick="return gtag_report_call_conversion(...)"` from tel: links, don't remove schema blocks.
4. **Match design tokens** — use the CSS custom properties already defined (`--primary`, `--accent`, etc.). Don't hardcode hex values.
5. **Keep the single-file architecture** — all CSS and JS stays inline.
6. **After substantive edits, push to GitHub:**
   ```
   cd /Users/apple/Desktop/fridge-repair-sample
   git add .
   git commit -m "<what changed>"
   git push
   ```
   Vercel redeploys automatically.
7. **Don't add features beyond what was asked.** No speculative abstractions, no extra configurability.

---

## 9. Key Files

```
/Users/apple/Desktop/fridge-repair-sample/
├── index.html          ← the entire site
├── hero-image.jpg      ← technician hero photo
├── .gitignore
└── BRAND_BRIEF.md      ← this file
```

---

## 10. Quick Commands

```bash
# Preview locally
open -a "Google Chrome" /Users/apple/Desktop/fridge-repair-sample/index.html

# Edit + redeploy
cd /Users/apple/Desktop/fridge-repair-sample
# (edit index.html)
git add . && git commit -m "your message" && git push

# Check live site
open https://fridge-repair-bangalore.vercel.app    # (actual URL after you finish Vercel import)

# See the repo
open https://github.com/yoga-star/fridge-repair-bangalore
```
