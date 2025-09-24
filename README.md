# Amazon Reviews Sentiment Analysis

## Overview
This project demonstrates an end-to-end pipeline for analyzing customer sentiment in Amazon reviews. It combines natural language processing (NLP), machine learning (ML), and business intelligence (BI) to turn raw unstructured text into actionable insights. The results are visualized in a branded Power BI dashboard.

## Objective
The goal of this project is to analyze Amazon Fine Food Reviews and:
- Clean and preprocess raw review data.
- Apply machine learning models to classify sentiment (Positive, Neutral, Negative).
- Engineer additional features such as review word count and top frequent words.
- Build an interactive Power BI dashboard to present key findings for stakeholders.

## Data
- **Source:** Amazon Fine Food Reviews dataset (`Reviews.csv`).
- **Cleaned Data:** `amazon_reviews_cleaned_with_labels.csv` with mapped sentiments and word counts.
- **ML Output for BI:** `amazon_reviews_sentiment_for_powerbi.csv` including predicted sentiment and probabilities.
- **Top Words Data:** `top_words_counts.csv` listing frequent terms by sentiment.

## Methodology
1. **Data Cleaning (Jupyter Notebook)**
   - Removed missing/empty reviews.
   - Converted Unix timestamps to proper dates.
   - Mapped star ratings (1–2 = Negative, 3 = Neutral, 4–5 = Positive).
   - Added review word count.

2. **Machine Learning**
   - Vectorized text using TF-IDF with stopword removal.
   - Trained Logistic Regression and Naive Bayes models.
   - Selected Logistic Regression for best accuracy (~85%).
   - Generated predictions and sentiment probabilities.

3. **Feature Engineering**
   - Created word count bins to analyze sentiment by review length.
   - Extracted top words by frequency per sentiment using Python.

4. **Dashboard (Power BI)**
   - Developed an interactive dashboard (`amazon_reviews_sentiment_analysis.pbix`).
   - Applied Amazon brand colors (Orange, Black, Blue).
   - Visuals include KPIs, sentiment distribution, sentiment by word count, sentiment trends, and example reviews.

## Dashboard Highlights
- **KPIs:** Total Reviews, % Positive, % Negative, Model Accuracy, Review Date Range.
- **Distribution:** Donut chart of Positive, Negative, and Neutral reviews.
- **Drivers of Sentiment:** Stacked columns by word count bins.
- **Trend:** Line chart of sentiment by year.
- **Context:** Table of recent reviews with actual sentiment.

![Dashboard Screenshot](dashboard/Amazon_Reveiws_Dashboard.png)

## Key Insights
- The dataset is dominated by positive reviews (~78%).
- Longer reviews tend to be more negative, reflecting detailed complaints.
- Review activity increased significantly after 2008.
- Common positive terms include "great", "love", "best"; common negative terms include "bad", "disappointed", "waste".

## Files
- `data/amazon_reviews_cleaned_with_labels.csv`: Cleaned dataset with sentiment labels.
- `data/amazon_reviews_sentiment_for_powerbi.csv`: ML outputs for Power BI.
- `data/top_words_counts.csv`: Word frequencies per sentiment.
- `notebooks/Amazon_Reviews_Sentiment_ML.ipynb`: Jupyter notebook with full pipeline.
- `dashboard/amazon_reviews_sentiment_analysis.pbix`: Power BI dashboard file.
- `dashboard/Amazon_Reveiws_Dashboard.png`: Dashboard screenshot.

## How to Use
1. Open the Jupyter Notebook to review data cleaning, ML, and feature engineering steps.
2. Explore `amazon_reviews_sentiment_for_powerbi.csv` and `top_words_counts.csv` for processed data.
3. Open the Power BI file (`.pbix`) to interact with the dashboard.
4. Review the README and screenshot for a quick overview of the project.

## Requirements
- Python 3.8+
- pandas, numpy, scikit-learn, matplotlib
- Power BI Desktop (for `.pbix` file)

## Conclusion
This project illustrates how raw customer reviews can be transformed into business insights through a combination of NLP, ML, and BI. The final dashboard enables stakeholders to quickly assess customer sentiment, spot trends, and identify factors driving positive and negative feedback.

