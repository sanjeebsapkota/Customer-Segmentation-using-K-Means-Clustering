# 🎯 Customer Segmentation using K-Means Clustering

> **Unsupervised Machine Learning project** that segments mall customers into distinct behavioral groups — enabling businesses to personalize marketing, optimize budgets, and improve customer retention.

---

## 🧩 Business Problem

Businesses often treat all customers the same — same promotions, same messaging, same offers. This is inefficient and costly.

**The question this project answers:**
> *"Which customers behave similarly, and how can we target each group more effectively?"*

By identifying distinct customer segments based on income and spending behavior, marketing teams can:
- Focus high-effort campaigns on **high-value customers**
- Re-engage **low-spending, high-income** customers who have untapped potential
- Avoid wasting budget on the wrong audience

---

## 📊 Dataset

**Mall Customers Dataset** — 200 customer records with the following features:

| Feature | Description |
|---|---|
| CustomerID | Unique identifier (dropped — not a behavioral feature) |
| Gender | Male / Female |
| Age | Customer age |
| Annual Income (k$) | Yearly income in thousands |
| Spending Score (1–100) | Spending behavior score assigned by the mall |

---

## 🔍 Project Workflow

```
Data Loading → Inspection → Cleaning → EDA → Feature Selection → Elbow Method → K-Means → Business Interpretation
```

### 1. Exploratory Data Analysis (EDA)
Explored distributions, gender breakdowns, age-group patterns, and income vs spending relationships using:
- Distribution plots (Age, Income, Spending Score)
- Violin plots by gender
- Age-group average income & spending analysis
- Income vs Spending Score scatter plot

### 2. Feature Selection
Selected **Annual Income** and **Spending Score** as clustering features — these two variables best capture purchasing behavior without introducing noise from age or gender.

### 3. Finding Optimal Clusters — Elbow Method
Tested K values from 1–10, calculated **WCSS (Within-Cluster Sum of Squares)**, and identified the "elbow" point:

> ✅ **Optimal K = 5** — best balance between cluster simplicity and accuracy

### 4. K-Means Clustering
Applied K-Means with K=5 to segment all 200 customers into 5 distinct groups.

---

## 🗂️ The 5 Customer Segments

| Segment | Income | Spending Score | Business Label | Strategy |
|---|---|---|---|---|
| 1 | High | High | 💎 Champions | Reward & retain — VIP programs |
| 2 | High | Low | 💤 Potential Sleepers | Re-engagement campaigns, exclusive offers |
| 3 | Low | High | 🛍️ Impulsive Buyers | Upsell bundles, loyalty rewards |
| 4 | Low | Low | 🔍 At-Risk | Low priority — cost-efficient outreach |
| 5 | Average | Average | 🎯 Mainstream | Standard marketing, volume-based offers |

> This business interpretation is the **most important output** — clustering alone is not enough. Naming and strategizing each segment is what makes this actionable.

---

## 💡 Key Business Insights

- **Segment 1 (Champions)** are the highest-value customers — retention is cheaper than acquisition
- **Segment 2 (Sleepers)** have the income to spend more but aren't — a targeted incentive campaign could unlock significant revenue
- **Segment 3 (Impulsive Buyers)** spend despite lower income — price-sensitive offers and loyalty programs will retain them
- The mall should allocate **~60% of marketing budget** toward Segments 1, 2, and 3

---

## 🛠️ Technologies Used

| Tool | Purpose |
|---|---|
| Python | Core programming language |
| Pandas & NumPy | Data manipulation and cleaning |
| Matplotlib & Seaborn | EDA visualizations |
| Scikit-learn | K-Means clustering, Elbow Method |
| Jupyter Notebook | Interactive analysis environment |

---

## 📁 Project Structure

```
Customer-Segmentation-K-Means/
│
├── customer_segmentation.ipynb   # Full analysis notebook
├── Mall_Customers.csv            # Dataset
├── README.md                     # Project documentation
└── images/                       # Visualization outputs
    ├── elbow_curve.png
    ├── cluster_scatter.png
    └── eda_plots.png
```

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/sanjeebsapkota/Customer-Segmentation-using-K-Means-Clustering.git

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

# Launch Jupyter Notebook
jupyter notebook customer_segmentation.ipynb
```

---


---


## 👤 Author

**Sanjeeb Sapkota** | Data & Business Analytics | Python | Power BI | Tableau | SAP B1

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Sanjeeb%20Sapkota-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/sanjeeb-sapkota-07b625226)
[![GitHub](https://img.shields.io/badge/GitHub-sanjeebsapkota-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/sanjeebsapkota)

---

*⭐ Star this repo if you found it useful!*
