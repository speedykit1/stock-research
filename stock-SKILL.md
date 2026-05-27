---
name: stock
description: Deep-dive institutional equity research analysis. Trigger when user types /stock TICKER (e.g. /stock goog). Delivers a 6-step Citadel/BlackRock/Ares institutional analysis including macro benchmarking, valuation tables, variant thesis, supply chain forensics, catalyst verification, and whale watching. Outputs analyst price targets, upside %, and BUY/HOLD/SELL recommendation with entry/exit levels.
compatibility: Financial Datasets tool (SEC filings, metrics, insider data), web search for alternative data
---

# Institutional Equity Research: /stock Analysis

## Overview
Executes a professional 6-step equity research workflow for any public stock ticker. Combines Citadel variant views, BlackRock Aladdin macro risk profiling, and Ares structural downside protection analysis.

**Trigger:** `/stock TICKER` (case-insensitive)  
**Output:** Structured markdown report with actionable recommendation

---

## Workflow at a Glance

### Step 1: Gather Core Data
- Extract current stock price, market cap, beta
- Pull 1y/3y/5y returns vs S&P 500 and Nasdaq
- Fetch analyst consensus price targets (high/low/average)
- Calculate upside/downside from current price

### Step 2: Macro Stress Testing (BlackRock Aladdin Framework)
Test stock performance under three scenarios:
- **Sticky Inflation / High Interest Rates:** Impact on cost structure, pricing power, debt servicing
- **Global Supply Chain Disruption:** Single-sourcing risks, inventory dynamics, geographic exposure
- **Severe Economic Recession:** Demand elasticity, margin compression, cash burn profile

### Step 3: Quantitative Valuation & Operating Leverage
Build a comparison table: Target vs. top 3–4 competitors  
Columns: Trailing P/E | Forward P/E | PEG Ratio | Free Cash Flow | Operating Margin  
Analyze margin trajectory to prove/disprove operating leverage thesis.

### Step 4: Citadel Variant View & Thesis Anchor
- Identify current Wall Street consensus
- Formulate where market is **misprice** or **misinterpreting** fundamentals
- Name the specific catalyst that unlocks edge (e.g., unpriced product launch, margin inflection, hidden pricing power)

### Step 5: Supply Chain & Customer Forensics
- Map competitors by market share / market cap
- List top 5 customers; flag concentration risk (>10% revenue)
- Identify single points of failure

### Step 6: Catalysts, AI Reality Check & Whale Watching
**Catalysts:** Recent 90-day milestones from earnings calls and press releases  
**AI Hype vs. Reality:** Distinguish capex spend from actual product monetization and LLM revenue  
**Insider & Institutional:** Form 4 cluster buys, 13F positions from elite managers (Buffett, specialized tech funds, activists)  
**Crowding & Sentiment:** Short interest, retail momentum (Reddit velocity), hedge fund saturation  
**Moat & Downside:** Debt maturity schedule, net debt-to-EBITDA, liquidity runway

---

## Data Sources to Reference
1. **SEC EDGAR:** 10-K, 10-Q, proxy statements (sec.report or investor relations)
2. **Financial Datasets tool:** (for earnings, metrics, insider trades, institutional holdings, stock prices)
3. **Web search:** Recent news, earnings call transcripts, press releases
4. **Alternative data:**
   - OpenInsider.com: Form 4 insider filings
   - Dataroma / WhaleWisdom: 13F institutional positions
   - ApeWisdom or Reddit sentiment trackers for crowding risk
   - Capitol Trades: Congressional trading disclosures
   - Company IR pages: Earnings call slides, forward guidance

---

## Report Structure (Use These Exact Headers)

```
# Institutional Equity Research Report: [COMPANY NAME / TICKER]

## Executive Summary & Variant View Thesis

## 1. Macro Benchmarking & Stress-Test Scenarios

## 2. Fundamental Valuation & Operating Leverage

## 3. Citadel Variant View Analysis (Consensus vs. The Anchor)

## 4. Supply Chain & Forensic Customer Concentrations

## 5. Recent Catalysts & AI Hype-vs-Reality Verification

## 6. Alternative Data, Institutional Whales, Moat & Crowding Risk

## Investment Recommendation Summary
**Recommendation:** [BUY / HOLD / SELL]  
**Target Entry:** [Price and rationale]  
**Target Exit:** [Price and rationale]  
**Analyst Consensus Price Target:** [Average | Range: Low–High]  
**Upside/Downside:** [%] from current price  
**Risk Rating:** [Low / Medium / High]  
**Time Horizon:** [3–6 months / 6–12 months / 12+ months]
```

---

## Key Execution Notes

### Variant View (Citadel Discipline)
Do not recite analyst consensus. Surface **where the market is wrong** and why. Include:
- Specific misinterpretation of data (e.g., market assumes margin compression; you show expansion inflection)
- Unpriced catalyst (e.g., new product adoption curve not reflected in guidance)
- Timing edge (e.g., macro inflection allows re-rating)

### Operating Leverage Proof
Show incremental margin math:
```
Revenue Growth: +X%
Operating Income Growth: +Y%
→ Incremental Operating Margin = (Y - X) / Revenue Growth
```
If Y > X, margins are expanding. If Y < X, margins are contracting.

### AI Reality Check Rigor
- **Real spend:** Parse 10-Q capex by category. Separate AI infrastructure from general capex.
- **Real revenue:** Search earnings call transcripts for LLM product revenue run-rate, customer count, attach rates.
- **Marketing:** Discard "AI" mentions in press releases without revenue/capex backing.
- **Monetization timeline:** Note when product is expected to generate revenue (not just cost).

### Whale Watching Discipline
- **13F position size:** Note if it's a core position (>2% of assets) or minor tracking trade
- **Form 4 pattern:** Distinguish one-off sales (vesting) from systematic buying (conviction)
- **Activist involvement:** If applicable, note thesis and expected catalysts
- **Short interest:** Flag if >15% (potential squeeze risk) or <2% (low crowding)

### Moat & Downside Metrics
- **Leverage:** Calculate Net Debt / EBITDA. Covenant headroom?
- **Liquidity:** Cash + credit facilities vs. 12-month debt maturity. Runway quarters?
- **Beta:** How volatile is this vs. market? High beta = higher downside in recession.

---

## Best Practices
1. **Always verify current price.** Use the Financial Datasets stock_price tool to get latest market data.
2. **Link to specific sources.** If citing earnings insights, reference the date and call quarter.
3. **Call out data gaps.** If a key metric (e.g., customer concentration) is not publicly disclosed, state that explicitly.
4. **Stress test your thesis.** Ask: What would have to break my variant view? What's the bear case?
5. **Time-bound catalysts.** Specify when catalysts are expected (next earnings, product launch date, policy decision).
