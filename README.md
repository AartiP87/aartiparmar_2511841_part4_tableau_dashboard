# Executive Sales Dashboard — README

**Currency:** All monetary values in USD millions ($Mn)

---

## Business Problem Summary

This project analyses two years of sales transaction data (January 2024 – December 2025) for a multi-region, multi-category retail business. The core business questions are:

- Where is the business growing, and where is it losing margin?
- Which regions, categories, and segments should receive investment vs. intervention?
- Are discounting and return patterns creating hidden value leakage?
- What should leadership prioritise in the next 90 days?

---

## Dataset Description

| Field | Type | Description |
|-------|------|-------------|
| order_id | String | Unique order identifier |
| order_date | Date | Date the order was placed |
| ship_date | Date | Date the order was shipped |
| customer_id | String | Unique customer identifier |
| customer_segment | Categorical | Consumer / Corporate / Home Office |
| region | Categorical | North / South / East / West |
| state | String | State name |
| city | String | City name |
| category | Categorical | Furniture / Office Supplies / Technology |
| sub_category | Categorical | 13 sub-categories |
| product_name | String | Individual product name |
| ship_mode | Categorical | Standard Class / Second Class / First Class / Same Day |
| sales | Numeric ($Mn) | Order revenue |
| quantity | Integer | Units ordered |
| discount | Numeric (0–1) | Discount rate applied |
| profit | Numeric ($Mn) | Net profit after discount and COGS |
| return_flag | Binary (0/1) | 1 = order was returned |
| delivery_days | Integer | Days between order date and ship date |
| customer_rating | Numeric (1–5) | Post-purchase satisfaction rating |
| campaign_channel | Categorical | Organic / Paid / Email / Social / Referral |

**Size:** 4,200 rows × 20 columns
**Date Range:** 1 Jan 2024 – 31 Dec 2025
**Source File:** `Data/Downloads/dashboard_sales_data.xlsx` (embedded in `executive_dashboard.twbx`)

---

## Tableau Workbook Description

**File:** `executive_dashboard.twbx` (Tableau Packaged Workbook)
**Data source embedded:** Yes
**Sheets included:**
- Sales Trend (dual-axis bar + line)
- Regional Performance (grouped bar + margin bar)
- Category Profitability (horizontal bar + grouped bar)
- Customer Segment Analysis (grouped bar)
- Discount Impact (bar with zero reference line)
- Ship Mode Performance (dual-axis bar + line)
- Campaign Channel Mix (pie chart)
- **Executive Dashboard** (compiled view of all 8 charts + 5 KPI cards)

---

## Calculated Fields Created

| Field Name | Formula / Logic | Purpose |
|------------|----------------|---------|
| Profit Margin % | `SUM([Profit]) / SUM([Sales])` | Margin KPI card and chart labels |
| Return Rate % | `SUM([Return Flag]) / COUNT([Order Id])` | Returns KPI card |
| Avg Delivery Days | `AVG([Delivery Days])` | Shipping KPI |
| Discount Band | Custom bins: 0%, 1-10%, 11-20%, 21-30%, 31-50%, 51%+ | Discount impact chart |
| Month-Year | `DATETRUNC('month', [Order Date])` | Time series x-axis |

---

## Dashboard Components

| # | Component | Chart Type | Key Figures |
|---|-----------|-----------|-------------|
| KPI 1 | Total Revenue | KPI Card | $217.02Mn |
| KPI 2 | Total Profit | KPI Card | $33.31Mn (15.3% margin) |
| KPI 3 | Total Orders | KPI Card | 4,200 |
| KPI 4 | Return Rate | KPI Card | 4.5% |
| KPI 5 | Avg Delivery Days | KPI Card | 3.6 days |
| Chart 1 | Monthly Sales & Profit Trend | Dual-axis Bar + Line | Peak: $10.86Mn (Aug 2025) |
| Chart 2 | Campaign Channel Mix | Pie Chart | Organic leads at $88.78Mn (40.9%) |
| Chart 3 | Regional Performance | Grouped Bar | South: $64.69Mn sales / $9.99Mn profit |
| Chart 4 | Sub-Category Profitability | Horizontal Bar | Copiers: $7.31Mn profit (highest) |
| Chart 5 | Customer Segment | Grouped Bar | Home Office: $74.50Mn / $11.56Mn |
| Chart 6 | Discount Impact | Bar + Zero Line | 31–50% band: –$0.002Mn avg profit |
| Chart 7 | Ship Mode | Dual-axis Bar + Line | Standard Class: 2,435 orders / 4.7 days |
| Chart 8 | Category Profitability | Grouped Bar + Labels | Technology: $153.90Mn / $28.04Mn / 18.2% |

---

## Filters and Interactions Used

| Filter | Type | Applied To |
|--------|------|-----------|
| Region | Quick Filter (dropdown) | All sheets |
| Category | Quick Filter (checkbox) | All sheets |
| Customer Segment | Quick Filter (dropdown) | All sheets |
| Order Date (Month-Year) | Range Slider | Trend charts |
| Ship Mode | Quick Filter (dropdown) | Ship mode chart + KPIs |
| Campaign Channel | Quick Filter (dropdown) | Channel chart + KPIs |

**Dashboard Action:** Click any regional bar → filters all other charts to that region (Filter Action: Source = Regional chart, Target = All sheets, Fields = Region).

---

## Key Business Insights

1. **Technology = 84% of total profit** — $28.04Mn of $33.31Mn at 18.2% margin
2. **Discounts above 30% are loss-making** — avg profit of –$0.002Mn per order in the 31–50% band
3. **South region leads** all others: $64.69Mn revenue / $9.99Mn profit
4. **East region is underperforming** — $48.86Mn revenue despite the highest margin (15.6%)
5. **Furniture return rate is 7.7%** — 2.6× higher than Technology — eroding its already-thin 6.9% margin
6. **Organic channel drives $88.78Mn (40.9% of revenue)** — a strength and a concentration risk
7. **Seasonal peaks in Jul–Aug and Oct–Nov** — $10.86Mn vs $7.19Mn trough in April (34% gap)
8. **All three customer segments have nearly identical margins** (~15.2–15.5%) — no premium pricing leverage

---

## Dashboard Story Summary

The business has built a $217.02Mn revenue base over two years, but the headline masks structural issues. Technology ($153.90Mn, 18.2% margin) is subsidising overall profitability while Furniture ($51.64Mn, 6.9% margin) and loss-making discounted orders (31–50% band: –$0.002Mn avg profit) actively destroy value. The South region demonstrates what a well-performing territory looks like; the East region has the margin quality to match it if given the right commercial investment. The most urgent leadership action is discount governance.

*Full story in: `outputs/dashboard_story.md`*

---

## Assumptions and Limitations

- Profit values are taken as given; COGS structure is not visible in the data
- Return reasons are not available — only a binary return flag
- Customer data is at order level only; no lifetime value (LTV) aggregation
- Campaign attribution is assumed single-touch (one channel per order)
- All monetary values displayed in USD millions ($Mn)
- Delivery days = ship_date – order_date; last-mile delivery not captured

---

## Screenshots Included

| File | Contents |
|------|----------|
| `screenshots/full_dashboard.png` | Complete 8-chart executive dashboard with 5 KPI cards |
| `screenshots/sales_trend_view.png` | Monthly sales and profit trend (Jan 2024 – Dec 2025) |
| `screenshots/regional_performance_view.png` | Regional sales, profit, and margin % comparison |
| `screenshots/category_profitability_view.png` | Category and sub-category profit breakdown |
| `screenshots/filter_interaction_view.png` | Filtered views: South / Technology / Corporate segment |

---

## Output Files

| File | Description |
|------|-------------|
| `outputs/business_insights.md` | 8 structured business insights with evidence and recommended actions |
| `outputs/dashboard_story.md` | Leadership narrative connecting all dashboard charts |
| `outputs/chart_selection_justification.md` | Design rationale for each of the 8 major charts |
| `README.md` | This file — full project documentation |
