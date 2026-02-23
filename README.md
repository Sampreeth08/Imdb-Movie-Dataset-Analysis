# IMDB Movie Dataset Analysis (Project 1)

## Overview

This repository contains an exploratory data analysis and ETL notebook for the IMDB movie dataset. The primary work is performed in the Jupyter notebook which cleans the data, applies business rules, and produces visualizations useful for movie business analysis and dashboarding.

## Repository Contents

- [IMDB Movie Business Rules and dashboard_problems statements.txt](IMDB%20Movie%20Business%20Rules%20and%20dashboard_problems%20statements.txt): Business rules and problem statements for the dashboard.
- [imdb_ddl.sql](imdb_ddl.sql): DDL for loading the cleaned dataset into a relational database.
- [imdb_movies.csv](imdb_movies.csv): Original raw dataset (CSV).
- [imdb_movies_cleaned.csv](imdb_movies_cleaned.csv): Cleaned and preprocessed dataset exported from the notebook.
- [imdbmovies_etl.ipynb](imdbmovies_etl.ipynb): Main Jupyter notebook performing ETL and analysis.

## Requirements and tools used

- Python 3.8+
- Jupyter or JupyterLab
- Common Python packages: `pandas`, `matplotlib`, `sql alchemy` (install via pip)

## How to run

1. Open the notebook: [imdbmovies_etl.ipynb](imdbmovies_etl.ipynb)
2. Run the cells sequentially to reproduce the ETL steps and visualizations.
3. After running, the notebook writes a cleaned CSV: [imdb_movies_cleaned.csv](imdb_movies_cleaned.csv).


## Steps Followed

### Data Cleaning in Python
- Removed duplicate movies using title and release year
- Generated missing movie IDs
- Fixed invalid ratings, budgets, and gross values
- Filled missing director and actor names with "Unknown"
- Handled missing release years using median values

### Data Loading to MySQL
- Connected Python to MySQL using SQLAlchemy
- Created a clean movies table
- Loaded the transformed dataset into the database

### SQL Analysis
- Found top grossing movies by year
- Calculated average rating by genre
- Identified top directors based on ratings
- Analyzed budget vs gross relationship
- Determined the most profitable movie genre

### Data Visualization
- Created bar charts, line charts, and scatter plots using Matplotlib
- Built simple dashboards to present business insights

### Dashboard Modules & Analysis

🔹 **Dashboard 1: Revenue Analysis**

<img width="571" height="489" alt="image" src="https://github.com/user-attachments/assets/659249b3-8626-4197-9634-b1ba36100628" />

- Top 10 highest grossing movies by year
- Year-wise revenue trends
- Comparison of gross revenue across different years

🔹 **Dashboard 2: Genre Performance Insights**
<img width="580" height="455" alt="image" src="https://github.com/user-attachments/assets/3cf82d94-d919-48c6-a89e-c7b8ee7d8c2e" />
- Average rating distribution across genres
- Total movies released per genre
- Genre-wise profitability comparison

🔹 **Dashboard 3: Director Performance Analysis**
<img width="585" height="455" alt="image" src="https://github.com/user-attachments/assets/248afcce-5207-49dd-9b25-c5e4cb01cbc3" />
- Top 5 directors based on average movie rating
- Director-wise movie count
- Comparison of director performance by ratings

🔹 **Dashboard 4: Budget & Profitability Analysis**
<img width="571" height="455" alt="image" src="https://github.com/user-attachments/assets/2369ada3-9e2a-411c-839b-3120e3123457" />
- Budget vs Gross revenue correlation
- Most profitable genre (Gross − Budget)
- Overall profit trends across movies

  🔹 **Dashboard 5: Most Profitable Genre Deep Dive**
<img width="589" height="455" alt="image" src="https://github.com/user-attachments/assets/70a5ab38-208e-46f8-91a7-c3b20e50088c" />
- Comprehensive genre profitability analysis
- Genre-wise profit margins
- Genre performance comparisons and trends

## Notebook highlights

- Data loading and initial inspection from [imdb_movies.csv](imdb_movies.csv).
- Cleaning steps: handling missing values, standardizing columns, parsing dates, and normalizing numeric fields.
- Business-rule applications as described in [IMDB Movie Business Rules and dashboard_problems statements.txt](IMDB%20Movie%20Business%20Rules%20and%20dashboard_problems%20statements.txt).
- Visualizations for release trends, top genres, rating distributions, and revenue analysis.

