# Supply chain performance analysis (Tableau)

In this project I looked at a supply chain dataset from two sides: money (sales, profit, markets, categories) and delivery (how many orders arrive on time and what affects it). I built two Tableau dashboards and wrote down what I found and what I would recommend to the company.

**Interactive dashboards on Tableau Public:** [Supply Chain Performance Analysis](https://public.tableau.com/app/profile/margarita.shved/viz/SupplyChainPerformanceAnalysis_17872519682360/ExecutiveOverview)

## Data

Dataset: DataCo Smart Supply Chain for Big Data Analysis, downloaded from Kaggle. Original source: Constante, F., Silva, F., Pereira, A. (2019), Mendeley Data, https://doi.org/10.17632/8gx2fvg2k6.5 (licence CC BY 4.0).

I loaded the data into Tableau from an Excel file and used orders from 2015 to 2017 (orders from 2018 are not included), so the YoY growth compares 2017 with 2016. For the delivery metrics I left out cancelled orders, because they were never delivered.

The dataset doesn't say which currency it uses. Most analyses of it treat the amounts as US dollars, so I do the same here.

The Tableau workbook is also in this repo: [Supply Chain Performance Analysis_.twbx](Supply%20Chain%20Performance%20Analysis_.twbx). Download it and open it in Tableau Public or Tableau Desktop to use the filters and see the calculated fields.

## Dashboard 1: Executive Overview

![Executive Overview dashboard](executive%20overview.png)

KPI cards, monthly sales and profit trend, category portfolio (sales vs profit margin) and sales contribution by market. Filters: year, market, category.

Total sales are about $36.5M and profit is $3.93M, so the profit margin is 10.8%. There are 63.6K orders and the average order value is $573. The latest year-over-year sales growth is -4.0%.

## Dashboard 2: Delivery & Operations Performance

![Delivery and Operations dashboard](delivery-operations.png)

KPI cards, late delivery rate by market, on-time delivery by shipping mode, on-time delivery trend and orders by shipping mode. Filters: year, market, shipping mode.

Of the orders that were actually shipped, 43% arrived on time and 57% were late. Average delivery time is 3.5 days. Cancelled orders (2,769, or 4.4%) are left out of the on-time and late rates, because they were never delivered.

## What I found

**The company makes a profit, but sales went down.** A 10.8% margin is fine, but -4.0% YoY growth is worth watching. If the trend continues, profit will drop too.

**Two markets bring most of the money.** Europe has 29.83% of sales and LATAM 28.19%, together about 58%. Pacific Asia has 21.79%, USCA 13.90% and Africa 6.29%.

**Monthly sales and profit go up and down, but there is no big fall over the period.** So the -4.0% is a slow decline, not a crash.

**Eight categories make 86% of sales, and their margins are almost the same.** Fishing alone is 19% of sales ($6.93M). The top eight are Fishing, Cleats, Camping & Hiking, Cardio Equipment, Women's Apparel, Water Sports, Men's Footwear and Indoor/Outdoor Games, and their margins are all between 10.4% and 11.2% (the overall margin is 10.8%). So profit depends mostly on how much these categories sell, not on which categories the company sells.

The biggest differences in margin are in small categories with under $100K in sales. The highest are Sporting Goods (17.7%) and Golf Bags & Carts (17.5%). The lowest are Strength Training (0.6%) and As Seen on TV! (3.5%). No category has a negative margin.

**Late delivery is the biggest operational problem, and it's the same everywhere.** The late rate in every market is between 56.8% (Africa) and 57.7% (Europe). The gap is less than one percentage point, so the cause is not in one region. The on-time rate also stays around 40–45% for the whole period and doesn't improve.

**Shipping mode makes the biggest difference:**

| Shipping mode | Orders | Promised (days) | Actual (avg days) | On time |
|---|---:|---:|---:|---:|
| Standard Class | 38,094 | 4 | about 4 | 60% |
| Same Day | 3,451 | 0 | under 0.5 | 52% |
| Second Class | 12,333 | 2 | about 4 | 20% |
| First Class | 9,751 | 1 | 2 | 0% |

## Why First Class is never on time

This was the most surprising part, so I checked it in more detail.

First Class promises delivery in 1 day, but the average actual delivery time is exactly 2 days, and not one of the 9,281 delivered First Class orders arrived on time. Second Class has a similar problem: it promises 2 days and takes about 4. Standard Class promises 4 days and takes about 4, and it has the best result even though it handles the most orders.

So the delays don't come from too many orders or from one market. The faster shipping modes promise a delivery time that the logistics can't meet.

My first version of the dashboard showed 5% on-time delivery for First Class. When I split the orders by `Delivery Status`, I saw that this 5% was exactly the cancelled orders (470 of 9,751). The `Late_delivery_risk` column marks cancelled orders as "not late", so my on-time metric counted them as delivered on time. I changed the calculated fields so cancelled orders are excluded. This moved the overall on-time rate from 45% to 43% and First Class from 5% to 0%.

## What I would recommend

1. Change the promised delivery time for First Class and Second Class to what the logistics can really do (2 and about 4 days), or make the actual delivery faster. Right now every First Class customer gets a promise that is broken.
2. Use Standard Class as the benchmark: its promise matches the real delivery time, and that's why it performs best.
3. Treat delivery as a company-wide issue. Since all markets have almost the same late rate, fixing one region won't help much.
4. Set a target for on-time delivery and track it by shipping mode. 43% is the starting point.
5. Follow sales by market and category every month to see if the -4.0% is a short dip or a longer trend.
6. Focus growth on the big categories (Fishing, Cleats, Camping & Hiking), because their margin is stable. Check pricing in Strength Training (0.6% margin) and As Seen on TV! (3.5%), but these are small and won't change the total much.

## Calculated fields

On-time and late delivery are based on the `Late_delivery_risk` column. Cancelled orders get NULL, so they are not counted. The average of each field gives a percentage.

```
// On-Time Delivery
IF [Delivery Status] = "Shipping canceled" THEN NULL
ELSEIF [Late_delivery_risk] = 0 THEN 1
ELSE 0
END

// Late Delivery
IF [Delivery Status] = "Shipping canceled" THEN NULL
ELSEIF [Late_delivery_risk] = 1 THEN 1
ELSE 0
END

// Profit Margin
SUM([Benefit per order]) / SUM([Sales])

// Average Order Value
SUM([Sales]) / COUNTD([Order Id])

// Sales YoY Growth
(SUM([Sales]) - LOOKUP(SUM([Sales]), -1)) / ABS(LOOKUP(SUM([Sales]), -1))

// Category Performance (10.8% is the overall margin)
IF [Profit Margin] >= 0.108 THEN "Above Avg Margin" ELSE "Below Avg Margin" END
```

## Tools

Tableau: calculated fields, table calculations (LOOKUP for YoY), interactive filters, dashboard layout, checking a metric against the raw status field.

## Files

```
Supply-Chain-Performance-Analysis/
├── README.md
├── Supply Chain Performance Analysis_.twbx
├── executive overview.png
└── delivery-operations.png
```

