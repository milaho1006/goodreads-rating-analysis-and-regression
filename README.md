# Goodreads Book Rating Analysis and Regression

## Introduction

This project was completed as part of COMP2200 at Macquarie University. I used Python to explore a Goodreads books dataset and investigate whether three features could help predict a book’s average reader rating: page count, number of ratings, and number of written reviews.

The notebook covers data preparation, exploratory analysis, and a comparison of multiple linear regression and polynomial regression.

## Dataset

The `books.csv` dataset contains book metadata and reader activity from Goodreads. It includes fields such as title, author, language code, page count, average rating, ratings count, and text review count.

| Role in the model | Dataset field |
| --- | --- |
| Target | `average_rating` |
| Predictor | `num_pages` |
| Predictor | `ratings_count` |
| Predictor | `text_reviews_count` |

[Goodreads Books dataset on Kaggle](https://www.kaggle.com/datasets/jealousleopard/goodreadsbooks/data)

## Methods

### 1. Data cleaning and preparation

- Inspected the dataset for missing values and checked column names and data types.
- Removed identifier fields such as ISBNs from the analysis.
- Selected the three numerical predictors and used average rating as the target variable.

### 2. Exploratory data analysis

- Plotted the distribution of average ratings to see where most books in the dataset were rated.
- Summarised the most common language codes to understand the composition of the dataset.
- Examined the relationship between the number of ratings a book received and its average rating.

### 3. Regression modelling and evaluation

- **Multiple linear regression** used the three predictors together to estimate average book ratings.
- **Degree-two polynomial regression** added squared terms and interactions to test whether a more flexible model could capture relationships that the linear model missed.
- **Model evaluation** compared performance on held-out data using R², which measures how much of the variation in average ratings the model explains.

## Key findings

Most books in the dataset had average ratings clustered near 4. The linear model explained only a small share of the variation in ratings on the test set, and adding polynomial terms did not improve performance. In this dataset, page count and reader activity counts had limited value for predicting a book's average rating.

Two predictors depend on readers having already rated or reviewed the book. This limits the model’s use for newly published books with little or no reader activity.

## Tools used

- **Python and pandas** for data preparation and exploration
- **Matplotlib** for visualisations
- **scikit-learn** for regression modelling and evaluation
- **Google Colab** for running the notebook

## How to run the notebook

1. Open the [book-data-regression.ipynd] in Google Colab or Jupyter.
2. Download `books.csv` and place it in the notebook’s working directory. In Colab, you can upload it through the **Files** sidebar.
3. Run the cells from top to bottom to reproduce the charts and model results.
