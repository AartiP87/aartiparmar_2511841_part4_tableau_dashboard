# Chart Selection Justification

**Dashboard:** Executive Sales Dashboard
**Dataset:** dashboard_sales_data | 4,200 orders | Jan 2024 – Dec 2025
**Currency:** All monetary values in USD millions ($Mn)

---

## Chart 1 — Monthly Sales & Profit Trend (Combo Bar + Line)

| Element | Detail |
|---------|--------|
| **Question answered** | How have sales and profit evolved month-over-month across two fiscal years? |
| **Chart type** | Dual-axis combo: bars for Sales, line for Profit |
| **Why appropriate** | Bars communicate volume magnitude for comparison. Overlaying a line on a secondary axis allows profit (a derived metric) to be tracked against revenue without visual confusion from two bar series at different scales. |
| **Color / encoding** | Blue bars (Sales $Mn), green line (Profit $Mn); both axes clearly labelled |
| **Key values** | Peak: Aug 2025 $10.86Mn sales / $1.74Mn profit. Trough: Apr 2025 $7.19Mn sales / $0.89Mn profit |
| **Design principle applied** | Dual axis used only where series have genuinely different scales; both axes labelled clearly |
| **Mistake avoided** | Did not use two bar series on the same axis (illegible at different scales); did not use a line/line combo (obscures volume magnitude) |

---

## Chart 2 — Campaign Channel Mix (Pie Chart)

| Element | Detail |
|---------|--------|
| **Question answered** | What proportion of total sales comes from each acquisition channel? |
| **Chart type** | Pie chart |
| **Why appropriate** | Pie charts are appropriate for ≤5 categories when the viewer needs part-to-whole composition. With 5 channels it communicates Organic's 40.9% dominance ($88.78Mn) at a glance. |
| **Color / encoding** | Five distinct palette hues; percentage labels inside each wedge |
| **Key values** | Organic $88.78Mn (40.9%), Paid $40.11Mn (18.5%), Email $34.51Mn (15.9%), Social $31.10Mn (14.3%), Referral $21.21Mn (9.8%) |
| **Design principle applied** | Part-to-whole composition; limited to ≤5 slices for readability |
| **Mistake avoided** | Did not use a pie for sub-categories (13 items — too many); did not use 3D pie which distorts area perception |

---

## Chart 3 — Regional Sales & Profit Performance (Grouped Bar)

| Element | Detail |
|---------|--------|
| **Question answered** | Which regions generate the most revenue and profit? |
| **Chart type** | Grouped bar chart (2 bars per region) |
| **Why appropriate** | Grouped bars allow direct comparison of two related metrics across 4 categories simultaneously. Sorted descending by Sales provides immediate ranking. |
| **Color / encoding** | One hue per region, consistent; Profit bars at 45% opacity to signal they are a subset of the same metric family |
| **Key values** | South: $64.69Mn sales / $9.99Mn profit. East: $48.86Mn sales / $7.60Mn profit (highest margin at 15.6%) |
| **Design principle applied** | Consistent color per category across the full dashboard; sorted for readability; value labels on bars for precision |
| **Mistake avoided** | Did not use a stacked bar (makes cross-region profit comparison impossible); did not rely solely on a map (loses the profit dimension) |

---

## Chart 4 — Sub-Category Profitability (Horizontal Bar)

| Element | Detail |
|---------|--------|
| **Question answered** | Which sub-categories are the most and least profitable? |
| **Chart type** | Horizontal bar chart, sorted ascending by profit |
| **Why appropriate** | Horizontal bars are ideal for long category labels. Ascending sort puts least profitable at top, most profitable at bottom — the natural reading direction for "what to fix" vs "what to scale". |
| **Color / encoding** | Green for positive profit, orange for negative; bar length encodes magnitude in $Mn |
| **Key values** | Copiers $7.31Mn (highest), Paper $0.32Mn (lowest). All sub-categories are profitable. |
| **Design principle applied** | Color used semantically (green = healthy, orange = at risk) rather than decoratively |
| **Mistake avoided** | Did not use vertical bars (label truncation); did not alphabetise (removes business ranking); did not combine sales and profit on the same chart here (single-metric view maximises clarity) |

---

## Chart 5 — Customer Segment Sales vs Profit (Grouped Bar)

| Element | Detail |
|---------|--------|
| **Question answered** | Do different customer segments have materially different revenue or profit contributions? |
| **Chart type** | Grouped bar chart |
| **Why appropriate** | With only 3 segments, grouped bars allow side-by-side comparison of both metrics without visual complexity. Bar height differences are immediately perceptible. |
| **Color / encoding** | Blue for Sales ($Mn), green for Profit ($Mn) — consistent with dashboard-wide color vocabulary |
| **Key values** | Home Office: $74.50Mn / $11.56Mn (15.5%). Consumer: $71.89Mn / $11.03Mn (15.3%). Corporate: $70.63Mn / $10.72Mn (15.2%) |
| **Design principle applied** | Consistent color vocabulary maintained throughout — blue = sales, green = profit |
| **Mistake avoided** | Did not use a pie per segment (6 pies required); did not stack the segments (destroys individual comparison) |

---

## Chart 6 — Discount Impact on Average Profit (Bar Chart)

| Element | Detail |
|---------|--------|
| **Question answered** | What is the relationship between discount level and average order profit? |
| **Chart type** | Single-series vertical bar with semantic coloring and zero reference line |
| **Why appropriate** | An ordered categorical x-axis (discount bands 0%→51%+) with a single metric (avg profit $Mn) produces a clear visual slope making the discount-to-profit decay immediately obvious. |
| **Color / encoding** | Green bars for positive profit, orange for negative; dashed horizontal zero reference line |
| **Key values** | 0% discount: avg $0.013Mn profit per order. 31–50% discount: avg –$0.002Mn per order (loss-making) |
| **Design principle applied** | Reference line anchors interpretation; semantic color drives action; chart answers a specific business question without decorative elements |
| **Mistake avoided** | Did not omit the zero line (which would mask the negative-profit revelation); did not use a scatter plot (harder for executive reading) |

---

## Chart 7 — Ship Mode Volume & Avg Delivery Days (Dual-Axis Combo)

| Element | Detail |
|---------|--------|
| **Question answered** | How are orders distributed across ship modes, and how does delivery time differ by mode? |
| **Chart type** | Bar (order count) + diamond marker line (avg delivery days) on dual axis |
| **Why appropriate** | Volume and delivery time are related but measured on different scales. Dual-axis communicates both in one view without requiring cross-referencing of two separate charts. |
| **Color / encoding** | Purple bars for order volume; orange diamonds for delivery days (orange signals urgency/time) |
| **Key values** | Standard Class: 2,435 orders / 4.7 days. Same Day: 241 orders / 0.4 days. First Class profit: $4.64Mn |
| **Design principle applied** | Dual axes clearly labelled; diamond markers differentiate from Chart 1's round markers |
| **Mistake avoided** | Did not normalise axes (would falsely imply a linear correlation); did not use a table (loses the visual pattern of delivery-time spread) |

---

## Chart 8 — Category Profitability Breakdown (Grouped Bar + Margin Labels)

| Element | Detail |
|---------|--------|
| **Question answered** | How do the three product categories compare in absolute sales, profit, and margin? |
| **Chart type** | Grouped bar + inline margin % annotation |
| **Why appropriate** | Three categories is ideal scope for grouped bars. Adding profit margin as a text annotation on the Profit bar introduces a third data dimension (ratio) without a third axis. |
| **Color / encoding** | One hue per category consistent with Chart 4; Profit bars at 40% opacity of Sales bars; margin % in grey text |
| **Key values** | Technology: $153.90Mn sales / $28.04Mn profit / 18.2% margin. Furniture: $51.64Mn / $3.56Mn / 6.9% margin |
| **Design principle applied** | Annotation replaces a third chart axis; consistent category color across Charts 4 and 8 |
| **Mistake avoided** | Did not use a 100% stacked bar (destroys absolute comparison); did not use three separate charts (forces cognitive switching) |

---

## General Design Principles Applied Across All Charts

| Principle | Implementation |
|-----------|----------------|
| **Minimal clutter** | No gridlines, no chart borders, no tick marks on redundant axes |
| **Consistent color vocabulary** | Blue = Sales, Green = Profit/Positive, Orange = Warning/Negative/Time, Purple = Volume/Operations |
| **Clear hierarchy** | Bold chart titles stating the business question; muted axis labels; faint reference lines |
| **Appropriate sorting** | All bar charts sorted by the primary metric, never alphabetically |
| **Business-friendly formatting** | All values in $Mn (e.g. $10.86Mn, $28.04Mn) — no raw large numbers |
| **No misleading scales** | Dual axes always labelled; zero baseline maintained on all bar charts |
| **Readable titles** | Each chart title states the question it answers, not just the metric name |
| **Semantic color** | Green = healthy/positive, Orange = risk/negative — applied consistently, not decoratively |
