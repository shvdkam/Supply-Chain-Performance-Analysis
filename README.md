
# Supply Chain Performance Analysis

## Tableau | Supply Chain Analytics | Business Intelligence

This project analyzes supply chain performance with a focus on sales, profitability, market contribution, order volume, and delivery efficiency.

The main goal was not only to visualize the data, but to build dashboards that help identify business performance patterns, operational problems, and areas that may require management attention.

Two interactive Tableau dashboards were created:

- **Executive Overview** — focused on overall financial and commercial performance.
- **Delivery & Operations Performance** — focused on delivery efficiency and shipping operations.

---

# 📊 Dashboards

## 1. Executive Overview

![Executive Overview](executive-overview.png)

The Executive Overview provides a high-level picture of business performance between **2015 and 2017**.

It combines the most important financial KPIs with sales trends, category performance, and market contribution.

### Key KPIs

| KPI | Result |
|---|---:|
| Total Sales | 36.5M zł |
| Sales YoY Growth | -4.0% |
| Total Profit | 3.93M zł |
| Profit Margin | 10.8% |
| Total Orders | 63.6K |
| Average Order Value | 573 zł |

### What this dashboard shows

The dashboard allows the user to quickly understand:

- how much revenue the business generates;
- how profitable the business is;
- whether sales are growing or declining;
- which markets contribute the most to sales;
- how categories compare in terms of sales and profitability;
- how sales and profit change over time.

The dashboard can also be filtered by **Year, Market, and Category**.

---

## 2. Delivery & Operations Performance

![Delivery & Operations Performance](delivery-operations.png)

The second dashboard focuses on operational efficiency and delivery performance.

It was created to understand how successfully orders are delivered and whether shipping mode or market may be connected with delivery problems.

### Key KPIs

| KPI | Result |
|---|---:|
| On-Time Delivery | 45% |
| Late Delivery Rate | 55% |
| Average Delivery Time | 3.5 days |
| Total Orders | 63.6K |

### What this dashboard shows

The dashboard compares:

- late delivery rates across markets;
- on-time delivery performance by shipping mode;
- changes in on-time delivery performance over time;
- total order volume handled by each shipping mode.

Filters allow the analysis to be adjusted by **Year, Market, and Shipping Mode**.

---

# 🔍 Key Findings

## 1. The business is profitable, but sales growth is negative

The company generated approximately **36.5M zł in sales** and **3.93M zł in profit**, with an overall profit margin of around **10.8%**.

However, **Sales YoY Growth is -4.0%**.

This means that the company is still profitable, but the decline in sales should be monitored. If this trend continues, it may eventually affect overall profitability.

---

## 2. Europe is the largest market by sales contribution

Europe represents approximately **29.83% of total sales**, making it the largest market in the dataset.

It is followed by:

| Market | Sales Contribution |
|---|---:|
| Europe | 29.83% |
| LATAM | 28.19% |
| Pacific Asia | 21.79% |
| USCA | 13.90% |
| Africa | 6.29% |

Europe and LATAM together account for a large share of total business activity.

This suggests that these markets are particularly important for overall company performance.

At the same time, heavy dependence on a few large markets can represent a business risk if demand in those regions decreases.

---

## 3. Sales and profit remain relatively stable over time

The monthly trend shows that sales and profit fluctuate throughout the analyzed period, but there is no dramatic long-term collapse.

There are several temporary peaks and declines, which may indicate seasonal effects or changes in order activity.

However, the negative YoY sales growth suggests that the overall direction should still be monitored carefully.

---

## 4. Category performance differs in profitability

The category portfolio analysis shows that categories with similar sales levels do not always generate the same profit margin.

Some categories generate relatively high sales but remain close to or below the average profitability level.

This is important because high revenue alone does not necessarily mean strong business performance.

Management should therefore evaluate categories using both **sales volume and profitability** rather than focusing only on revenue.

---

# 🚚 Delivery & Operations Findings

## 5. Delivery performance is the main operational concern

One of the strongest findings from the analysis is the high late delivery rate.

Only **45% of orders are delivered on time**, while approximately **55% are delivered late**.

This means that more than half of all orders experience delivery delays.

Such a high late delivery rate may negatively affect:

- customer satisfaction;
- customer retention;
- operational costs;
- brand reputation;
- future purchasing decisions.

Delivery performance should therefore be considered one of the main areas for operational improvement.

---

## 6. Late delivery rates are similar across markets

Late delivery rates are consistently high across all analyzed markets:

| Market | Late Delivery Rate |
|---|---:|
| Europe | 55.2% |
| Pacific Asia | 55.0% |
| USCA | 54.8% |
| Africa | 54.6% |
| LATAM | 54.4% |

The differences between markets are relatively small.

This is an important observation because it suggests that the delivery problem is probably **not isolated to one specific region**.

Instead, the issue may be connected with broader supply chain processes, logistics planning, carrier performance, or shipping strategy.

---

## 7. Shipping mode has a strong relationship with delivery performance

Delivery performance varies significantly depending on shipping mode.

| Shipping Mode | On-Time Delivery |
|---|---:|
| Standard Class | 62% |
| Same Day | 54% |
| Second Class | 23% |
| First Class | 5% |

**Standard Class performs best**, with approximately 62% of orders delivered on time.

At the same time, **First Class shows extremely weak on-time performance**, despite being expected to represent a faster delivery option.

This is one of the most interesting findings in the project.

It suggests that faster or premium shipping options do not necessarily result in better delivery reliability.

---

## 8. Standard Class handles most orders

Order volume is heavily concentrated in Standard Class.

| Shipping Mode | Orders |
|---|---:|
| Standard Class | 38,094 |
| Second Class | 12,333 |
| First Class | 9,751 |
| Same Day | 3,451 |

Standard Class handles by far the largest number of orders while also achieving the strongest on-time delivery performance.

This makes Standard Class particularly important from an operational perspective.

Its combination of **high volume and relatively strong delivery performance** may provide useful insights for improving other shipping modes.

---

## 9. On-time delivery performance remains relatively stable

The delivery trend remains around the mid-40% range for much of the analyzed period.

There are short-term fluctuations, but no clear sustained improvement.

This suggests that late deliveries may represent a persistent operational issue rather than a temporary problem.

---

# 💡 Business Recommendations

Based on the analysis, I would focus on several areas.

### Investigate First Class delivery performance

First Class has the weakest on-time delivery rate.

The company should investigate whether the problem is related to:

- unrealistic promised delivery times;
- carrier performance;
- warehouse processing delays;
- route planning;
- fulfillment capacity.

### Analyze why Standard Class performs better

Standard Class combines the highest order volume with the strongest on-time delivery performance.

Understanding what works well in this shipping mode could help improve other delivery options.

### Monitor the decline in sales

The company remains profitable, but negative YoY sales growth may become a risk if the trend continues.

Sales performance should be monitored by market and category to identify where the decline is coming from.

### Review category profitability

Categories should not be evaluated only by revenue.

Products or categories with strong sales but weaker margins may require pricing, discount, or cost optimization.

### Treat delivery performance as a company-wide issue

Because late delivery rates are similar across markets, the problem appears to be broader than a single geographical region.

This suggests that improvements should focus on the overall logistics process rather than only one market.

---

# 🎯 Overall Conclusion

The analysis shows a business that remains **profitable and generates significant sales volume**, but also faces two areas that deserve attention.

The first is the **decline in YoY sales growth**, which may become a financial risk if the trend continues.

The second — and more significant — issue is **delivery performance**.

More than half of orders are delivered late, and the problem appears across all markets.

The analysis also shows that shipping mode plays an important role in operational performance. Standard Class performs relatively well despite handling the largest number of orders, while First Class and Second Class show much weaker results.

Overall, the dashboards connect financial performance with operational efficiency and help identify where the company could improve both **profitability and customer experience**.

---

# 🛠 Tools Used

- **Tableau Public**
- Data visualization
- Dashboard design
- Calculated fields
- KPI development
- Filters
- Table calculations
- Business analysis
- Supply chain analytics

---

# 📐 Calculated Metrics

Several calculated fields were created during the analysis.

### On-Time Delivery

```text
IF [Late_delivery_risk] = 0 THEN
    1
ELSE
    0
END
```

This metric identifies whether an order was delivered on time.

---

### Late Delivery

```text
IF [Late_delivery_risk] = 1 THEN
    1
ELSE
    0
END
```

This metric was used to calculate the late delivery rate.

---

### Profit Margin

```text
SUM([Profit]) / SUM([Sales])
```

Used to evaluate profitability relative to sales.

---

### Sales YoY Growth

```text
(SUM([Sales]) - LOOKUP(SUM([Sales]), -1))
/
LOOKUP(SUM([Sales]), -1)
```

Used to measure the year-over-year change in sales.

---

# 📊 Dashboard Structure

The project contains two main dashboards.

### Executive Overview

Focuses on:

- Total Sales
- Sales YoY Growth
- Total Profit
- Profit Margin
- Total Orders
- Average Order Value
- Monthly Sales & Profit Trend
- Category Portfolio
- Sales Contribution by Market

### Delivery & Operations Performance

Focuses on:

- On-Time Delivery
- Late Delivery Rate
- Average Delivery Time
- Total Orders
- Late Delivery Rate by Market
- On-Time Delivery by Shipping Mode
- On-Time Delivery Trend
- Orders by Shipping Mode

---

# 🧠 Skills Demonstrated

This project demonstrates my ability to:

- transform raw business data into meaningful KPIs;
- create calculated fields in Tableau;
- build interactive dashboards;
- analyze sales and profitability;
- evaluate supply chain and delivery performance;
- identify patterns and operational problems;
- translate analytical results into business insights;
- communicate findings through clear data visualization.

---

# 📁 Project Files

```text
Supply-Chain-Performance-Analysis/
│
├── README.md
├── executive-overview.png
└── delivery-operations.png
```

---

# About the Project

This project was created as part of my Data Analytics portfolio.

My goal was to practice not only Tableau visualization, but also the full analytical process:

**business question → KPI selection → visualization → analysis → business recommendation**

The project demonstrates how Tableau can be used to turn operational and financial data into insights that can support business decisions.
