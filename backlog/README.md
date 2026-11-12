# FitRight – Product Backlog

This folder contains the product backlog for **FitRight**. Each user story, epic and spike is stored as a separate Markdown file.

*Last updated: 2026-11-12 – after the [backlog review](../reports/backlog-review-2026-11-12.md) and the [PO decisions](../docs/po-decision-log.md).*

## Overview

| ID | Title | Type | Epic | Release | Priority | Story Points | Status |
|---|---|---|---|---|---|---|---|
| [FR-001](FR-001.md) | Classify free-text return reasons into fit categories | Story | – | R1 – Fit Insights | Must have | 8 | Ready |
| [FR-002](FR-002.md) | Show fit hint on the product detail page | Story | – | R1 – Fit Insights | Must have | 5 | Ready |
| [FR-003](FR-003.md) | Review and approve fit hints before publishing | Story | – | R1 – Fit Insights | Must have | 5 | Ready |
| [FR-004a](FR-004a.md) | Import supplier size charts per article | Story | – | R1 – Fit Insights | High | 5 *(placeholder)* | New |
| [FR-005](FR-005.md) | Track fit hint impact with an A/B test | Story | – | R1 – Fit Insights | Must have | 3 | Ready |
| [FR-006](FR-006.md) | Personal size recommendation for logged-in customers | Story | – | R2 – My Size | Must have | 8 | Refined |
| [FR-007](FR-007.md) | Explain the size recommendation | Story | – | R2 – My Size | Should have | 3 | Refined |
| [FR-009](FR-009.md) | Fit profile for new customers | Story | – | R2 – My Size | Should have | 5 | Refined |
| [FR-011](FR-011.md) | Consent and opt-out for personalized size recommendations | Story | – | R2 – My Size | Must have | 5 | Refined |
| [FR-008](FR-008.md) | **Expand FitRight recommendations** | **Epic** | – | R3 (first slices) | Must have | 40 *(placeholder)* | Epic |
| [FR-008a](FR-008a.md) | Personal size recommendation for menswear | Story | FR-008 | R3 – Order Right | Must have | 5 *(placeholder)* | New |
| [FR-008b](FR-008b.md) | Personal size recommendation for shoes (length only) | Story | FR-008 | R3 – Order Right | Must have | 8 *(placeholder)* | New |
| [FR-012](FR-012.md) | Warn when the same item is ordered in several sizes | Story | – | R3 – Order Right | Must have | 5 | Refined |
| [FR-013](FR-013.md) | **Return insights for Category Management** | **Epic** | – | R3 – Order Right | Should have | 21 *(placeholder)* | Epic |
| [FR-013a](FR-013a.md) | Top fit problems in my category | Story | FR-013 | R3 – Order Right | Should have | – *(to be estimated)* | New |
| [FR-014](FR-014.md) | "Did it fit?" feedback after delivery | Story | – | R3 – Order Right | Should have | 3 | Refined |
| [FR-015a](FR-015a.md) | Analyze wrong size recommendations | Spike | – | R3 | High | Time-box 3 days | New |

*Placeholder* story points are rough estimates for roadmap planning only and are re-estimated by the team in refinement (see [Definition of Ready](../docs/definition-of-ready.md)).

### Closed / replaced items

| ID | Title | Status | Successor |
|---|---|---|---|
| [FR-004](FR-004.md) | Better size data | Replaced | [FR-004a](FR-004a.md) |
| [FR-010](FR-010.md) | Smarter shopping | Closed (duplicate) | – |
| [FR-015](FR-015.md) | Improve recommendation quality | Replaced | [FR-015a](FR-015a.md) (spike); follow-up story only after the spike result |

## Status Summary

| Status | Items |
|---|---|
| **Ready** | FR-001, FR-002, FR-003, FR-005 |
| **Refined** | FR-006, FR-007, FR-009, FR-011, FR-012, FR-014 |
| **New** | FR-004a, FR-008a, FR-008b, FR-013a, FR-015a |
| **Epic** | FR-008, FR-013 |
| **Closed / Replaced** | FR-004, FR-010, FR-015 |

**R1 risk:** FR-004a is the only R1 item that is not Ready – open questions must be clarified with the data team before sprint planning.

## Epics

| Epic | Goal | Stories | Remaining scope |
|---|---|---|---|
| [FR-008 – Expand FitRight recommendations](FR-008.md) | Extend personal size recommendations to further categories and channels, prioritized by return volume | FR-008a, FR-008b | Shoe width, mobile app, kids / accessories / lingerie / sportswear, newsletter, marketplace |
| [FR-013 – Return insights for Category Management](FR-013.md) | Article-level insight into fit problems for Category Managers, usable in supplier talks | FR-013a | Export, supplier reports, FitRight impact view, alerts, delisting recommendations, mobile |

## Discovery

Solution ideas that need validation before they can become stories (body scan / AR try-on, style and weather inputs, return forecasting, competitor comparison, CO₂ impact) are kept in the [discovery backlog](discovery.md).

## Releases

- **R1 – Fit Insights:** Fit hints on the product page based on classified return reasons
- **R2 – My Size:** Personal size recommendations, fit profile and consent
- **R3 – Order Right:** Multi-size warning, fit feedback loop, insights for Category Management and expansion to menswear and shoes

See the [main README](../README.md) for vision, personas, KPIs and roadmap.

## Story Format

Stories follow the format *As a … I want … so that …* with acceptance criteria in *Given / When / Then*. Story points use the Fibonacci scale (1, 2, 3, 5, 8, 13, …). An item is pulled into a sprint only when it meets the [Definition of Ready](../docs/definition-of-ready.md).
