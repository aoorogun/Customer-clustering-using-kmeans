# Customer-clustering-using-kmeans
A kMeans clustering of customer for a UK store

### README: RFM Clustering Analysis and Insights

---

#### **Overview**
This analysis involves segmenting customers into clusters using RFM (Recency, Frequency, and Monetary) metrics. The goal is to identify customer behavior patterns and derive actionable insights to optimize business strategies.

---

### **1. Objectives**
- Analyze customer purchasing behavior using RFM metrics.
- Perform clustering analysis to segment customers.
- Interpret clusters and provide actionable insights for improving engagement and retention.

---

### **2. Data Description**
The analysis uses transactional data spanning two sheets:
1. **Year 2009-2010**
2. **Year 2010-2011**

Each dataset contains:
- **Invoice**: Transaction ID
- **StockCode**: Product identifier
- **Description**: Product name
- **Quantity**: Number of units sold
- **InvoiceDate**: Date and time of the transaction
- **Price**: Unit price of the product
- **Customer ID**: Unique identifier for customers
- **Country**: Customer's location

---

### **3. Methodology**

#### **3.1 Data Preprocessing**
- **Cleaning**:
  - Dropped rows with missing `Customer ID`.
  - Filtered transactions with positive `Quantity` and `Price`.
- **Feature Engineering**:
  - Added a `TotalValue` column (`Quantity * Price`) to compute monetary value.
  
#### **3.2 RFM Calculation**
- **Recency**: Days since the last purchase (relative to the latest transaction date).
- **Frequency**: Number of unique transactions by each customer.
- **Monetary**: Total purchase value per customer.

#### **3.3 Clustering**
- RFM data was clustered into four groups using appropriate clustering algorithms.
- Clusters were visualized using violin plots for:
  - **Monetary Value by Cluster**
  - **Frequency by Cluster**
  - **Recency by Cluster**

---

### **4. Key Insights**

#### **Cluster Summary**
1. **Cluster 3 (High Value and Engagement)**:
   - High monetary value, high frequency, and low recency.
   - Represent top-tier customers who purchase frequently and recently.
   - **Action**: Focus on retention through loyalty programs and personalized offers.

2. **Cluster 1 (Low Value and Inactive)**:
   - Low monetary value, low frequency, and high recency.
   - Represent disengaged or one-time buyers.
   - **Action**: Re-engage through targeted campaigns, discounts, and improved communication.

3. **Clusters 0 and 2 (Mid-Tier Customers)**:
   - Moderate monetary value, frequency, and recency.
   - Represent potential growth customers.
   - **Action**: Encourage higher spending through upselling or cross-selling.

---

### **5. Recommendations**

#### **5.1 Improving Engagement for Cluster 1**
- **Re-engagement Campaigns**:
  - Offer exclusive discounts or free shipping for returning customers.
  - Use retargeting ads and "We Miss You" email campaigns.
- **Loyalty Incentives**:
  - Introduce points or rewards for repeat purchases.
- **Gamification**:
  - Add interactive features like spin-to-win discounts.

#### **5.2 Enhancing Retention for Cluster 3**
- **VIP Programs**:
  - Offer exclusive benefits such as early access to products or free gifts.
- **Personalization**:
  - Provide tailored recommendations and offers.

#### **5.3 Upselling Mid-Tier Customers**
- **Bundles and Deals**:
  - Offer product bundles or time-sensitive discounts.
- **Cross-Selling**:
  - Recommend complementary products based on purchase history.

---

### **6. Files in the Project**
1. **Dataset**:
   - `online_retail_II.xlsx`: Transactional data.
2. **Analysis Notebook**:
   - Includes code for data cleaning, RFM calculation, clustering, and visualization.
3. **Output Visualization**:
   - Violin plots showing RFM metrics by cluster.

---

### **7. Tools and Libraries**
- **Python**:
  - Pandas: Data cleaning and processing.
  - Matplotlib/Seaborn: Data visualization.
  - Scikit-learn: Clustering analysis.
  
---

### **8. Next Steps**
1. Automate RFM analysis for future datasets.
2. Integrate insights into a CRM system for targeted marketing.
3. Continuously monitor and update clustering strategies based on new data.

For further questions or collaboration, feel free to reach out! Shoutout to TrentDoesMath
