# SpaceX Launch Data Analysis: End-to-End Data Science Project

---

## Slide 1: Project Title

**Title:**  
SpaceX Launch Data Analysis: End-to-End Data Science Project

**Description:**  
- **Author:** Raffaele Schiavone  
- **Date:** [Month Year]  
- **Course:** IBM Data Science Professional Certificate (Capstone Project)  
- *(Optionally, include a SpaceX-related cover image.)*

---

## Slide 2: Executive Summary

**Executive Summary:**

### Summary of Methodologies:
- **Data Collection:**
  - Retrieve launch data from the SpaceX REST API.
  - Web scrape historical launch data from Wikipedia.
- **Data Wrangling:**
  - Clean and unify datasets by removing duplicates, handling missing values, and merging sources.
- **Exploratory Data Analysis (EDA):**
  - Generate visualizations using matplotlib/seaborn.
  - Execute SQL queries for additional insights.
- **Interactive Visual Analytics:**
  - Develop a map-based visualization using Folium.
  - Create an interactive dashboard with Plotly Dash.
- **Predictive Analysis:**
  - Build classification models (e.g., Logistic Regression, SVM, Decision Tree) to predict launch success.

### Summary of All Results:
- Identified key relationships between flight number, payload mass, and success rate.
- Determined the influence of orbit types and launch sites on launch outcomes.
- Produced an interactive map highlighting launch sites, outcomes, and proximity to infrastructure.
- Deployed a Plotly Dash dashboard displaying success counts, payload relationships, and success rates per site.
- Developed and compared multiple classification models to select the best performing one for predicting launch outcomes.

---

## Slide 3: Introduction

**Introduction:**

### Project Background and Context:
SpaceX’s mission is to reduce space transportation costs and enable Mars colonization. Analyzing launch performance is crucial for enhancing rocket reusability and overall mission success.

### Problems to Be Solved:
- Which factors (e.g., payload, orbit type, or launch site) are most correlated with successful launches?
- How do success rates vary over time and across different booster versions?
- How can a predictive model be built to forecast launch success?

*(Optionally, include a relevant image such as a SpaceX rocket.)*

---

## Slide 4: Methodology Overview

**Methodology:**

We adopted a structured approach:
- **Data Collection:**  
  - Gathered data via the SpaceX API and web scraping from Wikipedia.
- **Data Wrangling:**  
  - Cleaned, merged, and prepared the data.
- **Exploratory Data Analysis (EDA):**  
  - Performed analysis using visualizations and SQL queries.
- **Interactive Visual Analytics:**  
  - Employed Folium for geospatial mapping and Plotly Dash for an interactive dashboard.
- **Predictive Analysis:**  
  - Developed classification models to predict launch success.

*(A high-level flowchart of these steps can be included as needed.)*

---

## Slide 5: Data Collection - Overview

**Data Collection Methodology:**

### Process:
- **SpaceX API Calls:**  
  - Retrieve data on flight details, rocket names, payloads, and launch outcomes.
- **Web Scraping:**  
  - Extract historical data from Wikipedia (e.g., flight histories, payload masses, landing outcomes).
- **Data Storage:**  
  - Store raw data locally for subsequent cleaning and merging.

### Why These Sources?
- **SpaceX API:** Offers up-to-date, official launch data.
- **Wikipedia:** Provides additional historical context not available via the API.

*(A flowchart or bullet list outlining the data flow can be added.)*

---

## Slide 6: Data Collection – SpaceX API

**SpaceX REST API:**

### Process:
- Utilized Python’s `requests` library to call SpaceX API endpoints.
- Extracted flight information, rocket metadata, and launch outcomes.
- Converted JSON responses into pandas DataFrames for further processing.

**GitHub URL:** [Insert your GitHub link to the SpaceX API calls notebook here]

**Flowchart:**
- REST API Endpoint (e.g., `https://api.spacexdata.com/v4/launches`)
- `requests.get()`
- JSON to DataFrame
- Data stored locally

*(Optionally, insert a screenshot or flowchart.)*

---

## Slide 7: Data Collection – Web Scraping

**Web Scraping:**

### Process:
- Employed Python’s `BeautifulSoup` to parse HTML from Wikipedia’s "List of Falcon 9 and Falcon Heavy launches" page.
- Extracted tables containing flight histories, payload masses, and landing outcomes.
- Converted extracted HTML tables into pandas DataFrames.

**GitHub URL:** [Insert your GitHub link to the web scraping notebook here]

**Flowchart:**
- Request Wikipedia page
- Parse with BeautifulSoup
- Extract HTML table rows
- Convert to DataFrame

*(Optionally, insert a screenshot or code snippet.)*

---

## Slide 8: Data Wrangling

**Data Wrangling:**

### Steps:
- **Cleaning:**  
  - Remove duplicates and handle missing values (e.g., payload mass, orbit type).
- **Merging:**  
  - Combine API data and scraped data into a single master DataFrame.
- **Feature Engineering:**  
  - Create new columns (e.g., launch year, success/failure labels, landing outcome type).

**GitHub URL:** [Insert your GitHub link to the data wrangling notebook here]

*(Optionally, display a sample of the final DataFrame using `.head()` or a flowchart.)*

---

## Slide 9: EDA with Data Visualization

**EDA with Data Visualization (Summary):**

### Charts Plotted & Rationale:
- **Scatter Plots:**
  - Flight Number vs. Launch Site.
  - Payload vs. Launch Site.
- **Bar Chart:**
  - Success Rate vs. Orbit Type.
- **Additional Scatter Plots:**
  - Flight Number vs. Orbit Type.
  - Payload vs. Orbit Type.
- **Line Chart:**
  - Yearly average success rate trend.

**GitHub URL:** [Insert your GitHub link to the EDA Visualization notebook here]

---

## Slide 10: EDA with SQL

**EDA with SQL (Summary):**

### SQL Queries Performed:
- Retrieve distinct launch site names.
- Filter launch sites beginning with 'CCA'.
- Calculate total payload mass.
- Compute average payload mass by booster version (e.g., F9 v1.1).
- Determine the first successful ground landing date.
- Identify successful drone ship landings with payloads between 4000 and 6000.
- Count total mission outcomes (successes vs. failures).
- Find the booster that carried the maximum payload.
- Analyze 2015 failed drone ship landings.
- Rank landing outcomes between specific dates.

**GitHub URL:** [Insert your GitHub link to the EDA with SQL notebook here]

---

## Slide 11: Build an Interactive Map with Folium

**Interactive Map (Folium):**

### Map Objects:
- Markers representing each launch site.
- Color-coded markers indicating success or failure.
- Circles to show distances from key infrastructure (coastlines, railways, highways).

### Reasons:
- Visualize the geographic distribution of launch sites.
- Assess correlations between site proximity to infrastructure and launch success.

**GitHub URL:** [Insert your GitHub link to the Folium map notebook here]

*(Optionally, insert a screenshot of the Folium map.)*

---

## Slide 12: Build a Dashboard with Plotly Dash

**Dashboard (Plotly Dash):**

### Dashboard Components:
- Pie Chart showing total launch successes by site.
- Interactive Scatter Plot of payload vs. launch outcome with a range slider.
- Dropdown menu for selecting a specific launch site to filter results.

### Why:
- Enables interactive exploration of success distribution.
- Facilitates quick comparisons of payload ranges among booster versions.

**GitHub URL:** [Insert your GitHub link to the Plotly Dash notebook here]

*(Optionally, insert a screenshot of the live dashboard.)*

---

## Slide 13: Predictive Analysis (Classification)

**Predictive Analysis Overview:**

### Approach:
- **Train-Test Split:**  
  - Use features such as flight number, payload, orbit, booster version, launch site, etc.
  - Label: Success/Failure.
- **Model Building:**  
  - Implement models including Logistic Regression, SVM, Decision Tree, etc.
- **Hyperparameter Tuning:**  
  - Apply GridSearchCV or RandomizedSearchCV.
- **Evaluation:**  
  - Use metrics such as accuracy, confusion matrix, and classification report.

**GitHub URL:** [Insert your GitHub link to the predictive analysis notebook here]

**Flowchart:**
Data → Feature Selection/Engineering → Train/Test Split → Model Building → Evaluation → Optimization → Final Model

---

## Slide 14: Results – EDA Visuals: Flight Number vs. Launch Site

**Flight Number vs. Launch Site:**

### Scatter Plot Explanation:
- **X-axis:** Flight Number.
- **Y-axis:** Categorical representation of Launch Site.
- Shows how each launch site was utilized over successive flights.

*(Optionally, insert a screenshot of the scatter plot.)*

---

## Slide 15: Results – EDA Visuals: Payload vs. Launch Site

**Payload vs. Launch Site:**

### Scatter Plot Explanation:
- **X-axis:** Payload Mass.
- **Y-axis:** Categorical representation of Launch Site.
- Demonstrates which launch sites handle heavier payloads based on capacity.

*(Optionally, insert a screenshot of the scatter plot.)*

---

## Slide 16: Results – EDA Visuals: Success Rate vs. Orbit Type

**Success Rate vs. Orbit Type:**

### Bar Chart Explanation:
- **X-axis:** Orbit Type.
- **Y-axis:** Success Rate.
- Identifies orbit types with higher or lower success rates.

*(Optionally, insert a screenshot of the bar chart.)*

---

## Slide 17: Results – EDA Visuals: Flight Number vs. Orbit Type

**Flight Number vs. Orbit Type:**

### Scatter Plot Explanation:
- **X-axis:** Flight Number.
- **Y-axis:** Orbit Type.
- Reveals trends in orbit type usage across different flights.

*(Optionally, insert a screenshot of the scatter plot.)*

---

## Slide 18: Results – EDA Visuals: Payload vs. Orbit Type

**Payload vs. Orbit Type:**

### Scatter Plot Explanation:
- **X-axis:** Payload Mass.
- **Y-axis:** Orbit Type.
- Provides insights into which orbits handle heavier versus lighter payloads.

*(Optionally, insert a screenshot of the scatter plot.)*

---

## Slide 19: Results – EDA Visuals: Launch Success Yearly Trend

**Launch Success Yearly Trend:**

### Line Chart Explanation:
- **X-axis:** Launch Year.
- **Y-axis:** Average Success Rate.
- Illustrates the trend in launch success over time.

*(Optionally, insert a screenshot of the line chart.)*

---

## Slide 20: Results – EDA with SQL (Selected Queries): All Launch Site Names

**All Launch Site Names:**

### Query:
```sql
SELECT DISTINCT Launch_Site FROM SPACEXTBL;
Result Explanation:
Lists each unique launch site used by SpaceX.
(Optionally, insert a screenshot or table of the query result.)

Slide 21: Results – EDA with SQL (Selected Queries): Launch Site Names Begin with 'CCA'
Launch Site Names Begin with 'CCA':

Query:
sql
Copia
SELECT *
FROM SPACEXTBL
WHERE Launch_Site LIKE 'CCA%'
LIMIT 5;
Result Explanation:
Retrieves up to 5 records of launch sites starting with 'CCA'.
(Optionally, insert a screenshot of the query result.)

Slide 22: Results – EDA with SQL (Selected Queries): Total Payload Mass
Total Payload Mass:

Query:
sql
Copia
SELECT SUM(PAYLOAD_MASS__KG_) AS Total_Payload
FROM SPACEXTBL
WHERE Customer = 'NASA';
Result Explanation:
Calculates the total payload mass carried by NASA missions.
(Optionally, insert a screenshot of the query result.)

Slide 23: Results – EDA with SQL (Selected Queries): Average Payload Mass by F9 v1.1
Average Payload Mass by F9 v1.1:

Query:
sql
Copia
SELECT AVG(PAYLOAD_MASS__KG_) AS AvgPayload
FROM SPACEXTBL
WHERE Booster_Version='F9 v1.1';
Result Explanation:
Computes the average payload mass specifically for booster version F9 v1.1.
(Optionally, insert a screenshot of the query result.)

Slide 24: Results – EDA with SQL (Selected Queries): First Successful Ground Landing Date
First Successful Ground Landing Date:

Query:
sql
Copia
SELECT MIN(Date)
FROM SPACEXTBL
WHERE Landing_Outcome='Success (ground pad)';
Result Explanation:
Identifies the earliest date when a ground landing was successful.
(Optionally, insert a screenshot of the query result.)

Slide 25: Results – EDA with SQL (Selected Queries): Successful Drone Ship Landing with Payload 4000–6000
Successful Drone Ship Landing with Payload 4000–6000:

Query:
sql
Copia
SELECT Booster_Version
FROM SPACEXTBL
WHERE Landing_Outcome='Success (drone ship)'
  AND PAYLOAD_MASS__KG_ BETWEEN 4000 AND 6000;
Result Explanation:
Lists the booster versions that successfully landed on a drone ship with a payload in the range of 4000 to 6000 kg.
(Optionally, insert a screenshot of the query result.)

Slide 26: Results – EDA with SQL (Selected Queries): Total Number of Successful and Failed Outcomes
Total Number of Successful and Failed Outcomes:

Query:
sql
Copia
SELECT Landing_Outcome, COUNT(*) AS CountOutcome
FROM SPACEXTBL
GROUP BY Landing_Outcome;
Result Explanation:
Aggregates the count of each landing outcome (e.g., success, failure).
(Optionally, insert a screenshot of the query result.)

Slide 27: Results – EDA with SQL (Selected Queries): Boosters Carried Maximum Payload
Boosters Carried Maximum Payload:

Query:
sql
Copia
SELECT Booster_Version
FROM SPACEXTBL
WHERE PAYLOAD_MASS__KG_ = (SELECT MAX(PAYLOAD_MASS__KG_) FROM SPACEXTBL);
Result Explanation:
Identifies the booster(s) that carried the heaviest payload on record.
(Optionally, insert a screenshot of the query result.)

Slide 28: Results – EDA with SQL (Selected Queries): 2015 Launch Records
2015 Launch Records:

Query:
sql
Copia
SELECT Landing_Outcome, Booster_Version, Launch_Site
FROM SPACEXTBL
WHERE YEAR(Date)=2015
  AND Landing_Outcome='Failure (drone ship)';
Result Explanation:
Displays details (landing outcome, booster version, and launch site) for failed drone ship landings in 2015.
(Optionally, insert a screenshot of the query result.)

Slide 29: Results – EDA with SQL (Selected Queries): Rank Landing Outcomes Between 2010-06-04 and 2017-03-20
Rank Landing Outcomes Between 2010-06-04 and 2017-03-20:

Query:
sql
Copia
SELECT Landing_Outcome, COUNT(*) AS OutcomeCount
FROM SPACEXTBL
WHERE Date BETWEEN '2010-06-04' AND '2017-03-20'
GROUP BY Landing_Outcome
ORDER BY OutcomeCount DESC;
Result Explanation:
Lists each landing outcome along with its occurrence count within the specified date range, ordered from most to least frequent.
(Optionally, insert a screenshot of the query result.)

Slide 30: Folium Map Results: All Launch Sites on the Map
All Launch Sites on the Map:

Screenshot:
Displays a global map with markers representing each launch site.
Visualizes geographic distribution and proximity to coastlines.
(Optionally, insert a screenshot of the Folium map.)

Slide 31: Folium Map Results: Color-Labeled Launch Outcomes
Color-Labeled Launch Outcomes:

Screenshot:
Shows launch sites with color-coded markers indicating success or failure.
Helps visualize patterns in launch outcomes.
(Optionally, insert a screenshot of the color-coded markers.)

Slide 32: Folium Map Results: Proximity to Railway, Highway, Coastline
Proximity to Railway, Highway, Coastline:

Screenshot:
Illustrates a selected launch site with circles denoting distances to nearby infrastructure such as railways, highways, and coastlines.
Confirms that typical launch sites are located near coastlines for safety and logistical reasons.
(Optionally, insert a screenshot showing the map with distance circles.)

Slide 33: Plotly Dash Results: Launch Success Count for All Sites
Launch Success Count for All Sites:

Pie Chart Explanation:
Displays the distribution of total successful launches across all launch sites.
Highlights the site with the highest number of successful launches.
(Optionally, insert a screenshot of the Plotly Dash pie chart with insights.)

Slide 34: Plotly Dash Results: Launch Site with Highest Launch Success Ratio
Launch Site with Highest Launch Success Ratio:

Pie Chart Explanation:
Focuses on the launch site with the highest success ratio (successes divided by total launches).
Shows a detailed breakdown of successes vs. failures for that specific site.
(Optionally, insert a screenshot of the site-specific pie chart.)

Slide 35: Plotly Dash Results: Payload vs. Launch Outcome Scatter Plot
Payload vs. Launch Outcome Scatter Plot:

Scatter Plot Explanation:
X-axis: Payload Mass (with an interactive range slider).
Y-axis: Launch Outcome (Success/Failure).
Enables interactive exploration of how different payload ranges affect the launch outcome.
Provides insights on whether heavier payloads correlate with higher failure rates.
(Optionally, insert a screenshot of the interactive scatter plot.)

Slide 36: Predictive Analysis Results: Classification Accuracy
Classification Accuracy:

Bar Chart:
Compares accuracy metrics of various classification models (Logistic Regression, SVM, Decision Tree, etc.).
Highlights the best performing model (e.g., SVM at 88% accuracy).
Insights:
The highest accuracy model is the most reliable for predicting launch success.
Some models might require further tuning or additional data.
(Optionally, insert a screenshot of the accuracy comparison bar chart.)

Slide 37: Predictive Analysis Results: Confusion Matrix
Confusion Matrix:

Explanation:
Displays the true positives, false positives, false negatives, and true negatives for the best model.
Offers insight into which type of prediction errors are most common.
(Optionally, insert a screenshot of the confusion matrix with brief observations.)

Slide 38: Conclusion
Conclusion:

Key Points:
Launch Success Influencers:
Launch site location, payload mass, and orbit type significantly influence success.
Historical Trends:
Overall launch success rates have improved over time.
Predictive Model:
Classification models demonstrate high accuracy and are useful for forecasting launch success.
Future Directions:
Integrate additional features (e.g., weather data, rocket reuse information) to enhance predictive accuracy.
Slide 39: Appendix
Appendix:

Supplementary Materials:
Python code snippets.
Detailed SQL queries.
Notebook outputs and additional charts.
Further data references and model tuning details are available in the GitHub repository.
Thank you for reviewing this project.

Notebook Integration Explanation
I created a JSON file in Visual Studio Code and saved it as a .ipynb file so that it can be executed via the command line as a Jupyter Notebook. This notebook includes all projects from the IBM Data Scientist Professional Certificate curriculum and is structured into sections that mirror the slides presented. Each section explains a part of the project step by step, corresponding to the PowerPoint slides shown to the commission and students.

About the Author
Raffaele Schiavone
Data Scientist & Data Analyst, Data Engineer | Business Intelligence & Automation Expert | Python & SQL Developer | Problem-Solver

Email: RAFFAELE.AMMINISTRAZIONE.ONLINE@gmail.com
LinkedIn: https://www.linkedin.com/in/raffaele-schiavone-529090289/
This README provides a comprehensive overview of the project, detailing methodologies, analyses, and results. For more detailed code and documentation, please refer to the respective GitHub repository links provided in each section.

Copia

