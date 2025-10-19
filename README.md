# 3pl-Lab
## Overview

This project applies **three-parameter logistic (3PL)** item response theory modeling using R's MIRT package to evaluate test quality and examinee ability. The analysis examines model fit, item characteristics, and person-fit statistics for a 10-item assessment administered to 500 examinees.

## Research background

R can be used to model dichotomous and polytomous
data, and can be extremely flexible with different algorithms, item
types, constraints, priors, etc.

## Research Objectives
-   Evaluate **model fit indices** to determine which model fits out
    data best.
-   Summarize **classical item statistics**.
-   Extract and plot **item parameters**.
-   Evaluate **person-fit statistics**.
  
#  **Key Findings**

## **Model Estimation**

Using priors in the 3PL model significantly improved estimate stability:
- Reduced standard errors for item parameters, indicating more precise estimates
- Faster model convergence, enhancing computational efficiency
- Slightly improved fit indices compared to the model without priors

## **Item Quality**

**Classical Item Statistics**
-   Proportion correct values ranged from 0.334 (item 10) to 0.822 (Item
    1), suggesting varied item difficulty.
-   Item 7 showed the lowest biserial correlation (0.09), warranting
    further examination.

**Item Parameters**
-   Difficulty ranged from -2.560 (item 1) to 1.724 (item 10)
-   Lowest discrimination was item 7 at 0.340, and highest was item 8 at
    3.714. We saw item 8 contributed the most information, which could
    be indicative of over-fitting.
-   Guessing ranged from .148 to .245, affecting the lower asymptotes of
    the item characteristic curves.
-   The S-X2 statistic, which assesses item fit, showed no significant
    item misfit (p-values all \> 0.05).

**Examinee Parameters**
-   70 examinees (out of 500) had infit or outfit values outside of 1.5,
    suggesting that most response patterns align well with the model.
    This is a bit more than acceptable, so we should be cautious and
    evaluate the response patterns.
-   The empirical reliability estimate was 0.561, indicating moderate
    reliability.
    
## Recommendations
1. Revise Item 7 – Low discrimination and item-total correlation warrant content review or deletion
2. Investigate aberrant responders – Examine the 70 examinees with unusual response patterns
3. Monitor Item 8 – Validate its high discrimination on independent samples to rule out overfitting
4. Improve reliability – Consider item revision or selection of higher-discriminating items to boost overall test consistency

# References

<https://cran.r-project.org/web/packages/mirt/mirt.pdf>

Bond, T. G., & Fox, C. M. (2007). Applying the Rasch model: Fundamental
measurement in the human sciences (2nd ed.). Routledge.

De Ayala, R. J. (2009). The theory and practice of item response Theory.
Guilford Press.

Han, K. T. (2012). Fixing the c parameter in the three-parameter
logistic model. Practical Assessment, Research, and Evaluation, 17(1).
<https://doi.org/10.7275/f0gz-kc87>

Iwintolu, R. O., Opesemowo, O. A. G., & Adetutu, P. O. (2024). Effect of
2-PL and 3-PL models on the ability estimate in mathematics binary
items. Journal on Efficiency and Responsibility in Education and
Science, 17(3), 257–272. <http://dx.doi.org/10.7160/eriesj.2024.170308>

Linacre, J. (2002) What do infit and outfit, mean-square and
standardized mean? Rasch Measurement Transactions, 16, 878.

Robitzsch, A. (2022). Four-parameter guessing model and related item
response models. Mathematical and Computational Applications, 27(6), 95.
<https://doi.org/10.3390/mca27060095>
