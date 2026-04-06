# T-test
A T-test checks if observed differences between groups are real (statistically significant) or just due to random chance.
It used when number of sample value is less than 30.

## Formula:

$t_{test} = \frac{\bar{x} - \mu}{(\frac{s}{\sqrt{n}})}$

where:-  
$\bar{x}$ = Sample Mean  
$\mu$ = Population Mean  
$s$ = Standered deviation sample  
$n$ = Number of sample  

## Example 1:
A manufacturer claims that the average weight of a bag of potato chips is 150 grams. A sample of 25 bags is taken, and the average weight is found to 
to be 148 grams, with a standard deviation of 5 grams. Teast the manufacturer's claim using a one-tailed t-test with a significance level of 0.05.

### Solution
Given:
$\bar{x}$ = 148, 
$\mu$ = 150, 
$s$ = 5, 
$n$ = 25,

$H_o : \mu = 150$  
$H_a : \mu < 150$

we find using left tail test because $\mu$ less than 150
$\alpha = 0.05$  
find df  
df = n-1 = 25-1 = 24  

using t-test table $t_{table}$ = 1.711  

$t_{Cal} = \frac{\bar{x} - \mu}{(\frac{s}{\sqrt{n}})}$
$=\frac{148 - 150}{(\frac{5}{\sqrt{25}})}=-2$

Hance, Ha is wrong because $t_{table} > t_{cal}$


## Example 2
A company wants to test whether there is a difference in productivity between two teams.   
They randomly select 20 employees from each team and record their productivity scores.   
- The mean productivity score for Team A is 80 with a standard deviation of 5.  
- The mean productivity score for Team B is 75 with a standard deviation of 6.    
Test at a 5% level of significance whether there is a difference in productivity between the two teams.

### Solution:
Given data:
  - Mean of Team A: x̄₁ = 80
  - Standard deviation of Team A: s₁ = 5
  - Mean of Team B: x̄₂ = 75
  - Standard deviation of Team B: s₂ = 6

  Significance level: α = 0.05

🧠 Step 1: Define Hypotheses 
- Null hypothesis (H₀): μ₁ = μ₂  
- Alternative hypothesis (H₁): μ₁ ≠ μ₂  

⚙️ Step 2: Test Statistic Formula  
Two-sample T-test: 

$$
t = \frac{x̄_1 - x̄_2}{\sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}}
$$

🧮 Step 3: Calculate T-value

$$
t = \frac{80 - 75}{\sqrt{\frac{5^2}{20} + \frac{6^2}{20}}}
$$

$$
t = \frac{5}{\sqrt{\frac{25}{20} + \frac{36}{20}}}
$$

$$
t = \frac{5}{\sqrt{1.25 + 1.8}} = \frac{5}{\sqrt{3.05}}
$$

$$
t ≈ \frac{5}{1.747} ≈ 2.86
$$


📉 Step 4: Degrees of Freedom

$$
df = n_1 + n_2 - 2 = 20 + 20 - 2 = 38
$$


📌 Step 5: Critical Value  
- For α = 0.05 (two-tailed) and df = 38  
- Critical t ≈ ±2.024
  
✅ Step 6: Decision  
- Calculated t = **2.86**
- Critical t = **2.024**

Since:  
|t| > t_critical  
2.86 > 2.024  




