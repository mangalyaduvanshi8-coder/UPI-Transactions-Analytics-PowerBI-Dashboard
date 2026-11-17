# UPI Transactions Analytics — Interactive Power BI Dashboard

An interactive 2-page **Microsoft Power BI** business intelligence dashboard analyzing **20,000 UPI transactions** across **January–December 2024**. Built with **10 cross-page synced dropdown slicers**, a **4-bookmark dynamic chart switcher**, and a **conditional-formatted City × Month matrix** to evaluate transaction volume, remaining account balances, and multi-currency payment behavior.

---

## Dashboard Previews

### Page 1: Monthly Trend & Dynamic Bookmark Switcher
![Monthly Trend and Bookmark View](page-1-trend-bookmarks.png)

### Page 2: City & Multi-Currency Matrix Breakdown
![City and Currency Matrix View](page-2-city-matrix.png)

---

## Executive KPI Summary (FY 2024 Dataset)

| Metric | Value | Notes |
| :--- | :--- | :--- |
| **Total Transactions** | **20,000** | Full-year coverage (`Jan 1, 2024 – Dec 30, 2024`) |
| **Total Transaction Amount** | **19,872,274.03** | Mean: `993.61` \| Median: `983.40` |
| **Cumulative Remaining Balance** | **100,410,817.42** | Mean post-transaction balance: `5,020.54` |
| **Transaction Success Rate** | **80.0%** | `16,000` Success vs. `4,000` Failed (`20.0%` failure rate) |
| **Peak Transaction Month** | **May 2024 (`1,706,785.86`)** | Followed by Feb 2024 (`1,692,737.83`) & Oct 2024 (`1,691,412.50`) |
| **Top City by Volume** | **Mumbai (`5,052,564.92`)** | Followed by Delhi (`5,036,738.71`), Hyderabad & Bangalore |

---

## Report Architecture & Technical Features

* **Page 1 — Interactive Trend & Bookmark Navigator:**
  * Configured a **Bookmark Navigator** linked to **4 custom bookmarks** (`Line Chart Amount`, `Column Chart Amount`, `Line Chart Balence`, and `Column Charts Balence`), allowing users to toggle between **Sum of Amount** and **Sum of RemainingBalance** across line and column visualizations on a single canvas.
* **Page 2 — Granular City & Currency Matrix:**
  * Designed a drill-down **Matrix (Pivot Table)** mapping `Month` and `Currency` (`INR`, `USD`, `EUR`, `GBP`) against `City` (`Mumbai`, `Delhi`, `Hyderabad`, `Bangalore`), styled with **dual color-scale heatmaps** (green gradient for `Amount` and gold gradient for `RemainingBalance`).
* **10 Synchronized Cross-Page Slicers:**
  * Linked dropdown slicers across both pages using Power BI **Sync Slicers** for `BankNameSent`, `BankNameReceived`, `City`, `DeviceType`, `Gender`, `Age Group` (derived demographic bucket), `MerchantName`, `PaymentMethod`, `Purpose`, and `TransactionType`, plus a report-level `Currency` filter.
* **Fluent 2 Design Theme:**
  * Styled with the **Fluent 2** theme (`1920 × 1080` widescreen canvas) with custom border accents, bold data labels, and consistent visual alignment.

---

## Key Analytical Insights

* **Geographic & Banking Leaders:** **Mumbai** (`5,052,564.92`, avg `1,010.51`) and **Delhi** (`5,036,738.71`, avg `1,007.35`) generated the highest transaction value among the 4 metro cities. **HDFC Bank** led outbound sending volume (`5,052,564.92`), while **ICICI Bank** led inbound receiving volume (`5,052,564.92`).
* **Monthly Seasonality:** Transaction value peaked in **May 2024** (`1,706,785.86`) and dipped to its lowest point in **August 2024** (`1,598,708.63`), maintaining steady volume between `1,666` and `1,667` transactions per month.
* **Merchant & Purpose Distribution:** Across 5 merchant categories (`4,000` transactions each), **Zomato / Travel** (`3,998,155.96`) and **Flipkart / Shopping** (`3,996,787.08`) recorded the highest total spend, followed by **IRCTC**, **Swiggy**, and **Amazon**.
* **Channel & Payment Reliability:** Transactions were evenly distributed across **UPI ID / Mobile** (`6,642,887.48`), **Phone Number / Tablet** (`6,640,042.16`), and **QR Code / Laptop** (`6,589,344.39`), with an **80.0% overall success rate** and **20.0% failure rate** highlighting an opportunity to investigate failed payment retries.

--
## Author

**Mangal Yadav**  
*B.S. in Data Science and Applications — IIT Madras | Aspiring Data Analyst*  


