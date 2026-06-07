# Decoding the SpaceX IPO — A Forensic Teardown of the S-1

Companion repository to the *Alpha with AI* newsletter:
**"Claude Code Read Elon Musk's 277-Page SpaceX Prospectus So I Didn't Have To."**

This repo holds the verified, source-cited output behind every number in that edition. The newsletter tells the story. This repo is the proof. Every figure traces to an exact page in the SpaceX Form S-1 (filed May 20, 2026), or is clearly labeled as coming from outside the filing.

---

## Why this exists

A modern IPO prospectus runs hundreds of pages, most of it noise built to wear you down. The point was never to read all of it. The point is to find the five or six things that actually decide whether a business is worth owning, no matter how deep they are buried, and to never mistake the company's story for your own conviction.

The method here is not about SpaceX, and not about AI tools. SpaceX is just the hardest test case: no long track record, three businesses in one, the most famous founder alive, and a document designed to make you stop reading. The checklist below works on any company with a filing.

---

## The method

Each step is a principle. Each principle becomes one question. Each question becomes one tightly-worded prompt that forbids the tool from guessing, demands a page citation for every number, and makes it say "not disclosed" out loud when the filing is silent. The order is fixed on purpose: valuation comes last, so you never talk yourself into a price before you've checked whether the profit is real.

1. **Is the growth real?** Across years, not one good year dressed up as a trend.
2. **Does it fund itself?** Real operating cash, or dependence on outside money.
3. **Is the debt sane?** Or have the lenders quietly taken control.
4. **Is the profit real?** Does reported income show up as cash. The check that catches the frauds.
5. **Is the price sane?** Only after everything above.
6. **What changed after the filing was frozen?** The human-only check no tool can do.

The forensic middle (steps 1 to 5) was run with Claude Code reading the actual S-1, every figure re-verified on a second independent pass and saved to the files below. The judgment at the ends stays human.

---

## Files in this repo

| File | What it covers |
|------|----------------|
| `01_revenue_growth.md` | Total and segment revenue, 2023–2025, with page cites |
| `02_cash_flow.md` | Net income vs. operating cash flow, capex, free cash flow, by segment |
| `03_debt.md` | Debt, leases, net debt, maturity wall, covenants, lender control |
| `04_profit_quality.md` | Net income vs. cash from operations reconciled line by line |
| `05_valuation.md` | Share count, classes, voting control, valuation inputs |
| `06_anthropic_compute_deal.md` | The Anthropic compute agreement as disclosed in the filing, including the redacted-rate detail |
| `07_after_the_filing.md` | Facts NOT in the S-1: the June 3 IPO price and the June 5 Google deal, sourced and dated |

---

## In the filing vs. outside the filing

A core discipline of this teardown: every fact is labeled by source.

- **In the filing** → cited to an exact page of the S-1. Files 01 through 06.
- **Outside the filing** → the price (set June 3, 2026, in an amended filing) and the Google compute deal (announced June 5, 2026), both of which post-date the May 20 document. These are sourced to dated news and clearly fenced off in `07_after_the_filing.md`. They are never blended with what the document actually said.

A prospectus is a photograph frozen on its filing date. The world keeps moving. Knowing the difference is the whole job.

---

## Source

- **Primary:** Space Exploration Technologies Corp., Form S-1, filed with the SEC on May 20, 2026.
- All page citations refer to that filing.

---

## Disclaimer

This repository is for educational and informational purposes only. It is **not** investment advice, a recommendation, or a solicitation to buy or sell any security. Nothing here is a price target or a buy/sell/hold opinion.

The numbers are drawn from a single SEC filing dated May 20, 2026, and from dated public news for the clearly-labeled outside-the-filing items. Figures may be revised, restated, or superseded by later filings and events. Always verify against the original primary sources before making any decision.

The author is not a registered investment adviser or research analyst. AI tools were used to read and reconcile the filing; AI can make mistakes, and despite second-pass verification, errors may remain. Do your own research.

One disclosure specific to this analysis: Anthropic, the maker of the AI tool used for this teardown, is disclosed in the SpaceX S-1 as a major compute customer of SpaceX. That relationship is named openly in the analysis.
