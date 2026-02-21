This project provides a **comprehensive analysis of project management data**, including data cleaning, exploratory data analysis (EDA), natural language processing (NLP), and advanced analytics such as clustering and correlation analysis. It aims to deliver actionable insights into project performance, ROI, complexity, risk, and temporal trends.

## How It Works

### 1. Data Upload
- Project data is loaded from a CSV file.
- Libraries used: `pandas` and `numpy` for data manipulation.

### 2. Data Cleaning
Key steps include:
1. **Inspect data types and missing values:** Identify numeric, text, and categorical columns and detect missing data.
2. **Convert financial columns to numeric:** Remove commas and convert to `float` for cost and benefit columns.
3. **Convert Completion% to numeric:** Ensure values are within 0–100%.
4. **Convert dates to datetime:** Detect and handle invalid dates.
5. **Standardize categorical columns:** Trim whitespace and ensure consistent capitalization for columns like Project Type, Manager, Region, Department, Complexity, Status, and Phase.
6. **Handle missing values:** Fill text with "Unknown", categorical columns with mode, numeric columns with median, and drop rows with missing Start/End dates.
7. **Remove duplicates:** Based on Project Name and Year.
8. **Logical consistency checks:** Ensure Project Benefit ≥ Project Cost, End Date ≥ Start Date, valid Month and Year ranges.
9. **Clean text for NLP/analysis:** Remove punctuation, normalize spaces, lowercase text.
10. **Encode categorical columns:** Apply Label Encoding for analysis.
11. **Create derived columns:** Net Profit, Quarter, and Duration in months.
12. **Outlier detection (optional):** Use IQR to flag extreme values.
13. **Save cleaned dataset** for analysis.

### 3. Exploratory Data Analysis (EDA)
- **Numerical analysis:** Distribution, skewness, ROI, Net Profit, Duration.
- **Temporal analysis:** Project counts and trends by Year and Month.
- **Categorical analysis:** Count and percentage distributions by Project Type, Region, Department, Complexity, Status, Phase, and Project Manager.
- **Comparative analysis:** ROI and Net Profit across managers, departments, regions, and project types.
- **Visualizations:** Histograms, line plots, boxplots, scatter plots for better insights.

### 4. NLP Analysis
- **Text preprocessing:** Clean and tokenize Project Descriptions, remove stopwords.
- **WordCloud generation:** Visualize the most frequent words in project descriptions.
- **Topic modeling:** Use LDA to extract main topics from project descriptions.
- **Sentiment analysis:** Classify project descriptions as Positive, Neutral, or Negative and correlate sentiment with ROI and project status.
- **Comparative text analysis:** Examine common words for Completed vs. Cancelled projects.

### 5. Advanced Analytics
- **Clustering (KMeans):** Group projects based on Cost, Benefit, Duration, and Complexity.
- **Determine optimal clusters:** Using the Elbow Method.
- **Correlation analysis:** Examine numeric correlations between Cost, Benefit, Duration, and Completion%.
- **Visualizations:** Scatter plots for clusters, heatmaps for correlations.

---

This project provides a **full framework for analyzing project management datasets**, helping decision-makers optimize resource allocation, assess risks, and maximize ROI.
