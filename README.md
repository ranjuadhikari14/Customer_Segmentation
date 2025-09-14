# Customer_Segmentation

This project applies data preprocessing, exploratory data analysis (EDA), and clustering techniques to segment customers based on their purchasing behavior, recency, and frequency of orders.

The analysis is based on a customer transaction dataset (customer-data.csv) and aims to identify meaningful customer groups that can be targeted for marketing, retention, and sales growth strategies.

📂 Project Structure
.
├── customer-data.csv        # Input dataset
├── customer_segmentation.ipynb  # Jupyter notebook / Colab script
└── README.md                # Project documentation

⚙️ Steps in the Project
1. Data Preprocessing

Parsed date columns (First Time, Recent Time).

Removed invalid values (e.g., negative distances).

Handled missing values in # of Orders in last 7 days and last 4 weeks by replacing with 0.

Created derived features:

Orders in 3 weeks before last week

Amount in 3 weeks before last week

2. Exploratory Data Analysis (EDA)

Checked for negative or missing values.

Studied correlations between recent and past spending.

Plotted customer distributions by average distance from restaurant.

Performed Pareto analysis (80/20 rule) → Found ~25% of customers contribute to 80% of sales.

3. Feature Engineering

Calculated Recency (days since last order).

Built RFM-style dataset with:

# of Orders → Frequency

Amount → Monetary

Recency → Time since last order

4. Segmentation

Scaled data using StandardScaler.

Applied K-Means clustering with Elbow method to find optimal clusters.

Chose 4 clusters.

Visualized clusters in 3D (Orders, Amount, Recency).

📊 Results & Insights
Cluster Profiles
Cluster	Characteristics	Insights
1	Moderate frequency & spend, low recency	Loyal, active customers
2	Very low frequency, almost inactive	Lost/dormant customers
3	High frequency, high spend, recent orders	VIP / High-value customers
4	Low frequency, small spend, long recency	New or low-value customers

VIP customers (Cluster 3) are the top priority for retention.

Dormant customers (Cluster 2) need reactivation strategies.

Moderate customers (Cluster 1) can be nurtured into VIPs.

New customers (Cluster 4) may need onboarding offers.

🛠️ Tech Stack

Python

Pandas, NumPy → Data handling

Matplotlib → Visualization

Scikit-learn → Scaling & Clustering (K-Means, PCA)
