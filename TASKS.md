# GraMedica Website — Build Task Queue
# TASKS.md · Updated: March 2026
# Owner: Ryan Keyes, CBO
#
# HOW TO USE THIS FILE:
# Claude Code reads this at the start of every session.
# Work top-to-bottom through QUEUE. Move items to DONE when complete.
# Ryan updates this file to change priorities or add new tasks.
# Start of session instruction: "Read CLAUDE.md and TASKS.md then execute the top task."

---

## ⚠ ACTIVE DESIGN DIRECTION — READ BEFORE BUILDING ANYTHING

The website is LIGHT / CLINICAL / MEDICAL.
- Default background: white (#FFFFFF)
- Alternating sections: light gray (#F8F9FB)
- Navy (#0D1B2A) hero: homepage only, used sparingly
- Primary action color: #0071CA
- Reference: Arthrex.com, Paragon28.com — NOT dark tech startup
- The existing dark homepage build is being REPLACED

---

## 🔴 IN PROGRESS



---

## 🟡 QUEUE — work in this order

### TASK 1 — Fix V2 Homepage Issues
**Priority:** HIGHEST — do this before any new pages
**Brief:** The V2 homepage has two bugs and one design decision to action.

Fixes:
1. **Footer logo stretched** — find the `<img>` tag for the footer logo in index.html,
   add `style="max-width: 180px; height: auto;"` — do not distort aspect ratio
2. **Favicon missing** — add `<link rel="icon" type="image/png" href="assets/images/favicon.png">`
   to `<head>`. Use `BlkWhteSkruSqrV23.png` from assets as the favicon source
   (the square stacked logo — closest we have until a transparent icon is created).
   Convert to favicon.ico or use PNG directly.
3. **Nav logo review** — Ryan is undecided on white logo on dark nav.
   Create a CSS class toggle so both options are easy to switch:
   Option A (current): white nav BG #0D1B2A, white logo
   Option B (clinical): white nav BG #FFFFFF, black logo, #0071CA links
   Default to Option B (white nav) until Ryan confirms preference.
- Commit: "Fix footer logo stretch, add favicon, switch to white nav"

---
**Priority:** HIGHEST
**Brief:** The current index.html uses a dark-heavy design. Rebuild it with
the correct light/clinical direction described in CLAUDE.md.

Spec:
- Nav: white BG, black horizontal logo (assets/images/logo-nav-hz.png),
  #0071CA for nav links, clean top bar with phone + contact CTA
- Hero: navy (#0D1B2A) BG ONLY for this section, swoosh mark (SkruBluGlo.png),
  tagline verbatim "Restoring motion. Restoring life.", ONE clear CTA button
  in #0071CA, NO autoplay video
- Stats strip: white BG, 4 stats in large Outfit type —
  100,000+ implants · 99% success rate · 5.2% removal rate · <30 min surgery
- Dual CTA section: light gray BG (#F8F9FB), two cards side by side —
  "I'm a Surgeon" (navy card → /for-doctors/) and
  "I'm a Patient" (white card with blue border → /for-patients/)
- Product grid: white BG, 4-col grid, product name + one line description,
  link to product page. Products: HyProCure I, HyProCure II, Osteo-Wedge, Opti-Toe
- Evidence section: light gray BG, 3 study cards with stat + source label
  (use approved Class A stats from CLAUDE.md only)
- Footer: #F2F4F7 BG, black horizontal logo (assets/images/logo-footer-hz.png),
  4-col nav links, address, phone, copyright, "Rx Only" notice
- Commit with message: "Rebuild homepage — light clinical design"

---

### TASK 2 — Rebuild IFU Page (Light Design)
**Priority:** HIGH
**Brief:** Replace the existing dark IFU POC at /ifu/index.html with a
clean, light, clinical design. This is a regulatory-required page.

Spec:
- Header: white BG, black horizontal logo, "gramedica.com" + company name top right
- Hero section: white BG (NOT navy), "Digital IFU Library" label in #0071CA,
  "Instructions for Use" H1 in Outfit, brief description in DM Sans
- Warning banner: amber/yellow BG, "Platform Test — Not for Clinical Use" text
  (keep until QA sign-off — this is regulatory)
- Active Devices section: two cards (HyProCure I + II), each with:
  - Product name, description, ACTIVE badge in green
  - Language grid: EN + ES + DE as clickable buttons (href="[NEEDS CONFIRMATION]")
  - All other languages as disabled/grayed badges labeled "Soon"
- Legacy Devices section: OsteoWedge, OptiToe, K-Wire cards with LEGACY badge
  in amber, single EN language as "Pending QA" disabled state
- Footer: white BG left, regulatory info right —
  "Rx Only — Prescription Use Only · For single use only"
  "© 2026 Graham Medical Technologies"
  "GraMedica® and HyProCure® are registered trademarks of Graham Medical Technologies"
- Commit: "Rebuild IFU page — light clinical design"

---

### TASK 3 — Build /products/hyprocure/ Page
**Priority:** HIGH
**Brief:** HyProCure flagship product page. This is the most important
product page. Class A stats must be used verbatim — do not alter.

Spec:
- Clean light design consistent with homepage
- Hero: white BG, product name H1, one-line description, HyProCure product image
- Stats block: all 4 key Class A stats (use CLAUDE.md section verbatim)
- "What is HyProCure" section: procedure description, minimally invasive, sinus tarsi
- "Why HyProCure" section: 3-column benefit cards
- Clinical evidence callout: "100+ studies. 25 peer-reviewed." with link to /for-doctors/
- CTA section: two paths — "Find a Surgeon" and "I'm a Physician"
- Footer consistent with homepage
- Mark any clinical content sections: <!-- CLASS A — QA REVIEW REQUIRED -->
- Commit: "Build HyProCure product page"

---

### TASK 4 — Build /for-patients/ Hub Page
**Priority:** MEDIUM
**Brief:** Patient education entry point. Warm, clear, empathetic tone.
No clinical jargon. Benefit-focused.

Spec:
- Hero: light design, warm tone, "Understanding HyProCure" or similar
- Section: "What to Expect" — procedure overview in plain language
- Section: "Success Stories" — cards linking to /for-patients/success-stories/
- Section: "Find a Doctor" — CTA card linking to /for-patients/find-a-doctor/
- Section: "Frequently Asked Questions" — 4-5 common patient questions
  (use only Class C language — no clinical claims without [NEEDS CONFIRMATION])
- Footer consistent
- Commit: "Build for-patients hub page"

---

### TASK 5 — Build /for-doctors/ Hub Page
**Priority:** MEDIUM
**Brief:** Physician/surgeon entry point. Professional, evidence-based,
peer-to-peer tone. Clinical credibility first.

Spec:
- Hero: clean light design, surgeon-focused headline
- Section: "Clinical Evidence" — study count stats, link to evidence
- Section: "Surgical Education" → /for-doctors/hyprocure-education/
- Section: "Physician Endorsements" → /for-doctors/physician-endorsement/
- Section: "IFU Access" → /ifu/
- CTA: "Order HyProCure" → crm.gramedica.com (external link)
- Footer consistent
- Commit: "Build for-doctors hub page"

---

### TASK 6 — Build /about-us/ Page
**Priority:** MEDIUM

Spec:
- Company story section: founded 2004, Rochester MI, global reach
- Mission: "Restoring motion. Restoring life." — tagline verbatim
- Numbers bar: years in business · countries · implants · studies
- Team section: Leadership only (Joe Monroe, Ryan Keyes, Brandon Gehres)
  Name + title + email only. NO cell numbers. Phone = +1 586-677-9600.
- Parent company mention: Addvise Group (Swedish-listed)
- Footer consistent
- Commit: "Build about-us page"

---

### TASK 7 — Build /distributors/ Page
**Priority:** MEDIUM

Spec:
- Hero: "Join Our Global Distribution Network"
- Why GraMedica section: key selling points for distributors
- Currently operating in: 19 countries, 38 distributors (6 regions)
- Contact form or CTA → contact-us page
- Footer consistent
- Commit: "Build distributors page"

---

### TASK 8 — Build /contact-us/ Page
**Priority:** MEDIUM

Spec:
- Contact form: Name, Company, Email, Phone, Message, Submit
  (form action = [NEEDS CONFIRMATION] — leave as placeholder)
- Contact details: +1 586-677-9600, info@gramedica.com
- Address: 236 Mill Street, Rochester, MI 48307 USA
- LinkedIn + YouTube links
- Footer consistent
- Commit: "Build contact-us page"

---

### TASK 9 — Build Remaining Product Pages
**Priority:** LOW (after Tasks 1-8 complete)
- /products/hyprocure-ii/
- /products/osteo-wedge/
- /products/opti-toe/
- /products/instruments/
- /products/ (overview grid page)

---

### TASK 10 — Global CSS Audit
**Priority:** LOW
After all pages built, review css/global.css:
- Confirm two-blue rule is enforced via CSS variable comments
- Confirm no #27B1FA appears on white backgrounds anywhere
- Confirm all font declarations use Outfit/DM Sans with correct fallbacks
- Confirm mobile breakpoints are consistent across all pages
- Commit: "CSS audit and cleanup"

---

## ✅ DONE

- [Mar 21, 2026] Site structure scaffold — all folders and stub pages created
- [Mar 21, 2026] css/global.css — brand token system, two-blue rule, typography
- [Mar 21, 2026] Initial homepage (dark design — being replaced by Task 1)
- [Mar 21, 2026] IFU page moved to /ifu/index.html (dark POC — being replaced by Task 2)
- [Mar 21, 2026] SSH configured — Claude Code can push to GitHub without prompts
- [Mar 21, 2026] CLAUDE.md v2.0 added to repo root

---

## 📋 BACKLOG — Not yet scheduled

- /events/ page
- /for-patients/success-stories/ page
- /for-patients/find-a-doctor/ page (may need external tool/Podiatry Today integration)
- /for-doctors/hyprocure-education/ page
- /for-doctors/physician-endorsement/ page
- **Signature installer — future state (idle time / low priority):**
  Move from public Azure Static Web App to internal SharePoint page.
  Add employee onboarding form (name, title, email, phone) that auto-generates
  the signature HTML. New employees self-serve from SharePoint with no IT help needed.
  Access controlled via M365 — internal staff only, not publicly accessible.
- Mobile nav hamburger menu
- SEO meta tags audit across all pages
- Open Graph / social sharing tags
- sitemap.xml
- robots.txt
- 404 page
- Analytics integration (confirm tool with Ryan before adding)

---

*TASKS.md is Class C — Internal. No QA required.*
*Update this file whenever priorities change. Claude Code reads it each session.*
