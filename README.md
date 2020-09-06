# Data-Wrangling
## Objectives
After completing this lab you will be able to:

1. Handle missing values
2. Correct data format
3. Standardize and Normalize Data

## What is the purpose of Data Wrangling?
Data Wrangling is the process of converting data from the initial format to a format that may be better for analysis.

# How to work with missing data?

## Steps for working with missing data:

1. identify missing data
2. ideal with missing data
3. correct data format

# Identify and handle missing values

Identify missing values

Convert "?" to NaN

If missing data comes with the question mark "?". We replace "?" with NaN (Not a Number), which is Python's default missing value marker, for reasons of computational speed and convenience. Here we use the function:
.replace(A, B, inplace = True) 
to replace A by B

# Evaluating for Missing Data
The missing values are converted to Python's default. We use Python's built-in functions to identify these missing values. There are two methods to detect missing data:

1. .isnull()
2. .notnull()

## Count missing values in each column
Using a for loop in Python, we can quickly figure out the number of missing values in each column. As mentioned above, "True" represents a missing value, "False" means the value is present in the dataset. In the body of the for loop the method ".value_counts()" counts the number of "True" values.

# Deal with missing data
## How to deal with missing data?
### drop data

a. drop the whole row
b. drop the whole column

### replace data

a. replace it by mean
b. replace it by frequency
c. replace it based on other functions

*Whole columns should be dropped only if most entries in the column are empty. In our dataset, none of the columns are empty enough to drop entirely. We have some freedom in choosing which method to replace data; however, some methods may seem more reasonable than others. We will apply each method to many different columns:*

### Replace by mean:

"normalized-losses": 41 missing data, replace them with mean

"stroke": 4 missing data, replace them with mean

"bore": 4 missing data, replace them with mean

"horsepower": 2 missing data, replace them with mean

"peak-rpm": 2 missing data, replace them with mean

### Replace by frequency:

"num-of-doors": 2 missing data, replace them with "four".

Reason: 84% sedans is four doors. Since four doors is most frequent, it is most likely to occur

### Drop the whole row:

"price": 4 missing data, simply delete the whole row

Reason: price is what we want to predict. Any data entry without price data cannot be used for prediction; therefore any row now without price data is not useful to us

## Correct data format

###The last step in data cleaning is checking and making sure that all data is in the correct format (int, float, text or other).

In Pandas, we use

1. .dtype() to check the data type

2. .astype() to change the data type


## Data Normalization
### Why normalization?

Normalization is the process of transforming values of several variables into a similar range. Typical normalizations include scaling the variable so the variable average is 0, scaling the variable so the variance is 1, or scaling variable so the variable values range from 0 to 1

## Indicator variable (or dummy variable)
### What is an indicator variable?

An indicator variable (or dummy variable) is a numerical variable used to label categories. They are called 'dummies' because the numbers themselves don't have inherent meaning.

### Why we use indicator variables?

So we can use categorical variables for regression analysis in the later modules.

                                  *# Thank You*
