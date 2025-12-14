Finding Hidden Customer Segments
Project Overview

This project focuses on discovering hidden customer segments using unsupervised machine learning. The goal is to understand underlying customer behavior patterns from real-world transactional data and evaluate how different clustering strategies perform in capturing meaningful structure.

The work emphasizes experimentation, comparison, and interpretation rather than assuming a single model upfront.

Dataset

Source: Brazilian E-Commerce Public Dataset (Olist) from Kaggle

The dataset consists of multiple relational tables covering:

Orders

Customers

Products

Reviews

Payments

Shipping and delivery information

All tables were merged and reshaped into a customer-level analytical dataset tailored for segmentation.

Data Preparation & Feature Engineering

The raw data was extensively processed before modeling:

Merged multiple tables into a unified customer-centric dataset

Handled missing values (NaNs) and inconsistent records

Processed numerical and categorical features appropriately

Removed identifiers and non-informative fields

Created aggregated behavioral features per customer (purchase behavior, delivery experience, reviews, product characteristics, timing patterns)

Applied feature scaling to ensure fair distance-based learning

This resulted in a clean, high-dimensional behavioral dataset ready for unsupervised analysis.

Modeling & Experiments

Multiple clustering approaches were explored and compared:

K-Means

Gaussian Mixture Models (GMM)

HDBSCAN (density-based clustering)

Each method was evaluated:

With PCA (to analyze compressed feature space)

Without PCA (using original feature space)

Models were compared using:

Silhouette Score

Davies–Bouldin Index

Calinski–Harabasz Index

Visual inspection of cluster structure

Final Model Selection

After systematic comparison:

PCA + HDBSCAN was selected as the best-performing approach

It captured natural density-based groupings

Handled irregular customers as noise instead of forcing assignments

Produced clusters that aligned well with observed behavioral patterns

Interpretation & Insights

Clusters were interpreted by mapping cluster labels back to original features and analyzing:

Purchase and spending behavior

Delivery performance

Review and sentiment patterns

Product complexity

Time-based habits

The project focuses on behavioral understanding rather than static labels.

Current Status

Core data processing, modeling, evaluation, and clustering are complete

Models and outputs are saved and reproducible

Ongoing work: exploring business questions, strategies, and insights that can be derived from these customer segments
