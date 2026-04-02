# Financial Model Reference — Trade Launch Intelligence (Global)

## How to Use This File
This file provides globally-applicable financial modelling frameworks.
All currency symbols shown as [LOCAL] should be replaced with the
user's local currency at runtime. All Nigerian-specific examples are
labelled as such — use them as a structural template only, substituting
the user's actual country costs from web search and Phase 6 research.

## Table of Contents
1. Startup Cost Categories (Universal Framework)
2. Unit Economics Formula
3. Revenue Projection Model
4. ROI & Payback Calculator
5. Country-Specific Cost Factors (How to Derive Them)
6. Sensitivity Analysis Framework
7. Break-Even Formula + Example
8. Funding Structure Guide

---

## 1. Startup Cost Categories

Universal framework — fill in actual figures from country research.
Show all amounts in local currency AND USD equivalent.

### Category A — Legal & Compliance
| Item | Min [LOCAL] | Max [LOCAL] | USD Range | Notes |
|---|---|---|---|---|
| Business registration | | | $5–$200 | Varies widely by country |
| Tax ID / VAT registration | | | Usually free | |
| Export/import agency reg. | | | $30–$300 | |
| Product safety certification | | | $50–$2,000 | Food/cosmetics/manufactured |
| Standards certification | | | $50–$500 | Quality body — country-specific |
| Phytosanitary (if agro) | | | $20–$100/shipment | Per consignment |
| Halal certification | | | $200–$600 | For Muslim-majority markets |
| Legal / solicitor fees | | | $50–$500 | Contracts, compliance |
| **Subtotal A** | | | | |

### Category B — Infrastructure & Equipment
| Item | Min [LOCAL] | Max [LOCAL] | USD Range | Notes |
|---|---|---|---|---|
| Warehouse rent (3 months) | | | $150–$5,000 | Location/size dependent |
| Processing equipment | | | $200–$20,000 | Product-dependent |
| Packaging machinery | | | $100–$5,000 | If applicable |
| Storage infrastructure | | | $100–$2,000 | Pallets, racks, cold storage |
| Power / backup power | | | $100–$3,000 | Critical in many markets |
| Safety & fire equipment | | | $50–$500 | |
| **Subtotal B** | | | | |

### Category C — Inventory & Sourcing
| Item | Min [LOCAL] | Max [LOCAL] | USD Range | Notes |
|---|---|---|---|---|
| First inventory purchase | | | $500–$50,000 | Scale-dependent |
| Transportation to warehouse | | | $50–$1,000 | |
| Quality testing at source | | | $50–$500 | Accredited lab |
| Supplier deposit / advance | | | $100–$5,000 | Negotiated (max 30%) |
| **Subtotal C** | | | | |

### Category D — Marketing & Sales
| Item | Min [LOCAL] | Max [LOCAL] | USD Range | Notes |
|---|---|---|---|---|
| Brand identity (logo, design) | | | $30–$500 | |
| Packaging design & printing | | | $100–$2,000 | |
| Website + professional email | | | $50–$500 | See digital-presence.md |
| B2B portal subscriptions | | | $0–$500 | Free tiers first |
| Trade fair participation | | | $200–$3,000 | |
| Product samples for buyers | | | $50–$500 | |
| **Subtotal D** | | | | |

### Category E — Working Capital (3 months)
| Item | Min [LOCAL] | Max [LOCAL] | USD Range | Notes |
|---|---|---|---|---|
| Staff salaries (3 months) | | | $200–$5,000 | |
| Utilities (3 months) | | | $100–$800 | |
| Transport / logistics ops | | | $100–$2,000 | |
| Miscellaneous operational | | | $100–$500 | |
| **Subtotal E** | | | | |

### Category F — Contingency Buffer
Apply **10%** of total (A+B+C+D+E) as contingency. Non-negotiable.

---

**TOTAL STARTUP CAPITAL:**
[LOCAL CURRENCY] ________ / USD ________

**Funding Gap (if any):** [Total needed] − [Available capital] = [Gap]
→ See `funding-directory.md` for country-specific funding options.

---

## 2. Unit Economics Formula

```
ALL-IN COST PER UNIT:
= Purchase/farmgate price
+ Processing cost
+ Packaging cost
+ Local transport to warehouse
+ Export documentation cost (÷ total units per shipment)
+ Freight cost (÷ total units per shipment)
+ Cargo insurance (÷ total units per shipment)
+ Pre-shipment inspection (÷ total units per shipment)
+ Port / border fees (÷ total units per shipment)
+ Banking / FX charges (÷ total units per shipment)
─────────────────────────────────────────────────────
= TOTAL COST PER UNIT

GROSS MARGIN PER UNIT = Selling price − Total cost per unit
GROSS MARGIN %        = (Gross margin ÷ Selling price) × 100
CONTRIBUTION MARGIN   = Gross margin − Variable selling costs

BREAK-EVEN UNITS      = Total Fixed Costs ÷ Contribution margin/unit
BREAK-EVEN REVENUE    = Break-even units × Selling price
```

### Target Gross Margin Benchmarks by Category
| Category | Minimum | Good | Excellent |
|---|---|---|---|
| Raw agro commodity | 15% | 25% | 40%+ |
| Processed agro | 25% | 40% | 60%+ |
| Solid minerals | 20% | 35% | 55%+ |
| Cosmetics / personal care | 40% | 60% | 80%+ |
| Manufactured goods | 20% | 35% | 50%+ |
| Fashion / textiles | 30% | 50% | 70%+ |
| Imported goods (resale) | 15% | 25% | 40%+ |

---

## 3. Revenue Projection Model

### Key Assumptions Template
Document every assumption before building the model.
Undocumented assumptions are the #1 cause of projection disputes with investors.

```
YEAR 1 ASSUMPTIONS
─────────────────────────────────────────────────────
Months of operation (Year 1):         [e.g., 10 of 12 — 2 months setup]
Volume per shipment:                  [X tons / units]
Shipments per year:                   [X]
Total volume Year 1:                  [X tons / units]
Selling price (local):                [LOCAL] X per unit
Selling price (export FOB):           $X per unit
Local vs. export split:               [X]% local / [X]% export
FX rate used:                         1 USD = [X LOCAL] (date: __)
COGS as % of revenue:                 [X]%

YEAR 2 ASSUMPTIONS
─────────────────────────────────────────────────────
Volume growth vs Year 1:              +[X]% (conservative: 30–50%)
Price adjustment:                     +[X]% (inflation / value-add)
COGS efficiency gain:                 −[X]% (economies of scale)

YEAR 3 ASSUMPTIONS
─────────────────────────────────────────────────────
Volume growth vs Year 2:              +[X]%
New markets / product lines:          [Yes/No — describe]
```

### 3-Year Income Statement Template

| Line Item | Year 1 | Year 2 | Year 3 |
|---|---|---|---|
| Volume sold | | | |
| Revenue (local currency) | | | |
| Revenue (USD) | | | |
| Returns / Rejections (2%) | | | |
| **NET REVENUE** | | | |
| Raw material / procurement | | | |
| Processing & packaging | | | |
| Logistics / freight | | | |
| Export docs & inspection | | | |
| **TOTAL COGS** | | | |
| **GROSS PROFIT** | | | |
| **Gross Margin %** | | | |
| Staff salaries | | | |
| Rent / warehouse | | | |
| Utilities & power | | | |
| Marketing & trade fairs | | | |
| Bank charges & FX costs | | | |
| Professional fees | | | |
| Depreciation | | | |
| **TOTAL OPEX** | | | |
| **EBITDA** | | | |
| Corporate tax ([X]% — per country) | | | |
| **NET PROFIT** | | | |
| **Net Margin %** | | | |

---

## 4. ROI & Payback Calculator

```
SIMPLE ROI (Year 1):
= (Net Profit Year 1 ÷ Total Investment) × 100

3-YEAR CUMULATIVE ROI:
= ((Net Profit Y1 + Y2 + Y3) ÷ Total Investment) × 100

PAYBACK PERIOD:
= Total Investment ÷ Average Monthly Net Profit (Year 1)
= X months

IRR BENCHMARK (global SME standards):
> 30% = Attractive
> 50% = Excellent
< 20% = Marginal — reconsider or reduce costs
```

---

## 5. Country-Specific Cost Factors

Unlike the rest of this file, country costs CANNOT be pre-filled —
they vary too much. Use this framework to research and fill them in.

### Universal Cost Items (present in every country)
| Cost Item | Typical Rate | How to Find It |
|---|---|---|
| Export/import agency levy | 0.25–1% of FOB | Country's customs authority |
| Bank LC charges | 1–3% of LC value | Your business bank |
| TT bank transfer fees | 0.5–2% per transfer | Your business bank |
| Marine / cargo insurance | 0.5–1.5% of CIF | Insurance broker |
| Pre-shipment inspection | 0.75–1.5% of cargo value | SGS / Bureau Veritas / Cotecna |
| Port terminal handling (THC) | $80–$250/TEU | Port authority / freight forwarder |
| Freight forwarder fee | $100–$500/shipment | Get 3 quotes |
| FX volatility buffer | 3–10% of forex income | Based on currency stability |

### How to Find Country-Specific Costs
1. Search: "[country] export levy rate [current year]"
2. Search: "[country] port terminal handling charges"
3. Search: "[country] business registration cost [current year]"
4. Call your country's export promotion agency — they have fee schedules
5. Ask a licensed freight forwarder for a full cost breakdown quote

### Cost Factors to Never Miss
- Power / generator costs — critical in countries with unreliable power
- Road transport informals — tolls, levies, unofficial charges on routes
- Broker / middleman commissions at source markets (1–5%)
- Cold chain costs (if product is perishable)
- Port demurrage risk — budget for 2–3 days of potential delays

---

## 6. Sensitivity Analysis Framework

Run THREE scenarios for every financial model.
Present all three to investors and banks — transparency builds credibility.

| Metric | Conservative (Bear) | Base Case | Optimistic (Bull) |
|---|---|---|---|
| Volume | 60% of target | 100% | 130% |
| Selling price | −10% | As projected | +10% |
| Total costs | +15% | As estimated | −5% |
| FX rate impact | −15% on forex | Stable | Stable |
| Year 1 Revenue | | | |
| Year 1 Net Profit | | | |
| Year 1 Margin % | | | |
| Payback Period | | | |

**The Golden Rule:**
If the CONSERVATIVE scenario is still EBITDA-positive, the business
model is structurally sound. If not — reduce costs or increase price
before committing capital.

---

## 7. Break-Even Formula + Example

### Generic Formula
```
Monthly Fixed Costs:
  Warehouse/rent:        [X]
  Staff salaries:        [X]
  Utilities:             [X]
  Loan repayments:       [X]
  Other fixed overhead:  [X]
  ─────────────────────
  TOTAL FIXED COSTS:     [X] per month

Contribution Margin per unit:
  = Selling price per unit − Variable cost per unit

Break-even Volume:
  = Total Fixed Costs ÷ Contribution Margin per unit

Break-even Revenue:
  = Break-even volume × Selling price per unit
```

### Example (Cashew Nuts — Nigeria — for structural reference only)
```
Monthly Fixed Costs: ~$600/month (₦950,000 at ₦1,580/USD)
  - Warehouse: $315 | Staff: $190 | Utilities: $95

Variable Cost per ton: ~$595/ton
  - Farmgate: $505 | Processing: $32 | Packaging: $19 | Transport: $25 | Docs: $13

Selling Price (FOB): $822/ton

Contribution Margin: $822 − $595 = $227/ton
Break-even Volume: $600 ÷ $227 = 2.64 tons/month
Break-even Revenue: 2.64 × $822 = $2,170/month

→ Apply this exact structure using the user's local costs and prices.
```

---

## 8. Funding Structure Guide

→ For detailed country-specific funding sources, read `funding-directory.md`.

### Quick Funding Type Selector
| Business Stage | Best Funding Type | Why |
|---|---|---|
| Pre-launch, no revenue | Grant / TEF / angel | No repayment pressure |
| First inventory | Trade finance / working capital | Short-term, self-liquidating |
| Equipment purchase | Term loan / equipment finance | Matched to asset life |
| Export growth | EXIM bank / export credit | Designed for this purpose |
| Scaling to new markets | Equity / strategic partner | Capital + network |
| Managing buyer risk | Trade credit insurance | Protects revenue |

### Universal Trade Finance Products
- **Invoice discounting:** Bank advances 70–80% of confirmed invoice value
- **Warehouse receipt finance:** Use certified inventory as loan collateral
- **Letter of Credit:** Buyer's bank guarantees payment upon document compliance
- **Pre-shipment finance:** Bank finances sourcing costs against confirmed export order
- **Export credit guarantee:** Government body guarantees your bank loan to reduce collateral

### Funding Sequencing Strategy
Start with **grants** (no repayment) → then **concessionary government loans** (low rate)
→ then **development bank finance** → then **commercial bank** (market rate).
Layering these three is a common successful structure for SME exporters.

**The single most powerful action before any loan application:**
Open a dedicated business bank account and keep it active with regular
transactions for 6+ months. Bank statements are the primary risk signal
for every lender — in every country.
