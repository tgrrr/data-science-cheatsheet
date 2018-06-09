# STATS NOTES FINAL EXAM - modules

TODO:

[] Copy stats symbols accross


# 1. Types of variables

### Qualitative - category, values or %
  - Categorical
  - Yes/ no
  - Describe by values or percentages

### Quantitative - count or interval
- Discrete = countable
  - Countable
  - Finite number of variables
- Continuous = interval
  - Measurement falls into an interval
  - eg. Time or Height

### Nominal -> categorical
- no meaningful difference between categories

### Ordinal -> rank

### Interval -> equal interval
- Eg. Temperature

### Ratio -> has absolute zero
- Height

### TODO: Design of analysis

# 2 Summarising data

## Summarising data

- Graphical
- Numerical
  - ?Measures of central tendency

## ? Measures of central tendency

- ? Location of data
- Quantitative data
- Mean (ẍ - should be x bar but couldn’t find the simple)
  - Sensitive to each individual data value
  - Outliers
- Median
  - Divides data into two groups of equal sizes
  - Not impacted that much by outliers
  - Two formulas – don’t need to know
- Mode
  - Maximum frequency value
  - Repeated value
  - Can be bimodal etc.
  - Frequency table/ histogram

## Measures of variability

### Spread of your data

### Range
- Most common measure of variability
- Max value – min value
- Very sensitive to outliers

### Variance
> Variance: Sensitive to each individual data point

- TODO: formula
- Compared each sample to the mean
- Sensitive to each individual data point
- Remove outliers first?

> Remove outliers first?

### IQR
- Range of the middle 50% of data
- Q3 – Q1

### Outlier
- TODO: Any values less than Q1 – 1.5IQR or more than Q3 – 1.5IQR

```
Q1 – 1.5IQR or more than Q3 – 1.5IQR
```

### Boxplot - Is data symmetric?
- No statistical package shows your fences (defined above)
- Use to decide if data is symmetric or not
  - Whiskers are the same size
  - Q2 (or median) middle of IQR
- Compare to histogram
- Use to compare (variability) of data
  - Can look at median value
  - Or length of positive skew
  - Or largest Q3, etc

### Skew
- Positive skew – mean greater than median
- Negative skew – mean less than median

# 3. TODO: Probability using contingency table

## TODO: Probability using contingency table
## TODO: Events occurrence
## TODO: Mutually exclusive event
## TODO: Union
## TODO: Intersection
## TODO: Conditional probability


# 4. TODO: Binomial distribution

## TODO: Binomial distribution
- When outcome of each experiment is only two options
- Estimate number of success after n experiments
  - Two parameters
  - Number of trials
- Probability of success
- Discrete random variables only
- Expected value of success = mean

Not on exam:
Mean = n x p (not on exam)
Variance = np(1 – n) (not on exam)


## TODO: Poisson distribution
Rate of occurrence per unit time/ distances
1 parameter λ
Discrete random variables
Or any factor of that time/ distance variable
Mean = λ
Variance = λ

## TODO: Normal distribution

Symmetric
  Centre is always the mean
Bell shape
99.7% of values within µ ± 3σ
95% of values within µ ± 2σ
68% of values within µ ± σ
Z – standardised normal
  Same bell shape
  Mean = 0
  Variance = 1

TODO: formula here

Not fussed about >= or >
  Calculating area under the curve
  Continuous variables

# 5. TODO: Mean of sample distribution and properties
# 6. TODO: Point estimates
# 7. TODO: Hypothesis testing
# 9. TODO: Regression, y = ɑ + ɓx



# TODO FROM HERE ONWARDS -----------------------

----------- TODO FROM HERE ONWARDS -----------------------
Exam
Sample exam
Under assignments
Open book
2 double sided hand written/ typed A4 notes
Use Mali’s notes as a basis
Calculator
Not allowed a graphics calculator
But do need a simple calculator
15 minutes reading time
50 multiple choice questions
10 short answers (worth 50 marks)
Mali will send through notes of what she went through in the lecture today

### Module 1 - Definition of variables

Definition of variables
Nominal (categorical)
Ordinal (rank)
Interval (equal interval)
Ratio (absolute zero)

Design of analysis

### Module 2 - Summarising data
Summarising data
Graphical
Numerical
Measures of central tendency
Measures of central tendency
Location of data
Quantitative data
Mean (ẍ - should be x bar but couldn’t find the simple)
Sensitive to each individual data value
Outliers
Median
Divides data into two groups of equal sizes
Not impacted that much by outliers
Two formulas – don’t need to know
Mode
Maximum frequency value
Repeated value
Can be bimodal etc.
Frequency table/ histogram
Measures of variability
Spread of your data
Range
Most common measure of variability
Max value – min value
Very sensitive to outliers
Variance

Compared each sample to the mean
Sensitive to each individual data point
Remove outliers first?
IQR
Range of the middle 50% of data
Q3 – Q1
Outlier
Any values less than Q1 – 1.5IQR or more than Q3 – 1.5IQR
Boxplot
No statistical package shows your fences (defined above)
Use to decide if data is symmetric or not
Whiskers are the same size
Q2 (or median) middle of IQR
Compare to histogram
Use to compare (variability) of data
Can look at median value
Or length of positive skew
Or largest Q3, etc
Positive skew – mean greater than median
Negative skew – mean less than median

### Module 3 Probability using contingency table
Probability using contingency table
Events occurrence
Mutually exclusive event
Union
Intersection
Conditional probability


### Module 4 Binomial distribution

Binomial distribution
When outcome of each experiment is only two options
Estimate number of success after n experiments
Two parameters
Number of trials
Probability of success
Discrete random variables only
Expected value of success = mean
Mean = n x p (not on exam)
Variance = np(1 – n) (not on exam)


Poisson distribution
Rate of occurrence per unit time/ distances
1 parameter λ
Discrete random variables
Or any factor of that time/ distance variable
Mean = λ
Variance = λ
Normal distribution
Symmetric
Centre is always the mean
Bell shape
99.7% of values within µ ± 3σ
95% of values within µ ± 2σ
68% of values within µ ± σ
Z – standardised normal
Same bell shape
Mean = 0
Variance = 1

Not fussed about >= or >
Calculating area under the curve
Continuous variables

### Module 5 - Mean of sample distribution and properties
Mean of sample distribution and properties
Observation in samples change
Mean random variable on its own
Population (should double check these equation)
Mean µ
Variance σ2
E(ẍ) = n/x = µ
Var(ẍ) = σ2/x = σ2/n
SE = σ/√x =  σ/√n
Standard error of mean
Reduces as n increases
Inversely proportional
Central limit theorem
Distribution of sample mean
If n > 3σ and keep drawing samples to calculate mean
They will be different
Will follow a normal distribution
qqplot
For a normal population
Doesn’t matter about sample size
ẍ ~ N(µ, σ2/n)

### Module 6 - Point estimates
Point estimates
ẍ point estimate of µ (population mean) - Ṕ
Error = σ/√n
Confidence intervals
Define by ɑ significance level
(1 - ɑ)/ CI
 
Whether using z or n
These are the true values
If repeat sampling 100 times, get 100 CI
Actual population mean (µ) would have CI 95 of these intervals
Chance of not including value of µ in only 5%
Using shiny app
If increase sample size, CI will shrink
Mean becomes closer to actual mean of population
Increase level of CI (95 – 99.7), length of CI increases
Larger interval
For smaller samples
Proportion – didn’t do much
Use z statistic to calculate
Formula?

### Module 7 - Hypothesis testing
Hypothesis testing
Null hypothesis
Always value you have
Equal to something
Alternat hypothesis
Less than, greater than or not equal
Test whether it is significant or not
Significant at level ɑ if reject null
ɑ may differ
Making decisions
Use ɑ given to you
Usually not, then use 5%
Reject if
p < 0.05
µ doesn’t fall into 95% CI
Rejection region – not examinable
Type I and type II error
Every time you make a decision, bound to make an error
Type I error is when you reject null when not true
Sample may not be representative of the population
Type II error is when you accept null, falsely accept the null
ɓ
In experimental design
Work out whether type I or type II error is more of a risk
Design CI/ p value by reducing one error type
Reduce ɑ, increase ɓ

Two sample test
Two assumptions
Independent or not (paired t-test)
Variance equal
Levene test
σ12 = σ22
Have to test
Null hypothesis
Both populations are normal or n = 30
So can use the central limit theorem
Decision – testing th
Decision
Testing difference between mean of two populations
Accept if
p < ɑ
95% CI includes zero
Otherwise reject
Paired data
Problem should clearly state that it is a paired situation
Same population
Apply different conditions
Samples are not independent
One sample test
Only looking at different for each test subject
Null hypothesis: difference = 0
Alternat hypothesis: difference ≠ 0

Categorical data
Association
More than one categorical variable
Between them
In different levels
Formula expected =
Degrees of freedom = r1(c1 – 1)
Goodness of fit
Looking at proportions
Null assumptions
Categorical data has at least two variables
Pblack = 30%
Pblue = 20%
Alternat assumptions
For all categories together
Not for each category separately
Χ2 – chi square test
Degrees of freedom: number of categories – one
Minimum value for each category must be more than 5

E = expected value if assumption correct (30% black)

### Module 9 - Regression, y = ɑ + ɓx
Regression, y = ɑ + ɓx
Test for a significant relationship between y and x
Null: no relationship
Alternate: is a relationship
Look at p value for F statistic
Small p, reject null
Describe strength of relationship
Look at R value
R may be negative or positive
R > 0.75 – yes there is a strong relationship
ɓ = slope
Can be positive or negative
Change in y per unit x
ɑ = significance in model
ɑ = 0 vs ɑ ≠ 0
Will be given p value in R
Your residual must be normal
Mean = 0
Variance = σ2


# ROUGH STATS NOTES FINAL EXAM ROUGH

## Module 4

Which should I report?

### Binomial-distribution:
- = bi = only 2 options.
- applied to discreet only



Either they survive, or they die.

Defined by the number of trials
The probability of success.

### Conditional Probability


Calculate the mean
see if value is far from mean
Far from mean, less likely it will happen

P (B | A) = PA upside down U B

### Poisson distribution
lambda x t = per day


- refers to discreet random variables
When we use it:
- Rate of occurence per unit of time or distance
  - concentrate on time
  (eg deaths on the road per year)
  (number of passengers arriving on Xmas day in )
- Not use it if it's less than something

Only 1 param:
- Rate of occurance
- something about lambda
- What is the probab
Lambda * t is 10* 7 = 70

Have to multiply lambda

- Not expected to know formula

### Normal distribution
- Bell shaped
- centre is always mean
- is symmetric
- Tail is almost touching X

Regardless of p or d

1. X ~ N (mu, sigma squared)



99.7% of value fall between mu +- 3 sigma
95% of value fall bewee     mu +- 2 sigma
68% of value                mu +- 1 sigma

- We don't care if we have equals sign or not
- It's about area under your curve

If given mu and sigma, we can calculate X When something is given to you TODO:



## Module 5

For any

Population with mean


Not talking about distribution of population

Population with mean sigma variance sigma squaredu










## Central limit theorum


If sample size large
and some other stuff
If sample is drawn from normal po

Then



Define Xbar
mean is

variance is sigma^2 / n





## 6.


If Xbar is = point definition of


If asked for error

error is sigma / square root of n



P^ hat



## Confidence level

Significance level alpha

TODO copy formula here

This is when we might use T

If use T, we replace sigma with S


Every time I change the formula
My confidence interval keeps changing


If I increase size of sample
sigma divided by square root of n
Confidence interval shrinks

mean becomes closer to actual mu
becomes more accurate

If I increase the level of my confidence

If I want a higher level of confidence
then alpha is 1%.

Then

## Confidence interval for proportion

When sample size large, always normal distribution so use z



## 7. Hypothesis testing

H0
If testing mean or proportion value
always have equal sign to value
Eg. mean is equal to 100

Write H0 and H1

Write whether test is significance/or not
It's significant if we reject H0
Test is not significant when
at level alpha = 5%

If alpha is given to you, we have to use alpha.
If not, we can always assume alpha is 5%

! We reject if P value is less than alpha
If value of mu under H

We reject H0 if 100 falls in Confidence something is

Rejection region (not examinable)


Didn't examine this
Type I errors - sample is wrong, and
Type II errors


TODO: add pregnant and boy who cried wolf here

2 sample test

1. Assumption 1: 2 populations are independent
2. both populations are normal
3. Samples taken for two populations

We ahve to assume sigma^2 = sigma^2 of population

We use Levene test


If p value is less than alpha

or 95%


We're testing the difference between mu1 and mu2
m1 - m2

This is where we're looking for if the value of something falls around zero
(one is plus, the other is negative)




## Paired Data
-


## Module 8


Goodness of time

categorical variables

H0 P black = 20 p blue = 30% P yellow = 50%

Ha the above is not what is given under h0

Use chi squared test

df (degrees of freedom)

Called goodness of fit


## Test of association

More than one categorical variable
- Want to know if there is relationship
- or relationship between levels

Expected value

Expected value = n(
  
  

  )
  
  
  Then degrees of freedom
  
  
  Then we get something about goodness of fit
  
  
## mod 9. Regression equation

y = alpha (intercept) + B(slope)X

Testing if there's a significant relationship between Y and X

H0: there is no significant relation
HA: there is a signifcant relationship


Something about looking for P value
Look for positive or negative sign
