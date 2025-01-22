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
- **Logistic Regression**:
  - Accuracy: 84.8%
  - Precision: 89%
  - Recall: 95%
  - Area Under Curve (AUC): 0.848
- **Decision Tree**:
  - Accuracy: 71.6%
  - Precision: 88%
  - Recall: 97%
  - AUC: 0.716
- **Neural Networks**:
  - Accuracy: 87.4%
  - Best overall performance for prediction tasks.

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
- `Video_Games_Sales_Analysis.ipynb`: Jupyter Notebook containing the code for analysis and modeling.
- `data/`: Contains the dataset used for this project.
- [Analyzing Game Genres and Their Success (PDF Report)](https://github.com/cindy840823/Portfolio/blob/main/Video%20Games%20Genre%20Sales%20Analysis/Analyzing%20Game%20Genres%20and%20Their%20Success.pdf): A detailed report providing insights and analysis behind this project.

## Future Work
- Expand the dataset to include recent sales data for improved model accuracy.
- Incorporate additional features such as marketing spend and player demographics.
- Explore advanced machine learning models for better predictions.

## References
- Kaggle Dataset: [Video Games Sales (22 Dec 2016)](https://www.kaggle.com/datasets/xtyscut/video-games-sales-as-at-22-dec-2016csv?resource)
- "Top 10 Biggest Video Game Companies in the World" - All Top Everything
- "12 Most Popular Video Games in 2021" - Fossbytes
- Various articles from Statista and industry reports.
