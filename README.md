# Customer Segmentation

This project implements unsupervised machine learning for customer segmentation using K-Means clustering on retail customer data. The Jupyter notebook analyzes shopping behaviors to identify distinct customer groups based on spending patterns and demographics, enabling targeted marketing strategies.

## Project Overview

The notebook processes customer datasets with pandas and scikit-learn to perform clustering analysis. It uses elbow method and silhouette scores to determine optimal clusters, visualizing segments through scatter plots and pairplots.

## Core Analysis Workflow

The project follows a complete unsupervised learning pipeline for customer segmentation.

- File upload prompts for CSVs like 'Mall_Customers.csv', loading into DataFrames for initial inspection and EDA.  
- Data preprocessing includes feature scaling with StandardScaler on numeric columns like age, annual income, and spending score.  
- Clustering applies K-Means with elbow method (inertia plot) and silhouette analysis to find optimal k value, typically 5 clusters for standard mall customer data.

## Key Visualizations

Multiple plots illustrate clustering results and customer distributions.

- Elbow method plot shows inertia vs. number of clusters (k=1 to 10) to identify optimal segmentation point.  
- Silhouette score plots validate cluster quality and separation.  
- Scatter plots visualize clusters in 2D space (Annual Income vs. Spending Score), color-coded by cluster labels.  
- Pairplots and heatmaps reveal feature correlations and segment characteristics.

## Dataset Insights

Analysis typically reveals 5 customer segments: balanced spenders, high-income low-spenders, conservative shoppers, target high-value customers, and young high-spenders. These insights support personalized marketing, inventory planning, and customer retention strategies.

## Requirements

Python 3.6+  
Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn  
Environment: Google Colab (uses `google.colab.files` for upload) or local Jupyter with equivalent file handling.

No additional installations needed in Colab as libraries are pre-installed.

## Usage

**Open in Google Colab:**  
- Go to Google Colab.  
- Upload the notebook: `File > Upload notebook > Select "Customer-Segmentation.ipynb"`.

**Prepare Data:**  
Ensure you have a CSV file with customer data. Expected columns include:  
- `CustomerID`: Unique customer identifier.  
- `Gender`: Customer gender (Male/Female).  
- `Age`: Customer age.  
- `Annual Income`: Annual income in thousands.  
- `Spending Score`: Score assigned by mall (1-100 based on behavior).  

Example data source: Kaggle Mall Customer Segmentation dataset.

**Run the Notebook:**  
- Execute cells sequentially (Shift+Enter).  
- In the upload cell, provide your CSV when prompted.  
- The notebook performs EDA, finds optimal clusters, applies K-Means, and displays segmentation plots.

**Expected Outputs:**  
- Console prints: Dataset shape, feature statistics, optimal k value, silhouette score.  
- Plots:  
  - Elbow method for optimal k.  
  - Silhouette analysis.  
  - Cluster scatter plot (Income vs Spending Score).  
  - Segment distribution visualizations.
