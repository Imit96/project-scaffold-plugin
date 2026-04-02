# Document Visual Styling Guide — Trade Launch Intelligence
# How to produce beautiful, professional documents users are proud to share

## Design Philosophy
Every document produced by this skill must look like it was made by a
professional design agency — not a text editor. Visual quality signals
credibility before a single word is read. A potential investor or bank
officer should be visually impressed before they start reading.

## Table of Contents
1. Colour Palette & Brand System
2. Typography Rules
3. Document Structure Templates (Visual)
4. Table Styling Specifications
5. Status Indicators & Icons
6. Cover Page Templates
7. DOC 7 — HTML Dashboard Spec
8. DOC 9 — One-Page Snapshot HTML Spec
9. DOCX Generation Instructions
10. Visual Quality Checklist

---

## 1. COLOUR PALETTE & BRAND SYSTEM

### 1A — Default Palette (Option A)
Used when the user selects "Default" or gives no preference.

| Role | Name | Hex | Used For |
|---|---|---|---|
| Primary | Navy | #1B2E4B | Cover page BG, table headers, sidebar |
| Accent | Gold | #C8A951 | Divider lines, highlights, logo mark BG |
| Body | Slate | #4A5568 | Body text, secondary headings |
| Surface | Light Blue | #EBF4FF | Table alternating rows, info boxes |
| Background | Off-White | #F8F9FA | Page backgrounds |
| Base | White | #FFFFFF | Card surfaces, content areas |

---

### 1B — Custom Colour Derivation (Option B)
When the user provides a custom colour, build the full palette around it:

**Algorithm — given user's primary colour (P):**
```
Primary (P):      Use exactly as provided (or convert name → hex)
Accent:           Complementary warm tone — if P is cool/dark, use gold #C8A951
                  If P is warm, use a cool accent (e.g. #5B8DB8)
Table Header BG:  P at full opacity
Alt Row BG:       P at 8% opacity (very light tint)
Info Box BG:      P at 12% opacity
Cover Page BG:    P (full)
Cover Title:      White (#FFFFFF)
Cover Product:    Accent colour
Body Text:        #2C3E50 (always — for readability)
```

**Named colour → hex quick reference:**
| User says | Hex to use |
|---|---|
| "dark green" / "forest green" | #1A5E35 |
| "emerald" | #27AE60 |
| "royal blue" | #1F4E9E |
| "sky blue" / "light blue" | #2980B9 |
| "burgundy" / "wine red" | #7B1D2E |
| "purple" / "violet" | #6C3483 |
| "black" | #1A1A2E |
| "teal" | #0E7C7B |
| "orange" | #D35400 |
| "brown" / "chocolate" | #5D4037 |
| "red" | #C0392B |
| "grey" / "gray" | #374151 |

**Example — user says "forest green":**
```
Primary:    #1A5E35  (forest green)
Accent:     #C8A951  (gold — warm complement to cool green)
Header BG:  #1A5E35
Alt Row:    #F0F7F3  (very light green tint)
Info Box:   #E8F4ED  (light green)
Cover BG:   #1A5E35
Cover Text: White
```

---

### 1C — Suggested Palettes by Product Type (Option C)
When the user says "suggest one", auto-select based on their product:

| Product Category | Recommended Primary | Accent | Rationale |
|---|---|---|---|
| Agricultural / Agro-processing | #1A5E35 (Forest Green) | #C8A951 | Green = nature, gold = value |
| Cosmetics / Beauty / Shea | #8B3A62 (Plum/Berry) | #E8C96A | Premium, feminine, organic feel |
| Minerals / Mining / Metals | #1F3A5F (Steel Blue) | #B5B5B5 | Industrial strength, trust |
| Seafood / Marine / Fish | #0E5A7A (Ocean Blue) | #5BBCD4 | Water, freshness, purity |
| Textiles / Fashion / Leather | #2C1810 (Deep Brown) | #C8A951 | Craft, heritage, quality |
| Food / Spices / Beverages | #7B2D00 (Spice Brown) | #E67E22 | Warmth, flavour, origin |
| Technology / Digital | #1A237E (Deep Indigo) | #00BCD4 | Innovation, precision |
| Charcoal / Energy products | #1C1C1C (Charcoal) | #F39C12 | Power, energy, premium |
| Healthcare / Pharma | #155724 (Medical Green) | #2980B9 | Trust, health, safety |
| Construction / Granite | #37474F (Dark Slate) | #B0BEC5 | Strength, stability |
| Default / Unknown | #1B2E4B (Navy) | #C8A951 | Universal professional |

---

### 1D — Status Colours (Fixed — never change with brand theme)
These are semantic colours and must remain consistent regardless of brand palette:

| Status | Hex | Use |
|---|---|---|
| 🟢 Positive/Low Risk | #27AE60 | Proceed, compliant, low risk |
| 🟡 Moderate/Watch | #F39C12 | Caution, watch, moderate |
| 🔴 High Risk/Critical | #E74C3C | High risk, action required |
| ⚫ Crisis | #2C3E50 | Crisis, urgent |

---

### 1E — Document Colour Assignments
The primary brand colour becomes the cover page background for ALL documents.
Each document gets its own accent colour for section headers and dividers:

| Document | Section Accent | Use Brand Primary? |
|---|---|---|
| DOC 1 (Market Intelligence) | #2980B9 (Blue) | ✅ Cover page only |
| DOC 2 (Strategy) | #8E44AD (Purple) | ✅ Cover page only |
| DOC 3 (Financial) | #27AE60 (Green) | ✅ Cover page only |
| DOC 4 (Compliance) | #E67E22 (Orange) | ✅ Cover page only |
| DOC 5 (Supply Chain) | #16A085 (Teal) | ✅ Cover page only |
| DOC 6 (Risk) | #E74C3C (Red) | ✅ Cover page only |
| DOC 7 (Executive Summary) | Brand Accent colour | ✅ Full branding |
| DOC 8 (Pitch Pack) | Brand Accent colour | ✅ Full branding |
| DOC 9 (One-Page Snapshot) | Brand Accent colour | ✅ Full branding |
| DOC 10–13 (Outreach) | Brand Accent colour | Cover/header only |

---

### 1F — Logo Mark Generation
When the user provides brand initials (1–3 letters), render the logo mark as:

**In .docx documents:**
```
A circle or rounded square filled with Brand Accent colour
Initials centred in white, bold, sized to fit
Place top-left of every cover page and footer
```

**In HTML documents (DOC 7, DOC 9):**
```css
.logo-mark {
  width: 40px; height: 40px;
  background: var(--accent);        /* Brand accent colour */
  border-radius: 8px;
  display: flex; align-items: center; justify-content: center;
  font-weight: 900; font-size: 16px;
  color: var(--primary);            /* Brand primary for contrast */
  letter-spacing: -0.5px;
}
```

If user says "TBD" for brand name, use `TLI` (Trade Launch Intelligence) as placeholder initials.

---

## 2. TYPOGRAPHY RULES

### Fonts
- Primary font: **Arial** (universally supported in .docx)
- Monospace (for codes/data): **Courier New**
- Never use decorative fonts

### Size Scale
| Element | Size | Weight | Colour |
|---|---|---|---|
| Document title (cover) | 36pt | Bold | White on Navy |
| Section H1 | 18pt | Bold | #1B2E4B |
| Section H2 | 14pt | Bold | #2C3E50 |
| Section H3 | 12pt | Bold | #4A5568 |
| Body text | 11pt | Regular | #2C3E50 |
| Table header | 10pt | Bold | White |
| Table body | 10pt | Regular | #2C3E50 |
| Captions/footnotes | 9pt | Italic | #718096 |
| Call-out box | 11pt | Regular | #1B2E4B on #EBF4FF |

---

## 3. DOCUMENT STRUCTURE TEMPLATES (Visual)

### Every Document Must Have:
1. **Cover Page** — full navy background, white title, product name,
   company name, date, confidentiality notice, document number
2. **Table of Contents** — on page 2, auto-generated
3. **Executive Summary box** — shaded call-out at the start of the body
4. **Section dividers** — navy top border + section title + icon
5. **Footer** — page number + document title + confidentiality label
6. **Final page** — "End of Document" + contact details

### Cover Page Layout
```
┌─────────────────────────────────────────────────────┐
│  [Full navy background #1B2E4B]                     │
│                                                     │
│  [Gold horizontal line across full width]           │
│                                                     │
│  [Document type — e.g. MARKET INTELLIGENCE REPORT] │
│  [36pt, bold, white, centred]                       │
│                                                     │
│  [Product Name]                                     │
│  [28pt, gold #C8A951, centred]                      │
│                                                     │
│  [Country → Target Market]                          │
│  [16pt, white, centred]                             │
│                                                     │
│  [Gold horizontal line]                             │
│                                                     │
│  Prepared for: [Company Name]                       │
│  Date: [Date]                                       │
│  Version: [v1.0]                                    │
│  Classification: CONFIDENTIAL                       │
│  [12pt, white, left-aligned]                        │
│                                                     │
│  [Bottom: Trade Launch Intelligence badge]          │
└─────────────────────────────────────────────────────┘
```

---

## 4. TABLE STYLING SPECIFICATIONS

### Standard Data Table (for all analytical tables)
```
Header row:     Background #1B2E4B | White bold text | 10pt
Alternate rows: White | Light Blue #EBF4FF (alternate)
Borders:        Light grey #CCCCCC, 1pt
Cell padding:   Top/bottom 80 DXA | Left/right 120 DXA
Column widths:  Always set explicitly in DXA
```

### Viability Score Table (Phase 1.2)
```
Score column:   Coloured background by score:
                8–10: #27AE60 (green) | 5–7: #F39C12 (amber) | 1–4: #E74C3C (red)
Score text:     White, bold, centred
Dimension col:  Standard styling
Justification:  Italic grey text
Total row:      Navy background, white bold, gold score cell
```

### Risk Register Table (DOC 6)
```
Risk Score column:
  1–5 (Low):    #27AE60 background | white text
  6–12 (Med):   #F39C12 background | white text
  15–25 (High): #E74C3C background | white text
Row highlighting: High risks get full row #FFF5F5 background
```

### Financial Tables (DOC 3)
```
Revenue rows:         #EBF4FF (light blue) background
COGS rows:            #FFF9E6 (light gold) background
Profit rows:          #EFF7EF (light green) background
Negative numbers:     #E74C3C (red) colour
Total/subtotal rows:  Bold, slightly darker background
```

### Compliance Checklist Tables (DOC 4)
```
✅ Complete:    #EFF7EF background | #27AE60 text
⚠️ In Progress: #FFF9E6 background | #F39C12 text
❌ Not Started: #FFF5F5 background | #E74C3C text
```

---

## 5. STATUS INDICATORS & ICONS

### Traffic Light Badges (use in tables and summaries)
Render as coloured cell/text rather than emoji for docx:
- 🟢 HIGH / LOW RISK / PROCEED → Green box: background #27AE60, text white, bold
- 🟡 MODERATE / WATCH → Amber box: background #F39C12, text white, bold
- 🔴 LOW / HIGH RISK / CAUTION → Red box: background #E74C3C, text white, bold

### Section Icons (use text symbols in docx — no image dependencies)
| Section | Icon prefix |
|---|---|
| Executive Summary | ◆ |
| Market Intelligence | ◉ |
| Strategy | ▲ |
| Financial | ₿ (or $) |
| Compliance | ✓ |
| Supply Chain | ⬡ |
| Risk | ⚑ |
| Action Plan | → |

### Call-out Boxes
Three types — render as shaded paragraphs with left border:
```
💡 INSIGHT BOX:    Left border #2980B9 (4pt) | Background #EBF4FF
⚠️  WARNING BOX:   Left border #F39C12 (4pt) | Background #FFF9E6
🔴 CRITICAL BOX:   Left border #E74C3C (4pt) | Background #FFF5F5
```

---

## 6. COVER PAGE TEMPLATES — DOCX JAVASCRIPT

Before generating, inject the brand variables from the User Context Profile:

```javascript
// Brand variables — replace with actual values from User Context Profile
const BRAND = {
  companyName:  "[COMPANY NAME]",       // from Phase 0B
  logoMark:     "[AEG]",                // 1–3 initials from Phase 0B
  primaryColor: "1B2E4B",              // hex without # — from Phase 0B brand profile
  accentColor:  "C8A951",              // hex without # — from Phase 0B brand profile
  altRowColor:  "F0F4F8",              // derived: primary at ~8% opacity on white
  productName:  "[PRODUCT NAME]",      // from User Context Profile
  origin:       "[ORIGIN COUNTRY]",    // from User Context Profile
  target:       "[TARGET MARKET]",     // from User Context Profile
  docType:      "[DOCUMENT TYPE]",     // e.g. "MARKET INTELLIGENCE REPORT"
  date:         "[DATE]",
  version:      "v1.0",
};

// Cover Page — DOCX.js implementation
const coverPage = {
  properties: {
    page: {
      size: { width: 12240, height: 15840 },
      margin: { top: 0, right: 0, bottom: 0, left: 0 }
    }
  },
  children: [
    // Logo mark block (top-left)
    new Paragraph({
      shading: { fill: BRAND.primaryColor, type: ShadingType.CLEAR },
      spacing: { before: 1440, after: 0 },
      indent: { left: 720 },
      children: [
        new TextRun({
          text: `  ${BRAND.logoMark}  `,
          font: "Arial", size: 28, bold: true,
          color: BRAND.primaryColor,
          shading: { fill: BRAND.accentColor, type: ShadingType.CLEAR }
        }),
        new TextRun({
          text: `   ${BRAND.companyName}`,
          font: "Arial", size: 22, bold: false, color: "AAAAAA"
        })
      ]
    }),
    // Gold divider line
    new Paragraph({
      border: { bottom: { style: BorderStyle.SINGLE, size: 12, color: BRAND.accentColor } },
      shading: { fill: BRAND.primaryColor, type: ShadingType.CLEAR },
      spacing: { before: 720, after: 0 },
      children: [new TextRun({ text: " ", color: BRAND.primaryColor })]
    }),
    // Document type
    new Paragraph({
      alignment: AlignmentType.CENTER,
      shading: { fill: BRAND.primaryColor, type: ShadingType.CLEAR },
      spacing: { before: 480, after: 160 },
      children: [
        new TextRun({
          text: BRAND.docType,
          font: "Arial", size: 24, bold: true,
          color: "FFFFFF", allCaps: true, characterSpacing: 80
        })
      ]
    }),
    // Product name (accent colour)
    new Paragraph({
      alignment: AlignmentType.CENTER,
      shading: { fill: BRAND.primaryColor, type: ShadingType.CLEAR },
      spacing: { before: 160, after: 320 },
      children: [
        new TextRun({
          text: BRAND.productName,
          font: "Arial", size: 52, bold: true, color: BRAND.accentColor
        })
      ]
    }),
    // Trade route
    new Paragraph({
      alignment: AlignmentType.CENTER,
      shading: { fill: BRAND.primaryColor, type: ShadingType.CLEAR },
      spacing: { before: 0, after: 720 },
      children: [
        new TextRun({
          text: `${BRAND.origin}  →  ${BRAND.target}`,
          font: "Arial", size: 22, color: "AAAAAA"
        })
      ]
    }),
    // Second divider
    new Paragraph({
      border: { bottom: { style: BorderStyle.SINGLE, size: 12, color: BRAND.accentColor } },
      shading: { fill: BRAND.primaryColor, type: ShadingType.CLEAR },
      children: [new TextRun({ text: " ", color: BRAND.primaryColor })]
    }),
    // Meta info
    new Paragraph({
      shading: { fill: BRAND.primaryColor, type: ShadingType.CLEAR },
      spacing: { before: 400, after: 100 },
      indent: { left: 720 },
      children: [
        new TextRun({ text: "Prepared for:  ", font: "Arial", size: 20, color: "AAAAAA" }),
        new TextRun({ text: BRAND.companyName, font: "Arial", size: 20, bold: true, color: "FFFFFF" })
      ]
    }),
    new Paragraph({
      shading: { fill: BRAND.primaryColor, type: ShadingType.CLEAR },
      spacing: { before: 80, after: 80 },
      indent: { left: 720 },
      children: [
        new TextRun({ text: "Date:              ", font: "Arial", size: 20, color: "AAAAAA" }),
        new TextRun({ text: BRAND.date, font: "Arial", size: 20, color: "FFFFFF" })
      ]
    }),
    new Paragraph({
      shading: { fill: BRAND.primaryColor, type: ShadingType.CLEAR },
      spacing: { before: 80, after: 80 },
      indent: { left: 720 },
      children: [
        new TextRun({ text: "Version:          ", font: "Arial", size: 20, color: "AAAAAA" }),
        new TextRun({ text: BRAND.version, font: "Arial", size: 20, color: "FFFFFF" })
      ]
    }),
    new Paragraph({
      shading: { fill: BRAND.primaryColor, type: ShadingType.CLEAR },
      spacing: { before: 80, after: 80 },
      indent: { left: 720 },
      children: [
        new TextRun({ text: "Classification:  ", font: "Arial", size: 20, color: "AAAAAA" }),
        new TextRun({ text: "CONFIDENTIAL", font: "Arial", size: 20, bold: true, color: "E74C3C" })
      ]
    }),
    new PageBreak()
  ]
};
```

---

## 7. DOC 7 — EXECUTIVE DASHBOARD HTML SPEC

DOC 7 should be produced as a **single self-contained HTML file** — not a .docx.
It renders in any browser, can be emailed, and looks dramatically better than Word.

### Visual Structure
```
┌─────────────────────────────────────────────────────────┐
│  HEADER BAR (navy)                                      │
│  [Company Logo placeholder] | [Product Name] | [Date]  │
│  EXECUTIVE MASTER SUMMARY — INTERNAL USE ONLY          │
├────────────┬────────────────────────────────────────────┤
│  LEFT      │  MAIN DASHBOARD                           │
│  SIDEBAR   │                                           │
│  (navy)    │  ┌──────┬──────┬──────┬──────┐           │
│            │  │SCORE │MKTSIZE│MARGIN│PAYBACK│          │
│  Navigation│  │70/100│$2.4B │ 42%  │ 8 mo │           │
│  anchors   │  └──────┴──────┴──────┴──────┘           │
│  to each   │                                           │
│  section   │  ┌──────────────┬──────────────┐         │
│            │  │ MARKET       │ STRATEGY     │         │
│  • Market  │  │ 🟢 High      │ ▲ Option B   │         │
│  • Strategy│  │ demand       │ Export first │         │
│  • Finance │  └──────────────┴──────────────┘         │
│  • Comply  │                                           │
│  • Supply  │  ┌──────────────┬──────────────┐         │
│  • Risk    │  │ COMPLIANCE   │ RISK         │         │
│  • Actions │  │ 🟡 Medium    │ 🟡 Medium    │         │
│            │  │ 6 weeks      │ 3 high risks │         │
│            │  └──────────────┴──────────────┘         │
│            │                                           │
│            │  3-YEAR REVENUE CHART (CSS bar chart)    │
│            │  ████████ Y1: $XXK                       │
│            │  ████████████ Y2: $XXXK                  │
│            │  ███████████████████ Y3: $XXXK           │
│            │                                           │
│            │  TOP 10 ACTIONS TABLE                    │
│            │  VERDICT BADGE (PROCEED / CAUTION / NO)  │
└────────────┴────────────────────────────────────────────┘
│  FOOTER: Confidential | Generated by Trade Launch Intelligence │
└─────────────────────────────────────────────────────────────────┘
```

### HTML Generation Instructions
When generating DOC 7 and DOC 9, Claude must produce a **single .html file** with:
- All CSS embedded in `<style>` tags (no external dependencies)
- No JavaScript libraries (pure CSS for charts and interactions)
- Responsive layout using CSS Grid
- All data values injected directly as text (no API calls)
- Print stylesheet included (`@media print`)
- Self-contained — opens by double-clicking the file

### Brand Variables — Inject into :root from User Context Profile
```css
:root {
  /* ── BRAND (from User Context Profile — Phase 0B) ── */
  --primary:    #[Brand Primary Colour];   /* e.g. #1B2E4B for default navy */
  --accent:     #[Brand Accent Colour];    /* e.g. #C8A951 for default gold */
  --logo-mark:  "[Logo Initials]";         /* e.g. "AEG" — used in ::before pseudo */

  /* ── DERIVED FROM PRIMARY ── */
  --primary-light: [primary at 90% lightness];  /* for alternating rows */
  --primary-surface: [primary at 95% lightness]; /* for info boxes */

  /* ── FIXED SYSTEM COLOURS (never change with brand) ── */
  --green:      #27AE60;
  --amber:      #F39C12;
  --red:        #E74C3C;
  --text:       #2C3E50;
  --text-light: #718096;
  --border:     #E2E8F0;
  --white:      #FFFFFF;
  --off-white:  #F8F9FA;
}
```

**Practical derivation rules:**
- `--primary-light`: If primary is dark (lightness < 40%), use `F0F4F8` for navy, or lighten primary by mixing 92% white
- `--primary-surface`: Mix 96% white + 4% primary — gives a very subtle tint for info boxes

---

## 8. DOC 9 — ONE-PAGE SNAPSHOT HTML SPEC

Also produced as HTML (single file, print-ready A4).

```
┌─────────────────────────────────────────────────────┐  A4 PAGE
│ ┌──────────────────────────────────────────────────┐│
│ │ [NAVY HEADER]  [COMPANY NAME]    [Date]          ││
│ │ [PRODUCT NAME] — Business Snapshot              ││
│ └──────────────────────────────────────────────────┘│
│ ┌──────────────────┐ ┌────────────────────────────┐ │
│ │ [PRODUCT IMAGE   │ │ THE OPPORTUNITY            │ │
│ │  PLACEHOLDER]    │ │ ─────────────────────────  │ │
│ │ or product icon  │ │ [2-sentence opportunity    │ │
│ │                  │ │  statement]                │ │
│ └──────────────────┘ └────────────────────────────┘ │
│ ┌───────────┬──────────────┬────────────────────────┐│
│ │ STARTUP   │ GROSS MARGIN │ PAYBACK PERIOD         ││
│ │ $X,XXX    │    XX%       │   X months             ││
│ └───────────┴──────────────┴────────────────────────┘│
│ ┌───────────┬──────────────┬────────────────────────┐│
│ │ Y1 REV    │ Y3 REVENUE   │ 3-YEAR ROI             ││
│ │ $XX,XXX   │  $XXX,XXX    │   XXX%                 ││
│ └───────────┴──────────────┴────────────────────────┘│
│ ┌──────────────────────────────────────────────────┐ │
│ │ WHAT WE DO (1 sentence)                          │ │
│ └──────────────────────────────────────────────────┘ │
│ ┌──────────────────┐ ┌────────────────────────────┐ │
│ │ WHY US           │ │ CERTIFICATIONS             │ │
│ │ • [Point 1]      │ │ ✅ [Cert 1]                │ │
│ │ • [Point 2]      │ │ ✅ [Cert 2]                │ │
│ │ • [Point 3]      │ │ 🔄 [In progress]           │ │
│ └──────────────────┘ └────────────────────────────┘ │
│ ┌──────────────────────────────────────────────────┐ │
│ │ THE ASK (1 sentence — specific, actionable)      │ │
│ └──────────────────────────────────────────────────┘ │
│ ┌──────────────────────────────────────────────────┐ │
│ │ [Name] | [Email] | [WhatsApp] | [Website]        │ │
│ │ [City, Country]  Full docs available on request  │ │
│ └──────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────┘
```

Print-ready at A4. All data pulled from DOC 7.

---

## 9. DOCX GENERATION INSTRUCTIONS

When generating .docx documents (DOC 1–6, DOC 8, DOC 10–13):

### Step 1 — Install docx
```bash
npm install -g docx
```

### Step 2 — Follow docx SKILL.md rules exactly
Read `/mnt/skills/public/docx/SKILL.md` for all critical rules:
- Set page size explicitly (US Letter: 12240 × 15840 DXA)
- Never use unicode bullets — use LevelFormat.BULLET
- Tables need dual widths (columnWidths + cell width)
- Use ShadingType.CLEAR not SOLID
- Never use \n — use separate Paragraph elements

### Step 3 — Apply this skill's styling
Use the colour palette from Section 1.
Apply cover page from Section 6.
Apply table styles from Section 4.

### Step 4 — Validate
```bash
python scripts/office/validate.py document.docx
```

### Step 5 — Deliver to outputs
```bash
cp document.docx /mnt/user-data/outputs/
```

---

## 10. VISUAL QUALITY CHECKLIST

Before delivering any document, verify:

### .docx Documents
- [ ] Cover page present with navy background and gold accents
- [ ] Table of contents on page 2
- [ ] All headings use style hierarchy (H1/H2/H3)
- [ ] All tables have coloured headers (navy/white)
- [ ] Alternating row colours applied
- [ ] Score/status cells colour-coded (green/amber/red)
- [ ] Call-out boxes used for key insights and warnings
- [ ] Footer shows page number + document title
- [ ] No unicode bullet characters (use LevelFormat.BULLET)
- [ ] All numbers formatted with commas and currency symbols
- [ ] At least one visual element per major section

### HTML Documents (DOC 7, DOC 9)
- [ ] Fully self-contained (no external CSS/JS dependencies)
- [ ] Opens and renders correctly in browser by double-click
- [ ] All CSS variables defined in :root
- [ ] Print stylesheet included
- [ ] Metric cards display prominently above the fold
- [ ] Traffic light ratings shown as coloured badges (not text)
- [ ] Revenue chart rendered as CSS bars (no JS charting lib)
- [ ] Mobile-responsive layout

### All Documents
- [ ] No lorem ipsum or unfilled placeholders [like this]
- [ ] All numbers consistent with DOC 3 (Financial Model)
- [ ] User's local currency AND USD shown throughout
- [ ] Company name, country, date on every page
- [ ] "CONFIDENTIAL" label on every page
