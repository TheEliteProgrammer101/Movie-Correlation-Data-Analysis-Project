Movie Industry Correlation Analysis *
Does a higher budget guarantee a box office hit? This project analyzes a dataset of movies to find out which variables (like budget, votes, or production company) have the strongest correlation with Gross Earnings.

* The Objective
The goal is to test the hypothesis that Budget and Company have the highest correlation with revenue. Using Python, we clean the data and use statistical methods (Pearson) and heatmaps to find the truth.

* Tech Stack
Python (Data Analysis)
Pandas & NumPy (Data Manipulation)
Seaborn & Matplotlib (Statistical Visualization)

* Data Cleaning & Transformation
Before analyzing, the data was prepped to ensure accuracy:
Handling Missing Values: Filled numeric gaps with the mean and categorical gaps with "Unknown".
Data Typing: Converted budget and gross to integers for cleaner calculations.
Feature Engineering: Created a Year Corrected column by extracting the year from the release date string.
Data Numerization: Transformed categorical columns (like Company, Director, Genre) into Category Codes so they could be included in the correlation matrix.

* Visualizing the Insights
1. Budget vs. Gross Earnings
Tool: sns.regplot
Insight: A clear upward trend. As the budget increases, the gross revenue tends to follow, though there are significant outliers.
2. The Correlation Matrix
Tool: sns.heatmap
Method: Pearson Correlation.
Discovery: Visualizing the relationship between all numeric features (Votes, Budget, Runtime, etc.) to see what moves together.
3. The "Unstacked" View
Tool: df.corr().unstack()
Insight: By sorting correlation pairs, we filtered for values > 0.5 to pinpoint the strongest relationships.

* Key Findings
High Correlation: Votes and Budget have the highest correlation to Gross Earnings. If people are talking about/voting for a movie and the budget is high, the revenue is usually high.
Low Correlation: Surprisingly, the Company (production studio) has a very low correlation with a movie's financial success. A big name doesn't always mean big money.
