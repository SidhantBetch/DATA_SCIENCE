# Chi square Test

## Applicable in two types of situations
- Goodness
- Independence

## formula:
$\chi^2 = \sum \frac{(O_i - E_i)^2}{E_i}$

where:  
$\chi^2$ = Chi Square  
$O_i$ = Observed Value  
$E_i$ = expected Value

---------------------------------------------------------------------------------------------------------------------------------------------------------

## Example 1
A fair die is rolled 120 times and the following results are obtained.  
Face 1: 22 times  
Face 2: 17 times  
Face 3: 20 times  
Face 4: 26 times  
Face 5: 22 times  
Face 6: 13 times  
Test at a 5% level of significance whether the die is fair. give the solution in .md form
--------
### solution
A fair die is rolled 120 times and the following results are observed:

| Face | Observed Frequency (O) |
|------|------------------------|
| 1    | 22                     |
| 2    | 17                     |
| 3    | 20                     |
| 4    | 26                     |
| 5    | 22                     |
| 6    | 13                     |
| **Total** | **120**          |


🧠 Step 1: Hypotheses  
- **Null Hypothesis (H₀):** The die is fair (all outcomes equally likely)
- **Alternative Hypothesis (H₁):** The die is not fair  


⚙️ Step 2: Expected Frequencies  
For a fair die:

$E = \frac{Total\ Rolls}{Number\ of\ Faces} = \frac{120}{6} = 20$

So, expected frequency for each face = **20**  


🧮 Step 3: Chi-Square Statistic    
Formula:

$\chi^2 = \sum \frac{(O - E)^2}{E}$

| Face | O  | E  | (O - E) | (O - E)² | (O - E)² / E |
|------|----|----|---------|----------|--------------|
| 1    | 22 | 20 | 2       | 4        | 0.20         |
| 2    | 17 | 20 | -3      | 9        | 0.45         |
| 3    | 20 | 20 | 0       | 0        | 0.00         |
| 4    | 26 | 20 | 6       | 36       | 1.80         |
| 5    | 22 | 20 | 2       | 4        | 0.20         |
| 6    | 13 | 20 | -7      | 49       | 2.45         |
| **Total** |    |    |         |          | **5.10**     |

$\chi^2 = 5.10$


📉 Step 4: Degrees of Freedom  

$df = n - 1 = 6 - 1 = 5$


📌 Step 5: Critical Value  
- At α = 0.05 and df = 5  
- Critical value:

$\chi^2_{0.05,5} ≈ 11.07$


✅ Step 6: Decision  
- Calculated value = **5.10**
- Critical value = **11.07**


Since:  
χ² < χ²_critical
5.10 < 11.07
👉 Fail to reject the null hypothesis (H₀)

-----------------------------------------------------------------------------------------------------------------------------------

Example 2;
A study was conducted to investigate whether there is a relationship between gender and the perferred genre of music.
A sample of 235 people was selected, and the data collected is shown below. Test at a 5% level of signigicance wheter there is a significant association between gender and music perference.
  
________| Pop      | Hip Hop  | classical| Rock
--------|----------|----------|----------|------------
Male    | 40       | 45       | 25       | 10
Female  | 35       | 30       | 20       | 30

-------

### solution
📊 Observed Data

| Gender | Pop | Hip Hop | Classical | Rock | Row Total |
|--------|-----|---------|-----------|------|-----------|
| Male   | 40  | 45      | 25        | 10   | 120       |
| Female | 35  | 30      | 20        | 30   | 115       |
| **Column Total** | **75** | **75** | **45** | **40** | **235** |

- Significance level: **α = 0.05**  


🧠 Step 1: Hypotheses  
- **H₀ (Null Hypothesis):** Gender and music preference are independent  
- **H₁ (Alternative Hypothesis):** Gender and music preference are associated  


⚙️ Step 2: Expected Frequencies  
Formula:

$E = \frac{(Row\ Total \times Column\ Total)}{Grand\ Total}$


Expected Table (E)

| Gender | Pop | Hip Hop | Classical | Rock |
|--------|-----|---------|-----------|------|
| Male   | 38.30 | 38.30 | 22.98 | 20.43 |
| Female | 36.70 | 36.70 | 22.02 | 19.57 |


🧮 Step 3: Chi-Square Statistic  
Formula:

$\chi^2 = \sum \frac{(O - E)^2}{E}$  

| Cell | O | E | (O - E)² / E |
|------|---|----|-------------|
| Male-Pop | 40 | 38.30 | 0.08 |
| Male-HipHop | 45 | 38.30 | 1.17 |
| Male-Classical | 25 | 22.98 | 0.18 |
| Male-Rock | 10 | 20.43 | 5.32 |
| Female-Pop | 35 | 36.70 | 0.08 |
| Female-HipHop | 30 | 36.70 | 1.22 |
| Female-Classical | 20 | 22.02 | 0.19 |
| Female-Rock | 30 | 19.57 | 5.56 |
| **Total χ²** |  |  | **13.80** |

$\chi^2 ≈ 13.80$  


📉 Step 4: Degrees of Freedom  

$df = (r - 1)(c - 1) = (2 - 1)(4 - 1) = 3$  


📌 Step 5: Critical Value  
- At α = 0.05 and df = 3  
- Critical value:

$\chi^2_{0.05,3} ≈ 7.815$  


✅ Step 6: Decision  
- Calculated χ² = **13.80**  
- Critical χ² = **7.815**

Since:  
χ² > χ²_critical
13.80 > 7.815

👉 Reject the null hypothesis (H₀)
