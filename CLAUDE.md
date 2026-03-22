# GraMedica — Claude Code Session Context
# CLAUDE.md · Version 1.0 · March 2026
# Owner: Ryan Keyes, CBO
# Drop this file in the root of any GraMedica repo.

---

## WHO WE ARE

**Legal entity:** Graham Medical Technologies, LLC
**Brand name:** GraMedica
**Parent company:** Addvise Group (Swedish-listed)
**Address:** 236 Mill Street, Rochester, MI 48307, USA (USPS Mailbox #10)
**⚠ OLD Macomb, MI address is DEAD — never use it.**

**Website:** gramedica.com
**CRM:** crm.gramedica.com (DataSmart / IIS)
**IFU page (live/test):** witty-glacier-05fbc320f.2.azurestaticapps.net (custom domain pending)
**Main office phone:** +1 586-677-9600
**Fax:** +1 586-677-9615
**LinkedIn:** https://www.linkedin.com/company/gramedica
**YouTube:** https://www.youtube.com/@GraMedicaFootInnovations
**GitHub org:** gramedica (admin: github@gramedica.com)
**IT alert email:** GRAIT@gramedica.com

**Active tagline (verbatim only):** Restoring motion. Restoring life.
**RETIRED tagline — NEVER USE:** "Changing lives, one step at a time."

**Brand hierarchy rule:** GraMedica = company/brand. HyProCure = product. Always company first.

---

## PRODUCTS

| Product | Description | Status |
|---------|-------------|--------|
| HyProCure® I | Extra-Osseous TaloTarsal Stabilization — titanium sinus tarsi stent | Active — primary revenue |
| HyProCure® II | Second generation | Active — primary revenue |
| Osteo-Wedge® | Open Wedge Bone Locking System | Active |
| Opti-Toe® | Lesser toe reconstruction device | Active |
| K-Wire | Surgical instrument | Active — excluded from rep commissions |
| Stevens Tenotomy Scissors | Surgical instrument | Active |
| Graham Decompression Scissors | Surgical instrument | Active |
| General Forceps | Surgical instrument | Active |
| Foot Models | Educational/training models | Active |
| Soleus | Consumer product | Active — excluded from rep commissions |

**Key HyProCure stats (Class A — QA approved, do not alter):**
- 100,000+ implants worldwide since 2004
- 99% implant success rate (8-year Orthopaedic Surgery study, 2025)
- 100+ studies, 25 peer-reviewed
- 5.2% removal rate (vs. up to 58% for competing implants)
- Complaint rate as low as 0.1%
- Surgery takes less than 30 minutes
- Immediate weight-bearing in post-op shoe; full activity in 2 weeks

---

## BRAND COLOR SYSTEM

### THE TWO-BLUE RULE — CRITICAL
| Color | Hex | Use ONLY on |
|-------|-----|-------------|
| Primary Blue | #0071CA | White / light backgrounds ONLY |
| Digital / Accent Blue | #27B1FA | Navy / dark backgrounds ONLY |
| **⚠ NEVER swap these two blues across contexts** | | |

### Full Palette
| Name | Hex | Usage |
|------|-----|-------|
| Navy — Primary Dark | #0D1B2A | Backgrounds, dark sections, nav |
| Primary Blue | #0071CA | CTAs, accents on white/light BG |
| Digital Blue | #27B1FA | Accents on navy/dark BG only |
| Footer Gray | #F2F4F7 | Email footers ONLY |
| White | #FFFFFF | Body backgrounds |

### Context Rules
**Dark sections (hero, nav, dark cards):**
- BG: #0D1B2A
- Accent: #27B1FA
- Text: #FFFFFF

**Light sections (content, forms, standard pages):**
- BG: #FFFFFF
- Accent: #0071CA
- Text: #0D1B2A

**Accessibility note:** #27B1FA on white FAILS WCAG 2.1 AA (ratio ~2.8:1). Never use on white.

---

## TYPOGRAPHY

| Font | Role | Source |
|------|------|--------|
| Outfit | All headings H1–H4, labels, button text | fonts.google.com/specimen/Outfit — SIL OFL |
| DM Sans | All body copy, form fields | fonts.google.com/specimen/DM+Sans — SIL OFL |
| Arial / Segoe UI | Fallback ONLY (Outlook, Office, offline) | System font |

- Use Outfit for ALL headings — no exceptions
- DM Sans for all body text
- Arial/Segoe UI replaces Google Fonts ONLY when unavailable (Outlook email, offline environments)

---

## LOGO FILES

All logos have baked-in backgrounds — they are NOT transparent PNGs. Match variant to background. Never use CSS filters.

| File | Background | Use Case |
|------|-----------|----------|
| `BluWhtHzV212.png` | Blue BG / White logo | Email headers, dark digital contexts |
| `BlkWhtHzV24.png` | White BG / Black logo | Letterhead, email footers, documents |
| `WhtBlkHzV217.png` | Navy BG / White logo | Dark digital hero sections, print |
| `WhtBlkSqrV214.png` | White BG / Black logo (square stacked) | Email signatures ONLY — 100px wide |
| `BluWhteSqrV29.png` | Blue BG / White logo (square stacked) | Dark signature contexts |
| `SkruBluGlo.png` | Dark/digital glow variant | Approved for dark/digital contexts — deployed on IFU page |

**RETIRED:** Blue circle "G" wordmark — DO NOT USE on any new materials.
**Active mark:** New swoosh mark only.

---

## EMAIL TEMPLATE STANDARD — LOCKED Mar 11, 2026

All email templates follow the v2 HTML standard:

| Element | Spec |
|---------|------|
| Header | Navy/blue background with embedded white logo (`BluWhtHzV212.png`) |
| Secondary bar | Blue label bar (#0071CA) |
| Footer | Light gray #F2F4F7, black logo (`BlkWhtHzV24.png`) |
| Body accents | Left-bordered info blocks |
| Logo embedding | Base64 inline (Gmail + Outlook compatibility) |

### Image Handling Rule — LOCKED
- **Base64 embedded** → internal staff, US field reps, international distributors
- **Hosted images (ESP standard)** → any audience beyond those three, or when an ESP is involved

---

## EMAIL SIGNATURE STANDARD — LOCKED

| Element | Spec |
|---------|------|
| Logo variant | `WhtBlkSqrV214.png` — square stacked, 100px wide |
| Social icons | PNG image-based only (only reliable method to eliminate Outlook blue link border) |
| Hosting | Azure Static Web App (GitHub repo: Gramedica-web) |
| Current version | V9 — deployed March 2026 |

**Open items:** Kyan Flynn and Sheridan Geisler still need to provide real scheduling URLs (placeholders currently in signatures). Kyan needs to reinstall using V9.

---

## TECH STACK

| System | Details | Notes |
|--------|---------|-------|
| Microsoft 365 Business Premium (P2) | Productivity, email, SharePoint, Teams | Microsoft-first principle |
| Azure Static Web Apps | Static site hosting | East US 2. Auto-deploy from GitHub. Health alerts → GRAIT@gramedica.com |
| GitHub (org: gramedica) | Version control | Admin: github@gramedica.com |
| DataSmart CRM (crm.gramedica.com) | IIS environment | Direct hooks to Everest ERP |
| Everest ERP (DimeSoft) | On-prem legacy | **EOL — Win Server 2012, Win 10 client only. No further revisions. NO CHANGES without Tabitha Jaramillo. ERP migration = standalone project.** |
| SharePoint (M365) | Document hosting, Brand Central | gramedica.sharepoint.com |
| Cloudflare / VCS (Vistitude) | DNS | Ryan has no direct access. DNS requests go through Jason Alquiza. |
| Mac Mini M4 — 32GB / 1TB SSD | Local dev hardware | Delivered March 2026 |
| Power BI Desktop | BI | Deployment path TBD |

---

## CRM REDESIGN — ACTIVE WORKSTREAM

**Environment:** IIS / PHP. HTML/CSS-only changes — no PHP logic changes.
**Files produced:** `crm_login.html` · `crm_portal_shell.html`

### Priority Order
1. Login page (`crm_login.html`)
2. HyProCure Order Form — **HIGHEST PRIORITY for field mobile use**
3. Nav bar
4. Remaining portal forms

### Forms Queue (after Order Form)
1. HyProCure PO Billing Form
2. HyProCure II Order Form + PO Billing Form
3. New Prospect Registration
4. New Facility Credit Application
5. Remaining order/billing forms (Osteo-Wedge, Opti-Toe, Scissors)

### CSS Design Tokens
```css
--blue:       #1685D4;   /* primary brand blue */
--blue-dark:  #0F6BB0;   /* hover state */
--navy:       #0D1B2A;   /* header, login panel backgrounds */
--border:     #D5E1EC;   /* form field borders */
--red:        #D93025;   /* required field indicators */
```

### Deployment Rules
- Login: form POSTs to `index.php` with fields `username` and `password`. Add `?error=1` for error state.
- Viewport meta tag: Add `<meta name="viewport" content="width=device-width, initial-scale=1.0">` to any page missing it — immediate mobile fix, no other changes.
- Logo is base64-embedded in HTML files — no external image dependencies.

### Navigation Link Targets (CRM)
| Label | href |
|-------|------|
| Home | `home.php` |
| Reports | `custom.php?filename=reports.php` |
| Surgeries | `custom.php?filename=surgeries.php` |
| Doctors | `custom.php?filename=doctors.php` |
| Order History | `custom.php?filename=order_history.php` |
| Invoice History | `custom.php?filename=invoice_history.php` |
| Inventory | `custom.php?filename=inventory.php` |
| Accounts | `custom.php?filename=accounts.php` |
| Leads | `custom.php?filename=leads.php` |
| Tasks | `custom.php?filename=tasks.php` |
| CRM Users | `custom.php?filename=crm_users.php` |
| Forms | `custom.php?filename=forms.php` |
| My Settings | `custom.php?filename=settings.php` |

---

## WEBSITE — STATIC SITE (REBUILDING)

**Stack:** Static HTML/CSS/JavaScript — NO WordPress, NO CMS
**Hosting:** Azure Static Web Apps (auto-deploy from GitHub)
**IFU docs:** Stored in SharePoint. Site links OUT to SharePoint-hosted PDFs. Never store PDFs in the static site.
**Old site:** WordPress + Divi at gramedica.com — DO NOT REPLICATE. Heavy, slow, outdated.

### Target Site Architecture
```
/                     → Homepage
/about-us/
/products/
  /products/hyprocure/
  /products/hyprocure-ii/
  /products/opti-toe/
  /products/osteo-wedge/
  /products/instruments/
/for-patients/
  /for-patients/success-stories/
  /for-patients/find-a-doctor/
/for-doctors/
  /for-doctors/hyprocure-education/
  /for-doctors/physician-endorsement/
/distributors/
/events/
/ifu/
/contact-us/
```

### Homepage Priorities
1. Hero: Dark BG (#0D1B2A), swoosh mark visible, tagline verbatim
2. NO autoplay video on hero (performance)
3. Key stats block: 100,000+ implants · 99% success rate · 5.2% removal rate · <30 min surgery
4. Dual CTA paths: "I'm a Surgeon" / "I'm a Patient"
5. Product highlight grid
6. Trust signals: years, countries, patients

### IFU Page Design Direction
- Light background (white or very light gray) — NOT dark/navy
- Clinical and clean — think pharmaceutical insert library
- NOT the existing dark POC — that is being replaced
- "Soon" languages shown as disabled/grayed-out badges — no broken links
- Trust markers: "Rx Only — Prescription Use Only" · "For single use only"

### IFU Language Matrix
| Product | Live Languages | Soon |
|---------|---------------|------|
| HyProCure I | EN, ES, DE | PT, ZH-CN, ZH-TW, TH, RO, AR, SV |
| HyProCure II | EN, ES, DE | PT, ZH-CN, ZH-TW, TH, RO, AR, SV |
| OsteoWedge | EN | Pending QA inventory confirmation |
| OptiToe | EN | Pending QA inventory confirmation |
| K-Wire | EN | Pending QA inventory confirmation |

---

## REGULATORY CONTENT CLASSIFICATION — NON-NEGOTIABLE

| Class | Definition | QA Review |
|-------|-----------|-----------|
| A — Clinical/Promotional | Any clinical claims, indications, outcomes, comparative statements, study references | MANDATORY before distribution |
| B — Educational | Medical/anatomical info, no specific device claims | Recommended |
| C — Corporate/Brand | No medical content, no device claims | Not required |

**Hard rules:**
- Never paraphrase IFU language — verbatim or omit
- Never create new clinical claims or statistics
- When in doubt, classify up (treat as Class A)
- US and international claims may differ — always specify market scope
- Flag all Class A and B outputs: **[QA REVIEW REQUIRED]**
- All Class A/B content routes to: Angela Recchia AND Tabitha Jaramillo

---

## KEY PERSONNEL

| Name | Title | Email | Phone |
|------|-------|-------|-------|
| Joe Monroe | CEO | jmonroe@gramedica.com | O +1 586-677-9600 |
| Ryan Keyes | CBO | Ryan.Keyes@GraMedica.com | O 1.888.566.6459 · C 413-530-0284 |
| Brandon Gehres | CFO | bgehres@gramedica.com | O +1 586-677-9600 |
| Kyan Flynn | Director of Global Sales | kflynn@gramedica.com | O +1 586-677-9600 |
| Sheridan Geisler | Sales Manager | sgeisler@gramedica.com | O +1 586-677-9600 · C +1 313-744-2178 |
| Christie Bolda | Operations Manager AR/AP | cbolda@gramedica.com | O +1 586-677-9600 |
| Michaeleen Bartolone | Customer Service | mbartolone@gramedica.com | O +1 586-677-9600 |
| Angela Recchia | Director QA/RA — Mgmt Representative | arecchia@gramedica.com | O +1 586-677-9600 |
| Tabitha Jaramillo | VP QA & RA (truly remote — Canada) | tjaramillo@GraMedica.com | O +1 586-677-9600 x230 · C +1 514-699-0583 |
| Jason Alquiza | VCS/Vistitude — Managed IT | — | — |

**Public-facing rule:** NEVER display personal cell numbers on any public page. Main office +1 586-677-9600 for all staff on public/website pages. Ryan's 888 line and Tabitha's x230 are signature-only.

---

## LOCKED DECISIONS

| # | Decision | Date |
|---|----------|------|
| 1 | Brand hierarchy: GraMedica (company), HyProCure (product) | — |
| 2 | Email template standard v2: blue header, #F2F4F7 footer | Mar 11, 2026 |
| 3 | Address: 236 Mill Street, Rochester MI 48307. Macomb address DEAD. | Jan 1, 2026 |
| 4 | Typography: Outfit (headings) + DM Sans (body). Fallback: Segoe UI / Arial. | Mar 2026 |
| 5 | Two-blue system: #0071CA (light BG) + #27B1FA (dark BG) | Mar 2026 |
| 6 | Digital brand language: navy #0D1B2A + #27B1FA accent | Mar 2026 |
| 7 | SkruBluGlo.png approved for dark/digital contexts | Mar 2026 |
| 8 | Premier GPO contract number: KI-OR-044 (not BT-OR-044) | Mar 2026 |
| 9 | Rep comm framing: "Your Current Commission Rates Stay in Place" — never imply reset | — |
| 10 | CRM physician registration required before first surgery — Q2 Bridge hard gate | Mar 1, 2026 |
| 11 | Everest ERP: no changes without Tabitha. EOL. ERP migration = standalone project. | Mar 12, 2026 |
| 12 | QR codes through stable redirect URLs — never directly to SharePoint | — |
| 13 | Internal distributor tier/segment sheets — never external | — |
| 14 | Microsoft-first tooling principle | — |
| 15 | Brand Central = SharePoint ONLY (never Brandfolder, Bynder, etc.) | — |
| 16 | Azure health alerts configured — routing to GRAIT@gramedica.com | Mar 12, 2026 |
| 17 | Q2 Bridge Incentive: Activation $1,000 / Reactivation $800 / Accelerator $250/area. New physician rate 35%. Supersedes prior incentive programs for Q2. | Mar 2026 |
| 18 | Base64 logo embedding = standard for internal/field/distributor audiences | Mar 2026 |

---

## PHASE 0 REMAINING DELIVERABLES

### Brand Identity System (QUEUED)
- Color palette document (formal)
- Logo usage rules document
- Photography and imagery style guide
- Brand voice and tone guide (by audience)
- Master brand guide document

### Operational Assets — Class C (QUEUED)
- Letterhead (Word)
- Business card template
- PowerPoint master template
- Email template — account reactivation (US)
- Internal document templates

### Brand Central (SharePoint) — QUEUED
- Folder structure (00–08 numbered sections)
- Access controls (Admin / Internal / Distributor / Rep tiers)
- Version control protocol (aligned with QSP 4.2-3)
- Asset categorization

---

## NO-FABRICATION RULE

Never guess or infer specific factual details (addresses, names, URLs, figures, stats) not confirmed in this file or project docs.
Insert explicit `[NEEDS CONFIRMATION]` placeholders instead.
An incomplete-but-honest deliverable is always preferable to a complete-but-fabricated one.

---

## REFERENCE BRANDS (DESIGN BENCHMARKS)

- **Arthrex** — Surgeon education, clinical credibility
- **Paragon 28** — Foot & ankle brand execution
- **Thompson Retractor** — Clinical credibility architecture
- **VALD Performance** — Modern medical device web presence

---

*Classification: Class C — Internal. No QA review required.*
*GraMedica CLAUDE.md v1.0 · March 2026*
