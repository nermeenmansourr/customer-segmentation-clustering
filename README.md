# 🛍️ Customer Segmentation with K-Means Clustering
 
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nermeenmansourr/customer-segmentation-clustering/blob/main/customer_segmentation_clustering_.ipynb)
 
Grouping mall customers into 5 segments based on their income and spending behavior, so a business can target each group with the right marketing strategy.
 
## Business Question
 
Not all customers behave the same way. Which groups of customers exist in our data, and how should we approach each one differently?
 
## Dataset
 
**Mall Customers dataset** (200 customers, no missing values)
 
| Feature | Description |
|---|---|
| Gender | Male / Female |
| Age | 18 – 70 (average ≈ 39) |
| Annual Income (k$) | 15 – 137 (average ≈ 61) |
| Spending Score (1–100) | Score assigned by the mall based on customer behavior |
 
## Approach
 
1. **Data checking:** inspected the data types and summary statistics, and confirmed there were no null values.
2. **Univariate analysis:** looked at the distributions of age, income, and spending score, overall and split by gender (histograms, KDE plots, boxplots).
3. **Bivariate analysis:** scatter plots, a pairplot, and a correlation heatmap to see how the features relate.
4. **Clustering:** applied K-Means with **k = 5** on *Annual Income* and *Spending Score*.
5. **Visualization:** plotted the clusters on an income vs. spending scatter plot.
## Key Findings
 
- **Gender makes little difference.** Average spending is about 52 for women and 49 for men, so gender is not a strong way to separate customers.
- **Income and spending are almost uncorrelated** (r ≈ 0.01), so a wealthy customer is not necessarily a big spender.
- **Age and spending are moderately negatively correlated** (r ≈ -0.33): younger customers tend to have higher spending scores.
- **Five distinct customer groups appear** when income is plotted against spending:
| Segment | Profile | Customers | Suggested action |
|---|---|---|---|
| Average customers | Mid income, mid spending | 81 | Keep engaged with regular promotions |
| Big spenders | High income, high spending | 39 | VIP and loyalty programs |
| Untapped wealth | High income, low spending | 35 | Personalized offers to raise their spending |
| Budget enthusiasts | Low income, high spending | 22 | Discounts and seasonal deals |
| Cautious savers | Low income, low spending | 23 | Low-cost campaigns |
 
> Segment sizes come from one run of the model. Cluster numbers can change between runs.
 
![Customer clusters](images/clusters.png)
 
## Tools
 
Python · pandas · NumPy · scikit-learn · matplotlib · seaborn
 
## How to Run
 
```bash
git clone https://github.com/nermeenmansourr/customer-segmentation-clustering.git
cd customer-segmentation-clustering
pip install pandas numpy matplotlib seaborn scikit-learn
jupyter notebook customer_segmentation_clustering_.ipynb
```
 
Or click the **Open in Colab** badge at the top. Make sure `Mall_Customers.csv` is in the same folder as the notebook.
 
## Limitations and Next Steps
 
- Only income and spending score were used for clustering. Age could be added to find richer segments.
- Try feature scaling, and compare K-Means with other methods such as hierarchical clustering or DBSCAN.
- Validate the segments with a real marketing campaign.
- The dataset is small (200 rows), so the results are illustrative rather than conclusive.
## Author
 
**Nermeen Mansour**
[GitHub](https://github.com/nermeenmansourr) · [LinkedIn](#) · [Email](#)
 
