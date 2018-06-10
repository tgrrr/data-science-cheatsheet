# STATS NOTES FINAL EXAM - modules

# 1. Types of variables

**Qualitative** - category, values or percentage %

- Categorical
- Yes/ no
- Describe by values or percentages

**Quantitative** - count or interval

Discrete = countable
  - Countable
  - Finite number of variables

Continuous = interval
  - Measurement falls into an interval
  - eg. Time or Height

**Nominal** - aka categorical

no meaningful difference between categories

**Ordinal** - rank

**Interval** - equal interval

Eg. Temperature

**Ratio** - has absolute zero

Eg. Height

TODO:

- Design of analysis

# 2 Summarising data

- Graphical
- Numerical
  - Measures of central tendency

## Measures of central tendency

- ? Location of data
- Quantitative data
- Mean (x̅)
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

```
IQR <- Q3 – Q1
```

### Outlier

```
outliers < Q1 – 1.5IQR
# or
outliers > Q3 – 1.5IQR
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

> Positive skew

```
mean > median
```

> Negative skew

```
mean < median
```

# 3. TODO: Probability using contingency table

[] Copy stats symbols across




## TODO: Probability using contingency table
## TODO: Events occurrence

## Intersection (AND)

- Mutually exclusive event
```
Pr(  ∩  ) => mutually exclusive
```

## Union (OR)

```
Pr(1 serve ∪ < 1 serve)
```

## Conditional probability (given)

Pr(B|A) => conditional probability of B given A
The two events A and B are independent if and only if

> independent IF

```r
Pr(A|B) = Pr(A)
# OR
Pr(B|A) = Pr(B)
```

## Permutations

```r
factorial(6)/factorial(6-3)
> [1] 120
```

## Combinations

```r
choose(10,4)
> [1] 210
```

# 4. Binomial distribution

```r
binom(numberOfTrials,probability)
```

*Applies to discreet variables only*

- = bi => only 2 options for the outcome of each experiment
  - Eg. Either they survive, or they die.

- Estimate number of success after n experiments

> mean = expected value of success

```
E(x) = numberOfTrials * probability
```

> Variance

```shell
numberOfTrials * probability(1-probability)
```

### Standard Deviation (σ)

> Standard deviation

```shell
√numberOfTrials * probability(1-probability)
```

```r
standard.deviation <-
sqrt(numberOfTrials * probability(1-probability))
```

### Sample Standard Deviation (x̅)

> μ <- population mean

> x̅ <- sample mean

```r
sample.standard.deviation <-
sqrt(
  (x[i-n] - x̅)
  / (n-1))
```

## Poisson distribution (λ Lambda)

```
µ = λ * t
mean <- lambda * unitOfTime

variance σ^2^ <- Var(x) = λ

standard.deviation <- σ = √λ
```

The Poisson distribution has one parameter:
Lambda (λ) which can equal

Rate of occurrence:

- `E(x) = λ` the expected or
- `µ = λ` mean number of events
-  per unit time/distances

- Also Variance = λ ?

```r
dpois(x, lambda)
```

- Discrete random variables
- Or any factor of that time/ distance variable


### Example Poisson

```
mean <-
µ = E(x) = λ
mean.for.the.week <-
µ = λ * t = 16 * 7 = 112
```

Expected daily number of patients for a doctor during winter might be λ = 16 per day


> Pr(X <= x)

```r
> ppois(100, 16*7)
[1] 0.1378483
```

What is the probability that the doctor will see less than or equal to 100 patients in a week?

The questions asks

`Pr(X ≤ 100)`

We need to adjust the mean value to

`μ = 16*7 = 112`

### Plotting Poisson

TODO:

```r
plotDist("pois",
  lambda = 16,
  xlab = "No. Patients",
  main = "Poisson Distribution, Mean = 16",
  ylab = "probability",
  groups= x==16)
```




## Normal distribution

- Used for continuous (interval) variables

- Goal: Calculating area under the curve

Is:

- Symmetric
- The centre is always the mean (μ)
- Is Bell shape
- Tail is almost touching X

TODO:
1. X ~ N (mu, sigma squared)

If given mu and sigma, we can calculate X When something is given to you


```
99.7% of values within µ ± 3σ
95% of values within µ ± 2σ
68% of values within µ ± σ
```

Z – standardised normal distribution
- Same bell shape
- Mean = 0
- Variance = 1

TODO:

- formula here
- We don't care about >= or >
- Which should I report?
- ? Regardless of p or d

# 5. TODO: Mean of sample distribution and properties

## TODO: Mean of sample distribution and properties

## TODO: Observation in samples change

## TODO: Mean random variable on its own

## TODO: Population (should double check these equation)

```
Mean µ
Variance σ2
E(x̅) = n/x = µ
Var(x̅) = σ2/x = σ2/n
SE = σ/√x =  σ/√n
```
  - Standard error of mean
  - Reduces as n increases
  - Inversely proportional

## CLT - Central Limit Theorem

If a variables:
- population distribution is normally distributed
- sample distribution of the mean will be normally distributed

TODO: add math formula

Assume:
`µ <- 193 seconds` = mean and standard.deviation of youtube video duration is
`n <- 100` sample size

What's the probability of randomly selecting a
`sample mean duration < 150 seconds` ?

`n > 30`, therefore:

```
x̅ ~ N(µ, σ/√n)
x̅ ~ N(193, σ/√n)
x̅ ~ N(193, 193/sqrt(100))
= N(193, 19.3)
```

> then to get Pr(x̅ < 150)
```r
pnorm(150, 193, 19.3)
[1] 0.01294
```

What's the probability of randomly selecting a
`sample mean duration > 240 seconds` ?

```r
pnorm(240, 193, 19.3, lower.tail = F)
[1] 0.007441098
```

- Distribution of sample mean
- If n > 3σ and keep drawing samples to calculate mean
- They will be different
- Will follow a normal distribution

TODO:
```r
qqplot()
```
- For a normal population
- Doesn’t matter about sample size

```
x̅ ~ N(µ, σ2/n)
```

TODO:
- add my notes
- Calculate the mean
- see if value is far from mean
- Far from mean, less likely it will happen
- Population with mean
- Not talking about distribution of population
- Population with mean sigma variance sigma squaredu

# 6. TODO: Point estimates

`x̅ point estimate of µ (population mean) - Ṕ`

```
Error = σ/√n
```

> confidence.interval
> Define by ɑ significance level

```
(1 - ɑ)/ CI
(1 - significance.level)/confidence.interval
```

- larger sample = smaller Confidence Intervals
- Mean becomes closer to actual mean of population


TODO:

- Increase level of CI (95 – 99.7), length of CI increases
- Proportion – didn’t do much
- Use z statistic to calculate
- Formula?
- Whether using z or n
- These are the true values
- If repeat sampling 100 times, get 100 CI
- Actual population mean (µ) would have CI 95 of these intervals
- Chance of not including value of µ is only 5%


# 7. TODO: Hypothesis testing

Hypothesis testing
Null hypothesis
Always value you have
Equal to something
Alternate hypothesis
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

# 9. TODO: Regression, y = ɑ + ɓx

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


# TODO FROM HERE ONWARDS -----------------------

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




# ROUGH STATS NOTES FINAL EXAM ROUGH














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
