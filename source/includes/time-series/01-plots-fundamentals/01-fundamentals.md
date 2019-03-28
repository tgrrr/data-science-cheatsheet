

- Trend
- Seasonality - obvious repeating pattern
- change point
- Variation

### Goal:
Module 1: Introduction
Introduction to the week
Welcome to Week 1: You will study basic context of time series and stochastic processes including basic visualisations for time series data. Then, you will be given a number of tasks to be completed in hands-n tasks session.
Links to the learning objectives
This week will contribute to Course Learning Objectives:
1. Present time series in an informative way, both graphically and with summary statistics
Purpose
By completing the essential set text reading and reviewing the recorded lecture, followed by completing your self-check to ensure you have understood the key concepts, you will be able to begin work on Assignment 1.

### Module 1: 

### Tasks Basic Plots, Examples, and Fundamental Concepts

- MelbourneMonthlyRainfall.csv

1. 
- Load the Melbourne Airport annual rainfall data (MelbourneAnnualRainfall.csv) into R. 
- Then, produce the time series plot for the annual rainfall series in Melbourne Airport. 
- Do you think there is a trend in the series?
- Hint: Use the function `ts()` to convert the `data.frame` into a times series object in R.

2. 
- Simulate a completely random process of `length 48` with `independent, normal values`. 
- At this stage set the mean and variance of the normal distribution to arbitrary values.

- Display the time series plot without converting the generated data to a time series object and by converting the generated data to a time series object. Does it look “random?”
- Repeat this exercise several times with a new simulated dataset at each time. Does your view on the randomness of series change from one simulation to the other?
- Repeat this exercise with standard deviations of 0.1 and 10. What is the effect of variance of series on the resulting time series plot?

3. Simulate a completely random process of `length 48` with independent, `chi-square distributed values`, `each with 2 degrees of freedom`.
- Display the time series plot. Does it look “random?”
- Repeat this exercise several times with a new simulated dataset at each time. Does your view on the randomness of series change from one simulation to the other?
- Compare your results with those obtained in the second task.

4. 
- Load the Melbourne Airport monthly rainfall data (MelbourneMonthlyRainfall.csv into R.
 - Construct a time series plot in a blank graphics window. Is the seasonal effect is clearly seen from the time series plot?
- Construct a time series plot in a blank graphics window with monthly plotting symbols. 
- Is there any improvement in the ease of identification of the seasonal effect when the symbols are super-imposed onto the plot?

