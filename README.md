## ScrapeSmart: Amazon Edition
An advanced automated web scraping and machine learning system that collects, processes, and analyzes product data from Amazon India using Python, Selenium, and Logistic Regression.
This project scrapes data such as product names, prices, discounts, and monthly purchases, and then uses that data to build an ML-based popularity classifier, predicting whether a product is Popular or Less Popular based on its features and text description.

## Objectives
- Automate data extraction from Amazon India using Selenium.
- Collect key product details: name, price, discount, and monthly purchase statistics.
- Clean and preprocess scraped data for analysis and model training.
- Implement a Logistic Regression model for product popularity classification.
- Demonstrate integration between Data Engineering and Machine Learning.
- Provide a reusable framework for future e-commerce analytics and AI applications.

## Tools and Technologies
- Language = Python
- Automation = Selenium WebDriver
- Browser =	Google Chrome
- Data Storage = CSV File Handling
- Libraries Used = selenium, csv, time, pandas, numpy, scikit-learn, scipy, re
- Machine Learning Model = Logistic Regression
- Environment / IDE	= Jupyter Notebook

## Dataset Overview
The dataset amazon_face_cream.csv contains:

- Product Name — Text scraped from Amazon search results
- Selling Price — Extracted numeric price
- Discount — Offer percentage (if available)
- Monthly Purchases — e.g., “1K+ bought in past month”
- Page Number — Page index for tracking

## Code Overview
1. Scraping Script (amazon_face_cream.ipynb)
- This Jupyter Notebook automates the following steps:
- Opens Amazon search results for “face cream” using Selenium WebDriver
- Extracts product name, price, discount, and monthly purchases
- Navigates through multiple pages
- Stores all data into a structured CSV file (amazon_face_cream.csv)

Key Libraries:
- selenium, csv, time
- Core Steps:
- Launch Chrome WebDriver with custom user-agent
- Load search results for the specified keyword
- Parse product cards using CSS selectors
- Extract desired data fields
- Move to next pages and repeat the process
- Save all records to a CSV file

2. Machine Learning Module
- A Logistic Regression model is built using the scraped data to classify products into Popular and Less Popular categories.

Key Processes:
- Data Cleaning: Removing special characters and symbols from text
- Feature Extraction: TF-IDF vectorization on product names
- Feature Combination: Stacking text and numeric features using scipy.sparse.hstack
- Model Training: Logistic Regression using scikit-learn
- Evaluation: Accuracy score of approximately 72%
- Analysis: Top predictive keywords include hydration, gel, moisturizer, vegan, and oil

## Preview
<img width="437" height="247" alt="Screenshot 2025-11-13 214120" src="https://github.com/user-attachments/assets/78766ddc-8fdd-4ffe-a6ff-b310e0043545" />
<img width="1919" height="1078" alt="Screenshot 2025-11-13 214028" src="https://github.com/user-attachments/assets/e030b579-7fe2-4119-99cf-5fd419aeac11" />
<img width="1919" height="1078" alt="Screenshot 2025-11-13 214442" src="https://github.com/user-attachments/assets/a51c9641-3eb2-4c4b-865e-3eef832270f5" />
<img width="398" height="393" alt="image" src="https://github.com/user-attachments/assets/e5862308-b1b6-4efb-b734-e21c1309ea49" />
<img width="1082" height="612" alt="image" src="https://github.com/user-attachments/assets/f159cca3-62e8-479b-b3ed-124d98185aa6" />
