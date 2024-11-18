# **Social-Sell Insights: Analyzing Facebook Marketplace Engagement**

## **Project Overview**
Social-Sell Insights is a machine learning project focused on analyzing social media engagement data from Thai fashion and cosmetics sellers on Facebook Marketplace. By leveraging clustering techniques and visualizations, the project provides actionable insights to help sellers optimize customer engagement strategies.

---

## **Features**
- Analyze engagement metrics such as reactions, comments, and shares.
- Visualize correlations between various engagement metrics.
- Perform clustering using the K-Means algorithm to segment posts based on engagement patterns.
- Optimize the number of clusters using the elbow method.

---

## **Dataset**
**Source**: UCI Machine Learning Repository  
**Description**: The dataset contains 7050 posts from 10 Facebook pages in Thailand, covering various post types and engagement metrics.  
**Attributes**:
- **status_id**: Post identifier.
- **status_type**: Type of post (video, photo, link, or status).
- **status_published**: Timestamp of the post.
- **num_reactions**: Total number of reactions (likes, loves, etc.).
- **num_comments**: Total number of comments.
- **num_shares**: Total number of shares.
- **num_likes, num_loves, num_wows, num_hahas, num_sads, num_angrys**: Breakdown of reaction types.

---

## **Technical Details**
### **1. Data Preprocessing**
- Removed irrelevant columns and corrected data types.
- Handled messy and dirty data by resolving missing values.

### **2. Exploratory Data Analysis**
- Identified correlations between reactions, comments, and shares:
  - **Reactions vs Likes**: Near-perfect correlation (Pearson: 0.99, Spearman: 1.0).
  - **Reactions vs Comments**: Moderate correlation at low engagement levels (Pearson: 0.15, Spearman: 0.73).
  - **Reactions vs Shares**: Weak positive correlation (Pearson: 0.25, Spearman: 0.56).
- Visualized engagement patterns by post type:
  - **Videos** received the most comments (642) and shares (116) on average.
  - **Statuses** generated the most reactions (439).

### **3. K-Means Clustering**
- Trained K-Means clustering models to group posts based on engagement metrics.
- Used the elbow method to determine the optimal number of clusters (**k=3**).
- Achieved:
  - **Training Inertia**: 33393.57
  - **Test Inertia**: 10114.10

---

## **Technologies Used**
- **Programming Language**: Python
- **Libraries**: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
- **Tools**: Jupyter Notebook

---

## **Results**
- Engagement varies significantly by post type, with videos and statuses performing best in terms of comments and reactions, respectively.
- Posts cluster into 3 distinct groups based on engagement patterns, offering actionable segmentation for targeted strategies.
- Time of posting impacts engagement, with peaks in the early morning and late evening.

---

## **Future Scope**
- Integrate additional data sources (e.g., digital ad performance or audience demographics).
- Experiment with advanced clustering algorithms like DBSCAN or Hierarchical Clustering.
- Develop a web-based dashboard to present insights interactively.

---
