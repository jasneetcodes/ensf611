# Data Processing

Goals
- Introduce machine learning worflow
- Where to find sample datasets
- How to process data

## ML Workflow

1. Data Input
2. Data Processing
3. ML Model
4. Validation
5. Visualization of Results



## Common types of datasets

- Feature based data: Multiple attributes or characteristics of the data sample, such as heigh, weight, age, etc. Each column represents a different feature of the data sample.

- Time series data: Consts of values that change over time, such as stock prices, weather data, sensor data or audio data. Each entry represents a different point in time

- Image data: Consists of pixels, shape, colors such as images, drawings, logos, or icons. Each data entry represents one image

- Text data: Consists of words, sentences, documents such as tweets, reviews, news articles, or books. Each data sample contains a series of text or spoken words


## Data statistics

Recognize NaN values, assigned to empty cells by default.

Check metadata which describes the data and its attributes

Understanding analysis method, such as mean, variance and correlation


## What to do with missing data values?

Can choose to remove rows or columns that contain NaN values

Can replace them with specific value, or a calculated valued based on the rest of the data


## When do you drop NaN values?

Drop a column if it is missing a significant number of values

Drop a row if data sample is missing a significant number of values


## How to decide NaN fill method?

Fill with 0 : When there are a lot of 0s in the dataset

Forward/back fill: In time series data


## Errors and Noise: How to detect erroneous measurements?

You can use visualization and statics to spot errors by:

- Distance to the center of the data
- May have to consider each column seperately

## What to do with error measurements?

Replace them with NaN values and then fill them as you would 

## ML for error detection

Sometimes you cant detect errors with visualization and statistical methods.

ML methods have been developed to address these issues, and will be discussed later in this course


## Summary

Missing and error/noisy values need to be addressed before starting ML analysis

Data statistics can help you determine which ML method to use