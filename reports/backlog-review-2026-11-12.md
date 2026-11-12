# FitRight – Backlog Review (2026-11-12)

Automated quality review of all 15 stories in [`/backlog`](../backlog/README.md), in preparation for the next refinement meeting.
The story files themselves were **not** changed – all suggestions below are proposals for the Product Owner and team.

**Review criteria**

1. **Format** – written as *As a … I want … so that …*
2. **Acceptance criteria** – clear, testable *Given / When / Then*
3. **Size** – fits into one sprint (INVEST: Independent, Negotiable, Valuable, Estimable, Small, Testable); team guideline used here: ≤ 8 SP
4. **Business value** – the benefit is clear and can be linked to a FitRight KPI (see [main README](../README.md#product-goal--kpis))

---

## 1. Summary

| Story ID | Title | Status | Main issue |
|---|---|---|---|
| [FR-001](../backlog/FR-001.md) | Classify free-text return reasons | ✅ Ready | Minor: labeled test set (needed for AC3) does not exist yet – must be available before sprint start |
| [FR-002](../backlog/FR-002.md) | Fit hint on the product detail page | ✅ Ready | Minor: unclear whether "too tight / too long / too short" count toward the 60 % threshold |
| [FR-003](../backlog/FR-003.md) | Review and approve fit hints | ✅ Ready | Minor: how articles are mapped to "my categories" is not described |
| [FR-004](../backlog/FR-004.md) | Better size data | ❌ Needs work | No user story, no acceptance criteria, no clear scope – yet estimated (5 SP) and planned for R1 |
| [FR-005](../backlog/FR-005.md) | A/B test for fit hint impact | ⚠️ Needs work | No hypothesis / success metric; AC3 ("can be attributed") is not testable; 3 SP looks underestimated |
| [FR-006](../backlog/FR-006.md) | Personal size recommendation | ⚠️ Needs work | AC2 exception has no defined outcome; fallback for customers with insufficient data is missing (listed in R2 roadmap) |
| [FR-007](../backlog/FR-007.md) | Explain the size recommendation | ✅ Ready | Minor: dependency on FR-006 and FR-009 (fit profile) not listed |
| [FR-008](../backlog/FR-008.md) | Size recommendation for all customers and categories | ❌ Needs work | Epic (40 SP) mixing many features; ACs not testable ("customers are happy") |
| [FR-009](../backlog/FR-009.md) | Fit profile for new customers | ✅ Ready | Minor: AC2 lists weight as input while AC3 makes it optional; "supported category" not defined; dependency on FR-011 missing |
| [FR-010](../backlog/FR-010.md) | Smarter shopping | ❌ Needs work | Vague one-liner without user role, scope or ACs; duplicates the product vision / FR-006 / FR-008 |
| [FR-011](../backlog/FR-011.md) | Consent and opt-out | ✅ Ready | Minor: DPO sign-off on consent text is a Definition-of-Ready blocker; re-ask behavior after "Not now" undefined |
| [FR-012](../backlog/FR-012.md) | Multi-size warning in the cart | ⚠️ Needs work | Case "no personal recommendation **and** no fit hint" undefined; dependency on FR-006 / FR-002 not listed |
| [FR-013](../backlog/FR-013.md) | Category Management Dashboard | ❌ Needs work | Epic (21 SP, 11 features); generic value ("better decisions"); ACs not testable |
| [FR-014](../backlog/FR-014.md) | "Did it fit?" feedback | ✅ Ready | Minor: "marketing / service e-mails" consent is ambiguous – clarify legal basis with DPO |
| [FR-015](../backlog/FR-015.md) | Improve recommendation quality | ❌ Needs work | No user story, not estimable ("?"), AC "better than before" not measurable |

**Result:** 7 Ready · 3 Needs work (minor gaps) · 5 Needs work (major rewrite or split)

Additional observations:
- All five "New" stories already carry story points (except FR-015) although they are not yet refined – estimates should be removed or treated as placeholders until the stories are refined.
- FR-004 is the only R1 story that is not ready. Since R1 depends on reliable size data, it is a **risk for the R1 scope**.

---

## 2. Stories that need work – problems and improved versions

### FR-004 – Better size data

**Problems**
- No user story format, no persona, no "so that".
- No acceptance criteria; "somehow" and "talk to the data team" are open tasks, not requirements.
- Combines two different topics: (a) supplier data delivery and (b) cleanup of existing data.
- Estimated with 5 SP although the scope is unknown → not estimable.

**Recommendation:** Run a short analysis together with the data team first (what exactly is "not good enough"?). Then split into (a) supplier size chart import and (b) data cleanup. Proposal for slice (a):

> **FR-004a: Import supplier size charts per article**
>
> **As a** Category Manager,
> **I want** the measurements of each size (e.g. chest, waist, length in cm) to be imported from the supplier's size chart for every new article,
> **so that** fit hints and size recommendations are based on real garment measurements instead of only the size label.

**Acceptance Criteria**

- **AC1 – Import of valid size chart**
  - **Given** a supplier delivers a size chart in the agreed template (CSV) for a new article
  - **When** the article is created in the PIM
  - **Then** the measurements per size are stored with the article and are visible in the backoffice article view
- **AC2 – Missing mandatory measurements**
  - **Given** the size chart of an article in a supported category is missing a mandatory measurement (defined per category)
  - **When** the import runs
  - **Then** the article is flagged "size data incomplete" and the responsible Category Manager sees it in a list
- **AC3 – Implausible values**
  - **Given** a measurement decreases from a smaller to a larger size (e.g. waist of M < waist of S)
  - **When** the import runs
  - **Then** the article is flagged "size data implausible" and the values are not used for recommendations
- **AC4 – Coverage reporting**
  - **Given** the import has run for at least one week
  - **When** I open the size data report
  - **Then** I see the share of active articles with complete size data per category and supplier

*Open questions for refinement:* Which categories are in scope for R1? Which measurements are mandatory per category? Is the template already agreed with suppliers?

---

### FR-005 – Track fit hint impact with an A/B test

**Problems**
- Business value is clear, but the test has no **hypothesis, primary metric or minimum detectable effect** – the team cannot decide when the test is "done" or successful.
- AC3 ("can be attributed in the reporting") is not testable – which report, which fields?
- AC4 assigns non-consenting visitors to group A. They are not tracked anyway, so this is harmless technically – but it should be explicit that they are **excluded from the analysis**, otherwise group sizes look skewed.
- 3 SP for persistent assignment, event tracking and order/return attribution across systems seems low – re-estimate.

**Improved version**

> **As a** Product Owner,
> **I want** fit hints to be rolled out as a 50/50 A/B test with tracking of hint views, orders and returns per test group,
> **so that** I can prove that fit hints reduce the item return rate of affected articles (hypothesis: –3 pp) without lowering PDP conversion (guardrail: ≥ 2.9 %).

**Acceptance Criteria**

- **AC1 – Group assignment** – *unchanged*: random, persistent 50/50 assignment of consenting visitors to group A (no hint) or B (hint).
- **AC2 – Event tracking** – *unchanged*: `fit_hint_viewed` with article ID, hint type and test group.
- **AC3 – Order and return attribution**
  - **Given** a visitor in group A or B places an order containing an article that has an approved fit hint
  - **When** the order and any returns of these order lines are processed
  - **Then** each order line and return record in the data warehouse contains the field `fit_test_group` (A/B)
  - **And** the A/B report shows per group: PDP sessions, conversion rate, ordered items, returned items and item return rate
- **AC4 – Consent**
  - **Given** a visitor has not given analytics consent
  - **When** they open a product page
  - **Then** no fit hint and no tracking event is shown/sent, and the visitor is excluded from the test population
- **AC5 – Test documentation**
  - **Given** the test is started
  - **When** it is configured in the experimentation tool
  - **Then** hypothesis, primary metric, guardrail metric, minimum sample size and planned runtime (≥ 6 weeks + 30 days return window) are documented

---

### FR-006 – Personal size recommendation for logged-in customers

**Problems**
- AC2: "the recommendation is L, unless the article has a fit hint 'runs large'" – the outcome in the exception case is not defined (M? no recommendation?).
- The R2 roadmap explicitly lists a "fallback when data is insufficient", but no AC covers customers who do not meet the threshold (fewer than 2 kept items, no consent).
- AC1 and AC2 together cover a lot of logic; 8 SP is the upper limit – consider splitting the calculation logic (backend) from the display (frontend) if the team re-estimates higher.

**Improved version** (story text unchanged; ACs adjusted)

> **As a** logged-in customer with previous orders,
> **I want** to see a personal size recommendation on the product page,
> **so that** I can order the size that fits me without ordering several sizes.

**Acceptance Criteria**

- **AC1 – Recommendation shown** – *unchanged*.
- **AC2 – Based on kept and returned items**
  - **Given** I returned an item in size M with the reason "too small" and kept an item of the same brand in size L
  - **When** the recommendation for another item of this brand is calculated
  - **Then** the recommendation is L
- **AC2b – Article fit hint is considered**
  - **Given** my history-based size is L
  - **And** the article has the approved fit hint "Runs large"
  - **When** the recommendation is calculated
  - **Then** the recommendation is M (one size down)
  - **And** if the history-based size and the fit hint lead to a difference of more than one size, no personal recommendation is shown
- **AC3 – Size not available** – *unchanged*.
- **AC4 – Performance** – *unchanged*.
- **AC5 – Not enough data (fallback)**
  - **Given** I am logged in but have kept fewer than 2 items in this category in the last 24 months, or I have not given consent
  - **When** I open a product page
  - **Then** no personal recommendation is shown
  - **And** the non-personal fit hint (FR-002) is shown if available
  - **And** if I have no fit profile, I see the entry point to the fit profile questionnaire (FR-009)

---

### FR-008 – Size recommendation for all customers and categories

**Problems**
- This is an **epic**, not a story: 40 SP and at least 8 independent topics (guests, new customers, 7 categories, shoe widths, body scan, AR try-on, app, newsletter, marketplace, style preferences, weather).
- "So that I **never** have to return anything" is an unrealistic promise – the value should link to the KPI (return rate, recommendation accuracy).
- ACs are not testable ("customers are happy").
- Overlaps with FR-006 (logged-in) and FR-009 (new customers).
- Body scan / AR try-on are solution ideas that need discovery, not delivery stories.

**Recommendation:** Convert FR-008 into the epic **"Expand FitRight recommendations"**, remove the story points and split it by **category** and **channel**, prioritized by return volume. Move body scan / AR and style/weather into a discovery backlog. Proposed split:

| New story | Scope | Rough size |
|---|---|---|
| FR-008a | Personal recommendation for menswear (roadmap R3) | 5 |
| FR-008b | Personal recommendation for shoes (length only) | 5–8 |
| FR-008c | Shoe width recommendation | 5 |
| FR-008d | Show recommendation in the mobile app | 5 |
| FR-008e | Discovery: body scan / AR try-on for guests (spike, time-boxed) | spike |
| … | Kids, lingerie, sportswear, newsletter, marketplace | later |

**Improved version of the first slice**

> **FR-008a: Personal size recommendation for menswear**
>
> **As a** logged-in customer buying menswear,
> **I want** to see a personal size recommendation on menswear product pages,
> **so that** I order the right size the first time and do not need to return the item.

**Acceptance Criteria**

- **AC1 – Recommendation in menswear**
  - **Given** I am logged in, have given consent (FR-011) and kept at least 2 menswear items in the last 24 months
  - **When** I open a menswear product page (tops, trousers, jackets)
  - **Then** I see "Your recommended size: [size]" next to the size selector, as in FR-006
- **AC2 – Menswear size systems**
  - **Given** the article uses a numeric size system (e.g. 48/50/52 or waist/length 32/34)
  - **When** the recommendation is calculated
  - **Then** the recommended size is shown in the article's own size system
- **AC3 – Quality gate before go-live**
  - **Given** a backtest on menswear orders of the last 12 months
  - **When** the model is evaluated
  - **Then** at least 80 % of historical items ordered in the recommended size were kept (KPI "recommendation accuracy")
- **AC4 – Fallback** – same behavior as FR-006 AC5.

---

### FR-010 – Smarter shopping

**Problems**
- "User" is not a persona; "smarter about sizes" is not a requirement; no ACs, no release.
- The content is already covered by the product vision and by FR-002, FR-006, FR-008 and FR-012 → duplicate.
- 3 SP is estimated without any scope.

**Recommendation:** **Close FR-010** (or use its text as the goal statement of the FR-008 epic). If the PO had a concrete idea in mind, the original requester should be asked. A concrete, sprint-sized interpretation that is *not* yet covered in the backlog would be an interactive size chart:

> **FR-010 (rewritten): Show the article's size chart in my body measurements**
>
> **As a** customer who is unsure about the size and has no personal recommendation,
> **I want** to see the article's garment measurements for each size directly next to the size selector,
> **so that** I can compare them with a garment I own and choose the right size.

**Acceptance Criteria**

- **AC1 – Size chart available**
  - **Given** the article has complete size data (see FR-004a)
  - **When** I tap "Size chart" on the product page
  - **Then** I see a table with the measurements (cm) for every size of this article
- **AC2 – Highlight a size**
  - **Given** the size chart is open
  - **When** I select a size in the size selector
  - **Then** the corresponding column is highlighted in the size chart
- **AC3 – No size data**
  - **Given** the article has no or incomplete size data
  - **When** I open the product page
  - **Then** the "Size chart" link is not shown
- **AC4 – Tracking**
  - **Given** analytics consent is given
  - **When** I open the size chart
  - **Then** the event `size_chart_opened` with article ID is tracked

---

### FR-012 – Warn when the same item is ordered in several sizes

**Problems**
- AC4 covers "no personal recommendation", but not the case where there is **also no fit hint** – the hint text in AC1 would then be empty.
- Dependencies on FR-006 (personal recommendation) and FR-002 (fit hint) are not listed, although the story cannot be tested without them.
- Otherwise a good, valuable story directly linked to the KPI "multi-size orders".

**Improved version** (story text unchanged; ACs added)

> **As a** customer who is unsure about the size,
> **I want** to be informed when I have the same item in my cart in several sizes and get help choosing one,
> **so that** I can avoid an unnecessary return.

**Acceptance Criteria**

- **AC1 – AC3, AC5** – *unchanged*.
- **AC4 – No personal recommendation, but fit hint available**
  - **Given** no personal size recommendation is available for me
  - **And** the article has an approved fit hint (e.g. "Runs small")
  - **When** the cart contains the article in several sizes
  - **Then** the hint shows "You have this item in [n] sizes. Customers say: [fit hint]." without a "Keep only size" button
- **AC6 – Neither recommendation nor fit hint**
  - **Given** neither a personal recommendation nor an approved fit hint is available
  - **When** the cart contains the article in several sizes
  - **Then** the hint shows "You have this item in [n] sizes." with a link to the size chart / fit profile questionnaire (FR-009)
- **AC7 – Tracking**
  - **Given** analytics consent is given
  - **When** the hint is shown and the customer chooses "Keep only size" or "Keep all sizes"
  - **Then** the events `multisize_hint_shown` and `multisize_hint_action` (with the chosen action) are tracked, so the KPI "multi-size orders" can be measured

**Dependencies:** FR-002, FR-006, FR-009 (optional link)

---

### FR-013 – Category Management Dashboard

**Problems**
- **Epic**, not a story: 21 SP and 11 features (incl. competitor comparison, forecasting, delisting recommendations, CO₂, Teams alerts, mobile).
- Value "make better decisions" is generic; Markus' persona gives a much sharper need: *identify articles with fit problems early and use the data in supplier talks*.
- ACs are not testable ("data is correct", "Category Managers like the dashboard").
- Some items need separate data sources (competitors, CO₂) that may not exist.

**Recommendation:** Convert to the epic **"Return insights for Category Management"** and deliver a thin first slice focused on fit problems (the core of FitRight). Later slices: export, supplier reports, FitRight impact view (re-using FR-005 data), alerts. Forecasting, delisting recommendations, competitor comparison and CO₂ go to discovery.

**Improved version of the first slice**

> **FR-013a: Top fit problems in my category**
>
> **As a** Category Manager,
> **I want** to see the articles in my categories with the highest share of size-related returns, including the distribution of fit categories,
> **so that** I can address fit problems with suppliers during the season instead of waiting for the monthly report.

**Acceptance Criteria**

- **AC1 – Article ranking**
  - **Given** I am logged in to the backoffice with the role "Category Manager"
  - **When** I open "Return Insights"
  - **Then** I see the 50 articles of my categories with the highest item return rate in the last 30 days, with columns: article, brand, supplier, shipped items, return rate, share of size-related returns
- **AC2 – Fit category distribution**
  - **Given** the article list is displayed
  - **When** I open an article
  - **Then** I see the distribution of fit categories from FR-001 (too small, too large, too tight, too long, too short, true to size, not fit-related) per size
- **AC3 – Filter**
  - **Given** the article list is displayed
  - **When** I filter by brand, supplier or time period (7 / 30 / 90 days)
  - **Then** the list and all figures update accordingly within 3 seconds
- **AC4 – Data freshness**
  - **Given** the nightly classification job (FR-001) has finished
  - **When** I open the dashboard
  - **Then** the data includes all returns up to the previous day and the "data as of" date is shown
- **AC5 – Minimum data**
  - **Given** an article has fewer than 30 returns in the selected period
  - **When** it is listed
  - **Then** it is marked "low data" and the fit distribution is shown greyed out

---

### FR-015 – Improve recommendation quality

**Problems**
- No user story format; the value ("customers say the recommendations are wrong") is anecdotal.
- AC "better than before" is not measurable – there is no baseline.
- Story points "?" – not estimable because the solution ("more data or a different model") is open.
- Improvement work of this kind usually needs a **spike / analysis** first.

**Recommendation:** Split into (1) a time-boxed analysis spike and (2) a measurable improvement story once the root causes are known. The KPI "recommendation accuracy ≥ 80 %" from the main README is the natural success criterion.

**Improved version**

> **FR-015a (Spike, time-box 3 days): Analyze wrong size recommendations**
>
> **As a** Product Owner,
> **I want** to know in which categories, brands and customer segments the size recommendation is most often wrong,
> **so that** we invest model improvements where they reduce the most returns.

**Acceptance Criteria**

- **AC1** – **Given** order and return data of the last 3 months, **when** the analysis is done, **then** recommendation accuracy (kept items / items ordered in the recommended size) is reported per category, brand and data situation (history-based vs. fit-profile-based).
- **AC2** – **Given** the analysis results, **when** the spike is closed, **then** the top 3 root causes are documented with an estimated impact on the return rate and a proposal for follow-up stories.

> **FR-015b: Improve recommendation accuracy for [segment from spike]**
>
> **As a** customer in [segment],
> **I want** the size recommendation to fit me reliably,
> **so that** I can trust it and do not need to return items because of the size.

**Acceptance Criteria**

- **AC1 – Offline quality gate**
  - **Given** the improved model and the current model are evaluated on the same backtest data set
  - **When** the evaluation is run
  - **Then** recommendation accuracy for [segment] improves from [baseline from spike] to at least [target, e.g. 80 %]
  - **And** accuracy in all other segments does not decrease by more than 1 pp
- **AC2 – Controlled rollout**
  - **Given** the new model passed the offline quality gate
  - **When** it is rolled out
  - **Then** it runs as an A/B test against the current model and the return rate of items ordered in the recommended size is reported per group
- **AC3 – Rollback**
  - **Given** the new model shows lower accuracy or higher return rates in the A/B test after 4 weeks
  - **When** the PO decides to roll back
  - **Then** the previous model can be reactivated by configuration without a deployment

---

## 3. Top 3 recommendations for the next refinement meeting

1. **Split the two epics FR-008 (40 SP) and FR-013 (21 SP).**
   Together they hold more than 60 SP of unrefined scope. Agree on the epic goals, pick one thin first slice each (proposals: FR-008a menswear, FR-013a top fit problems) and move speculative ideas (body scan, AR, weather, forecasting, competitor comparison, CO₂) to a discovery backlog. Remove placeholder estimates from un-refined stories.

2. **Resolve the vague stories FR-004, FR-010 and FR-015 – starting with FR-004 because it is an R1 risk.**
   Invite the data team to clarify what "better size data" means and decide on the scope for R1. Close FR-010 as a duplicate (or replace it with the size chart story). Turn FR-015 into a time-boxed spike so the team gets a measurable baseline for recommendation accuracy before committing to model work.

3. **Close the remaining gaps in the "Ready/Refined" stories and introduce a Definition-of-Ready checklist.**
   Fix the open edge cases (FR-006 AC2 + fallback, FR-012 "no data" case), add missing dependencies (FR-007 → FR-009, FR-009 → FR-011, FR-012 → FR-002/FR-006) and add a hypothesis/success metric to FR-005. Make external prerequisites explicit DoR items: labeled test set for FR-001, DPO sign-off on consent texts for FR-011 and FR-014. A short DoR checklist (format, testable ACs, dependencies listed, ≤ 8 SP, KPI link) would prevent most of the issues found in this review.

---

*Generated by an automated backlog review routine. Story files in `/backlog` were not modified.*
