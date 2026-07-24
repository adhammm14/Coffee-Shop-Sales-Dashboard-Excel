# Coffee Shop Sales Dashboard

**Microsoft Excel · PivotTables · Interactive Dashboard**

An interactive Excel dashboard analysing **149,116 transactions** and **$698,812 in revenue**
across three New York coffee shop locations over the first half of 2023 — built with
PivotTables, PivotCharts, and slicers to explore sales by location, product, time, and day.

---

## Dashboard

<!--
  ADD A SCREENSHOT HERE. GitHub shows .xlsx only as a downloadable file, so
  without an image nobody sees the dashboard without opening Excel.

  1. Open the workbook, go to the Dashboard tab.
  2. Screenshot it (Cmd+Shift+4 on Mac).
  3. Save it as dashboard.png next to this README.
  4. Uncomment the line below.
-->

<!-- ![Coffee Shop Sales Dashboard](dashboard.png) -->

---

## Headline Numbers

| Metric | Value |
|---|---|
| Total revenue | **$698,812** |
| Transactions | **149,116** |
| Units sold | **214,470** |
| Average transaction value | **$4.69** |
| Period covered | **Jan – Jun 2023** (181 days) |
| Locations | **3** — Hell's Kitchen, Astoria, Lower Manhattan |

---

## Key Findings

**1. Revenue grew 104% over six months.**
Monthly revenue climbed from **$81,678 in January** to **$166,486 in June** — more than
doubling. Growth accelerated in the spring: May (+32% MoM) and June were the two strongest
months, suggesting a seasonal uplift as the weather warmed.

**2. The three locations are near-identical in size.**
Hell's Kitchen ($236,511), Astoria ($232,244), and Lower Manhattan ($230,057) each contribute
roughly a third of revenue. No single store carries the business — a healthy, balanced
footprint with a spread of just 2.8% between the top and bottom performer.

**3. Coffee and Tea are two-thirds of the business.**
Coffee (38.6%) and Tea (28.1%) together drive **66.7%** of revenue. Bakery (11.8%) and
Drinking Chocolate (10.4%) round out the core, while retail lines — coffee beans, branded
goods, packaged chocolate — contribute under 10% combined.

**4. The morning rush is the entire day.**
The **8–10am** window alone generates **$256,543** — 37% of all revenue in three hours.
The 10am hour is the single busiest ($88,673). Demand falls off sharply after 11am and never
recovers to morning levels, confirming a commuter-driven, breakfast-led business.

**5. Sales are flat across the week.**
Revenue barely moves by weekday — every day falls between $96,894 (Saturday) and $101,677
(Monday), a spread under 5%. There is no weekend dip or spike, reinforcing that this is a
routine-driven commuter business rather than a leisure destination.

**6. Barista Espresso is the top product line.**
Barista Espresso ($91,406) leads all product types, followed by Brewed Chai Tea ($77,082) and
Hot Chocolate ($72,416). The top three lines alone account for over a third of revenue.

---

## What's in the Workbook

| Tab | Contents |
|---|---|
| `Dashboard` | Interactive dashboard — PivotCharts for revenue by month, transactions by weekday and hour, category breakdown, and a Top 15 products table, all driven by slicers |
| `Transactions` | The full 149,116-row transaction table, enriched with derived columns (month, weekday, hour) |

**Interactivity:** the dashboard uses slicers, so figures update when you filter by location or
category. (Totals shown for a single filtered location will be lower than the $698K grand total.)

---

## Data Model

The `Transactions` tab is one row per line item, with these fields:

| Field | Description |
|---|---|
| `transaction_id`, `transaction_date`, `transaction_time` | When the sale happened |
| `transaction_qty`, `unit_price`, `revenue` | What it was worth (`revenue = qty × unit_price`) |
| `store_id`, `store_location` | Which of the three shops |
| `product_category`, `product_type`, `product_detail` | Product hierarchy |
| `month`, `month_name`, `weekday`, `weekday_name`, `hour` | Derived time dimensions for pivoting |

---

## Skills Demonstrated

- Structuring a 149K-row dataset into a clean, pivotable table
- Deriving time dimensions (month, weekday, hour) to enable trend analysis
- Building PivotTables and PivotCharts across multiple dimensions
- Wiring slicers for interactive, self-service filtering
- Turning a raw transaction log into an executive-readable one-page dashboard

---

## About

Built as a portfolio project to demonstrate end-to-end analysis in Excel — from raw
transaction data to an interactive dashboard that answers real operational questions about
when, where, and what a coffee business sells.

*Dataset: Maven Analytics "Coffee Shop Sales" sample data.*
