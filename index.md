---
layout: default
mathjax: true
---
---
title: "The Effect of TCJA 2017 on Capital Investment"
author: "Yizhe Huang"
date: "March 2025"
---

# **Abstract**  
This study examines the impact of the Tax Cuts and Jobs Act (TCJA) of 2017 on capital investment across various industries in the United States.  
Using firm-level data from 2011 to 2023 and a difference-in-differences framework, we find that capital-intensive firms experienced substantial increases in capital expenditures, while non-capital-intensive firms showed limited or negative investment responses.  

# **Introduction**
The Tax Cuts and Jobs Act (TCJA) of 2017 reduced the corporate tax rate from 35% to 21%, aiming to stimulate economic growth. However, the impact varied across industries. This study evaluates the TCJA’s heterogeneous effects on capital investment using firm-level data from 2011 to 2023.

# **Theory**
The optimal investment \( I \) satisfies:
$$
\Pi = \Pi_1 + \beta \cdot \Pi_2
$$
where:
$$
\Pi_1 = (1 - \tau) R_1 - C(I) + \omega \tau I
$$
$$
C(I) = \alpha I^2
$$
$$
R(K) = A K^\theta
$$
$$
K_2 = (1 - \delta) K_1 + I
$$

### **First-Order Condition**
The first-order condition for optimal investment:
$$
-2\alpha I + \omega \tau + \beta (1 - \tau) A \theta \left[(1 - \delta) K_1 + I\right]^{\theta - 1} = 0.
$$

### **Effect of Tax Deductions (\( \frac{dI}{d\omega} \))**
$$
\frac{dI}{d\omega} = \frac{-\tau}{-2\alpha + \beta (1 - \tau) A \theta (\theta - 1) \left[(1 - \delta) K_1 + I\right]^{\theta - 2}}
$$

# **Data**
We use data from Capital IQ (2011-2023). Key variables include:

| Variable        | Description                      |
|----------------|--------------------------------|
| Capex\_Value   | Capital expenditures           |
| ROA            | Return on assets               |
| TOTAL\_REV     | Total revenue                  |
| RD\_EXP\_FN    | R&D expenditures               |
| NAICS\_CODE    | Industry classification        |
| State          | U.S. state                      |
| Year           | Year of observation            |

# **Methodology**
We employ a **Difference-in-Differences (DID)** framework:
$$
CapEX_{i,t} = \beta_0 + \beta_1 \cdot Post_t + \beta_2 \cdot Capital\_Intensive_i + \beta_3 \cdot Post_t \cdot Capital\_Intensive_i + \sum_{k} \beta_k Control_{i,k,t} + \delta_t + \delta_{State} + \epsilon_{i,t}
$$
where \(Post_t\) is a dummy variable for post-TCJA periods, and \(Capital\_Intensive_i\) is a dummy for capital-intensive firms.

# **Results**
## **Baseline Regression**
\[
Post\_CapitalIntensive = -71,160^{***}, p<0.01
\]
This suggests capital-intensive firms experienced a significant increase in CapEx post-TCJA.

## **Parallel Trend Test**
The pre-TCJA trends in CapEx for capital-intensive and non-capital-intensive firms were statistically indistinguishable (\( p > 0.1 \)), validating the DID approach.

# **Discussion**
The TCJA benefited capital-intensive firms through accelerated depreciation, while non-capital-intensive firms showed limited responses. Policy adjustments should target tax incentives for non-capital-intensive firms.

# **References**
1. **Crawford, S., & Markarian, G. (2024).** The effect of the Tax Cuts and Jobs Act of 2017 on corporate investment. *Journal of Corporate Finance*.
2. **Gale, W. G., Hoopes, J. L., & Pomerleau, K. (2024).** Sweeping changes and an uncertain legacy: The Tax Cuts and Jobs Act of 2017. *Journal of Economic Perspectives*.
3. **Wagner, A. F., Zeckhauser, R. J., & Ziegler, A. (2020).** The Tax Cuts and Jobs Act: Which firms won? Which lost? *NBER Working Paper No. 27470*.

