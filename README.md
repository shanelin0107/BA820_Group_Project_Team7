# BA820_Group_Project_Team7 San Francisco Building Complaints Segmentation

## Project Overview
**Project Title:** San Francisco Building Complaints Segmentation  
**Course:** BA820 – Project Milestone 1  
**Team:** B1 Team7  
**Team Members:**  
- Yu-Hsiang (Rick) Wang  
- Ching-Hsuan (Shawn) Lin  
- Kuang-Ching (Amanda) Ting  
- Ming-Hua (Jasmine) Tsai  

**Date:** February 19, 2025

## Problem Statement
Managing building complaints and inspections in San Francisco is resource-intensive, with manual classification leading to inefficient prioritization and assignment. Our objective is to leverage unsupervised machine learning methods to identify patterns, classify complaints by severity, and improve resource allocation. By uncovering hidden patterns in both structured and unstructured data, our approach aims to streamline issue resolution and enhance decision-making.

## Data Source
- San Francisco Government's Open Data: [SF Open Data](https://reurl.cc/eGKE5K)
- Additional references include audit reports and budget documents from SF agencies.

## Analysis Plan
1. **Data Preprocessing**  
   - **Structured Data:** Remove complaint descriptions to build an initial model using features such as complaint type, location, and time.  
   - **Text Data:** Later, reintroduce the complaint descriptions and perform text preprocessing (remove stop words, punctuation, and special characters; convert text to lowercase; apply lemmatization).

2. **Initial Clustering**  
   - Build a **K-Means** model using the structured features to quickly segment complaints and assess severity-level distinctions.
   - Compare these results with **Hierarchical Clustering** to evaluate which method yields more interpretable and actionable groupings.

3. **Text Mining & Topic Modeling**  
   - After text preprocessing, convert the cleaned text into numerical representations (using TF-IDF or Bag-of-Words).
   - Apply **Latent Dirichlet Allocation (LDA)** to uncover latent topics in the complaint descriptions.

4. **Dimensionality Reduction & Visualization**  
   - Use PCA or t-SNE to visualize clustering results across different algorithms and to integrate text-derived features.
   - Visualize and assess cluster separability, identify potential outliers, and refine the segmentation.

## Preliminary Results
- **K-Means Clustering:**  
  Initial results indicate that the data naturally splits into two main groups (as suggested by silhouette scores), though the elbow method indicates that four clusters may provide a more granular segmentation. This trade-off will be explored further.
- **Clustering Evaluation:**  
  Comparison between K-Means and Hierarchical Clustering will help determine the optimal balance between general segmentation (k = 2) and detailed clustering (k = 4).

## Future project timeline
**Week 1 (Feb 20 – Feb 26):**
- Implement Hierarchical Clustering and compare with K-Means results.
- Reintroduce complaint descriptions and perform text preprocessing.
- Convert text data to numerical vectors (TF-IDF, Bag-of-Words).

**Week 2 (Feb 27 – Mar 5):**
- Apply LDA (or an alternative topic modeling approach) to extract latent topics.
- Use dimensionality reduction techniques (PCA or t-SNE) for visualization.
- Integrate clustering and topic modeling insights to assign severity levels.
- Finalize and prepare the milestone report.

## GitHub Repository
The project is hosted on GitHub. Please refer to the repository for the source code and additional documentation:  
[BA820_Group_Project_Team7](https://github.com/shanelin0107/BA820_Group_Project_Team7.git)

## References
- San Francisco Open Data: Building Complaints and Violations Dataset (2017-2022)
- City and County of San Francisco, Department of Building Inspection (DBI) Annual Budget Reports (2018-2022)
- San Francisco Controller’s Office, Audit Report on Building Complaint Classification Efficiency (2021)
- ChatGPT conversation and analysis insights

