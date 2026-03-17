# Customer Segmentation using K-Means Clustering

## Project Overview
This project focuses on **customer segmentation** using the **Mall Customers dataset**.  
The main goal is to divide customers into different groups based on their purchasing behavior so businesses can better understand their customers and create targeted marketing strategies.

In this project, I performed:
- Data loading and inspection
- Data cleaning
- Exploratory Data Analysis (EDA)
- Customer grouping using **K-Means Clustering**
- Visualization of the final customer segments

---

## Dataset
The dataset used in this project contains the following columns:

- **CustomerID** – Unique ID of each customer
- **Gender** – Male or Female
- **Age** – Age of the customer
- **Annual Income (k$)** – Customer's yearly income
- **Spending Score (1-100)** – Score assigned based on customer spending behavior

---

## Objective
The objective of this project is to identify different customer groups based on:
- **Annual Income**
- **Spending Score**

This helps businesses:
- understand customer behavior
- identify high-value customers
- create better marketing campaigns
- improve customer targeting

---

## Technologies Used
- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## Project Workflow

### 1. Importing Libraries
I imported the required Python libraries for:
- data handling
- visualization
- machine learning

### 2. Loading the Dataset
The dataset was loaded into a Pandas DataFrame using `pd.read_csv()`.

### 3. Data Inspection
I checked:
- first few rows with `head()`
- last few rows with `tail()`
- dataset shape
- statistical summary
- data types

### 4. Data Cleaning
I removed the `CustomerID` column because it is only an identifier and does not help in customer behavior analysis.

### 5. Exploratory Data Analysis (EDA)
I explored the data using different plots:
- distribution plots for Age, Annual Income, and Spending Score
- gender count plot
- violin plots by gender
- age-group analysis
- average income and spending score by age group
- spending score range analysis
- scatter plot of income vs spending score

### 6. Feature Selection
For clustering, I selected:
- **Annual Income (k$)**
- **Spending Score (1-100)**

These two features were used to identify customer groups.

### 7. Why K-Means Clustering?
K-Means was used because this project is about **grouping similar customers together**.  
It is a simple and effective clustering algorithm that works well when we want to find natural groups in numeric data.

In simple terms, K-Means helps answer this question:

**Which customers behave similarly in terms of income and spending?**

### 8. Finding the Best Number of Clusters
I used the **Elbow Method** to find the optimal number of clusters.

- I tested cluster values from 1 to 10
- calculated WCSS (Within-Cluster Sum of Squares)
- plotted the elbow graph
- selected **K = 5** as the best number of clusters

### 9. Applying K-Means
After choosing `K = 5`, I applied K-Means clustering to group customers into 5 segments.

### 10. Final Visualization
Finally, I plotted the clusters using a scatter plot, where:
- X-axis = Annual Income
- Y-axis = Spending Score
- different colors = different customer segments

---

## Meaning of K in K-Means
In K-Means, **K** means the number of groups (clusters) we want to create.

For example:
- K = 2 → 2 groups
- K = 3 → 3 groups
- K = 5 → 5 groups

In this project, I selected **K = 5** because the Elbow Method showed that 5 clusters gave a good balance between simplicity and accuracy.

---

## Key Insight
This project shows that customers can be divided into different groups such as:
- high income, high spending
- high income, low spending
- low income, high spending
- low income, low spending
- average customers

These segments can help businesses make better decisions.

---

## Conclusion
This project successfully applied **K-Means Clustering** to segment mall customers based on their annual income and spending score.  
It demonstrates how machine learning can be used in a simple and practical way for business decision-making and customer analysis.

---

## Future Improvements
Some possible improvements for this project:
- include Age in clustering
- scale the features before clustering
- analyze each cluster in more detail
- assign business-friendly names to each cluster
- build an interactive dashboard for visualization

---

## Author
**Sanjeeb Sapkota**
