# Dashboard Story — Executive Sales Review
### Prepared for: Senior Leadership Team
### Period: January 2024 – December 2025 | Source: dashboard_sales_data
### Currency: All monetary values in USD millions ($Mn)

---

## Executive Summary

Over the past two fiscal years, the business generated **$217.02Mn in total revenue** and **$33.31Mn in net profit**, representing a blended profit margin of **15.3%** across 4,200 orders. While top-line performance is solid and the Technology category is delivering exceptional returns, the dashboard reveals a business that is simultaneously growing and silently leaking value — through aggressive discounting, high Furniture returns, and an underperforming East region.

The data does not point to a business in crisis. It points to a business at a crossroads: the foundation is strong, but three or four structural decisions made in the next 90 days could determine whether the next two years sustain or erode the margins achieved so far.

---

## What Is Performing Well

**Technology is the profit engine.** Despite representing only 33% of total orders, Technology contributes 84% of total profit — $28.04Mn of $33.31Mn — at an 18.2% margin. Sub-categories Copiers ($7.31Mn profit), Accessories ($7.19Mn), and Phones ($7.10Mn) are all individually profitable at scale. This is the business's most valuable asset and deserves continued investment in range expansion and sales focus.

**The South region is the top-performing geography.** At $64.69Mn in revenue and a 15.4% profit margin generating $9.99Mn in profit, South outperforms all other regions in both volume and absolute profit. The region's consistent performance across all categories suggests a mature distribution network and strong customer relationships that the business should replicate elsewhere.

**Organic customer acquisition is working.** $88.78Mn — 40.9% of total revenue — arrives through organic channels, the highest of any single channel. This indicates strong brand awareness and product-market fit without heavy paid media reliance, reducing customer acquisition costs and improving overall unit economics.

**Same Day and First Class shipping demonstrate strong fulfilment capability.** Customers choosing premium shipping receive orders in under 2 days on average, and Same Day delivers in just 0.4 days. This operational capability is a competitive differentiator currently being underutilised by the majority of customers.

---

## What Is Underperforming

**Furniture is a margin liability.** At a 6.9% profit margin — compared to 18.2% for Technology — Furniture generates $51.64Mn in revenue but only $3.56Mn in profit. Worse, Furniture carries a 7.7% return rate (more than double Technology's 3.0%), which silently erodes an already thin margin through reverse logistics and restocking costs. The true effective margin on Furniture, once returns are accounted for, is likely below 5%.

**The East region is leaving revenue on the table.** East holds the highest margin of any region (15.6%) yet generates only $48.86Mn in revenue — trailing South by $15.83Mn. This divergence between margin quality and revenue volume is the clearest geographic growth opportunity in the dataset. The margin efficiency is there; the commercial investment is not.

**Discounting is destroying value at the high end.** Orders in the 31–50% discount band generate an average profit of –$0.002Mn per order — a loss. This means a segment of the sales team's activity is actively destroying value while appearing as revenue in top-line reports. Without governance, this pattern compounds as teams chase volume targets.

**Standard Class shipping dominates despite poor speed.** 58% of all orders use Standard Class with a 4.7-day average delivery. Given that First Class and Same Day already exist in the fulfilment infrastructure, the business is defaulting customers to a slower experience that likely suppresses satisfaction scores and repeat purchase rates.

---

## What Risks Are Visible

**1. Discount governance risk.** Without a formal cap on discounting, the trend toward loss-making orders will accelerate as sales teams pursue volume. A single quarter of aggressive discounting in a high-season period (Jul–Aug or Oct–Nov) could materially erode the $33.31Mn profit base.

**2. Channel concentration risk.** $88.78Mn — 40.9% of revenue — from a single Organic channel creates dangerous dependency. Any shift in search algorithms, competitive spending, or brand sentiment could impact revenue within a single quarter and is not within management's direct control.

**3. Furniture returns compounding.** At 7.7% return rate, Furniture's reported $3.56Mn profit overstates true contribution. Once reverse logistics and potential product write-offs are included, the category may be contributing significantly less — or in some sub-categories, net negative value.

**4. Seasonal revenue volatility.** A $3.67Mn gap between the weakest month (April 2025: $7.19Mn) and the strongest (August 2025: $10.86Mn) creates recurring working capital pressure. Without demand-smoothing mechanisms, the business faces cash flow stress bi-annually.

---

## What Opportunities Are Visible

**1. East region revenue expansion.** If East's revenue were brought in line with South's, the region could generate an additional $15–16Mn annually at its existing 15.6% margin — adding approximately $2.4Mn in incremental profit with no margin dilution.

**2. Premium shipping upsell programme.** Converting 10% of Standard Class orders to First Class — particularly on high-value Technology purchases — could meaningfully improve customer satisfaction while generating incremental shipping revenue. The fulfilment infrastructure already supports it.

**3. Referral programme launch.** Referral is currently the smallest channel at $21.21Mn in sales and $3.34Mn in profit. A structured referral incentive programme could realistically double this within 12 months, diversifying channel dependency at low acquisition cost.

**4. Technology cross-sell to Furniture buyers.** Customers purchasing Furniture are fitting out offices or workspaces — a natural purchase occasion for Technology accessories. Cross-sell prompts at checkout or in post-purchase communications could increase Technology attach rates and improve the overall basket margin.

---

## Recommended Business Actions

| Priority | Action | Owner | Timeframe |
|----------|--------|-------|-----------|
| 🔴 Critical | Implement discount governance: cap at 20%, require approval above 25% | Sales Director | 30 days |
| 🔴 Critical | Audit Furniture returns by SKU — identify top 3 root causes | Ops + Merchandising | 45 days |
| 🟠 High | Launch East-region sales initiative with targeted marketing budget | Regional VP | 60 days |
| 🟠 High | Design and pilot a referral programme for B2B customers | Marketing | 60 days |
| 🟡 Medium | Introduce First Class upgrade prompts for Technology orders above $0.025Mn | Product / eCommerce | 90 days |
| 🟡 Medium | Build seasonal demand planning model to pre-position inventory for Jul–Aug and Oct–Nov | Supply Chain | 90 days |
| 🟢 Ongoing | Expand Technology range, especially Copiers and Accessories | Buying | Rolling |

---

## Limitations of the Dashboard

- **No customer lifetime value (LTV) data.** The dataset tracks orders, not customers over time. Repeat purchase rates and churn are not visible.
- **No cost breakdown beyond profit.** We cannot separate COGS erosion from discount-driven margin loss without a full P&L.
- **Returns are binary.** The dataset does not capture return reason, resale value, or processing cost — making it impossible to calculate the true net cost of a return.
- **Campaign attribution is single-touch.** The `campaign_channel` field reflects how a customer first came to the business, not the full journey that led to conversion.
- **No intra-regional granularity.** Regional performance masks significant state-level variation. A single high-performing state can pull a region's average up.

---

## Suggested Next Analysis

1. **Customer cohort analysis** — Track revenue, margin, and return rate by acquisition cohort to identify which channels produce the highest-LTV customers.
2. **SKU-level Furniture margin analysis** — Decompose Furniture profitability to product level to identify which SKUs should be discontinued or repriced.
3. **Discount elasticity modelling** — Test whether revenue would hold if discounts were capped at 20%, using historical data to estimate price elasticity by category and segment.
4. **State-level geographic heat map** — Drill below region to state and city level to find white-space markets and high-concentration risks.
5. **Delivery speed vs. return rate correlation** — Test whether faster delivery reduces return probability to build the business case for subsidising shipping upgrades.

---

*This story was produced from executive_dashboard.twbx. All monetary values in USD millions ($Mn). Analysis period: January 2024 – December 2025.*
