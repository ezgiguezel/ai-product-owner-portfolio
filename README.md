# FitRight – AI-Powered Fit Guidance to Reduce Fashion Returns

> **Portfolio note:** FitRight is a fictional product created to demonstrate how I work as a Product Owner and how I use AI in my day-to-day PO work. All company names, figures and baselines are illustrative assumptions.

---

## Table of Contents

- [Product Vision](#product-vision)
- [Problem](#problem)
- [Target Group](#target-group)
- [Personas](#personas)
- [Product Goal & KPIs](#product-goal--kpis)
- [Roadmap](#roadmap)
- [Product Backlog](#product-backlog)
- [AI Workflows](#ai-workflows)

---

## Product Vision

**For** online fashion shoppers **who** are unsure which size will fit them,
**FitRight** is an AI-powered fit assistant embedded in the shop
**that** recommends the right size, explains how an item fits and nudges customers away from "bracketing" (ordering several sizes).
**Unlike** static size charts, FitRight learns from each customer's purchase and return history and from the return reasons of thousands of other customers.

**Vision statement:** *Every customer orders the right size the first time – so fewer parcels travel back, customers are happier and the business is more profitable and sustainable.*

### Core capabilities

| Capability | Description |
|---|---|
| **Personal size recommendation** | Suggests a size per product, based on the customer's kept and returned items, optional body data and aggregated return reasons. |
| **Fit hints on the product page** | Shows insights such as "Runs small – 64 % of customers recommend one size up", generated from structured and free-text return reasons. |
| **Multi-size order warning** | Detects when the same item is in the cart in several sizes and offers a recommendation instead of a bracketing order. |

---

## Problem

Germany is one of Europe's leaders in e-commerce returns, and fashion is the category hit hardest. Research by the *Retourenforschung* group at the University of Bamberg estimates that hundreds of millions of parcels are returned in Germany every year, and fashion return rates of **40–50 %** are commonly reported for German online fashion retailers. Free returns are a customer expectation, so the cost lands entirely on the retailer.

**Wrong size or poor fit is the most frequently cited return reason in fashion.** As a result, many customers deliberately order the same item in two or three sizes and send back what doesn't fit.

### Impact for our (fictional) shop

| Area | Impact |
|---|---|
| **Cost** | Every return costs shipping, handling, inspection and repackaging – often an estimated €10–20 per parcel. Some returned items can only be sold at a discount or not at all. |
| **Margin** | High return rates turn many orders unprofitable, especially in low-price categories. |
| **Customer experience** | Ordering, trying on, repacking and waiting for refunds is frustrating – customers who have to return often buy less often. |
| **Sustainability** | Additional transport, packaging and disposal of returned goods contradict our sustainability commitments. |
| **Merchandising** | Category Management lacks structured insight into *why* specific articles are returned and therefore can't act on it with suppliers. |

### Assumed baseline (fictional)

- Return rate (fashion, by item): **48 %**
- Share of returns with reason "too small / too large / doesn't fit": **~55 %**
- Share of orders containing the same article in ≥ 2 sizes: **~18 %**
- Conversion rate on product detail pages (PDP → order): **2.9 %**

---

## Target Group

**Primary:** Customers of our online fashion shop in Germany (DACH), predominantly 25–45 years old, who buy apparel online several times per year and are uncertain about sizes across brands.

**Secondary (internal):**
- **Category Management / Buying** – needs return insights per article and brand to improve the assortment and supplier size specifications.
- **Customer Service** – wants fewer "which size should I take?" requests.
- **Logistics / Returns Handling** – benefits from lower return volume.
- **Finance & Sustainability** – track the cost and CO₂ impact of returns.

---

## Personas

### Persona 1 – Lena, the uncertain online shopper

| | |
|---|---|
| **Age / Location** | 32, Cologne |
| **Occupation** | Marketing Manager |
| **Shopping behavior** | Orders fashion online 1–2 times per month, mostly on mobile in the evening. Buys from 5–6 different brands. |
| **Quote** | *"I'm an M in one brand and an L in the next. So I just order both – and then I have to go to the parcel shop again."* |

**Goals**
- Find clothes that fit without having to order several sizes.
- Spend less time on returns and waiting for refunds.
- Shop more sustainably.

**Pain points**
- Size charts are inconsistent across brands and hard to apply to her body.
- Reviews mention fit ("runs small") but are buried and contradictory.
- Returns cost her time; she feels guilty about the environmental impact.

**What FitRight must do for Lena**
- Give a clear, trustworthy size recommendation with a short explanation.
- Warn her *before* she orders two sizes – without patronizing her.
- Respect her data: transparent and easy to opt out.

---

### Persona 2 – Markus, Category Manager Womenswear

| | |
|---|---|
| **Age / Location** | 41, Hamburg (head office) |
| **Role** | Category Manager Womenswear (Dresses & Tops) |
| **Responsibilities** | Assortment planning, supplier negotiations, margin and return-rate targets for his category. |
| **Quote** | *"I know that some dresses have a 60 % return rate – but I don't know whether it's the size, the material or the photos. Without that, I can't push suppliers to change anything."* |

**Goals**
- Reduce the return rate in his category to meet his margin targets.
- Get reliable, article-level insight into fit problems.
- Have data-backed arguments for supplier talks (e.g. "your size 38 is cut like a 36").

**Pain points**
- Return reasons are in a data warehouse, free text is not analyzed at all.
- Reports arrive monthly – too late to react during a season.
- No influence on what customers see on the product page.

**What FitRight must do for Markus**
- Surface articles with fit problems early, with aggregated reasons.
- Let him review and, if needed, correct AI-generated fit hints before they go live.
- Show the effect of FitRight on returns in his category.

---

## Product Goal & KPIs

**Product Goal (next 12 months):**
> *Reduce size-related returns in fashion by helping customers choose the right size the first time – measurably lowering the return rate without hurting conversion.*

| KPI | Baseline (assumed) | Target after 12 months | How measured |
|---|---|---|---|
| **Return rate (fashion, item-based)** | 48 % | **≤ 42 %** (–6 pp) | Returned items / shipped items, A/B test vs. control group |
| **Size-related returns** (share of all returns) | 55 % | **≤ 45 %** | Return reason codes + classified free text |
| **Multi-size orders** (same article, ≥ 2 sizes) | 18 % of orders | **≤ 12 %** | Order line analysis |
| **PDP conversion rate** | 2.9 % | **≥ 2.9 %** (no decrease; stretch: +0.2 pp) | Orders / PDP sessions |
| **Recommendation adoption** | – | **≥ 35 %** of orders use the recommended size | Ordered size = recommended size |
| **Recommendation accuracy** | – | **≥ 80 %** of items ordered in the recommended size are kept | Kept / ordered in recommended size |
| **Customer satisfaction with fit** | – | **≥ 4.2 / 5** | Post-delivery "Did it fit?" survey |

**Guardrails:** No decline in average order value; no increase in customer service contacts related to sizes; GDPR-compliant processing with explicit consent for body data.

---

## Roadmap

A rough, outcome-oriented roadmap. Scope is refined continuously in the backlog.

### Release 1 – "Fit Insights" (MVP) · Q1
*Goal: Validate that fit information on the product page reduces size-related returns.*
- Fit hints on the PDP based on aggregated return reasons ("runs small / large / true to size")
- AI classification of free-text return reasons into fit categories
- Review workflow for Category Management before hints go live
- Tracking & A/B test setup

### Release 2 – "My Size" · Q2
*Goal: Personal size recommendations for logged-in customers.*
- Personal size recommendation based on purchase and return history
- Optional fit profile (height, weight, fit preference) for new customers
- Explanation of the recommendation ("Based on 3 items you kept from this brand")
- Consent & privacy settings, fallback when data is insufficient

### Release 3 – "Order Right" · Q3
*Goal: Reduce bracketing and close the feedback loop.*
- Multi-size warning in the cart with a one-click size choice
- Post-delivery "Did it fit?" feedback to improve the model
- Return insights dashboard for Category Management
- Expansion to further categories (shoes, menswear)

---

## Product Backlog

The product backlog lives in [`/backlog`](backlog/README.md). Each user story is a separate Markdown file (`FR-001.md` … `FR-015.md`).

---

## AI Workflows

*Coming soon – this section will document how I use AI as a Product Owner (e.g. backlog refinement, story quality checks, acceptance criteria generation, stakeholder communication).*
