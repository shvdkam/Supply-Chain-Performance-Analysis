# Supply Chain Performance Analysis

**Tableau | Supply Chain Analytics | Business Intelligence**

This project analyzes supply chain performance with a focus on sales, profitability, market contribution, order volume, and delivery efficiency.

The goal was to build an interactive Tableau solution that connects financial performance with operational efficiency and helps identify areas that may require management attention.

The project contains two dashboards:

- **Executive Overview** — financial and commercial performance
- **Delivery & Operations Performance** — delivery efficiency and operational performance

---

# Dashboards

## 1. Executive Overview

![Executive Overview](executive-overview.png)

The Executive Overview provides a high-level view of the company's financial and commercial performance.

### Key KPIs

| KPI | Result |
|---|---:|
| Total Sales | 36.5M zł |
| Sales YoY Growth | -4.0% |
| Total Profit | 3.93M zł |
| Profit Margin | 10.8% |
| Total Orders | 63.6K |
| Average Order Value | 573 zł |

The dashboard helps answer several important business questions:

- How are sales and profit performing?
- Is the business growing or declining?
- Which markets contribute the most to total sales?
- How do product categories compare in terms of sales and profitability?
- How do sales and profit change over time?

The dashboard can be filtered by **Year, Market, and Category**.

---

## 2. Delivery & Operations Performance

![Delivery & Operations Performance](delivery-operations.png)

The second dashboard focuses on delivery performance and operational efficiency.

### Key KPIs

| KPI | Result |
|---|---:|
| On-Time Delivery | 45% |
| Late Delivery Rate | 55% |
| Average Delivery Time | 3.5 days |
| Total Orders | 63.6K |

The dashboard helps analyze:

- late delivery rates across markets;
- on-time delivery performance by shipping mode;
- changes in delivery performance over time;
- order volume by shipping mode.

The dashboard can be filtered by **Year, Market, and Shipping Mode**.

---

# Tableau Workbook

The complete Tableau workbook is included in this repository.

**File:** [Supply Chain Performance Analysis.twbx](Supply%20Chain%20Performance%20Analysis.twbx)

Download and open the workbook in Tableau to explore the complete project, including dashboards, interactive filters, calculated fields, and individual worksheets.

---

# Key Findings

## 1. The company is profitable, but sales growth is negative

The company generated approximately **36.5M zł in total sales** and **3.93M zł in profit**, resulting in an overall **10.8% profit margin**.

However, the latest Sales YoY Growth is **-4.0%**.

This suggests that the company remains profitable, but the decline in sales should be monitored. If the trend continues, it may eventually affect overall profitability.

---

## 2. Europe and LATAM are the largest markets

Europe represents approximately **29.83% of total sales**, making it the largest market in the dataset.

LATAM follows closely with **28.19%**.

| Market | Sales Contribution |
|---|---:|
| Europe | 29.83% |
| LATAM | 28.19% |
| Pacific Asia | 21.79% |
| USCA | 13.90% |
| Africa | 6.29% |

Together, Europe and LATAM account for approximately **58% of total sales**.

This makes these two markets particularly important for the company's overall performance.

---

## 3. Sales and profit remain relatively stable over time

Monthly sales and profit fluctuate throughout the analyzed period, with several temporary peaks and declines.

There is no dramatic long-term collapse in performance.

However, the negative YoY sales growth indicates that the overall sales direction should continue to be monitored.

---

## 4. Category profitability varies

The category portfolio analysis shows that similar sales levels do not always generate similar profit margins.

Some categories generate significant sales while remaining around or below the average profitability level.

This shows why categories should be evaluated using both **sales and profitability**, rather than revenue alone.

---

# Delivery & Operations Findings

## 5. Delivery delays are the main operational issue

Only **45% of orders are delivered on time**, while approximately **55% are delivered late**.

This means that more than half of all deliveries fail to meet the expected delivery time.

A high late delivery rate may negatively affect customer satisfaction, customer retention, operational costs, and the overall customer experience.

---

## 6. Delivery problems exist across all markets

Late delivery rates are very similar across the analyzed markets.

| Market | Late Delivery Rate |
|---|---:|
| Europe | 55.2% |
| Pacific Asia | 55.0% |
| USCA | 54.8% |
| Africa | 54.6% |
| LATAM | 54.4% |

The difference between the highest and lowest market is less than one percentage point.

This suggests that delivery delays are not isolated to one specific market.

Instead, the issue appears to be connected with broader operational or supply chain processes.

---

## 7. Shipping mode has a major impact on delivery performance

Delivery performance varies significantly depending on the shipping mode.

| Shipping Mode | On-Time Delivery |
|---|---:|
| Standard Class | 62% |
| Same Day | 54% |
| Second Class | 23% |
| First Class | 5% |

**Standard Class performs best**, while **First Class has the weakest on-time delivery performance**.

The extremely low performance of First Class is particularly interesting because it is expected to represent a faster delivery option.

This suggests that faster shipping does not necessarily result in more reliable delivery.

---

## 8. Standard Class handles most orders

Standard Class accounts for the largest share of order volume.

| Shipping Mode | Orders |
|---|---:|
| Standard Class | 38,094 |
| Second Class | 12,333 |
| First Class | 9,751 |
| Same Day | 3,451 |

Standard Class handles significantly more orders than any other shipping mode while also achieving the strongest on-time delivery performance.

This suggests that high order volume itself is probably not the main reason for delivery delays.

---

## 9. Delivery performance has not improved significantly over time

The on-time delivery rate remains relatively stable throughout the analyzed period, generally staying around the mid-40% range.

There are short-term fluctuations, but no clear sustained improvement.

This suggests that delivery delays represent a persistent operational problem rather than a temporary issue.

---

# Business Recommendations

Based on the analysis, I would focus on the following areas.

## 1. Investigate First Class delivery performance

First Class has only a **5% on-time delivery rate**, making it the weakest shipping mode by a significant margin.

The company should investigate whether this is connected with:

- unrealistic promised delivery times;
- warehouse processing delays;
- carrier performance;
- fulfillment capacity;
- transportation or route planning.

---

## 2. Use Standard Class as a benchmark

Standard Class combines the **highest order volume** with the **strongest on-time delivery performance**.

Understanding what works well in this process could help identify improvements for First Class and Second Class.

---

## 3. Treat delivery performance as a company-wide issue

Late delivery rates are almost identical across markets.

Instead of focusing only on individual geographical regions, the company should review the overall fulfillment and logistics process.

---

## 4. Monitor negative sales growth

The company remains profitable, but the latest YoY sales growth is **-4.0%**.

Management should monitor sales performance by market and category to understand whether the decline is temporary or part of a longer trend.

---

## 5. Review category profitability

High sales do not always result in high profit margins.

Categories with strong sales but weaker profitability should be reviewed for possible improvements in:

- pricing;
- discounts;
- product mix;
- operational costs.

---

## 6. Set clear delivery performance targets

The current **45% on-time delivery rate** provides a clear baseline.

The company could establish a target for improving this KPI and continue monitoring performance by shipping mode over time.

---

# Overall Conclusion

The analysis shows a company that generates significant sales and remains profitable, but also faces several areas that require attention.

From a financial perspective, the business generated **36.5M zł in sales** with a **10.8% profit margin**. However, the negative **-4.0% YoY sales growth** may become a risk if the trend continues.

From an operational perspective, delivery performance represents the biggest concern. More than half of all orders are delivered late, and this problem appears across all markets.

Shipping mode has a much stronger relationship with delivery performance. Standard Class performs relatively well despite handling the largest number of orders, while First Class and Second Class show significantly weaker results.

Overall, the dashboards connect **financial performance with operational efficiency** and help identify areas where the company could improve both profitability and customer experience.

---

# Calculated Metrics

Several calculated fields were created in Tableau to support the analysis.

## On-Time Delivery

```text
IF [Late_delivery_risk] = 0 THEN
    1
ELSE
    0
END
```

The average of this calculated field represents the percentage of orders delivered on time.

---

## Late Delivery

```text
IF [Late_delivery_risk] = 1 THEN
    1
ELSE
    0
END
```

The average of this calculated field represents the late delivery rate.

---

## Profit Margin

```text
SUM([Profit]) / SUM([Sales])
```

This metric measures profit relative to total sales.

---

## Sales YoY Growth

```text
(
    SUM([Sales])
    - LOOKUP(SUM([Sales]), -1)
)
/
ABS(LOOKUP(SUM([Sales]), -1))
```

This calculation measures the year-over-year percentage change in sales.

---

# Tools & Skills

### Tools

- Tableau
- Tableau calculated fields
- Interactive filters
- Table calculations
- Dashboard design

### Analysis

- KPI analysis
- Sales analysis
- Profitability analysis
- Trend analysis
- Market analysis
- Category analysis
- Supply chain analysis
- Delivery performance analysis

### Skills Demonstrated

This project demonstrates my ability to:

- transform business data into meaningful KPIs;
- create calculated fields in Tableau;
- design interactive dashboards;
- analyze financial and operational performance;
- identify patterns and potential business problems;
- compare performance across different segments;
- translate analytical findings into business recommendations;
- communicate results through clear data visualizations.

---

# Project Structure

```text
Supply-Chain-Performance-Analysis/
│
├── README.md
├── Supply Chain Performance Analysis.twbx
├── executive-overview.png
└── delivery-operations.png

---

# About This Project

This project was created as part of my **Data Analytics portfolio**.

My goal was to practice the complete analytical process rather than only creating visualizations:

**Business Question → KPI Selection → Data Visualization → Analysis → Business Recommendation**

The project demonstrates how Tableau can be used to transform business and supply chain data into clear insights that can support decision-making.
