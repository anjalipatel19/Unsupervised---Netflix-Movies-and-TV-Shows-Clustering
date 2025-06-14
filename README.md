# Netflix Movies and TV Shows Clustering

## Project Overview

This project performs **unsupervised learning** on Netflix’s catalog of movies and TV shows to uncover natural groupings based on content features. The goal is to cluster titles using attributes like genre, cast, country, rating, and description—ultimately helping with recommendation systems and content categorization.

> **Project Type**: Unsupervised Learning  
> **Contributor**: *Anjali Patel*

## Project Summary

With fierce competition in the OTT space, Netflix's success is heavily dependent on providing personalized content to its audience. This project uses clustering techniques to analyze and group content based on descriptive metadata.

The analysis was conducted on a dataset containing \~12 columns and thousands of titles. Key steps include:

* Data Cleaning: Removing missing values in `director`, `cast`, `country`, `date_added`.
* EDA: Understand Netflix content distribution by year, rating, country, etc.
* Feature Engineering: TF-IDF vectorization on textual data like `description`, `cast`, `director`.
* Dimensionality Reduction: PCA to reduce features from 10,000+ to 3000, preserving 80% variance.
* Clustering: Using K-Means (5 clusters) and Agglomerative Clustering (7 clusters).
* Recommendation System: Built using cosine similarity between content features.

## Tools & Technologies Used

* **Language**: Python 3
* **Environment**: Jupyter Notebook
* **Libraries**:
  * `pandas`, `numpy` – data manipulation
  * `matplotlib`, `seaborn`, `plotly` – visualizations
  * `sklearn` – TF-IDF, PCA, clustering models
  * `scipy` – dendrograms and hierarchical clustering
  * `nltk` – natural language processing (if used)

## Key Insights

* **Content Type**: Netflix has more movies (\~5372) than TV shows (\~2398).
* **Rating**: `TV-MA` is the most frequent rating for both movies and shows, indicating a mature content focus.
* **Release Trends**:
  * Peak for movies: **2017–2018**
  * Peak for TV shows: **2020**
  * A sharp decline in content addition post-2020.
* **Seasonality**: Most content is added between **October and January**.
* **Geography**:
  * **USA** contributes the most content overall.
  * **India** ranks high, especially in movie production.
* **Clustering**:
  * **K-Means** found 5 optimal clusters.
  * **Agglomerative Clustering** suggested 7, visualized with a dendrogram.

## Visual Insights

Below are some visualizations from the analysis:

1. **Distribution of Movies vs TV Shows**
   ![1](https://github.com/user-attachments/assets/bd72706c-5bb8-4d15-87dd-67f0dce4f617)
   Shows the count of Movies and TV Shows available on Netflix.

2. **Top 15 Countries by Content Count**
   ![2](https://github.com/user-attachments/assets/69f99e2a-9aec-4d98-94f7-f4419d9e1279)
   Reveals how countries like USA and India dominate Netflix's catalog.

3. **Monthly Content Addition Trend**
   ![3](https://github.com/user-attachments/assets/17096aa7-3b02-4a25-beb9-649a8b0719f3)
   Highlights content upload patterns across months, peaking from October to January.

4. **Top 10 Most Common Ratings**
   ![4](https://github.com/user-attachments/assets/c43470b5-7b71-4b76-9c1e-71b419c9364c)
   Indicates that TV-MA is the most frequently used rating.

5. **Movies Released in last 20 Years**
   ![5](https://github.com/user-attachments/assets/1c6ca001-4b8a-4351-a7bd-25d23e453285)
   Tracks how the release volume has changed year-over-year.

6. **K-Means Clustering Visualization**
   ![6](https://github.com/user-attachments/assets/7bd20f88-c8c9-459b-b105-72d7f96f3364)
   Visualizes how the content was grouped into 5 clusters using PCA.

7. **Agglomerative Clustering Dendrogram & Histogram**
   ![7](https://github.com/user-attachments/assets/f215bfaf-2d61-40b9-b98a-d40be6750ede)
   ![71](https://github.com/user-attachments/assets/9b57a45a-c704-4eda-a6af-45270c4c1ff3)
   Tree structure that suggests 7 natural groupings based on content metadata.

## Algorithms Used

* **TF-IDF Vectorization**: To convert textual columns into numerical vectors.
* **PCA (Principal Component Analysis)**: Reduced features to speed up clustering.
* **K-Means Clustering**: Used Elbow Method to determine 5 optimal clusters.
* **Agglomerative Clustering**: Hierarchical method visualized through dendrogram.

## Recommendation System

A **content-based recommender** was implemented using **cosine similarity** on TF-IDF vectors.
It recommends similar shows/movies based on user preferences (description, cast, genre, etc.).

## Repository Structure

* **Unsupervised - Netflix Movies and TV Shows Clustering** – Main project folder
  * **Unsupervised on Netflix Movies and TV Shows Clustering.ipynb** – Jupyter Notebook containing the full analysis
  * **NETFLIX MOVIES AND TV SHOWS CLUSTERING.csv** – Dataset used for analysis
* **LICENSE** – MIT License file
* **README.md** – Documentation explaining the project

##  License

This project is licensed under the **MIT License**. See the `LICENSE` file for more information.
