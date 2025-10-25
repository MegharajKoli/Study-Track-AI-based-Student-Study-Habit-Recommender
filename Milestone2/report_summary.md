#  Milestone 2 : Clustering and Pattern Detection

##  Objective: 
The primary objective of Milestone 2 was to segment the student population into distinct, actionable **Study Profiles** using unsupervised learning (K-Means). This process established the necessary student segments for building a targeted recommendation system in the next phase.

***

##  Dataset Source
Dataset Name - Student Habits and Academic Performance Dataset 
Source URL [https://www.kaggle.com/datasets/aryan208/student-habits-and-academic-performance-dataset](https://www.kaggle.com/datasets/aryan208/student-habits-and-academic-performance-dataset) 
Nature- Synthetic (Simulated) 
Used the cleaned dataset from EDA (Milestone1)

***

##  Tools Used
* **Pandas** & **NumPy** (Data manipulation and preparation).
* **Scikit-learn** (`StandardScaler`, `PCA`, and `KMeans` Clustering).
* **Matplotlib** & **Seaborn** (Visualization).

***

## Steps Followed (Milestone 2)

1.  **Feature Selection and Scaling:** Twelve key numerical features (representing habits, psychological state, and performance) were selected. These were then **standardized** using the **StandardScaler** to ensure all variables contributed equally to clustering.
2.  **Dimensionality Reduction:** **Principal Component Analysis (PCA)** was applied, reducing the high-dimensional feature set to **2 Principal Components (PC1 & PC2)** for visualization (retaining 40% of the variance).
3.  **Optimal K Determination:** The **Elbow Method** was executed, leading to the selection of **$K=4$** as the optimal number of student segments.
4.  **Clustering and Labeling:** The **K-Means model** was fitted with $K=4$, and the resulting cluster labels were added as a new column in the main DataFrame.
5.  **Visualization and Profiling:** Cluster separation was confirmed using a PCA Scatter Plot. A final **Cluster Mean Analysis** was performed on the original, unscaled features to define the unique characteristics of each of the four Study Profiles.

***

##  Key Insights and Study Profiles

The clustering analysis successfully segmented students into four distinct profiles, proving that a single "more study time" recommendation is insufficient.

| Cluster Label | Assigned Profile Name | Key Characteristics | Recommendation Focus |
| :--- | :--- | :--- | :--- |
| **Cluster 0** | **🔴 At-Risk/Struggling** | Lowest Score ($\approx 72.32$). Lowest Motivation, Lowest Study Hours, **Highest Anxiety**. | **Immediate Intervention** on Motivation and Time Management. |
| **Cluster 1** | **🟢 Well-Balanced Achievers** | High Score ($\approx 94.24$). **Highest Motivation, Very Low Stress/Anxiety**. | **Role Model Behavior:** Maintain holistic habits; provide advanced challenges. |
| **Cluster 2** | **🟡 Stressed High Performers** | High Score ($\approx 94.17$). **Highest Study Hours, Highest Stress, Lowest Mental Health**. | **Wellness Priority:** Recommend stress reduction and study efficiency. |
| **Cluster 3** | **🔵 Naturally Gifted/Calm** | Highest Score ($\approx 94.82$). **Lowest Stress, Highest Mental Health, High Efficiency**. | **Enrichment:** Offer advanced resources to maintain challenge. |

#### Visualization Insight

The **Bar Plots** were critical in profiling, showing that high-performing clusters (1, 2, and 3) are differentiated primarily by **Stress Level** and **Mental Health Rating**. This confirmed that the recommendation system must be **psychologically tailored** to address the specific root cause of the student's struggle or success.
