# Hypothesis Testing(Z Test)

## Formula:
### $Z_{test} = \frac{\bar{x} - \mu}{(\frac{\sigma}{\sqrt{n}})}$

where:
- $\bar{x}$ = Sample Mean
- $\mu$ = population Mean
- $\sigma$ = Population Standard Deviation
- n = number of sample data

## Example 1:
A teacher claims that the mean score of students in his class is greater than 82 with a standard deviation of 20. If a sample of 81 students was selected with a mean score of 80. ❓

### Solution:
$H_o = \mu \not= 82$  
$H_a = \mu > 82$  

$\alpha = 0.05$   
$\mu = 0.95$

$Z_{value} = 1.6 + 0.04 = 1.64 (based on z table) $

formulat: $Z = \frac{\bar{x} - \mu}{(\frac{\sigma}{\sqrt{n}})}$

$Z_{cal} = \frac{90 - 82}{(\frac{20}{\sqrt{81}})} = 36 $


## Example 2

### Scenario
Imagine you work for an e-commerce company, and your team is responsible for analyzing customer purchase data. You want to determine whether a new website design has led to a significant increase in the average purchase amount compared to the old design.

### Data
You have collected data from a random sample of:
- **30 customers** who made purchases on the **old website design**
- **30 customers** who made purchases on the **new website design**
You have the sample means, sample standard deviations, and sample sizes for both groups.


### Old Design Data
[45.2, 42.8, 38.9, 43.5, 41.0, 44.6, 40.5, 42.7, 39.8, 41.4, 44.3, 39.7,41.5, 39.6, 44.0, 43.1, 38.7, 43.9, 42.0, 41.9, 42.8, 43.7, 41.3, 40.9,42.5, 41.6]

### New Design Data
[48.5, 49.1, 50.2, 47.8, 48.7, 49.9, 48.0, 50.5, 49.8, 49.6,50.1, 48.6, 48.3, 49.0, 50.0, 48.4, 49.3, 49.5, 48.8, 50.6,50.4, 48.1, 49.2, 50.7]

### Additional Information
- Population standard deviation: **2.5**


### Solution
$H_o = web_{new} = web_{old}$  
$H_a = web_{new} > web_{old}$  

$\sigma = 2.5$    
$\mu_{new} = \mu_{old}$  
$n >=30$

$Z_{value} = 1.6448536269514722 (based on z table) $

formulat: $Z = \frac{\bar{x} - \mu}{(\frac{\sigma}{\sqrt{n}})}$

$Z_{cal} = 14.304392023560741$
