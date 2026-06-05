# Sales and Operations Analysis

## 1. Project Objective 
The primary objective of this project is to conduct an end-to-end analysis of historical transactional records for a global business. The project focuses on cleaning, normalizing, and consolidating isolated tables to calculate baseline business performance KPIs, identify geographic development indicators, evaluate logistical efficiency, and analyse seasonal variations in product demand

---

## 2. Methodology & Data Engineering 

### A. Data Integration: 
Consolidated transactional, geographic, and product dimension tables into a single DataFrame to enable downstream analysis

### B. Data Cleaning & Quality Assurance (DQA)
* **Schema Standardization:** Standardized all column headers across tables to a uniform format
* **Handling Missing Values:** Evaluated null-value ratios across tables and executed a subset cleanup : `country_code` (~6.16%) and transactional `units_sold` (~0.15%) to preserve data distribution accuracy.
* **Type Conversion:** Formatted date sequences 
* **Anomaly Auditing:** Executed a financial logic check to ensure data integrity

### C. Feature Engineering
* Calculated the raw revenue footprint feature and engineered a clean net profit feature
---

## 3. Data Analysis & Empirical Conclusions

### Key Performance Indicators (KPIs)
* **Total Gross Revenue Generated:** `$1,598,983,761`
* **Total Net Profit Captured:** `$473,709,035`
* **Overall Portfolio Profit Margin:** `29.63%`
* **Total Volume of Valid Orders Fulfilled:** `1,246`
* **Average Order Value (AOV):** `$1,283,293.55` per invoice
* **Average Physical Volume per Transaction:** `4,953 units`
* **Active International Footprint:** `45 Unique Countries` captured across distinct macro-regions.

### Historical Growth Velocity & Financial Performance

* **-** Market scaling reached peak efficiency in 2012, driven by a **+24.90% YoY revenue expansion** that successfully maximized profitability at a historical high of **$83,070,056.18**
* **-** Discovered an operational divergence in 2015. While revenue remained almost entirely flat (**-1.38% YoY**), net profits dropped disproportionately from **$65.9M to $58.2M**. 
* **-** Post-2015, the marketplace entered a continuous structural contraction, bottoming out in 2017 with a steep **-29.74% revenue decline** and a period-low profit of **$35,926,071.66**. Because net profit shrank faster than top-line revenue, the trend exposes a high fixed-cost infrastructure that failed to scale down as customer transaction volumes dropped.
* * **-** Post-2015, the marketplace entered a continuous structural contraction, bottoming out in 2017 with a steep **-29.74% revenue decline** and a period-low profit of **$35,926,071.66**.This trend highlights an inflexible cost structure, where expenses failed to decrease at the same rate as falling sales volumes.

## Geographic Portfolio Performance

* **-** Ukraine and San Marino represent the highest-performing markets, simultaneously ranking in the Top 5 for both total revenue generation and absolute net profitability
* **-** The Czech Republic leads the global portfolio with a peak revenue of **$53.54M**, with Bosnia and Herzegovina and North Macedonia also driving substantial sales scale. However, none of these high-volume markets rank in the Top 5 for profitability, indicating severe, localized margin pressure
* **-** Andorra and Malta emerge as highly efficient, high-margin territories with exceptional pricing power. They serve as primary candidates for targeted strategic expansion, subject to localized market size and scalability audits

 ## Logistical Operations & Fulfillment Analysis

* **-** The data proves that historical variations in shipping turnaround times carry no statistical correlation or financial penalty regarding absolute revenue generation or net profitability.
* **-** Warehouse processing velocities vary significantly by product type. While **Personal Care** products clear processing channels in an efficient **20-day average**, categories such as **Baby Food, Cereal, and Office Supplies** experience handling friction, extending their turnaround by an additional week.
* **-** The automated priority processing infrastructure shows a bottleneck. "Critical" and "High" priority shipments navigate fulfillment lines on identical timelines as "Low" priority orders, presenting an operational risk to contractual trust and client retention.
* **-** Europe acts as the highest-volume operational engine in the dataset, closely mirrored by Asia. Both regions maintain stable, parallel processing benchmarks across their respective volume footprints.

* ##  Demand Dynamics & Temporal Volatility

Cross-referencing historical transaction volumes across days of the week, months, and macro seasons reveals distinct cyclical purchasing behaviors:

### Intra-Week Volume Distribution
* **-** Demand peaks sharply over the weekend, led by **Sunday (987,776 units)** and **Saturday (970,549 units)**, with solid residual momentum extending into **Monday (933,677 units)**. 
* **-** Operational volume bottoms out consistently on Fridays (**787,802 units**), representing an approximate **20.2% drop** from the Sunday maximum.
* *Strategic Action:* Align marketing campaigns, inventory restocks, and promotional events to execute between Saturday morning and Monday afternoon to optimize conversions during this high-intent window.

### Monthly Sales Volatility
* **-** **March** stands out as the single highest-performing month of the year (**635,482 units**), followed closely by **January (594,625 units)**.
* **-** August marks a severe operational drop, collapsing to **408,220 units**—a sharp **35.7% decline** compared to the March peak.
* **-** The dataset captures an isolated mid-summer demand surge across **June (555,833 units)** and **July (563,203 units)** immediately preceding the August downturn.
* **-** Contrary to standard retail patterns, the fourth quarter (October through December) remains highly stable and flat, maintaining a tight baseline band of **450k–500k units per month** with an absence of holiday-buying spikes.

### Macro Seasonal Performance Rankings
Aggregating monthly counts into standardized seasonal intervals establishes a clear operational hierarchy:
1. **Spring (#1 Ranked - 1,628,300 units sold):** Serves as the primary demand engine of the calendar year, heavily driven by the high transaction volume in March.
2. **Winter (#2 Ranked - 1,590,564 units sold):** Retains strong secondary volume, supported by high sustained purchasing cycles in January and a stable December.
3. **Autumn (#3 Ranked - 1,425,551 units sold):** Tracks as the weakest season overall, dragged down by low baseline spending habits in September and November.
