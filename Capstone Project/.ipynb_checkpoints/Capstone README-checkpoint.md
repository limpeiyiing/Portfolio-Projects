# DSI30 Capstone Project : Predicting Sales - Time Series Analysis and Forecasting 

*by Lim Pei Yiing*

## Background

### The Company

[1C Company](https://1c.ru/eng/title.htm) is an independent software developer, distributor and publisher with headquarters in Moscow, Russia. It **develops, manufactures, licenses, supports and sells computer software, related services and video games.** It reported 37 billion rubles ($650 million) in annual revenue in 2016. 

### Business Case for this Study

A **good sales forecast** is an important core for every business. It helps in overall business planning, budgeting, and risk management. 

Fundamentally, a sales forecast addresses the following:
1) **WHAT** products are going to be sold
2) **HOW MUCH** of the product is expected to sell
3) **WHERE** will the product be sold
4) **WHEN** will the product be sold

An inaccurate sales forecast can be a risk to the business in several ways. Mainly:
1) **Underforecasting**:   If insufficient product arrives too late or at the wrong location to be sold, the business loses revenue opportunities and customer confidence. 
2) **Overforecasting**:   If too much product is supplied based on an over-estimated forecast, resources are wasted to manage the storing and handling of slow-moving product. Such resources could have better been directed into other investments that are more profitable for the business. 

The forecasting process can get increasingly complex and time-consuming to perform manually when large number of location-category-item combinations are involved, or historical data is missing or limited. 


## Problem Statement:

**The client/audience**:   
The management (decision-makers) and Demand Planning team (executives) of 1C Company. 

**Task**: 
1) Prepare an preliminary study on the sales trends between Jan'13 to Oct'15. 
2) Build a model that can predict total sales for every product and store in the next month. The best model that can best predict sales units will be determined by Root Mean Squared Error (RMSE).

**Objectives of the study**:

Build and optimize a **regression model** to predict sales volume by item and store in the next month.

This model aims to **automate** the bulk of the current Demand Planning process with **higher accuracy**, so that the team may redivert their resources to work on other tasks that can add-value to the Sales and Operations Planning process.


## The Dataset

An overview of the different data files used in this study can be found here on [Kaggle](https://www.kaggle.com/competitions/competitive-data-science-predict-future-sales/data).

## Findings

1. All 3 models built (**LSTM, CNN, XGBoost Regressor**) performed better against the baseline model RMSE score of 1.21756. The best model selected was the **XGBoost Regressor** based on a score of **1.03877**, which means it performed reasonably well at addressing the following complexities:
    - **Seasonality** and **trends** at the granular level
    - The **scale and range** of product categories and shops in the company
    - **Limited historical data** for most product-shop combinations
   
   
2. The XGBoost model is also **relatively quick**, and can complete training and predicting in under 10 mins.  

## Future Works

1) **Fine-tune features:**
   - At the moment, clusters were created based on total units sold. We can consider using other characteristics to cluster items or stores. For example, by actual geographical location of stores, or by average rate of sales per item. 
   
   
2) **Optimize model parameters or transformation thresholds**
   - For example, we can optimize the threshold used to round predictions to full integers. 
   
   
3) **Explore other models and approaches for better results.** 
   - For example, instead of using a purely bottoms-up forecasting approach, we can experiment with a combination of top down and bottoms up approach with a Hierarchical Time Series model.