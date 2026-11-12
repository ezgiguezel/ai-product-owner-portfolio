# FitRight – PO Decision Log

This log documents my decisions as Product Owner on the recommendations of the automated backlog quality check.
Principle: **AI suggests, the PO decides.** Every recommendation is reviewed; only accepted changes are applied to the backlog.

## Review of 2026-11-12

**Source:** [Backlog review report 2026-11-12](../reports/backlog-review-2026-11-12.md) · **Decided on:** 2026-11-12 · **Decided by:** Product Owner

### Decisions

| # | Item | Recommendation from the report | Decision | Reason |
|---|---|---|---|---|
| 1 | FR-004 | Clarify "better size data" with the data team, split into (a) supplier size chart import and (b) cleanup of existing data; proposal FR-004a | **Partly** | FR-004 replaced by [FR-004a](../backlog/FR-004a.md) (import supplier size charts), kept in R1 because recommendations and fit hints depend on reliable size data. The cleanup slice (b) is not created now – the scope will be clarified with the data team together with the open questions of FR-004a. |
| 2 | FR-005 | Add hypothesis, primary/guardrail metric, minimum sample size; make AC3 testable; exclude non-consenting visitors from the analysis; re-estimate 3 SP | **Accepted** | Without a hypothesis and success metric the team cannot decide when the test is successful. Changes applied to [FR-005](../backlog/FR-005.md); re-estimation is left to the team in refinement. |
| 3 | FR-006 | Define the outcome of the AC2 exception (fit hint "runs large"); add a fallback AC for customers with insufficient data or no consent; consider splitting if re-estimated > 8 SP | **Accepted** | The fallback is part of the R2 roadmap and every exception needs a defined outcome. AC2, AC2b and AC5 applied to [FR-006](../backlog/FR-006.md); missing dependencies FR-002 / FR-009 added. |
| 4 | FR-007 | Add missing dependencies FR-006 and FR-009 | **Accepted** | Dependencies must be visible for sprint planning. Added to [FR-007](../backlog/FR-007.md). |
| 5 | FR-008 | Convert into the epic "Expand FitRight recommendations", split by category and channel (FR-008a–e), move body scan / AR and style / weather to discovery, remove story points | **Partly** | Epic created ([FR-008](../backlog/FR-008.md)) with only two stories for now: [FR-008a](../backlog/FR-008a.md) (menswear) and [FR-008b](../backlog/FR-008b.md) (shoes, length only) – the next slices with the highest return volume. Shoe width, app and further categories stay as remaining scope in the epic. Body scan / AR and style / weather moved to [discovery](../backlog/discovery.md). Story points are kept (see #14). |
| 6 | FR-009 | Add missing dependency FR-011 | **Accepted** | Storing body data requires explicit consent (AC4). Added to [FR-009](../backlog/FR-009.md). |
| 7 | FR-010 | Close as duplicate | **Accepted** | Already covered by the product vision and FR-002, FR-006, FR-008, FR-012. [FR-010](../backlog/FR-010.md) closed. |
| 8 | FR-010 | Alternatively add a new story "Show the article's size chart in my body measurements" | **Rejected** | Does not support our product goal (reducing returns) strongly enough for now. |
| 9 | FR-012 | Define the case "no personal recommendation and no fit hint"; add tracking for the KPI "multi-size orders"; list dependencies FR-002 / FR-006 | **Accepted** | Closes an undefined edge case and makes the KPI measurable. AC4, AC6, AC7 and dependencies applied to [FR-012](../backlog/FR-012.md). |
| 10 | FR-013 | Convert into the epic "Return insights for Category Management" with first slice FR-013a; move forecasting, delisting recommendations, competitor comparison and CO₂ to discovery | **Partly** | Epic created ([FR-013](../backlog/FR-013.md)) with [FR-013a](../backlog/FR-013a.md) (top fit problems in my category) – this addresses Markus' core need. Forecasting, competitor comparison and CO₂ moved to [discovery](../backlog/discovery.md). Delisting recommendations stay in the epic's remaining scope for now. |
| 11 | FR-015 | Split into a time-boxed spike FR-015a and an improvement story FR-015b | **Partly** | FR-015 replaced by the spike [FR-015a](../backlog/FR-015a.md) (time-box 3 days). FR-015b is **not** created yet – its segment, baseline and target depend on the spike result. |
| 12 | Top 3 – #3 | Introduce a Definition-of-Ready checklist (format, testable ACs, dependencies listed, ≤ 8 SP, KPI link, external prerequisites) | **Accepted** | Prevents most of the issues found in this review. Created as [Definition of Ready](definition-of-ready.md). |
| 13 | Top 3 – #3 | Make external prerequisites explicit DoR items (labeled test set for FR-001, DPO sign-off on consent texts for FR-011 and FR-014) | **Accepted** | Included as a general criterion in the [Definition of Ready](definition-of-ready.md) (criterion 6). The individual stories are not changed. |
| 14 | General / Top 3 – #1 | Remove story points from un-refined stories (status *New*) | **Rejected** | The team uses these estimates as rough placeholders for roadmap planning. They are marked as placeholders and must be re-estimated before an item becomes *Ready* (see DoR). |
| 15 | Top 3 – #2 | Resolve FR-004 first because it is an R1 risk; invite the data team | **Accepted** | FR-004a is the only R1 item that is not Ready – the open questions will be clarified with the data team before the next sprint planning. |

### Open points – not decided in this round

The report also listed minor gaps in Ready stories. They were **not** changed in this round and will be discussed in the next refinement meeting:

| Item | Point from the report |
|---|---|
| FR-001 | Labeled test set for AC3 does not exist yet – must be available before sprint start. |
| FR-002 | Unclear whether "too tight / too long / too short" count toward the 60 % threshold. |
| FR-003 | Mapping of articles to "my categories" not described. |
| FR-009 | AC2 lists weight as input while AC3 makes it optional; "supported category" not defined. |
| FR-011 | DPO sign-off on consent text; re-ask behavior after "Not now" undefined. |
| FR-014 | Ambiguous "marketing / service e-mails" consent – clarify legal basis with DPO. |
| FR-012 | AC6 (applied from the report) links to a "size chart"; since the size chart story (#8) was rejected, the link target must be clarified in refinement. |
