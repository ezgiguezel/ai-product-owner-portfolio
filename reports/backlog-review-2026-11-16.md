# FitRight – Backlog Review (2026-11-16)

Automated weekly quality review of all items in [`/backlog`](../backlog/README.md), in preparation for the next refinement meeting.
The story files themselves were **not** changed – all suggestions below are proposals for the Product Owner and team.

**Review criteria**

1. **Format** – written as *As a … I want … so that …* with a concrete persona / role
2. **Acceptance criteria** – clear, testable *Given / When / Then*, including edge cases and fallbacks
3. **Size** – INVEST; estimated by the team and ≤ 8 SP (fits into one sprint)
4. **Business value** – the benefit is clear and linked to a FitRight KPI (see [Product Goal & KPIs](../README.md#product-goal--kpis))

Items were also checked against the [Definition of Ready](../docs/definition-of-ready.md) (DoR), which was introduced after the last review. PO decisions from the [decision log](../docs/po-decision-log.md) are respected: the **rejected** recommendations (size chart story, removing placeholder story points) are **not** proposed again.

---

## 0. Changes since the last review (2026-11-12)

- All 15 PO decisions were applied correctly: FR-004 → FR-004a, FR-010 closed, FR-015 → spike FR-015a, FR-008 and FR-013 converted into epics with first slices, discovery backlog and DoR created.
- The **7 open points** listed in the decision log (FR-001, FR-002, FR-003, FR-009, FR-011, FR-012, FR-014) are **still open** – none of the story files has changed since 2026-11-12. They are carried over into this report.
- Now that a DoR exists, the stories marked *Ready* can be checked against it. **None of the four R1 stories marked "Ready" fully meets the DoR yet** (see section 1).

---

## 1. Summary

| Story ID | Title | Status | Main issue |
|---|---|---|---|
| [FR-001](../backlog/FR-001.md) | Classify free-text return reasons | ⚠️ Needs work *(minor)* | Marked Ready, but the labeled test set for AC3 is still "to be created" (DoR #6); AC4 (removal of personal data) has no measurable pass criterion |
| [FR-002](../backlog/FR-002.md) | Fit hint on the product detail page | ❌ Needs work | **Logic flaw:** AC2 shows "True to size" when e.g. 55 % "too small" + 40 % "too large"; cases like 70 % "too tight" have no defined outcome |
| [FR-003](../backlog/FR-003.md) | Review and approve fit hints | ⚠️ Needs work *(minor)* | No lifecycle for approved hints when the data changes; "my categories" mapping undefined; no *Dependencies* section |
| [FR-004a](../backlog/FR-004a.md) | Import supplier size charts per article | ❌ Needs work | 3 open questions, not estimated by the team, CSV template not agreed; **no R1 story consumes the measurements** – R1 placement questionable |
| [FR-005](../backlog/FR-005.md) | A/B test for fit hint impact | ⚠️ Needs work *(minor)* | Marked Ready while its own note says "team to re-estimate" (DoR #7); guardrail defined twice (≥ 2.9 % vs. "no decrease vs. A") |
| [FR-006](../backlog/FR-006.md) | Personal size recommendation | ❌ Needs work | No quality gate (FR-008a/b have one, the base story does not); no tracking for KPI "recommendation adoption"; R2 categories not named; AC2b "more than one size" clause can never trigger |
| [FR-007](../backlog/FR-007.md) | Explain the size recommendation | ✅ Ready | Minor: behavior for guests with a session-only fit profile (FR-009 AC5) not stated – AC3 link to account settings does not apply to guests |
| [FR-008](../backlog/FR-008.md) | **Epic:** Expand FitRight recommendations | ✅ OK *(epic – not sprint-able)* | Goal, KPIs, slices and remaining scope are clear |
| [FR-008a](../backlog/FR-008a.md) | Personal size recommendation for menswear | ⚠️ Needs work *(minor)* | Two-dimensional sizes (waist/length 32/34) not handled; "2 kept menswear items" mixes tops and trousers; no outcome if quality gate fails |
| [FR-008b](../backlog/FR-008b.md) | Personal size recommendation for shoes | ⚠️ Needs work *(minor)* | History in different size systems (EU/UK/US) needs a conversion source – not listed; no outcome if quality gate fails; 8 SP at the limit |
| [FR-009](../backlog/FR-009.md) | Fit profile for new customers | ❌ Needs work | How height/weight/usual size become a size is undefined (hidden dependency on garment measurements, FR-004a); minimum input unclear; "supported category" undefined |
| [FR-011](../backlog/FR-011.md) | Consent and opt-out | ⚠️ Needs work *(minor)* | DPO sign-off open; re-ask after "Not now" undefined; unclear whether FR-009's "consent to store body data" is this consent or a second one |
| [FR-012](../backlog/FR-012.md) | Multi-size warning in the cart | ⚠️ Needs work *(minor)* | AC1 lacks the precondition "personal recommendation available" (conflicts with AC4); AC6 still links to a "size chart" that will not be built |
| [FR-013](../backlog/FR-013.md) | **Epic:** Return insights for Category Management | ✅ OK *(epic – not sprint-able)* | Goal, KPIs, first slice and remaining scope are clear |
| [FR-013a](../backlog/FR-013a.md) | Top fit problems in my category | ❌ Needs work | Story ranks by "share of size-related returns", AC1 ranks by "item return rate"; not estimated; "my categories" undefined |
| [FR-014](../backlog/FR-014.md) | "Did it fit?" feedback after delivery | ❌ Needs work | KPI "fit satisfaction ≥ 4.2 / 5" cannot be measured with a 3-option answer; AC3 ("same way as a kept or returned item") not testable; consent basis open |
| [FR-015a](../backlog/FR-015a.md) | Analyze wrong size recommendations (spike) | ✅ Ready | Meets DoR spike rules. Minor: needs ≥ 3 months of live R2 data **plus** the 30-day return window – add as dependency |
| FR-004, FR-010, FR-015 | *Closed / replaced* | – | Not reviewed (archived) |

**Result:** 17 active items reviewed · **4 Ready / OK** (FR-007, FR-015a, epics FR-008 and FR-013) · **7 Needs work – minor** · **6 Needs work – major** (FR-002, FR-004a, FR-006, FR-009, FR-013a, FR-014)

**Cross-cutting observations**

- **R1 is not sprint-ready.** All five R1 items have at least one open DoR point; FR-002 has a logic flaw that would show wrong hints to customers.
- **Shared definitions differ between stories:** minimum data ("30 classified size-related returns" in FR-002 vs. "30 returns" in FR-013a), "my categories" (FR-003, FR-013a), "category" for purchase history (FR-006, FR-008a), "supported category" (FR-009).
- **Quality gates and KPI tracking are inconsistent:** FR-008a/b have an 80 % accuracy gate, the base story FR-006 does not; no story tracks the KPI *recommendation adoption* (ordered size = recommended size).
- **Missing *Dependencies* sections** (DoR #5): FR-003, FR-004a, FR-014, FR-015a.

---

## 2. Stories that need work – problems and improved versions

ACs marked *unchanged* stay as they are in the story file.

### FR-001 – Classify free-text return reasons into fit categories

**Problems**
- Status *Ready*, but the labeled test set needed for AC3 is still "to be created together with Customer Service" → DoR #6 (external prerequisites) not fulfilled. *(open point from 2026-11-12)*
- AC4 says personal data "is removed", but there is no pass criterion – how is this verified?
- No defined outcome if the nightly job fails (DoR #4).

**Improved version** (story text unchanged)

> **As a** Category Manager,
> **I want** free-text return comments to be automatically classified into fit categories ("too small", "too large", "too tight", "too long", "too short", "true to size", "not fit-related"),
> **so that** I can see the real fit problems of an article instead of only the generic reason codes.

- **AC1 – AC3** – *unchanged*. **DoR prerequisite:** the labeled test set (1,000 comments) exists and is stored in the data warehouse before sprint start.
- **AC4 – Personal data**
  - **Given** a test set of 200 return comments containing names, phone numbers, e-mail and postal addresses
  - **When** the comments are processed
  - **Then** none of these values is contained in the text sent to the classification model (verified by an automated test)
- **AC5 – Job failure** *(new)*
  - **Given** the nightly classification job fails or does not finish by 06:00
  - **When** the failure is detected
  - **Then** the data team is alerted and the previous day's classification results remain in use (no partial data is published)

---

### FR-002 – Show fit hint on the product detail page

**Problems**
- **Logic flaw in AC2:** "True to size" is shown whenever no category exceeds 60 %. An article with 55 % "too small" and 40 % "too large" returns would be labeled "True to size" – a wrong statement to the customer.
- **Undefined cases:** if "too tight", "too long" or "too short" exceed 60 %, neither AC1 nor AC2 applies. *(open point from 2026-11-12)*
- "Size-related returns" is not defined (does "true to size" count? does "unclear" from FR-001 AC2 count?).

**Improved version**

> **As a** customer browsing a product page (persona: Lena),
> **I want** to see a short hint on how the item fits (e.g. "Runs small – we recommend one size up"),
> **so that** I can choose the right size before ordering and avoid a return.

**Definition:** *size-related returns* = returns classified as "too small", "too large", "too tight", "too long" or "too short" (FR-001). "True to size", "not fit-related" and "unclear" are excluded.

- **AC1 – Runs small / runs large**
  - **Given** an article has at least 30 size-related returns
  - **And** at least 60 % of them are "too small" (or "too large")
  - **When** I open the product detail page
  - **Then** I see "Runs small – we recommend one size up" (or "Runs large – we recommend one size down") directly above the size selector
- **AC2 – True to size**
  - **Given** an article has at least 30 classified returns
  - **And** size-related returns make up less than 20 % of all its classified returns
  - **When** I open the product detail page
  - **Then** I see the hint "True to size"
- **AC2b – Mixed or other fit problems** *(new)*
  - **Given** an article has at least 30 size-related returns
  - **And** neither AC1 nor AC2 applies (e.g. 55 % "too small" / 40 % "too large", or 70 % "too tight")
  - **When** I open the product detail page
  - **Then** no size hint is shown, and the article is listed for the Category Manager as "fit issue – no hint" (input for FR-013a)
- **AC3 – Not enough data** – *unchanged* (threshold: 30 size-related returns).
- **AC4 – Only approved hints** – *unchanged*.
- **AC5 – Mobile** – *unchanged*.

> The 20 % threshold in AC2 is a proposal – the PO and Category Management should agree on the value.

---

### FR-003 – Review and approve fit hints before publishing

**Problems**
- No lifecycle after approval: what happens when new returns change the proposed hint (e.g. "Runs small" → "True to size")? The approved hint would stay live and become wrong.
- How articles are mapped to "my categories" is not described. *(open point from 2026-11-12)*
- "Predefined alternative texts" (AC4) are not listed anywhere.
- No *Dependencies* section (DoR #5) although it depends on FR-001 and FR-002.

**Improved version** (story text unchanged)

> **As a** Category Manager,
> **I want** to review AI-generated fit hints for my category before they go live,
> **so that** customers only see hints that I consider correct and that do not damage the relationship with our suppliers.

- **AC1 – Review list**
  - **Given** I am logged in with the role "Category Manager" and am assigned to one or more categories in the PIM category assignment
  - **When** I open the "Fit Hints" view
  - **Then** I see all pending fit hints for articles in my assigned categories with article, brand, proposed hint, number of underlying returns and distribution of fit categories
- **AC2, AC3, AC5** – *unchanged*.
- **AC4 – Edit** – *unchanged*; the predefined texts are listed in the story (proposal: the three hints from FR-002 plus "Some customers find it small" / "Some customers find it large").
- **AC6 – Changed data** *(new)*
  - **Given** a hint is approved and live
  - **When** the daily generation job proposes a different hint for the article (FR-002 rules)
  - **Then** the live hint is removed from the product page, the new proposal appears as "pending" in my review list and the change is mentioned in the daily summary e-mail
- **Dependencies:** FR-001 (classification), FR-002 (hint rules).

---

### FR-004a – Import supplier size charts per article

**Problems**
- Three open questions (categories, mandatory measurements, CSV template) block implementation (DoR #6, #8); the 5 SP are a placeholder, not a team estimate (DoR #7).
- **Value / release fit:** none of the R1 stories (FR-001, FR-002, FR-003, FR-005) uses garment measurements – fit hints are based on returns only. The first consumer is the fit profile (FR-009, R2). The story is labeled the "R1 risk", but it may not be on the R1 critical path at all.
- AC2 "supported category" and AC4 "active articles" are undefined; no *Dependencies* section.

**Improved version** – *proposal; the PO decided on 2026-11-12 to keep the story in R1. This is raised as a question for the PO, not a change of that decision.*

> **As a** Category Manager Womenswear (persona: Markus),
> **I want** the garment measurements per size (chest, waist, hip, length in cm) to be imported from the supplier's size chart for every new article in Dresses & Tops,
> **so that** the fit profile recommendation (FR-009) can match customers' body data to real garment measurements, reducing size-related returns for first-time buyers.

- **AC1 – Import of valid size chart**
  - **Given** a supplier delivers a size chart in the agreed CSV template (version 1.0) for a new article in Dresses & Tops
  - **When** the article is created in the PIM
  - **Then** the measurements per size are stored with the article and visible in the backoffice article view
- **AC2 – Missing mandatory measurements**
  - **Given** the size chart lacks a mandatory measurement (Dresses: chest, waist, hip, length; Tops: chest, length)
  - **When** the import runs
  - **Then** the article is flagged "size data incomplete" and appears in the responsible Category Manager's list
- **AC3 – Implausible values** – *unchanged*.
- **AC4 – Coverage reporting**
  - **Given** the import has run for at least one week
  - **When** I open the size data report
  - **Then** I see, per category and supplier, the share of articles online in the shop with complete and plausible size data
- **Dependencies / prerequisites:** CSV template agreed with the top 10 suppliers of the category (before sprint start); consumer: FR-009.

> Categories and mandatory measurements above are proposals to make the story estimable – to be confirmed with the data team.

---

### FR-005 – Track fit hint impact with an A/B test

**Problems**
- Status *Ready*, but the story's own note says "team to re-estimate in refinement" – DoR #7 not yet met.
- The guardrail is defined twice: "PDP conversion ≥ 2.9 %" (absolute) and "no decrease vs. group A" (relative). The two can contradict each other.
- No defined decision after the test (roll out / stop) – what happens if the guardrail is breached?
- AC4: it should be explicit that non-consenting visitors see no hint **only during the test** – otherwise this becomes a permanent product decision.

**Improved version** (story text unchanged)

> **As a** Product Owner,
> **I want** fit hints to be rolled out as a 50/50 A/B test with tracking of hint views, orders and returns per test group,
> **so that** I can prove that fit hints reduce the item return rate of affected articles (hypothesis: –3 pp) without lowering PDP conversion.

- **AC1 – AC3, AC5** – *unchanged*. Guardrail in the success-metrics table: **PDP conversion in group B is not significantly lower than in group A** (the 2.9 % baseline is for reference only).
- **AC4 – Consent** – *unchanged*, plus: **And** after the test has ended, the fit hint is shown to all visitors independent of analytics consent (tracking events are still only sent with consent).
- **AC6 – Guardrail breach** *(new)*
  - **Given** the A/B test is running
  - **When** the weekly check shows a statistically significant drop in PDP conversion in group B
  - **Then** the PO is notified and can stop group B by configuration without a deployment

---

### FR-006 – Personal size recommendation for logged-in customers

**Problems**
- **No quality gate:** FR-008a and FR-008b require ≥ 80 % backtest accuracy before go-live – the base story that introduces the feature has none.
- **No tracking** for the KPI *recommendation adoption* (≥ 35 % of orders use the recommended size) – DoR #9.
- **R2 scope not named:** the epic FR-008 says R2 covers "the initial categories", but FR-006 does not say which ones. "Same category" in AC1 is also undefined (womenswear? dresses?).
- **AC2b:** a fit hint always shifts by exactly one size, so "a difference of more than one size" can never happen – the clause is untestable as written.
- AC3 (back-in-stock notification) may depend on a feature that does not exist yet – not listed as a dependency.
- With the additions, 8 SP is very likely exceeded → split (as already noted in the story).

**Improved version** – proposed split into two stories

> **FR-006a – Calculate personal size recommendation (womenswear)**
> **As a** logged-in customer with previous orders (persona: Lena),
> **I want** FitRight to calculate my size per article from the items I kept and returned,
> **so that** I can order the size that fits me without ordering several sizes.

- **AC1 – Data requirement:** **Given** I have consented (FR-011) and kept at least 2 items in the same product group (e.g. dresses, tops, trousers) of womenswear in the last 24 months, **When** a recommendation is requested for an article in this product group, **Then** a size is calculated.
- **AC2 – Kept and returned items** – *unchanged*.
- **AC2b – Fit hint:** **Given** my history-based size is L **And** the article has the approved fit hint "Runs large", **When** the recommendation is calculated, **Then** it is M. **And Given** my history-based size is the smallest (or largest) available size and the fit hint points further down (or up), **Then** no personal recommendation is calculated.
- **AC3 – Quality gate** *(new)*: **Given** a backtest on womenswear orders of the last 12 months, **When** the model is evaluated, **Then** ≥ 80 % of items ordered in the recommended size were kept; **otherwise** the feature is not switched on and the PO is informed.
- **AC4 – Performance** – *unchanged* (≤ 300 ms p95, page loads without the service).

> **FR-006b – Show personal size recommendation on the product page**
> **As a** logged-in customer (persona: Lena),
> **I want** to see my recommended size directly at the size selector,
> **so that** I pick the right size the first time.

- **AC1 – Display** – *as FR-006 AC1* ("Your recommended size: [size]" + highlighted).
- **AC2 – Size not available** – *as FR-006 AC3*; the back-in-stock option only if that feature already exists (add as dependency).
- **AC3 – Fallback** – *as FR-006 AC5*.
- **AC4 – Adoption tracking** *(new)*: **Given** a recommendation was shown, **When** I add an article to the cart and place the order, **Then** the order line stores `recommended_size` and `ordered_size`, so that the KPIs *recommendation adoption* and *recommendation accuracy* can be calculated.

---

### FR-008a – Personal size recommendation for menswear

**Problems**
- AC2 mentions waist/length sizes (32/34) – this is a **two-dimensional** size. It is not defined whether both waist and length are recommended (similar to shoe width, which was scoped out of FR-008b).
- AC1 "kept at least 2 menswear items" mixes size systems – kept tops say little about trouser waist size.
- AC3 quality gate has no outcome if it fails (DoR #4).

**Improved version** (story text unchanged)

> **As a** logged-in customer buying menswear,
> **I want** to see a personal size recommendation on menswear product pages,
> **so that** I order the right size the first time and do not need to return the item.

- **AC1 – Recommendation in menswear:** **Given** I am logged in, have consented (FR-011) and kept at least 2 items **of the same product group** (tops, trousers or jackets) in the last 24 months, **When** I open a product page of this product group, **Then** I see "Your recommended size: [size]" as in FR-006.
- **AC2 – Size systems:** **Given** the article uses a numeric size system (48/50/52) or a waist/length system (32/34), **When** the recommendation is calculated, **Then** it is shown in the article's own size system **And** for waist/length sizes both waist and length are recommended *(or: waist only with the note "Recommendation refers to waist only" – PO to decide)*.
- **AC3 – Quality gate** – *unchanged*, plus: **otherwise** the feature is not switched on for that product group.
- **AC4 – Fallback** – *unchanged*.

---

### FR-008b – Personal size recommendation for shoes (length only)

**Problems**
- AC2: the customer's history may be in a different size system (kept EU 39 from one brand, article in UK sizes). A conversion source (per brand) is needed but not listed as a dependency.
- AC4 quality gate has no outcome if it fails.
- 8 SP placeholder is at the upper limit – re-estimate; if higher, split off the UK/US conversion.

**Improved version** (story text unchanged)

> **As a** logged-in customer buying shoes,
> **I want** to see a personal shoe size recommendation on shoe product pages,
> **so that** I order the right shoe size the first time and do not need to return the shoes because they are too small or too large.

- **AC1, AC3, AC5** – *unchanged*.
- **AC2 – Shoe size systems:** **Given** my kept shoes and the article use different size systems (EU, UK, US, incl. half sizes), **When** the recommendation is calculated, **Then** the size is converted using the brand's conversion table **And** if no conversion table exists for the brand, no personal recommendation is shown.
- **AC4 – Quality gate** – *unchanged*, plus: **otherwise** the feature is not switched on and the PO is informed.
- **Dependencies:** add "brand size conversion tables for shoes (data team)".

---

### FR-009 – Fit profile for new customers

**Problems**
- **How the recommendation is calculated is undefined.** Turning height, weight and "usual size in one brand" into a size for another brand requires garment measurements or brand size mappings – a hidden dependency on FR-004a (not listed).
- AC2 lists weight and fit preference as inputs, AC3 makes them optional – the outcome with only the mandatory fields (height + usual size) is not defined. *(open point from 2026-11-12)*
- "Supported category" (AC1) is undefined.
- No quality gate (unlike FR-008a/b) and no tracking of questionnaire completion.

**Improved version**

> **As a** new customer without order history (persona: Lena, first order),
> **I want** to enter a few details about my body and fit preferences,
> **so that** I also receive a size recommendation for my first order and do not need to order two sizes.

- **AC1 – Entry point:** **Given** I have no order history and no fit profile, **When** I open a product page in a category with complete size data (FR-004a), **Then** I see the link "Find your size in 30 seconds".
- **AC2 – Minimum input:** **Given** I opened the questionnaire, **When** I enter only height and my usual size in one known brand and submit, **Then** I see a size recommendation for the current product.
- **AC2b – Optional input:** **Given** I additionally enter weight and/or fit preference, **When** I submit, **Then** these values are used to refine the recommendation (e.g. "loose" → one size up if between two sizes).
- **AC2c – No recommendation possible** *(new)*: **Given** the article has no complete size data or my usual-size brand is unknown, **When** I submit, **Then** I see "We can't recommend a size for this item yet" and the non-personal fit hint (FR-002) if available.
- **AC3 – Validation, AC4 – Save profile, AC5 – Guest usage** – *unchanged*.
- **AC6 – Quality gate** *(new)*: ≥ 80 % recommendation accuracy in a backtest / pilot before go-live (KPI *recommendation accuracy*).
- **Dependencies:** FR-011 (consent), **FR-004a (garment measurements)**.

---

### FR-011 – Consent and opt-out for personalized size recommendations

**Problems**
- DPO sign-off on the consent text is still pending (DoR #6). *(open point from 2026-11-12)*
- Behavior after "Not now" is undefined – will the dialog appear on every product page? *(open point from 2026-11-12)*
- FR-009 AC4 asks for "explicit consent to store body data"; FR-011 covers "order, return and body data". It is unclear whether these are one or two consents.
- AC3 deletes the fit profile on withdrawal – what about "Did it fit?" feedback (FR-014)?

**Improved version** (story text unchanged)

> **As a** customer,
> **I want** to decide whether my order, return and body data is used for size recommendations,
> **so that** I stay in control of my personal data.

- **AC1, AC4** – *unchanged*. **DoR prerequisite:** consent text version 1.0 signed off by the DPO.
- **AC1b – "Not now"** *(new)*: **Given** I selected "Not now", **When** I open further product pages, **Then** the dialog is not shown again for 30 days; I can opt in at any time in my privacy settings.
- **AC1c – Body data** *(new)*: **Given** I want to save a fit profile (FR-009), **When** I have not given separate consent for body data, **Then** a second, explicit consent for body data is requested (history-based recommendations stay possible without it). *(DPO to confirm: one or two consents.)*
- **AC2** – *unchanged*.
- **AC3 – Withdraw consent** – *unchanged*, plus: **And** my "Did it fit?" feedback (FR-014) is no longer used for recommendations.

---

### FR-012 – Warn when the same item is ordered in several sizes

**Problems**
- AC1 says "Based on your data, [size] should fit you best" but its *Given* does not require a personal recommendation – this overlaps with AC4 / AC6.
- AC6 links to "the size chart / fit profile questionnaire". The size chart story was rejected on 2026-11-12, so the link target must be the questionnaire only. *(open point from 2026-11-12)*
- Unclear whether a guest's session fit profile (FR-009 AC5) counts as "personal recommendation".

**Improved version** (story text unchanged)

> **As a** customer who is unsure about the size (persona: Lena),
> **I want** to be informed when I have the same item in my cart in several sizes and get help choosing one,
> **so that** I can avoid an unnecessary return.

- **AC1 – Warning in the cart:** **Given** my cart contains the same article (same color) in 2 or more sizes **And** a personal size recommendation (FR-006, or a session fit profile from FR-009) is available for this article, **When** I open the cart, **Then** I see "You have this item in [n] sizes. Based on your data, [size] should fit you best."
- **AC2 – AC5, AC7** – *unchanged*.
- **AC6 – Neither recommendation nor fit hint:** **Given** neither a personal recommendation nor an approved fit hint is available, **When** the cart contains the article in several sizes, **Then** the hint shows "You have this item in [n] sizes." with a link to the fit profile questionnaire (FR-009).

---

### FR-013a – Top fit problems in my category

**Problems**
- **Inconsistency:** the story wants the articles with the highest **share of size-related returns**; AC1 ranks by the highest **item return rate**. These lists differ (an article can have a high return rate because of colour or quality).
- Not estimated (DoR #7); "my categories" undefined (same gap as FR-003).
- AC5 uses "fewer than 30 returns", FR-002 uses "30 size-related returns" – different thresholds for the same idea.
- AC4 still says "dashboard".

**Improved version**

> **As a** Category Manager (persona: Markus),
> **I want** to see the articles in my categories with the most size-related returns, including the distribution of fit categories,
> **so that** I can address fit problems with suppliers during the season instead of waiting for the monthly report – and reduce size-related returns in my category.

- **AC1 – Article ranking:** **Given** I am logged in with the role "Category Manager" and assigned to categories in the PIM, **When** I open "Return Insights", **Then** I see the 50 articles of my categories with the highest **number of size-related returns** in the last 30 days, with columns: article, brand, supplier, shipped items, item return rate, share of size-related returns; sortable by each column.
- **AC2, AC3** – *unchanged*.
- **AC4 – Data freshness:** **Given** the nightly classification job (FR-001) has finished, **When** I open "Return Insights", **Then** the data includes all returns up to the previous day and the "data as of" date is shown.
- **AC5 – Minimum data:** **Given** an article has fewer than 30 size-related returns (same threshold as FR-002) in the selected period, **When** it is listed, **Then** it is marked "low data" and the fit distribution is shown greyed out.

---

### FR-014 – "Did it fit?" feedback after delivery

**Problems**
- **KPI mismatch:** the KPI *customer satisfaction with fit (≥ 4.2 / 5)* is measured with "the post-delivery 'Did it fit?' survey" – but this story only collects "too small / fits well / too large". The KPI cannot be calculated.
- AC3 "in the same way as a kept or returned item" is not testable – a **kept** item rated "too small" is neither.
- Consent basis ("marketing / service e-mails") unclear – needs DPO decision. *(open point from 2026-11-12)*
- "Fashion items" – are shoes included? One-click links without login need protection against manipulation.
- No *Dependencies* section (FR-006, FR-011).

**Improved version**

> **As a** customer who received an order (persona: Lena),
> **I want** to quickly tell the shop how the items fit,
> **so that** my future size recommendations become more accurate and I return fewer items.

- **AC1 – Feedback request:** **Given** my order was delivered 5 days ago **And** I have consented to service e-mails *(legal basis confirmed by the DPO)*, **When** the daily feedback job runs, **Then** I receive one e-mail "Did it fit?" for up to 3 clothing or shoe items of the order that I have not returned.
- **AC2 – One-click feedback:** **Given** I opened the e-mail, **When** I click "too small", "fits well" or "too large" for an item, **Then** my feedback is saved via a personal, single-use link (valid 30 days) without login and I see a thank-you page.
- **AC2b – Satisfaction rating** *(new)*: **Given** I am on the thank-you page, **When** I rate "How satisfied are you with the fit?" on a 1–5 scale, **Then** the rating is stored per item (KPI *customer satisfaction with fit*).
- **AC3 – Usage in recommendations:** **Given** I kept an item and rated it "too small" (or "too large"), **When** my next recommendation for this brand and product group is calculated, **Then** the item is treated like a return with reason "too small" (or "too large"); "fits well" is treated like a kept item.
- **AC4 – Returned items** – *unchanged*.
- **Dependencies:** FR-006 (recommendation logic), FR-011 (consent / withdrawal).

---

## 3. Top 3 recommendations for the next refinement meeting

1. **Make R1 really sprint-ready – starting with the FR-002 logic flaw.**
   All five R1 items still have open DoR points. Decide in the meeting: (a) the fit hint rules in FR-002 (definition of "size-related", the "True to size" condition and the mixed-signal case), (b) the hint lifecycle in FR-003 when data changes, (c) the date the labeled test set for FR-001 will be available, (d) the team re-estimate of FR-005. Also ask the PO to confirm whether FR-004a really belongs to R1 – no R1 story consumes garment measurements, so moving it to R2 (as a prerequisite of FR-009) would remove the "R1 risk" instead of managing it.

2. **Make the R2 recommendation measurable and its data basis explicit.**
   Add an 80 % accuracy quality gate and `recommended_size` / `ordered_size` tracking to FR-006 (as FR-008a/b already have), name the R2 categories, and split FR-006 into calculation (FR-006a) and display (FR-006b). Clarify with the data team how FR-009 turns body data into a size (dependency on FR-004a), and with the DPO whether body data needs a separate consent (FR-009 ↔ FR-011) – both before R2 refinement continues.

3. **Agree on shared definitions and close the KPI gaps.**
   Several stories define the same thing differently. Agree once (e.g. as a short glossary next to the DoR) on: minimum data threshold (30 size-related returns), "my categories" (PIM category assignment), "product group" for purchase history, and the outcome when a quality gate fails. Fix the two KPI gaps found in this review: FR-013a must rank by size-related returns (not return rate) and FR-014 must collect a 1–5 rating, otherwise the KPI *customer satisfaction with fit* cannot be measured. Add the missing *Dependencies* sections to FR-003, FR-004a, FR-014 and FR-015a.

---

*Generated by the weekly automated backlog review routine on 2026-11-16. Story files in `/backlog` were not modified. All proposals are input for the PO – "AI suggests, the PO decides".*
