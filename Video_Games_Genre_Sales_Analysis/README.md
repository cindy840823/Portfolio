# Video Games Genre Sales Analysis

## Overview
This project analyzes the sales performance of video games based on various attributes such as genre, platform, publisher, and region. The primary goal is to determine what factors contribute to a game achieving sales exceeding 1 million units globally. Additionally, the project evaluates different machine learning models to predict game success and provides actionable insights for game developers and publishers.

## Objectives
- Identify sales trends across regions, platforms, and genres.
- Determine the most successful game publishers and developers.
- Analyze the correlation between critical scores and sales performance.
- Predict game success using machine learning models.

## Dataset
- **Source**: [Kaggle Dataset - Video Games Sales as at 22 Dec 2016](https://www.kaggle.com/datasets/xtyscut/video-games-sales-as-at-22-dec-2016csv?resource)
- **Size**: 16,717 instances, 16 attributes.
- **Attributes**: Includes game name, platform, publisher, year of release, genre, sales by region (NA, EU, JP), global sales, critic score, user score, developer, and rating.
- **Preprocessing**:
  - Addressed missing values in key attributes (e.g., year of release, critic score, user score).
  - Handled categorical variables and standardized numerical values for analysis.

## Exploratory Data Analysis (EDA)
- **Sales Trends**:
  - Global sales peaked between 2008 and 2010.
  - Action games dominate in terms of game count and sales.
- **Top Platforms**:
  - PS2 leads with over 2,000 games, followed by DS, PS3, Wii, and Xbox 360.
- **Top Publishers and Developers**:
  - Electronic Arts (EA) published the most games (over 1,300).
  - Ubisoft is the leading developer with around 200 games.
- **Correlation Analysis**:
  - A strong positive correlation exists between global sales and critic scores.

## Machine Learning Models
**Target:** `Hit` = 1 if a game sold 1 million+ units globally. In the test set only 402 of 2,395 games (about 17%) are hits, so a model that always predicts "not a hit" would already score about 83% accuracy. Accuracy alone is misleading here; precision and recall on the **hit** class are what matter.

Results on the 30% hold-out test set (after grid-search tuning):

| Model | Accuracy | Hit precision | Hit recall |
|---|---|---|---|
| Naive baseline (always "not a hit") | ~83% | – | 0% |
| Decision Tree (tuned) | 86% | 66% | 33% |
| Logistic Regression (tuned for recall) | 86% | 63% | 40% |

10-fold cross-validated accuracy for other models: Logistic Regression 0.81, Decision Tree 0.78, Neural Network (MLP) 0.82, Random Forest 0.81, Naive Bayes 0.29.

**Takeaway:** the models beat the naive baseline only modestly and catch fewer than half of the real hits. Critic score, platform, genre, and publisher carry some signal, but predicting a hit before launch needs richer features (see Future Work).

*Note: the PDF report was written from an earlier run of the analysis, so its figures differ slightly from the notebook. The numbers above match the current notebook outputs.*

## Insights
- **Most Successful Genres**:
  - Action games dominate sales but face market saturation.
  - Other genres offer opportunities for growth due to less competition.
- **Key Factors for Success**:
  - High critical scores significantly boost sales.
  - Strategic selection of platforms and publishers is essential.

## Recommendations
- **For Game Developers**:
  - Focus on underrepresented genres to capture untapped markets.
  - Improve critical scores through better gameplay and design to enhance sales.
- **For Publishers**:
  - Leverage historical data to predict and prioritize successful game launches.
  - Expand into emerging markets to boost regional sales.

## Files
- `Video_Games_Genre_Sales_Analysis.ipynb`: data cleaning, exploratory analysis, and modeling.
- [Analyzing Game Genres and Their Success (PDF Report)](./Analyzing%20Game%20Genres%20and%20Their%20Success.pdf): written report on the analysis and findings.
- Dataset: download `Video_Games_Sales_as_at_22_Dec_2016.csv` from Kaggle (link under Dataset) and place it in this folder before running the notebook.

## Future Work
- Expand the dataset to include recent sales data for improved model accuracy.
- Incorporate additional features such as marketing spend and player demographics.
- Explore advanced machine learning models for better predictions.

## References
- Kaggle Dataset: [Video Games Sales (22 Dec 2016)](https://www.kaggle.com/datasets/xtyscut/video-games-sales-as-at-22-dec-2016csv?resource)
- "Top 10 Biggest Video Game Companies in the World" - All Top Everything
- "12 Most Popular Video Games in 2021" - Fossbytes
- Various articles from Statista and industry reports.
