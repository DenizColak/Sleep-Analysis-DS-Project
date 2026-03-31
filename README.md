# Sleep Schedule Based Data Analysis

## Overview

In this project I will be analyzing my sleep schedule over a three month period and compare it with the data of which activies performed prior to sleep. Specifically, the goal is to determine whether reading a book late at night correlates positively with the time of the sleeping. A positive correlation would suggest that reading at late hours delays the time of sleep for this individual case.

## Obtaining Data

Data for sleeping hours will come from phone's health application and I will try to reduce margin of error for sleeping times. Obtaining data for books or other activities will come with more challanges. There will be multiple sources for data to choose (Amazon Kindle history, google history) and some personal insertions for the physical book data may be warrented. I will try to get other activities prior to sleep by comparing phone activity time and time of the sleep.

## Preproccessing

For EDA I will use several different graphs with same data so not changing the original data is paramount, this made preprocessing a necessity for each individual chart theese are some methods I used for various charts:
 - Removed invalid or missing timestamps.
 - Merged daily data for both sleep and reading sessions.
 - Changed miliseconds to hours for better representation.
 - Only preprocessed data after midnight for hypothesis testing.

## EDA (Exploratory Data Analysis)

After giving my data a better visual representation with broken bar graphs I did notice some patterns. The analysis revealed a noticeable pattern: on nights when I engaged in late-night reading, there was similarities with my sleeping time. One another question I aim to answer is if the total hour of reading hours may result in a tiredness which may lead to lesser sleep duration. 

## Correlation

Correlation for my first idea that there may be similarities between late-night reading and time of sleep resulted in 0.97 positive correlation but after analyzing my data I noticed this significant result may caused by the overlap between kindle data and phone usage data that provided me sleep data. My other idea that there may be some relationship between total rading time and sleeping duration is resulted with -0.40 correlation value and did not signify something important.
Then minding these results I created a valid alternative hypothesis.

## Hypothesis Testing 

Null Hypothesis: There is no significant relationship between the total duration of reading after midnight and the total duration of sleep on the same day.
Alternative Hypothesis: There is a significant relationship between the total duration of reading after 00:00 (midnight) and the total duration of sleep on the same day.
Sample size is smaller than 30 so T-test is used with significence level (α = 0.05).

## Findings

Results of the T-Test shows us P-Value is 2.31e-07 well below significence level of α = 0.05, Reading Duration (Mean ± SD): 1.66 ± 1.17 hours and Sleep Duration (Mean ± SD): 6.09 ± 1.28 hours, these shows significent results meaning we reject null hypothesis in the favor of the alternative hypothesis.  My initial assumptions about correlation (in correlation section) seem to have complicated results. This shows that more data samples and more refined gathering system may needed for further findings.  

## Machine Learning

To explore potential predictive capabilities within the data, I implemented machine learning models aimed at forecasting sleep duration and sleep onset time based on late-night reading activity using linear regression. %80 of the data ıs split for training and remaining %20 is used for testing the model. Too few sample for the training hurts the overall accuracy of the model, but the results are not overfitted and meaningfull data can be earned from the model.

## Limitations

Sample Size: The dataset used in this project consists of data collected over a three-month period, which may not be sufficient to generalize findings. The small sample size also limits the robustness of hypothesis testing and machine learning models.

Data Reliability: The sleep data extracted from the phone's health application and reading data from activity logs are subject to inaccuracies. Manual input for physical books adds an additional layer of potential error.
Overlapping data sources, such as Kindle activity and phone usage, may introduce bias or redundancy.

Uncontrolled Variables: Factors such as stress, physical activity, diet, and screen time prior to sleep were not accounted for and may significantly influence sleep patterns.

## Future Work

Extended Data Collection: Gather data over a longer period to improve the robustness of the analysis and hypothesis testing.

Refinement of Data Sources: Enhance data accuracy by automating physical book reading tracking and refining overlap in data from Kindle and phone usage. Another application for sleep data may enchance the validness of the results by removing intermeditary apps.

Model Optimization: Optimize machine learning models using advanced techniques (e.g., hyperparameter tuning) for improved prediction accuracy that is based solely on the available dataset.








