# Text Mining and Topic Modeling with LSA

## Overview
This project applies **Latent Semantic Analysis (LSA)** and text mining techniques to analyze NFT whitepapers, with a focus on identifying patterns and trends related to the gaming industry. Using a dataset of NFT whitepapers collected from rarity.tools, we performed topic modeling to uncover key themes and assess the relevance of NFTs within the gaming ecosystem.

## Objectives
- Extract meaningful insights from NFT whitepapers using text mining techniques.
- Apply **Latent Semantic Analysis (LSA)** for topic modeling.
- Investigate the popularity and significance of NFTs in the gaming universe.

## Dataset
- **File**: `NFT_Whitepapers - Sheet1.csv`
- **Source**: Whitepapers collected from rarity.tools.
- **Description**:
  - Contains details about various NFTs, including text extracted from their whitepapers.
  - Focuses on NFTs related to gaming, community building, and blockchain applications.

## Tools and Techniques
- **Programming Language**: Python
- **Libraries**:
  - pandas, numpy, matplotlib, seaborn (data preprocessing and visualization)
  - sklearn (Latent Semantic Analysis and text vectorization)
  - wordcloud (visualizing topic distributions)
- **Key Techniques**:
  - Text preprocessing: Tokenization, stopword removal, stemming.
  - Topic modeling: Latent Semantic Analysis (LSA) to identify key themes.

## Methodology
1. **Data Collection**:
   - Extracted text data from NFT whitepapers and stored in a CSV format.
2. **Text Preprocessing**:
   - Removed stopwords, punctuation, and redundant characters.
   - Tokenized text and converted it to lowercase.
3. **Topic Modeling**:
   - Applied **LSA** to identify major topics and trends.
   - Visualized key topics using word clouds and bar charts.

## Results
- Key topics identified included **community**, **players**, **blockchain**, **land**, and **voxie**.
- NFTs associated with gaming showed higher popularity and price ceilings, particularly those offering in-game utilities.

## Files
- `Text_Mining_and_Topic_Modeling_with_LSA.ipynb`: Jupyter Notebook containing the full analysis and code.
- `NFT_Whitepapers - Sheet1.csv`: Dataset used for the analysis.
- `Report.pdf`: Detailed report summarizing the research findings and methodology.

## Visualizations
Visualizations include:
- Word clouds of key topics.
- Bar charts showing the distribution of themes across NFTs.

## Insights
- NFTs integrated with gaming ecosystems are more likely to gain popularity and higher valuations.
- Topic modeling highlights the importance of community engagement and unique game assets in NFT success.

## Future Work
- Expand the dataset to include more whitepapers across industries.
- Experiment with advanced topic modeling techniques like **Latent Dirichlet Allocation (LDA)**.
- Analyze additional factors such as NFT prices and transaction volumes.

## References
- Data collected from [rarity.tools](https://rarity.tools).
- "Immaterial Gains: The NFT Boom Comes for Fashion" - Whitney Bauck.
- Various articles from **Vogue Business** and **Nintendo Life**.
