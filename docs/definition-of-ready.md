# FitRight – Definition of Ready (DoR)

A backlog item can only be pulled into a sprint when **all** points below are fulfilled. The checklist is based on the recommendations of the [backlog review of 2026-11-12](../reports/backlog-review-2026-11-12.md) and is also used by the weekly automated backlog quality check (see [AI Workflows](../README.md#ai-workflows)).

## Checklist for user stories

| # | Criterion | Check |
|---|---|---|
| 1 | **Format** | Written as *As a [persona/role] … I want … so that …* – with a concrete persona or role, not "user". |
| 2 | **Business value & KPI link** | The "so that" describes a clear benefit that can be linked to at least one FitRight KPI (see [Product Goal & KPIs](../README.md#product-goal--kpis)). |
| 3 | **Testable acceptance criteria** | All ACs are written in *Given / When / Then* and can be verified objectively – no wording like "better", "happy", "correct" without a measurable definition. |
| 4 | **Edge cases & fallbacks** | Exception paths are defined (e.g. no data, no consent, service not available) – every "unless" or "if" has a defined outcome. |
| 5 | **Dependencies listed** | All stories the item depends on are listed in a *Dependencies* section, and their status is known. |
| 6 | **External prerequisites available** | Everything needed from outside the team is available before sprint start, e.g. labeled test data (FR-001), DPO sign-off on consent texts (FR-011, FR-014), agreed supplier templates (FR-004a). |
| 7 | **Size** | Estimated by the team and **≤ 8 SP** (fits into one sprint). Larger items are epics and must be split. |
| 8 | **Open questions resolved** | No open questions that block implementation remain. |
| 9 | **Tracking defined** (if relevant) | Events needed to measure the KPI are part of the ACs. |

## Rules for other item types

- **Epics** are never pulled into a sprint. They hold the goal, the linked KPIs and the remaining scope; only their child stories go through this DoR.
- **Spikes** need a clear question, a time-box and a defined output (e.g. "top 3 root causes documented").
- **Solution ideas** without validated value (e.g. body scan, AR try-on) belong in the [discovery backlog](../backlog/discovery.md), not in the product backlog.

## Note on story points

Story points on items with status *New* are allowed as **rough placeholders for roadmap planning**. They must be re-estimated by the team during refinement before the item can become *Ready* (criterion 7).

## Status flow

**New** → **Refined** (story and ACs discussed with the team, gaps may remain) → **Ready** (all DoR criteria fulfilled)
