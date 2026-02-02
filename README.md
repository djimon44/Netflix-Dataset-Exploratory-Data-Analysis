# 🎬 Netflix Content Strategy Analysis (EDA)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-Pandas%20%7C%20Seaborn%20%7C%20Matplotlib-orange)
![Status](https://img.shields.io/badge/Status-Completed-green)

## 📌 Project Overview
This project performs an Exploratory Data Analysis (EDA) on the Netflix dataset to understand the platform's content strategy, focusing on the shift between Movies and TV Shows, global content distribution, and audience targeting. 

The analysis covers data cleaning, univariate analysis (distributions), bivariate analysis (correlations), and genre trends.

## 📂 Dataset
- **Source:** [Kaggle - Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- **Rows:** ~8,800 entries
- **Columns:** 12 features (Type, Title, Director, Cast, Country, Date Added, Release Year, Rating, Duration, Listed In, Description)

---

## 🔍 Key Findings & Insights

### 1. The "TV Show" Pivot
* **Insight:** While Movies historically make up **70%** of the library, data from 2016–2021 reveals a strategic pivot. The number of TV Shows added annually has grown faster than movies, narrowing the gap significantly in recent years.

### 2. Global Content Strategy
* **Top Producers:** The **United States** is the dominant producer, followed by **India** and the **United Kingdom**.
* **Duration Differences:** Indian movies have a significantly higher median duration (**~125 mins**) compared to US/UK movies (**~95 mins**), reflecting cultural differences (e.g., Bollywood intermissions) that Netflix accommodates.

### 3. Audience Targeting (Maturity)
* **Dominant Rating:** The library is heavily skewed towards **TV-MA** (Mature Audiences) and **TV-14**.
* **Gap in Market:** There is a lower volume of **TV-Y** (Kids) content compared to adult content, suggesting Netflix prioritizes adult retention over functioning as a primary "digital babysitter."

### 4. Genre Trends
* **Top Genres:** "International Movies", "Dramas", and "Comedies" are the most tagged categories.
* **Strategy:** The high prevalence of the "International" tag confirms Netflix's aggressive localization strategy to capture non-English speaking markets.

---

## 🛠️ Technical Process

### 1. Data Cleaning
* **Missing Values:** Handled high missing rates in `Director` (30%) and `Cast` columns by filling with placeholders. Dropped minimal missing rows in `Date_Added`.
* **Data Types:** Converted `date_added` to datetime objects for temporal analysis.
* **Text Cleaning:** Cleaned the `duration` column (removing " min" and " Seasons") to allow for numerical calculations.

### 2. Visualizations
The analysis includes:
* **Univariate:** Histograms for release years, Countplots for ratings, and Horizontal Bars for top countries.
* **Bivariate:** Boxplots comparing movie duration across countries, and Heatmaps showing the relationship between Rating and Content Type.
* **Text Analysis:** Word Cloud visualization for the most popular Genres.
