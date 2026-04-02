# Change Management & Version Control
# Trade Launch Intelligence Skill

## Overview

This file governs how the skill handles changes after the initial
research and document package has been produced. It answers:
- When should we amend vs. fully revise?
- How do we track what changed and why?
- How do we keep all 13 documents in sync?
- How do we avoid version chaos?

---

## The Two-Layer Change System

### Layer 1 — Amendment (for small, targeted changes)

Use an Amendment when:
- A price or market figure has been updated
- A regulation or licence fee has changed
- A new target market has been added
- A supplier has been swapped
- A financial assumption needs adjusting
- A certification status has changed (obtained / rejected / delayed)

**What to do:**
1. Identify ONLY the affected documents (not all 13)
2. Add an Amendment Note block at the top of each affected document
3. Update the specific section/table inside the document
4. Log the change in CHANGE-LOG.md (see template below)
5. Do NOT touch unaffected documents

**Amendment Note Block (paste at top of affected document):**
```
╔══════════════════════════════════════════════════════════╗
║  AMENDMENT NOTICE                                        ║
║  Date: [DD/MM/YYYY]                                      ║
║  Amended by: [Name / "Trade Launch Intelligence Skill"]  ║
║  Section changed: [Section number and title]             ║
║  Reason: [1 sentence]                                    ║
║  Previous value: [What it was]                           ║
║  New value: [What it is now]                             ║
║  Documents also updated: [List other affected docs]      ║
╚══════════════════════════════════════════════════════════╝
```

---

### Layer 2 — Full Revision (for major strategic changes)

Use a Full Revision when:
- The product itself has changed
- The country of operation has changed
- The trade direction has fundamentally shifted (e.g., local → export)
- The target market has completely changed
- The business model has changed (e.g., raw export → processing play)
- Capital available has changed significantly (e.g., 5× increase or decrease)
- More than 4 documents need substantial rewrites

**What to do:**
1. Declare the revision formally: "This is a Version [X.0] revision"
2. Create a Revision Cover Sheet (template below)
3. Re-run only the affected Phases (not all 10 phases)
4. Regenerate only the affected documents
5. Produce an updated DOC 7 (Executive Master Summary)
6. Produce an updated DOC 9 (One-Page Snapshot) — always updated on full revision
7. Log the revision in CHANGE-LOG.md
8. Keep the previous version accessible — never delete old versions

**Revision Cover Sheet (prepend to each revised document):**
```
╔══════════════════════════════════════════════════════════════╗
║  REVISION NOTICE — VERSION [X.0]                             ║
║  Document: [DOC number and title]                            ║
║  Original version date: [DD/MM/YYYY]                         ║
║  This version date: [DD/MM/YYYY]                             ║
║  Revised by: [Name / "Trade Launch Intelligence Skill"]      ║
║                                                              ║
║  WHAT CHANGED:                                               ║
║  [Bullet 1 — specific change]                                ║
║  [Bullet 2]                                                  ║
║  [Bullet 3]                                                  ║
║                                                              ║
║  WHY IT CHANGED:                                             ║
║  [1–2 sentences explaining the trigger for this revision]    ║
║                                                              ║
║  IMPACT ON OTHER DOCUMENTS:                                  ║
║  [List which other documents were also updated]              ║
╚══════════════════════════════════════════════════════════════╝
```

---

## Change Trigger Decision Tree

When a user reports a change, run this decision tree:

```
USER REPORTS A CHANGE
        │
        ▼
Does it affect the PRODUCT ITSELF?
        │
        ├─► YES ──► Does it affect more than 4 documents?
        │                   │
        │                   ├─► YES ──► FULL REVISION (v2.0)
        │                   └─► NO  ──► AMENDMENT (targeted)
        │
        └─► NO ──► Is it a PRICE / MARKET DATA update?
                        │
                        ├─► YES ──► AMENDMENT
                        │           Affects: DOC 1, DOC 3, DOC 7, DOC 9
                        │
                        └─► NO ──► Is it a REGULATORY change?
                                        │
                                        ├─► YES ──► AMENDMENT
                                        │           Affects: DOC 4, DOC 7
                                        │
                                        └─► NO ──► Is it a STRATEGY change?
                                                        │
                                                        ├─► Minor ──► AMENDMENT
                                                        │             Affects: DOC 2, DOC 8
                                                        │
                                                        └─► Major ──► FULL REVISION
```

---

## CHANGE-LOG.md Template

Every project should maintain a CHANGE-LOG.md file. When this skill
makes any amendment or revision, it must update this log.

```
# CHANGE LOG — [PRODUCT NAME] BUSINESS PACKAGE
Company: [Name] | Country: [Country]
Package created: [DD/MM/YYYY]
Last updated: [DD/MM/YYYY]

═══════════════════════════════════════════════════════════════

CHANGE #001
─────────────────────────────────────────────────────────────
Date:           [DD/MM/YYYY]
Type:           Amendment / Full Revision
Change Level:   Minor / Moderate / Major
Triggered by:   [What prompted the change]

What changed:
  - [Specific change 1]
  - [Specific change 2]

Documents updated:
  ☑ DOC [X] — [section changed]
  ☑ DOC [X] — [section changed]

Documents NOT requiring update:
  [List documents confirmed as unaffected]

Key numbers before vs. after:
  | Metric           | Before          | After           |
  |──────────────────|─────────────────|─────────────────|
  | [e.g., price]    |                 |                 |
  | [e.g., margin]   |                 |                 |

Signed off by: [User name]
─────────────────────────────────────────────────────────────

CHANGE #002
[Same structure]

═══════════════════════════════════════════════════════════════
PACKAGE VERSION HISTORY
─────────────────────────────────────────────────────────────
v1.0 — [DD/MM/YYYY] — Initial package created
v1.1 — [DD/MM/YYYY] — [Brief description of amendment]
v1.2 — [DD/MM/YYYY] — [Brief description]
v2.0 — [DD/MM/YYYY] — [Full revision — brief reason]
```

---

## Document Sync Rules

When any document is amended or revised, check these sync
dependencies before closing:

| If you change...    | Also check and update...               |
|─────────────────────|────────────────────────────────────────|
| DOC 1 (market data) | DOC 2, DOC 3, DOC 7, DOC 9, DOC 13    |
| DOC 2 (strategy)    | DOC 7, DOC 8, DOC 13                   |
| DOC 3 (financials)  | DOC 7, DOC 8, DOC 9, DOC 10, DOC 13   |
| DOC 4 (compliance)  | DOC 7, DOC 5 (if sourcing affected)    |
| DOC 5 (supply chain)| DOC 3 (if costs change), DOC 6, DOC 7  |
| DOC 6 (risk)        | DOC 7, DOC 8 (risk slide)              |
| DOC 7 (master summ) | DOC 8, DOC 9, DOC 10, DOC 11, DOC 13  |
| DOC 8 (pitch pack)  | No downstream dependencies             |
| DOC 9 (snapshot)    | No downstream dependencies             |
| DOC 10–13 (outreach)| No downstream dependencies             |

**Golden Rule:** Numbers in DOC 9–13 must ALWAYS match DOC 3 and DOC 7.
If they don't match, trust DOC 3 and update Tier 3 accordingly.

---

## What NEVER Gets Changed Without User Confirmation

The following require explicit user confirmation before any amendment:

1. **The product itself** — changing the product invalidates most of
   the research; always confirm before re-running phases
2. **Financial projections** — never adjust revenue or margin figures
   without telling the user the old vs. new numbers first
3. **The target country** — changing country invalidates regulatory,
   compliance, and sourcing sections entirely
4. **The Ask (funding amount)** — in DOC 8, DOC 9, DOC 10 — always
   user-confirmed, never auto-updated
5. **Risk rating changes** — if overall risk moves from 🟡 to 🔴,
   always surface this to the user explicitly before updating

---

## Handling Contradictory Information

Sometimes new research contradicts earlier findings. Protocol:

1. **Surface the contradiction** — tell the user clearly:
   "Our original research showed X. New data shows Y. They conflict."

2. **Explain the implication** — what does the discrepancy mean for
   the business? Does it change viability? Margins? Risk?

3. **Recommend a resolution** — which data source is more credible?
   More recent? More relevant to this specific user's context?

4. **Get user sign-off** — never silently overwrite old data with new

5. **Document it in CHANGE-LOG** — contradictions are valuable
   intelligence about market volatility

---

## Version Naming Convention

| Version | When to Use                                      |
|─────────|──────────────────────────────────────────────────|
| v1.0    | Initial package (first full research run)        |
| v1.1    | Minor amendment (1–2 documents updated)          |
| v1.2    | Another minor amendment                          |
| v1.x    | Any additional minor amendments                  |
| v2.0    | Major revision (product / country / model change)|
| v2.1    | Amendment after v2.0                             |
| v3.0    | Another major revision                           |

File naming recommendation:
`[ProductName]-[DocumentTitle]-v[X.X]-[YYYYMMDD].docx`
Example: `SheaButter-FinancialModel-v1.2-20250315.docx`

---

## Proactive Change Monitoring

The skill should proactively flag when it detects that certain
types of information may have become stale:

| Data Type               | Suggested Review Frequency  | Flag if older than |
|─────────────────────────|─────────────────────────────|────────────────────|
| Commodity price data    | Monthly                     | 30 days            |
| Exchange rate used      | Per shipment                | 14 days            |
| Regulatory fees         | Quarterly                   | 90 days            |
| Competitor landscape    | Quarterly                   | 90 days            |
| Market size / CAGR      | Annually                    | 12 months          |
| Trade agreement tariffs | Annually                    | 12 months          |
| Buyer contact details   | Quarterly                   | 90 days            |

When the skill is asked to revisit a document, it should check
the date of the original research and flag any sections that
may require a data freshness check before use.
