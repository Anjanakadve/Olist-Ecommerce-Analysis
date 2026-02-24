
# 📦 Olist E-Commerce Analytics Project

## 🏬 Company Overview
Olist is a Brazilian "Unicorn" startup that operates as a SaaS (Software as a Service) platform for e-commerce. It functions as a massive department store that allows small and medium-sized businesses from all over Brazil to sell their products directly through Olist's accounts on the largest marketplaces (like Amazon, Mercado Livre, and Americanas).

## 📖 Project Objective
This project analyzes the **Olist Brazilian E-Commerce Dataset** to transform 100k+ records into strategic business intelligence regarding revenue and growth. By evaluating **KPIs, churn, and seasonality**, the study identifies critical drivers for customer retention and optimized inventory planning. Using **Market Basket Analysis** and visual impact studies, the project delivers data-driven recommendations for targeted marketing and pricing strategies.
## 🗂️ Data Overview
The dataset consists of multiple tables containing information on orders, products, sellers, and customers in Brazil from 2016 to 2018. The tables are linked via a **Star Schema** with the `orders` table at the core.

### 🔑 Key Tables & Relationships:
* **`customers`**: Contains customer locations and unique IDs used to track repeat buyers.
* **`orders`**: The central table tracking order status, timestamps (purchase, approved, delivered), and estimated delivery.
* **`order_items`**: Connects orders to products and sellers, including price and freight values.
* **`products`**: Detailed attributes of items, including category names, dimensions, and the **number of photos**.
* **`payments`**: Includes payment methods (credit card, voucher, etc.) and installment details.
* **`reviews`**: Customer feedback and satisfaction scores.
* **`sellers`**: Information on the origin of products sold through the Olist platform.
* **`geolocation`**: Zip code coordinates for mapping and calculating shipping distances.

## 🛠️ Data Cleaning & Transformation
Before analysis, the raw data underwent a rigorous cleaning process using **Python (Pandas)** to ensure accuracy and consistency. The processed data was then exported as CSV files and loaded into **Power BI** for visualization.

### Key Transformation Steps:
* **Handling Missing Values:** Implemented strategies to fill or remove nulls in product categories and delivery timestamps.
* **Feature Engineering:** * Created a **`Quantity`** column by aggregating order item rows.
    * Developed custom date features to track **Seasonality** and **Churn**.
* **Data Formatting:** Standardized text formats for category names and ensured all price/freight columns were converted to numeric types.
* **Schema Optimization:** Cleaned and verified primary/foreign keys (e.g., `order_id`, `product_id`) to ensure seamless table relationships in the Power BI Data Model.

* ## 🛠️ Tools & Technologies
This project leverages a modern data stack to handle ETL, advanced analytics, and visualization:

* ![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black) — Used for creating interactive dashboards, KPI tracking, and final business reporting.
* ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) — Used for primary data cleaning, feature engineering, and handling large-scale CSV transformations.
* ![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white) — Utilized for data manipulation, handling missing values, and restructuring relational tables.
* ![DAX](https://img.shields.io/badge/DAX-005A9C?style=for-the-badge&logo=microsoft&logoColor=white) — Applied within Power BI to create complex measures, calculated columns, and time-intelligence functions for churn and seasonality analysis.

## 📈 Key Business Insights (Power BI Analysis)

### 1. Executive KPIs & Retention
* **Customer Base:** The marketplace serves **99.44K total customers**, with **75.65K active ordering customers**.
* **Dormancy Alert:** Identified **41K inactive customers** (no purchase in 12 months), representing a significant opportunity for re-engagement.
* **Churn Customers:** A total of **23,788 customers churned**, requiring a deeper look into loyalty programs and retention strategies.

### 2. Operational & Category Performance
* **Logistics Bottleneck:** The average delivery time is **262.12 hours**, a key metric that directly impacts customer satisfaction and review scores.
* **Market Diversity:** Analyzed **72 distinct product categories** across **27 Brazilian states**, highlighting the massive geographical and inventory scale of Olist.
* **Visual Conversion:** Verified the relationship between **product photo counts** and sales, proving that better visuals drive higher volume across all 72 categories.

### 3. Strategic Market Intelligence
* **Market Basket Analysis:** Discovered frequently purchased product pairings to drive **cross-selling** and optimized bundling strategies.
* **Seasonality & Pricing:** Detected recurring monthly demand cycles and analyzed how price fluctuations influenced buying behavior over the last year.
* **Local Market Opportunity:** Identified high-rated sellers (>4.5 score) with low local penetration (<10% in-state sales) across the 27 states.

## 💡 Strategic Recommendations

Based on the analysis of the Olist ecosystem, the following actions are recommended to drive growth and operational efficiency:

### 1. Optimize Logistics to Reduce Delivery Time
* **The Problem:** Average delivery time is currently **262.12 hours (~11 days)**.
* **The Solution:** Establish regional distribution centers in high-volume states to shorten the "Last Mile" delivery. Prioritize the 27 states based on order density to reduce the 262-hour bottleneck.

### 2. Re-engagement Campaign for Inactive Customers
* **The Problem:** There are **41K inactive customers** and **23,788 churned users**.
* **The Solution:** Launch a "Win-Back" email marketing campaign targeting the 41K dormant users with personalized coupons. Use the **Market Basket Analysis** results to suggest products they are likely to buy based on their previous history.

### 3. Enhance Visual Merchandising
* **The Problem:** Correlation analysis shows products with fewer photos sell less.
* **The Solution:** Implement a "Minimum Photo Requirement" (e.g., at least 3-5 high-quality images) for sellers in underperforming categories to boost conversion rates across the **72 product categories**.

### 4. Hyper-Local Seller Growth
* **The Problem:** High-rated sellers (>4.5) are failing to capture their local state markets (<10% local sales).
* **The Solution:** Introduce "Local Hero" badges or reduced shipping rates for in-state purchases. This encourages customers to buy from nearby sellers, which simultaneously solves the long delivery time issue.

## 🧠 Skills & Knowledge Gained

Through this end-to-end analysis, I developed a deep understanding of both technical data science and business strategy:

### 📈 Business & Domain Knowledge
* **Market Basket Analysis (MBA):** Learned how to apply association rules to identify product affinities and drive cross-selling strategies.
* **Churn & Retention Modeling:** Mastered the logic of identifying lost customers and calculating retention rates to evaluate business health.
* **Stakeholder Perspective:** Developed the ability to translate complex data (like 262-hour delivery lags) into actionable insights for business executives.
* **E-commerce Operations:** Gained insight into the logistics of a multi-seller marketplace, including fulfillment stages and regional seller performance.

### 💻 Technical Proficiency
* **Advanced DAX:** Authored complex measures for BOGO simulations, time-intelligence for churn, and dynamic color-coding for category contribution.
* **ETL Pipeline Management:** Established a workflow between **Python (Pandas)** for heavy data cleaning and **Power BI** for final reporting.
* **Data Modeling:** Built a robust relational schema (Star Schema) to connect 9+ tables efficiently without compromising dashboard performance.














