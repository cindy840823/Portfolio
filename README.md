# Te-Hsin (Cindy) Kung — Data Analytics Portfolio

MS in Data Science (University of Maryland, College Park) · BS in Business Administration, Computer Information Systems (Cal Poly Pomona, Magna Cum Laude)

I turn raw business data into answers people can act on: cleaning messy real-world datasets, querying them with SQL and Python, and explaining what the numbers mean for the business. This repository collects my analytics and data science projects, with the business-focused analyses first.

**Core tools:** Python (pandas, matplotlib, seaborn, scikit-learn, statsmodels) · SQL (SQL Server) · Tableau Public · Jupyter / Google Colab

---

## Business & Analytics Projects

### 1. [Lazada Thailand Health Product Analysis](./Lazada_Health_Product_Analysis) · [▶ Tableau dashboard](https://public.tableau.com/views/LazadaThailandHealthProductsDashboard/LazadaDashboard)
**Question:** Which health product categories and price points move the most volume on Lazada Thailand, and where are the top sellers based?
- Found and fixed two data-quality errors: 68,499 scraped rows held only 2,497 unique products, and a parsing bug read "5,786" as 5; the fixes changed which categories came out on top
- Products under ฿300 are 50% of listings but 81% of units sold; Protein leads units and 23% of estimated revenue
- Built an interactive Tableau Public dashboard with KPIs, category and price-band views, and a region filter
- **Tools:** Python (pandas, matplotlib), Tableau Public

### 2. [Facebook Ad Campaign Performance & Budget Reallocation](./Facebook_Ad_Campaign_Analysis)
**Question:** Which audiences convert most cost-effectively across three Facebook ad campaigns, and where should budget move?
- Calculated CTR, CPC, CPM, approval rate and cost per approved conversion (CPA) for 1,143 ads, and flagged 207 zero-click, zero-spend ads that still recorded conversions
- Found that ages 45–49 took 35% of spend but brought 19% of approved conversions, at about 3× the CPA of ages 30–34
- Modeled a budget shift that would add about 116 approved conversions (+11%) at the same spend, with the assumptions stated
- **Tools:** Python (pandas, matplotlib)

### 3. [Cross-Platform Ads Performance: Google vs. Meta vs. TikTok](./Cross_Platform_Ads_Performance) *(simulated data)*
**Question:** Which ad platforms and campaign types return the most revenue per dollar, where should budget move, and which weeks need attention?
- Compared CTR, CPC, CPM, CVR, CPA and ROAS across 1,800 campaign-days; Google took 57% of spend but returned 41% of revenue (ROAS 3.47 vs. 7.62 on TikTok)
- Showed that averaging row-level ROAS overstates performance by 32%, and calculated every ratio from totals
- Modeled a 20% budget shift to TikTok (+9.7% revenue, upper estimate) and built a weekly monitor that flags weeks more than 20% below their 4-week ROAS baseline
- **Tools:** Python (pandas, matplotlib)

### 4. [Video Games Genre Sales Analysis](./Video_Games_Genre_Sales_Analysis)
**Question:** What separates a hit game (1M+ global sales) from the rest?
- Analyzed 16,717 titles across genre, platform, publisher, region (NA, EU, JP), and critic score
- Found a strong positive link between critic scores and global sales; Action dominates game count and sales but is crowded
- Built hit/no-hit classifiers and evaluated them against a naive baseline, since only about 17% of titles are hits
- **Tools:** Python, pandas, scikit-learn, matplotlib, seaborn

### 5. [Product Sales Data Warehouse](./Product_Sales_Data_Warehouse)
**Question:** How should product sales data be structured so the business can analyze trends, products, and customers?
- Designed a star schema with a `FactProductSales` fact table and Customer, Product, Store, SalesPerson, and Date dimensions
- Wrote the SQL to build and populate the warehouse, plus an ERD of table relationships and cardinalities
- Queried sales trends and product performance to recommend seasonal promotions and gift-card campaigns
- **Tools:** SQL Server (SSMS), SQL

### 6. [Real-Time Bitcoin Sentiment Analysis Using txtai](./Real-Time_Bitcoin_Sentiment_Analysis_Using_txtai)
**Question:** Can news sentiment help explain short-term Bitcoin price movements?
- Built a pipeline that pulls live Bitcoin headlines (NewsAPI), scores their sentiment with txtai, and merges them with historical prices (CoinGecko)
- Cleaned the time series (duplicate dates, daily resampling, forward-filled gaps) and forecast prices 7 days ahead with ARIMA(5,1,2)
- API keys are loaded from environment variables, not hardcoded
- **Tools:** Python, txtai, pandas, statsmodels (ARIMA), matplotlib, seaborn

---

## Machine Learning & NLP Projects

### 7. [Heart Disease Risk Prediction](./Heart_Disease_Analysis_Project) *(team project)*
- Modeled heart disease risk from 300,000+ CDC BRFSS survey responses, where only about 9% of respondents have heart disease
- Chose recall on the heart-disease class over raw accuracy: balanced Logistic Regression caught 77% of cases (ROC-AUC 0.83), while Random Forest reached 90% accuracy but caught only 10%
- **Tools:** Python, scikit-learn, imbalanced-learn (SMOTE), Lasso, matplotlib, seaborn

### 8. [Text Mining and Topic Modeling with LSA](./Text_Mining_and_Topic_Modeling_with_LSA)
- Applied Latent Semantic Analysis to NFT whitepapers to surface key themes, with a focus on gaming
- **Tools:** Python, scikit-learn, pandas, wordcloud

### 9. [Binary Classification with PCA](./Binary_Classification_Project)
- Compared LDA, Decision Tree, k-NN, and SVM on loan-approval data using type 1 and type 2 error rates, with and without PCA
- **Tools:** Python, scikit-learn, pandas, matplotlib

### 10. [Neural Networks for MNIST Classification](./Neural_Networks_MNIST_Project)
- Compared a feedforward network and a CNN over 5 runs each: **94.27%** vs. **99.03%** average test accuracy
- **Tools:** Python, TensorFlow, Keras

---

## Skills Demonstrated
- **Data cleaning & preparation:** deduplication, text-to-number parsing, missing values, time-series gaps, categorical encoding, class imbalance
- **Analysis & communication:** exploratory analysis, segment comparisons, business recommendations, interactive dashboards (Tableau)
- **SQL & data modeling:** star-schema design, fact and dimension tables, analytical queries
- **Statistics & ML:** classification, model evaluation beyond accuracy (precision, recall, ROC-AUC, baselines), ARIMA forecasting, PCA
- **NLP:** sentiment analysis, topic modeling

## Contact
- **Email:** tehsinkung@gmail.com
- **LinkedIn:** https://www.linkedin.com/in/te-hsin-kung-umd2025/
- **GitHub:** https://github.com/cindy840823
