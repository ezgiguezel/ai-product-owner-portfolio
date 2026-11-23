# FitRight – Backlog Review (2026-11-23)

Weekly automated quality check of all items in [`/backlog`](../backlog/README.md), in preparation for the next refinement meeting.
The story files themselves were **not** changed. Everything below is a proposal for the Product Owner and the team. **AI suggests, the PO decides.**

**Scope:** 17 active items were reviewed: 14 stories, 1 spike and 2 epics. The 3 closed or replaced items (FR-004, FR-010, FR-015) were only checked for correct archiving.
**Baseline:** [Backlog review 2026-11-12](backlog-review-2026-11-12.md) and [PO decision log](../docs/po-decision-log.md). Recommendations the PO **rejected** on 2026-11-12 are not repeated here: no size chart story, and placeholder story points stay.

**Review criteria** (aligned with the [Definition of Ready](../docs/definition-of-ready.md))

1. **Format:** *As a … I want … so that …* with a concrete persona or role
2. **Acceptance criteria:** clear, testable *Given / When / Then*, and every edge case has a defined outcome
3. **Size:** INVEST, fits into one sprint (≤ 8 SP, estimated by the team)
4. **Business value:** the benefit is clear and linked to a FitRight KPI (see [main README](../README.md#product-goal--kpis))

---

## 1. Summary

| Story ID | Title | Current status | Review status | Main issue |
|---|---|---|---|---|
| [FR-001](../backlog/FR-001.md) | Classify free-text return reasons | Ready | ✅ Ready | *Condition:* the labeled test set for AC3 is still "to be created" (DoR #6). It must exist before sprint start. |
| [FR-002](../backlog/FR-002.md) | Fit hint on the product detail page | Ready | ⚠️ Needs work | Undefined outcome when "too tight / too long / too short" is > 60 % (neither AC1 nor AC2 applies). The time window for the 30 returns is not defined. |
| [FR-003](../backlog/FR-003.md) | Review and approve fit hints | Ready | ✅ Ready | Minor: how articles map to "my categories" is still open. It is unclear whether an approved hint needs re-approval when the underlying data changes. |
| [FR-004a](../backlog/FR-004a.md) | Import supplier size charts per article | New | ❌ Needs work | 3 open questions are still unresolved (R1 risk). No R1 or R2 story uses the imported measurements, so the value is not realized yet. There is no AC for a wrong file format. |
| [FR-005](../backlog/FR-005.md) | A/B test for fit hint impact | Ready | ✅ Ready | *Condition:* the team re-estimate of 3 SP is still pending (DoR #7). Minor: the guardrail is defined twice ("≥ 2.9 %" vs. "no decrease vs. group A"). |
| [FR-006](../backlog/FR-006.md) | Personal size recommendation | Refined | ❌ Needs work | Contradicts FR-009 on two points: when the fit profile entry point is shown, and whether a fit profile alone triggers a recommendation. The AC2b "more than one size" rule can never trigger. The "initial categories" are not defined. |
| [FR-007](../backlog/FR-007.md) | Explain the size recommendation | Refined | ✅ Ready | Minor: no example reason for fit-profile-based recommendations. Can move to *Ready* after a team estimate check. |
| [FR-008](../backlog/FR-008.md) | Epic: Expand FitRight recommendations | Epic | ✅ OK (epic) | The epic structure is fine. Minor: "prioritized by return volume" has no numbers behind it yet. |
| [FR-008a](../backlog/FR-008a.md) | Size recommendation for menswear | New | ⚠️ Needs work | No outcome if the quality gate (AC3) fails. It is unclear whether "2 menswear items" means any menswear or the same sub-category. Two-dimensional sizes (waist/length) may not fit 5 SP. |
| [FR-008b](../backlog/FR-008b.md) | Size recommendation for shoes (length only) | New | ⚠️ Needs work | No outcome if the quality gate (AC4) fails. Converting between EU/UK/US sizes (history vs. article) is not covered. 8 SP is the upper limit. |
| [FR-009](../backlog/FR-009.md) | Fit profile for new customers | Refined | ⚠️ Needs work | Carry-over: is weight mandatory or optional? "Supported category" is not defined. It also has the same conflict with FR-006 described above. |
| [FR-011](../backlog/FR-011.md) | Consent and opt-out | Refined | ⚠️ Needs work | Carry-over: what happens after "Not now" is undefined. Unclear whether one toggle covers the explicit body-data consent that FR-009 AC4 requires. DPO sign-off is still pending. |
| [FR-012](../backlog/FR-012.md) | Multi-size warning in the cart | Refined | ⚠️ Needs work | Carry-over: the AC6 link points to a "size chart", but that story was rejected. Undefined case: the recommended size is not one of the sizes in the cart. |
| [FR-013](../backlog/FR-013.md) | Epic: Return insights for Category Management | Epic | ✅ OK (epic) | The epic structure is fine. |
| [FR-013a](../backlog/FR-013a.md) | Top fit problems in my category | New | ❌ Needs work | AC1 ranks articles by **total** return rate, but the story asks for the **share of size-related** returns. There is no minimum volume, so low-data articles would top the list. Not estimated. |
| [FR-014](../backlog/FR-014.md) | "Did it fit?" feedback | Refined | ⚠️ Needs work | No *Dependencies* section (FR-006, FR-011). Undefined conflict when an item is returned after "fits well" feedback. The KPI "fit satisfaction ≥ 4.2 / 5" cannot be measured with 3 answer options. Carry-over: e-mail consent basis. |
| [FR-015a](../backlog/FR-015a.md) | Spike: analyze wrong size recommendations | New | ✅ Ready | Meets the DoR rules for spikes (question, time-box and output are defined). Minor: exclude orders that are still inside the 30-day return window from the accuracy baseline. |

**Result:** 5 Ready (2 with a sprint-start condition) · 2 epics OK · 7 Needs work (minor) · 3 Needs work (major)

**Closed or replaced items:** FR-004, FR-010 and FR-015 are archived correctly, with their successor and reason. No action needed.

### Progress since the last review (2026-11-12)

- ✅ All 15 PO decisions are visible in the backlog. The epics, spike, discovery backlog and DoR exist.
- ⚠️ **None of the 7 open points** from the [decision log](../docs/po-decision-log.md#open-points--not-decided-in-this-round) has been resolved yet (FR-001, FR-002, FR-003, FR-009, FR-011, FR-012, FR-014).
- ⚠️ **FR-004a** is still *New*, and its open questions are unanswered. It remains the only R1 item that is not Ready.
- ⚠️ 3 of the 4 *Ready* R1 stories do not fully meet the new DoR: FR-001 (#6 test set), FR-002 (#4 undefined outcome) and FR-005 (#7 re-estimate).

---

## 2. Stories that need work: problems and improved versions

Legend: ✏️ changed AC · ➕ new AC · *unchanged* = keep as in the story file.

### FR-002 – Show fit hint on the product detail page

**Problems**
- **Undefined outcome (DoR #4):** suppose an article has 30+ size-related returns and 65 % of them are "too tight". AC1 does not apply (it covers only "too small / too large"), and AC2 does not apply either (one category exceeds 60 %). Nothing defines what the customer sees. This is the open point from 2026-11-12, and it turns out to be a real gap rather than a wording issue.
- **Time window:** it is not defined whether the 30 returns and the 60 % share are counted all-time or over a rolling window. If they are counted all-time, a hint stays visible even after the supplier has corrected the cut.
- **Data basis:** it is not stated whether "unclear" classifications (FR-001 AC2) and "not fit-related" returns are excluded from the denominator.

**Improved version** (story text unchanged)

> **As a** customer browsing a product page,
> **I want** to see a short hint on how the item fits (e.g. "Runs small – most customers recommend one size up"),
> **so that** I can choose the right size before ordering and avoid a return.

**Acceptance Criteria**

- ✏️ **AC1 – Hint for articles running small or large**
  - **Given** an article has at least 30 size-related returns in the last 180 days, counting only the categories "too small", "too large", "too tight", "too long" and "too short" and excluding "unclear", "true to size" and "not fit-related"
  - **And** at least 60 % of them are "too small" (or "too large")
  - **When** I open the product detail page
  - **Then** I see the fit hint "Runs small – we recommend one size up" (or "Runs large – we recommend one size down") directly above the size selector
- ✏️ **AC2 – True to size**
  - **Given** an article has at least 30 size-related returns in the last 180 days (same counting rule as AC1)
  - **And** no single fit category reaches 60 %
  - **When** I open the product detail page
  - **Then** I see the hint "True to size"
- ➕ **AC2b – Dominant cut problem (tight / long / short)**
  - **Given** an article has at least 30 size-related returns in the last 180 days
  - **And** "too tight", "too long" or "too short" reaches at least 60 %
  - **When** I open the product detail page
  - **Then** I see the hint for that category from the predefined texts (e.g. "Cut is narrow", "Runs long", "Runs short") *(PO to confirm the texts with FR-003)*
- **AC3 – AC5** – *unchanged* (AC3 uses the same 180-day window).

**Dependencies:** FR-001, FR-003 (predefined hint texts must include the AC2b texts)

---

### FR-004a – Import supplier size charts per article

**Problems**
- **The open questions are still unresolved** 11 days after the decision. Which categories are in scope, which measurements are mandatory, and is the CSV template agreed? The story cannot be estimated or made Ready until these are answered, and it remains an **R1 risk**.
- **Value not realized:** the "so that" says fit hints and size recommendations will use the measurements. But FR-002 (fit hints) uses only return reasons, and FR-006 (personal recommendation) uses only order history. No story in R1 or R2 consumes the imported data, so the story delivers data that nobody uses yet. The PO should either (a) name the consuming story (e.g. measurement-based size comparison in FR-006 or FR-009), or (b) move FR-004a to R2 and remove the R1 risk.
- **Missing edge cases:** a supplier delivers a file that does not follow the template, or no size chart at all. Size charts for articles that already exist (cleanup slice (b)) are not covered, so the coverage report (AC4) will show low values by design.

**Improved version**

> **As a** Category Manager,
> **I want** the measurements of each size (e.g. chest, waist, length in cm) to be imported from the supplier's size chart for every new article in the R1 categories,
> **so that** size recommendations (FR-006 / FR-009) can compare garment measurements across brands instead of relying only on the size label, which reduces size-related returns.

**Acceptance Criteria**

- **AC1 – AC3** – *unchanged*. AC2 references the agreed list of mandatory measurements per category (attach it to the story).
- ➕ **AC1b – Invalid or missing file**
  - **Given** a supplier delivers no size chart, or a file that does not match the agreed CSV template
  - **When** the import runs
  - **Then** the article is flagged "size data missing" with the reason (e.g. "column 'waist_cm' missing")
  - **And** the responsible Category Manager sees it in the same list as AC2
- ✏️ **AC4 – Coverage reporting**
  - **Given** the import has run for at least one week
  - **When** I open the size data report
  - **Then** I see the share of **new** articles (created after go-live) with complete and plausible size data, per category and supplier

**Before Ready:** answer the 3 open questions with the data team. Decide on the release (R1 vs. R2) based on the consuming story. Get a team estimate to replace the 5 SP placeholder.

---

### FR-006 – Personal size recommendation for logged-in customers

**Problems**
- **Contradiction with FR-009 (entry point):** AC5 shows the fit profile entry point to any logged-in customer with < 2 kept items and no fit profile. FR-009 AC1 shows it only to customers with *no order history*. A customer with 1 kept item would see the entry point under FR-006 but not under FR-009.
- **Contradiction with FR-009 (use of the profile):** FR-009 AC4 says a saved fit profile "is used for future recommendations". FR-006 AC1 and AC5, however, show no personal recommendation unless the customer has kept 2 items. A logged-in customer who has a fit profile but no history would never get a recommendation.
- **AC2b rule can never trigger:** fit hints only ever shift the size by one (up or down), so the history-based size and the hint can never be "more than one size" apart. The intended rule is probably "the history-based size **already** corrects for the fit (e.g. the customer kept a size up in this brand)". This needs to be clarified.
- **AC2b only covers "Runs large"**. The symmetric "Runs small" case is implied but not stated.
- **"Category" granularity** ("same category", "initial categories") is not defined. It could mean womenswear as a whole or individual sub-categories such as dresses. FR-008a and FR-008b depend on this definition.
- **Size:** with 7 ACs (including back-in-stock notification and performance), 8 SP is at the upper limit. The split proposed on 2026-11-12 (backend logic vs. display) is still an option.

**Improved version** (story text unchanged)

> **As a** logged-in customer with previous orders,
> **I want** to see a personal size recommendation on the product page,
> **so that** I can order the size that fits me without ordering several sizes.

**Acceptance Criteria**

- ✏️ **AC1 – Recommendation shown**
  - **Given** I am logged in and have given consent to personalized recommendations (FR-011)
  - **And** I have kept at least 2 items in the same **sub-category** (e.g. dresses, tops; list attached to the story) within the last 24 months, **or** I have a saved fit profile (FR-009)
  - **When** I open a product page in a supported sub-category
  - **Then** I see "Your recommended size: [size]" next to the size selector
  - **And** the recommended size is highlighted in the size selector
  - **And** if both history and fit profile are available, the history-based size is used
- **AC2** – *unchanged*.
- ✏️ **AC2b – Article fit hint is considered**
  - **Given** my history-based size is L and the article has the approved fit hint "Runs large" (or "Runs small")
  - **When** the recommendation is calculated
  - **Then** the recommendation is M (one size down), or XL for "Runs small"
  - **And** the adjustment is applied only once: if my history already contains a kept item of **this article**, the size of that item is used without any adjustment
- **AC3, AC4** – *unchanged*.
- ✏️ **AC5 – Not enough data (fallback)**
  - **Given** I am logged in but meet neither the history nor the fit profile condition of AC1, or I have not given consent
  - **When** I open a product page
  - **Then** no personal recommendation is shown
  - **And** the non-personal fit hint (FR-002) is shown if available
  - **And** if I have no fit profile, I see the entry point to the fit profile questionnaire (FR-009) *(FR-009 AC1 must be aligned to this rule)*

**Dependencies:** FR-001, FR-002, FR-009, FR-011. **Before Ready:** a team re-estimate; split into backend and frontend if it comes out above 8 SP.

---

### FR-008a – Personal size recommendation for menswear

**Problems**
- **AC3 quality gate has no outcome if it fails** (DoR #4). If the backtest reaches only 72 %, it is unclear what happens: no go-live, go-live for some sub-categories only, or a new spike?
- **Data condition is ambiguous:** "2 menswear items" could mean any menswear (2 shirts → recommendation for trousers?) or the same sub-category, as in FR-006.
- **Two-dimensional sizes** (waist/length 32/34) need two separate recommendations (waist and length). This is more complex than one size axis and is a risk for the 5 SP placeholder.
- **Business value:** the epic says slices are "prioritized by return volume", but no menswear return figures are given to justify this slice.

**Improved version**

> **As a** logged-in customer buying menswear,
> **I want** to see a personal size recommendation on menswear product pages,
> **so that** I order the right size the first time and do not need to return the item (menswear size-related returns: *[add figure]*).

**Acceptance Criteria**

- ✏️ **AC1 – Recommendation in menswear**
  - **Given** I am logged in, have given consent (FR-011) and kept at least 2 items in the **same menswear sub-category** (tops, trousers, jackets) in the last 24 months
  - **When** I open a menswear product page of that sub-category
  - **Then** I see "Your recommended size: [size]" next to the size selector, as in FR-006
- ✏️ **AC2 – Menswear size systems**
  - **Given** the article uses a numeric size system (e.g. 48/50/52) or waist/length (e.g. 32/34)
  - **When** the recommendation is calculated
  - **Then** the recommended size is shown in the article's own size system
  - **And** for waist/length sizes, both values are recommended (e.g. "W32 / L34"). If only one dimension can be derived, no recommendation is shown.
- **AC3 – Quality gate before go-live** – *unchanged*.
- ➕ **AC3b – Quality gate not reached**
  - **Given** the backtest accuracy is below 80 % for a sub-category
  - **When** the go-live decision is made
  - **Then** the recommendation is not activated for that sub-category, the result is documented, and the PO decides on a follow-up
- **AC4 – Fallback** – *unchanged*.

---

### FR-008b – Personal size recommendation for shoes (length only)

**Problems**
- **AC4 quality gate has no outcome if it fails** (the same gap as FR-008a).
- **Size conversion:** a customer's history may be in EU sizes (brand A) while the article uses UK sizes (brand B). AC2 says to "show the article's own size system" but does not define how history from another system is converted, or what happens when the conversion is ambiguous (e.g. UK 7 = EU 40.5 or 41).
- **8 SP** (placeholder 5–8) is at the upper limit. If the conversion logic is added, the story may need to be split (e.g. one size system first).
- Minor: the FR-001 categories have no "too narrow / too wide". Width-related shoe returns will end up in "too tight", which could distort the length recommendation.

**Improved version** (story text unchanged)

> **As a** logged-in customer buying shoes,
> **I want** to see a personal shoe size recommendation on shoe product pages,
> **so that** I order the right shoe size the first time and do not need to return the shoes because they are too small or too large.

**Acceptance Criteria**

- **AC1, AC3, AC5** – *unchanged*.
- ✏️ **AC2 – Shoe size systems**
  - **Given** the article uses a specific shoe size system (EU, UK or US, including half sizes)
  - **And** my kept shoes may use a different size system
  - **When** the recommendation is calculated
  - **Then** my history is converted using the brand's conversion table, and the recommended size is shown in the article's own size system
  - **And** if no conversion table exists for the brand, no recommendation is shown
- **AC4 – Quality gate before go-live** – *unchanged*.
- ➕ **AC4b – Quality gate not reached**
  - **Given** the backtest accuracy is below 80 %
  - **When** the go-live decision is made
  - **Then** the shoe recommendation is not activated, and the result and the main error sources are documented for the PO
- ➕ **AC6 – Width-related returns excluded**
  - **Given** a returned pair was classified "too tight" and the comment refers to width (e.g. "too narrow")
  - **When** the length recommendation is calculated
  - **Then** this return is not counted as "too small"

**Dependencies:** FR-006, FR-011, FR-001 (shoe-specific classification), brand size conversion tables (external prerequisite, DoR #6)

---

### FR-009 – Fit profile for new customers

**Problems**
- **Carry-over 1:** AC2 lists weight as a questionnaire input, while AC3 makes it optional. It is not defined whether a recommendation is possible without weight.
- **Carry-over 2:** "supported category" is still undefined. It should use the same sub-category list as FR-006.
- **Conflict with FR-006** (see above): the AC1 entry point condition ("no order history") differs from FR-006 AC5 ("< 2 kept items and no fit profile").
- **"Usual size in one known brand"** needs a defined brand list. Free text cannot be used for a calculation.
- Minor: AC2 "immediately" is not measurable.

**Improved version**

> **As a** new or occasional customer without enough order history for a personal recommendation,
> **I want** to enter a few details about my body and fit preferences,
> **so that** I also receive a size recommendation for my first orders and do not need to order several sizes.

**Acceptance Criteria**

- ✏️ **AC1 – Entry point**
  - **Given** I have no fit profile and do not meet the history condition of FR-006 AC1 (or I am a guest)
  - **When** I open a product page in a supported sub-category (same list as FR-006)
  - **Then** I see the link "Find your size in 30 seconds"
- ✏️ **AC2 – Short questionnaire**
  - **Given** I opened the fit profile questionnaire
  - **When** I enter height and my usual size in one brand from a selectable brand list, and optionally weight and fit preference ("tight", "regular", "loose")
  - **Then** I see a size recommendation for the current product within 2 seconds after submitting
- **AC3 – Optional fields and validation** – *unchanged* (now consistent with AC2).
- ✏️ **AC4 – Save profile**
  - **Given** I am logged in and complete the questionnaire
  - **And** I have given explicit consent to store my body data (FR-011)
  - **When** I submit the questionnaire
  - **Then** the fit profile is saved to my account and used for future recommendations as defined in FR-006 AC1
- **AC5 – Guest usage** – *unchanged*.

**Dependencies:** FR-006 (shared rules for sub-categories and entry point), FR-011

---

### FR-011 – Consent and opt-out for personalized size recommendations

**Problems**
- **Carry-over: no defined behavior after "Not now"** (DoR #4). If the dialog shows again on every product page, it can hurt the conversion guardrail. If it never shows again, R2 adoption stays low.
- **Consent scope is unclear:** this story uses **one** toggle for order, return **and** body data. FR-009 AC4 requires a **separate, explicit** consent for body data. The two stories need to agree on whether this is one consent or two.
- **Carry-over:** DPO sign-off on the consent text is still pending (DoR #6).

**Improved version** (story text unchanged)

> **As a** customer,
> **I want** to decide whether my order, return and body data is used for size recommendations,
> **so that** I stay in control of my personal data.

**Acceptance Criteria**

- **AC1 – Ask for consent** – *unchanged*.
- ✏️ **AC2 – No consent**
  - **Given** I selected "Not now" or have withdrawn my consent
  - **When** I open a product page
  - **Then** no personal recommendation is shown and only non-personal fit hints (FR-002) are displayed
  - **And** after "Not now", the consent dialog is not shown again for 30 days *(PO to confirm the interval)*. I can still opt in at any time in my privacy settings.
- **AC3, AC4** – *unchanged*.
- ➕ **AC5 – Separate consent for body data**
  - **Given** I have given consent to personalized recommendations based on order and return data
  - **When** I want to save a fit profile with body data (FR-009)
  - **Then** I am asked for a separate, explicit consent to store body data, which can be withdrawn independently

**Before Ready:** DPO sign-off on both consent texts.

---

### FR-012 – Warn when the same item is ordered in several sizes

**Problems**
- **Carry-over:** AC6 links to the "size chart / fit profile questionnaire". The size chart story was **rejected** (decision #8), so only the fit profile link is possible.
- **Undefined case:** the cart contains M and L, but the personal recommendation is S. AC2 "Keep only size S" would remove all items and leave a size that is not in the cart.
- **Undefined case:** the recommended size is in the cart but is now sold out.

**Improved version** (story text unchanged)

> **As a** customer who is unsure about the size,
> **I want** to be informed when I have the same item in my cart in several sizes and get help choosing one,
> **so that** I can avoid an unnecessary return.

**Acceptance Criteria**

- **AC1 – AC5, AC7** – *unchanged*.
- ➕ **AC1b – Recommended size not in the cart**
  - **Given** my cart contains the article in several sizes
  - **And** my recommended size is not one of them
  - **When** I open the cart
  - **Then** the hint shows "You have this item in [n] sizes. Based on your data, [size] should fit you best." with the button "Replace with size [size]" (if in stock) instead of "Keep only size"
- ✏️ **AC6 – Neither recommendation nor fit hint**
  - **Given** neither a personal recommendation nor an approved fit hint is available
  - **When** the cart contains the article in several sizes
  - **Then** the hint shows "You have this item in [n] sizes." with a link to the fit profile questionnaire (FR-009)

**Dependencies:** FR-002, FR-006, FR-009

---

### FR-013a – Top fit problems in my category

**Problems**
- **AC1 contradicts the story.** The story wants articles with the highest **share of size-related returns**, but AC1 ranks by **total item return rate**. An article returned mostly for colour or quality would rank high, even though it has no fit problem.
- **No minimum volume for the ranking.** An article with 2 shipped and 2 returned items (100 %) would top the list. AC5 only greys out the fit distribution and does not exclude the article from the ranking.
- **"My categories" mapping** is the same open point as in FR-003.
- **Not estimated** (DoR #7).
- Minor: AC4 says "dashboard", while the view is called "Return Insights" in AC1.

**Improved version**

> **As a** Category Manager (persona: Markus),
> **I want** to see the articles in my categories with the highest share of size-related returns, including the distribution of fit categories,
> **so that** I can address fit problems with suppliers during the season instead of waiting for the monthly report, which reduces size-related returns in my category.

**Acceptance Criteria**

- ✏️ **AC1 – Article ranking**
  - **Given** I am logged in to the backoffice with the role "Category Manager"
  - **When** I open "Return Insights"
  - **Then** I see the 50 articles of my categories with the highest **share of size-related returns** in the last 30 days
  - **And** only articles with at least 100 shipped items and 30 returns in the period are ranked *(team to confirm thresholds)*
  - **And** the columns are: article, brand, supplier, shipped items, item return rate, share of size-related returns
- **AC2, AC3** – *unchanged*.
- ✏️ **AC4 – Data freshness**
  - **Given** the nightly classification job (FR-001) has finished
  - **When** I open "Return Insights"
  - **Then** the data includes all returns up to the previous day and the "data as of" date is shown
- ✏️ **AC5 – Minimum data**
  - **Given** an article in my categories does not meet the thresholds of AC1
  - **When** I search for it or open it directly
  - **Then** it is marked "low data" and the fit distribution is shown greyed out

**Dependencies:** FR-001, the article-to-Category-Manager mapping (shared with FR-003)

---

### FR-014 – "Did it fit?" feedback after delivery

**Problems**
- **No *Dependencies* section** (DoR #5). AC3 depends on FR-006, and using the feedback for recommendations requires FR-011 consent.
- **Undefined conflict:** a customer clicks "fits well" on day 5 and returns the item on day 20 with "too small". AC3 treats the feedback "like a kept item", but it is not stated which signal wins.
- **KPI mismatch:** the README measures "Customer satisfaction with fit ≥ 4.2 / 5" via this survey, but the story only offers 3 options (too small / fits well / too large). The KPI cannot be measured as defined. Either the KPI definition or the story has to change.
- **Carry-over:** whether "marketing / service e-mails" is the right legal basis is still open (DPO).
- Minor: the login-free link (AC2) needs protection against manipulation (e.g. a signed one-time link).

**Improved version**

> **As a** customer who received an order,
> **I want** to quickly tell the shop how the items fit,
> **so that** my future size recommendations become more accurate and I return fewer items (KPIs: recommendation accuracy, fit satisfaction).

**Acceptance Criteria**

- **AC1** – *unchanged* (pending DPO decision on the e-mail consent basis).
- ✏️ **AC2 – One-click feedback**
  - **Given** I opened the feedback e-mail
  - **When** I click "too small", "fits well" or "too large" for an item
  - **Then** my feedback is saved via a personal, signed link without requiring a login, and I see a thank-you page
  - **And** I can optionally rate the overall fit on a scale of 1–5 on the thank-you page *(only if the PO keeps the KPI "≥ 4.2 / 5")*
- ✏️ **AC3 – Usage in recommendations**
  - **Given** I gave fit feedback for an item
  - **And** I have given consent to personalized recommendations (FR-011)
  - **When** my next size recommendation is calculated
  - **Then** the feedback is taken into account in the same way as a kept or returned item
- ➕ **AC3b – Return after feedback**
  - **Given** I gave fit feedback for an item and returned it later
  - **When** my next size recommendation is calculated
  - **Then** the return and its reason are used, and the earlier feedback is ignored
- **AC4 – Returned items** – *unchanged*.

**Dependencies:** FR-006, FR-011. **Before Ready:** DPO decision on the e-mail legal basis, and a PO decision on the KPI definition.

---

### Ready items with minor notes (no rewrite proposed)

| Item | Note |
|---|---|
| FR-001 | The labeled test set (1,000 comments) has to be created with Customer Service **before** sprint start. Without it, AC3 cannot be verified and the story does not meet DoR #6. |
| FR-003 | (a) Add how articles are mapped to "my categories", e.g. from the PIM category assignment. FR-013a needs the same mapping. (b) Define whether a published hint needs re-approval when the daily job proposes a different hint (e.g. "Runs small" → "True to size"). If FR-002 adds AC2b, the predefined texts need the new hint types. |
| FR-005 | (a) The team re-estimate (decided on 2026-11-12) is still pending, so status *Ready* is premature under DoR #7. (b) Pick one guardrail definition: an absolute "≥ 2.9 %" or relative "group B not significantly below group A". (c) AC4 hides fit hints for visitors without analytics consent. Confirm that this applies only during the test. |
| FR-007 | Add an example reason for fit-profile-based recommendations (e.g. "Based on your fit profile"). AC2 makes sure no values are shown. Link the value to the KPI "recommendation adoption". |
| FR-015a | The accuracy baseline should only include orders older than 30 days, because the return window must be closed. Otherwise accuracy is overstated. |

---

## 3. Top 3 recommendations for the next refinement meeting

1. **Make R1 really Ready, and decide on FR-004a.**
   Only one R1 story (FR-003) fully meets the DoR today. Fix the undefined "too tight / long / short" case in FR-002 (AC2b proposal above). Confirm a delivery date for the FR-001 test set, and have the team re-estimate FR-005. For **FR-004a**, the decision is no longer only about the open questions. No R1 or R2 story consumes the size measurements yet. **Decision needed:** name the consuming story, or move FR-004a to R2 and remove the R1 risk.

2. **Align the R2 personalization rules in one session (FR-006, FR-009, FR-011, FR-007), with the DPO.**
   The three stories describe the same customer journey with different rules: who sees the fit profile entry point, whether a fit profile alone triggers a recommendation, and whether body data needs a separate consent. A one-page decision table (*data situation × consent → what the customer sees*) would remove the contradictions. It would also fix the "sub-category" definition that FR-008a and FR-008b depend on. In the same DPO slot, get sign-off on the consent texts (FR-011) and the e-mail legal basis (FR-014).

3. **Work off the 7 carry-over open points, and define "what if it fails" for every quality gate and KPI.**
   None of the open points from 2026-11-12 has moved. Give each one an owner and a target date in the decision log. In the same pass, add a fail outcome to the quality gates in FR-008a and FR-008b. Correct the FR-013a ranking (size-related share instead of total return rate). Resolve the KPI mismatch "fit satisfaction ≥ 4.2 / 5" vs. the 3-option feedback in FR-014. These are small text changes, but without them the team cannot test the stories or measure the KPIs.

---

*Generated by the weekly automated backlog review routine on 2026-11-23. Story files in `/backlog` were not modified.*
