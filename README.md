# 🎶Spotify Most Streamed Songs Analysis

## Overview
This project explores Spotify’s most streamed tracks using Python, Pandas, Seaborn, and Matplotlib. It focuses on listener patterns, popularity metrics, audio features, and temporal trends to understand how musical characteristics relate to track success over time.

## 🔗Dataset
The analysis is based on the `tracks.csv` file from the following public dataset:  
https://www.kaggle.com/datasets/lehaknarnauli/spotify-datasets

Because the dataset is large, it is **not** included in this repository. To reproduce the analysis, download `tracks.csv` from Kaggle and place it in a local `data/` folder as described below.

## 📁Project Structure
A suggested structure for this repository is:
*** 
spotify-most-streamed-analysis/
├─ spotify_eda.ipynb              # Main EDA notebook
├─ requirements.txt               # Python dependencies
├─ data/                          # Local data folder (not tracked)
│  └─ tracks.csv                  # Downloaded from Kaggle
***

## 📊Methods and Analysis
The notebook includes the following main steps:​

### Data loading and cleaning
Import tracks.csv, inspect schema, handle missing values.
Convert release_date to a datetime index and derive duration in seconds from duration_ms.​

### Descriptive statistics and filtering
Summary statistics for popularity, duration, energy, danceability, tempo, valence, etc.
Identification of least and most popular tracks and basic popularity distributions.​

### Correlation analysis
Pearson correlation matrix across numeric audio features (e.g., energy, loudness, acousticness, valence).
Heatmap to highlight strong positive and negative relationships.​

### Feature relationships
Scatter plots with regression lines:
Loudness vs energy (energetic songs tend to be louder).
Popularity vs acousticness (more acoustic songs often appear less popular).​

### Temporal trends
Histogram of number of songs released per year.
Bar plot of total song duration per year to explore changes in typical track length.

## 💻Dashboard-Style Visualizations
To align with the “dashboard” description, the project can include a summary section with:​
Top genres by average popularity (bar chart)
Top artists by number of tracks or average popularity (bar chart).
Yearly trends in song count and total duration with simple trend lines (line/column plots).​
Optionally, the same dataset can feed a separate Power BI report for interactive exploration of genre performance, artist dominance, and temporal trends.

## 🌐How to Run Locally
- Clone the repository
***
bash
git clone https://github.com/<your-username>/spotify-most-streamed-analysis.git
cd spotify-most-streamed-analysis
***
- Install dependencies
***
bash
pip install -r requirements.txt
***
- Download the dataset
Visit: https://www.kaggle.com/datasets/lehaknarnauli/spotify-datasets
- Download tracks.csv.
Create a data/ folder in the project root and place tracks.csv inside: data/tracks.csv.​
- Run the notebook
***
bash
jupyter notebook
***
- Open spotify_eda.ipynb and run all cells to reproduce the analysis and visualizations.

## 🧱Tech Stack
Python, Jupyter Notebook
Pandas, NumPy
Matplotlib, Seaborn
(Optional) Power BI for interactive dashboards.

## ⚠️Notes and Limitations
This project is intended for educational and analytical purposes only.
All data is sourced from Spotify metadata via the Kaggle dataset and may not represent the complete Spotify catalog or all regions.
