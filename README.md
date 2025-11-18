# ScrapeSmart: Amazon Edition

ScrapeSmart: Amazon Edition is a complete web scraping and machine learning pipeline designed to extract skincare product data from Amazon India and classify products as Popular or Less Popular using Logistic Regression.

## Objectives
- Automate data extraction from Amazon using Selenium WebDriver.
- Collect structured fields including product name, price, discount, and monthly purchases.
- Clean, preprocess, and transform scraped data for ML usage.
- Build a Logistic Regression model for popularity classification.
- Identify high-impact keywords influencing product popularity.
- Provide a reusable end-to-end framework combining scraping, feature engineering, and ML modeling.
- Include basic dataset visualizations for analytical insights.

## Tools and Technologies
- Language: Python
- Automation: Selenium WebDriver
- Browser: Google Chrome
- Data Storage: CSV
- Libraries: selenium, csv, time, pandas, numpy, scikit-learn, scipy, re, matplotlib
- Model: Logistic Regression
- Environment: Jupyter Notebook

## Dataset Overview
The dataset `amazon_face_cream.csv` consists of:
- Product Name
- Selling Price (numeric)
- Discount (numeric percentage)
- Monthly Purchases (converted into integers, e.g., 1K → 1000)
- Page Number

This dataset is generated entirely from the scraper and then used for ML classification.

## Web Scraping Module (amazon_face_cream.ipynb)
The scraping script performs:
1. Launching Chrome WebDriver with a custom user-agent.
2. Opening Amazon search results for “face cream”.
3. Extracting:
   - Product name
   - Selling price
   - Discount
   - Monthly purchases
4. Navigating through multiple pages automatically.
5. Collecting all products into a list.
6. Saving all scraped records into `amazon_face_cream.csv`.

Core libraries: selenium, csv, time.

## Machine Learning Module
A Logistic Regression classification model is built on top of the scraped dataset.

### Key Steps:
1. Data Cleaning:
   - Removing special characters from price and discount.
   - Converting purchase patterns (e.g., “1K+ bought in past month”) into numbers.

2. Feature Extraction:
   - TF-IDF vectorization applied on Product Name.
   - Numeric features (Price, Discount) combined using `scipy.sparse.hstack`.

3. Model Definition:
   - Logistic Regression with max_iter=1000.

4. Training and Testing:
   - 80/20 train-test split.
   - Achieved ~72% accuracy.

5. Keyword Analysis:
   - Identification of top text features contributing to high popularity.
   - Example high-impact terms: hydration, gel, moisturizer, vegan, oil.

## Visualizations
Basic visualizations generated using matplotlib include:
- Distribution of Selling Price
- Frequency of Discounts
- Scatter plot of Price vs Monthly Purchases

These help understand product patterns before classification.

## Summary
ScrapeSmart: Amazon Edition demonstrates a complete pipeline:
- Automated scraping
- Data cleaning and preprocessing
- Text vectorization
- Combined feature modeling
- Logistic Regression-based popularity classification
- Meaningful keyword insights
- Dataset visualizations

This framework can be extended to additional product categories, added models, or integrated into larger e-commerce analytics systems.


## Preview
<img width="437" height="247" alt="Screenshot 2025-11-13 214120" src="https://github.com/user-attachments/assets/78766ddc-8fdd-4ffe-a6ff-b310e0043545" />
<img width="1919" height="1078" alt="Screenshot 2025-11-13 214028" src="https://github.com/user-attachments/assets/e030b579-7fe2-4119-99cf-5fd419aeac11" />
<img width="1919" height="1079" alt="Screenshot 2025-11-13 214052" src="https://github.com/user-attachments/assets/5f141588-9d3a-4c13-a93d-a806c6679977" />
<img width="1919" height="1078" alt="Screenshot 2025-11-13 214442" src="https://github.com/user-attachments/assets/a51c9641-3eb2-4c4b-865e-3eef832270f5" />
<img width="398" height="393" alt="image" src="https://github.com/user-attachments/assets/e5862308-b1b6-4efb-b734-e21c1309ea49" />
<img width="1082" height="612" alt="image" src="https://github.com/user-attachments/assets/f159cca3-62e8-479b-b3ed-124d98185aa6" />
