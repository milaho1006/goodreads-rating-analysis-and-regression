# Goodreads Rating Regression

This Macquarie University coursework project explores whether page count, number of ratings, and number of written reviews can help predict a book's average Goodreads rating.

## What I did

- Cleaned the dataset and explored the distribution of book ratings.
- Examined the relationship between rating counts and average ratings.
- Compared multiple linear regression and degree-two polynomial regression using the same train/test split.

## Key finding

The three predictors explained little of the variation in average ratings on the test set. Adding polynomial terms did not improve performance. The models also rely on reader activity, so this approach requires ratings and reviews to have already been collected.

## Notebook and data

- [View the regression notebook](book-data-regression.ipynb)
- [Goodreads Books dataset on Kaggle](https://www.kaggle.com/datasets/jealousleopard/goodreadsbooks/data)

To reproduce the analysis, download `books.csv`, place it in the notebook's working directory, and run the cells in order.
