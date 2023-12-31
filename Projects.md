---
layout: page
title: "Projects"
---

## Capstone: Data Science Consulting

In the Capstone course, I had the opportunity to experience the career of a consultant. I completed 5 projects in the Capstone, and I had the experience of juggling between multiple projects at the same time, which was a typical pattern for a consultant.

[**Project 1: Medication Adherence Analysis for a Health Insurance Company**](https://github.com/alphaB8T/Medication-Adherence-Analysis-for-a-Health-Insurance-Company)

In this project, I worked with a health insurance company to analyze how well patients with heart disease take their medications (ACE Inhibitors, Beta Blockers, Statins). I had the data that included a number of important clinical factors about their baseline conditions. Then, starting from the time of their initial diagnoses of heart disease, the patients were tracked based upon which medications were filled at the pharmacy. The medication records are presented in the form of panel data.

Given the panel form of the data, I spent much efforts manipulating data to answer questions from the client. I analyzed questions related to adherence patterns (follow-up length, one-year adherence rate, percentage of patients filled prescription in the first two weeks, etc.) and differences among groups of patients with different adherence patterns. I also analyzed the impact of different factors on the one-year adherence to each medication and the impact of filling a prescription in the first two weeks impact adherence using linear regression, and I analyzed the impact of different factos on the likelihood of initiating a medication within 14 days using logistic regression.

[**Project 2: Citi Bike in Jersey City**](https://github.com/alphaB8T/Citi-Bike-in-Jersey-City/tree/main)





## Developing predictive models to forecast the closing price movements of stocks

[Project Link]()

In this project from Optiver's Kaggle Competition, our group used LightGBM and XGBoost model to forecast the closing price movements of Nasdaq listed stocks using data from the order book and the closing auction of the stock.

The data we had was like panel data, which had records of each stock across many timestamps, and it had many features like imbalance size, bid and ask price, near and far price, weighted average price, and so on.

To increase the accuracy of our models, we implemented feature engineering and added more features:
We introduced four size features—liquidity imbalance, size imbalance, volume, and imbalance ratio to capture the order book's size dynamics.
To better understand market dynamics, we added price features like Imbalance Momentum, Price Spread, Spread Intensity, and Price Pressure.
Time features like lagged features and moving averages were also added.

We also tried different methods for managing missing values.

We initiated our analysis by constructing baseline models for both LGBM and XGBoost without incorporating any new features. The purpose of this step was to establish a reference point for assessing the effectiveness of different preprocessing methods and to gauge the performance improvement by new features. Both models are evaluated based on mean absolute error (MAE). Upon determining the most effective preprocessing method and establishing the baseline models, we developed a function to incorporate new features into the model and quantify their impact.

Overall, our model’s best MAE scores were 5.4371 for LightGBM and 5.5482 for XGBoost, translating into a 15% and 13% improvement, respectively, from Optiver’s baseline model (MAE of 6.4078).





## Building a database for a grocery chain company

[Project Link]()

In this project, I built a PostgreSQL database for a fictional grocery chain company. Information on staffing, inventory, vendors, deliveries, sales, accounting, and more has been stored in spreadsheets and paper binders. Now with the expansions, management wants a better system to handle the data and have real-time dashboards on important aspects of the business.

I started by designing and drawing the E-R diagram and the Normalization plan. In the end, the database had 16 tables, including entity sets and relationship sets. I used Python to simulated data in a way that was similar to the original raw data as recorded. I could then implemented the ETL process in Python to transform the data based on the E-R diagram and the Normalization plan, so  the data could be loaded into tables in the database through the connection to the PostgreSQL database in Python.

I did some cool "trigger" stuff in the database. The Inventory table would update automatically when there were new sales (inventory decrease) or new deliveries to the inventory (inventory increase). When the inventory of a product at a store went below a certain threshold, there would also be a popup warning to remind reordering the product.

Finally, I made a dashboard to show some results using Metabase. It was connected to the PostgreSQL database, and I could write queries and get the visualizations I wanted accordingly. I wrote queries and got insights for things like: top 5 products in terms of sales from each store by month, vendors that supply the most popular products in terms of quantity sold in stores, which group of customers generate the most revenue, and so on.





##  Building a data processing system for NYC motor vehicle collisions data

In this project, I developed a PostgreSQL database that could store and interact with NYC motor vehicle collisions data. I imported the most recent 1.5 million rows of real-time data into Python using NYC OpenData API. I then used PySpark to clean and transform the data and load it into the PostgreSQL database.

Using the Streamlit framework, I then built a webpage that had a simple search engine. The user could type a street name in the search box, and the user could get information of collisions on that street. I also made a map that could show locations where latest collisions happened.



