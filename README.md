# Clean Data, Clear Insights

Imagine you're cooking a meal, but you're using spoiled ingredients. No matter how well you cook it, the meal will be spoiled and inedible. Similarly, if you're trying to use data to make important decisions, but the data is incorrect or incomplete, the decisions you make will also be incorrect.

One of the tools to cleanse the data is using the NumPy library in Python. Please pay close attention to the scenario below to gain insight into what we should do with raw data

## TLDR 🎉

We're data analysts at EuroBank.

Assigned the task of **pre-processing data** to be used by the Data Science team to create a Credit Risk model that measures the probability of default for every personal account

⚠️ **Documentation only available in Bahasa**

## Project Goal 🎯

- Obtain a clean and preprocessed dataset
- Note down all the changes we're making to the original dataset in the documentation file

This information will be invaluable to the data scientist who will work with this data after us.

## What's Inside? 📦

- **Loan-Data.csv** --> files to be cleaned
- **Loan-Data-Preprocessed.csv** --> cleaned files
- **Loan Dataset Dictionary.xlsx** --> Business team documentation that describes every data columns
- **NumPy-Practical.ipynb** --> pre-processing documentation with python
- **EUR-USD.csv** --> exchange rate Euros to USD

## Scenario 📑

The data provided by the business team is very messy, so we must always communicate with them when cleaning the data. Finally, we asked for data samples to plan how to clean all the data later and make documentation.

Data was obtained from affiliated banks in the United States. Hence all values in Loan-Data.csv are in Dollars.

The DataScience team asks that every absolute number must be quantified.
We need to change any text columns into numbers based on the information they contain
They give a clue that the Issue Date is sufficiently categorized by month. Meanwhile, for other categorical columns, they only care if they provide positive or negative connotations.

DS team also warns to be highly risk-averse and distrustful of unavailable data.
Missing information suggests foul play because loan applications are self-reported. There is an incentive to withhold information which can lower their chances of getting a loan. EuroBank prefers to give out loans to applicants who can repay them.

We'll assume the worst if the Data is NaN (unavailable).
However, what is worst varies from one column to the next. So the business team has provided casting directions for each variable in the dataset.

## To Do List 📝

- [x] Since we work for the European Union, **all data must be converted to Euros**
- [x] **Turn every categorical data into dummy variables** that hold either 0 or 1 (except Issue Date)
- [x] As we go through the dataset, we'll know whether we want to use the min, max, or other values when **taking care of missing data**
