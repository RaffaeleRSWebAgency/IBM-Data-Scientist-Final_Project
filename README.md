# IBM Data Scientist Final Project

This repository contains the final capstone project for the **IBM Data Scientist Professional Certificate**. The primary focus is on end-to-end data science processes using SpaceX launch data (or any other dataset relevant to your final project). It includes data collection, data wrangling, exploratory data analysis (EDA), interactive visualizations, dashboards, and a predictive modeling component.

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Data Sources](#data-sources)
3. [Project Architecture](#project-architecture)
4. [Installation and Environment Setup](#installation-and-environment-setup)
5. [Usage Instructions](#usage-instructions)
6. [Detailed Notebooks/Scripts](#detailed-notebooksscripts)
7. [Results and Insights](#results-and-insights)
8. [Dashboards and Visualizations](#dashboards-and-visualizations)
9. [Predictive Modeling](#predictive-modeling)
10. [Folder Structure](#folder-structure)
11. [Roadmap and Future Work](#roadmap-and-future-work)
12. [License](#license)
13. [References and Acknowledgments](#references-and-acknowledgments)
14. [Contact Information](#contact-information)

---

## Project Overview

This capstone project aims to showcase the end-to-end workflow of a Data Scientist, applying concepts and techniques learned during the IBM Data Scientist Professional Certificate. Specifically, it covers:

- **Data Collection**: Retrieving data through APIs (e.g., [SpaceX API](https://api.spacexdata.com/)) and web scraping (e.g., from [Wikipedia](https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches)).
- **Data Wrangling**: Cleaning, transforming, merging, and preparing datasets for analysis.
- **Exploratory Data Analysis (EDA)**: Visualizing and exploring data patterns, distributions, and relationships using libraries like Matplotlib, Seaborn, and SQL queries.
- **Interactive Visualization**: Creating dashboards using Plotly Dash and interactive geospatial maps using Folium.
- **Predictive Modeling**: Building machine learning models (Logistic Regression, SVM, Decision Tree, etc.) to predict future outcomes (e.g., launch success).
- **Results & Conclusions**: Presenting findings, offering actionable insights, and discussing further improvements.

---

## Data Sources

1. **SpaceX API**  
   - Endpoint: `https://api.spacexdata.com/v4/launches`  
   - Provides official data about SpaceX launches, including rocket details, payload information, and success/failure outcomes.

2. **Wikipedia Web Scraping**  
   - Page: [List of Falcon 9 and Falcon Heavy launches](https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches)  
   - Historical records, launch manifests, landing outcomes, and additional metadata.

3. **(Optional) Additional Data**  
   - For weather, you might use external APIs (e.g., OpenWeatherMap) or archived data.  
   - For cost, reusability metrics, or timeline data, reference official SpaceX sources or third-party aggregators.

> **Disclaimer**: Data sources may contain inaccuracies or change over time. Validate your data and handle missing/erroneous fields appropriately.

---

## Project Architecture

Below is a high-level view of the typical workflow in this project:

1. **Data Ingestion**  
   - Fetch data via REST API and store JSON locally.  
   - Scrape Wikipedia with Python’s `BeautifulSoup` and parse HTML tables.

2. **Data Storage**  
   - Load, combine, and store data into a local SQLite database (or keep it in CSV files, depending on preference).

3. **Data Wrangling**  
   - Clean & transform columns (e.g., date parsing, type casting, handling missing values).  
   - Feature engineering (e.g., extracting year, categorizing orbits).

4. **Exploratory Data Analysis**  
   - Create plots with Matplotlib and Seaborn.  
   - Perform SQL queries for deeper insights.

5. **Visualization & Dashboard**  
   - Create an interactive map using Folium to visualize launch sites and outcomes.  
   - Build a Plotly Dash dashboard to allow interactive filtering (e.g., payload slider, site dropdown).

6. **Machine Learning**  
   - Prepare features for classification.  
   - Compare multiple models (Logistic Regression, SVM, Decision Tree, etc.) using train/test sets, accuracy scores, confusion matrices.

7. **Reporting & Conclusion**  
   - Summarize findings in slides or a markdown report.  
   - Discuss limitations and potential enhancements.

---

## Installation and Environment Setup

1. **Clone the Repository**  
   ```bash
   git clone https://github.com/<YourUsername>/IBM-Data-Scientist-Final_Project.git
   cd IBM-Data-Scientist-Final_Project
