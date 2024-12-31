# FIN-Econ-FF3-Sorting-Strategy

## Overview

**FIN-Econ FF3 Chinese Sorting Trading Strategies To Select Portfolios**  

This program is part of a course project for **FIN ECON**, demonstrating a trading strategy that leverages the **Fama-French three-factor model (FF3)**, sorted by **Earning/Market values (EM)** and **Free-Cash-Flow (FCF)**.  

### Highlights:
- **Target:** Chinese STSE stock market  
- **Annual Return:** ~30% (historical performance)  
- **Accessibility:** Easily replicable even for beginners  
- **Purpose:** Exchange of trading ideas among students  

> ⭐ **If you find this useful (e.g., for homework, research, or trading), please support by starring this repository!** 🌟🌟🌟🌟🌟🌟  

---

## Project Link

You can access the full project and its source code on GitHub:  
👉 **[FIN-Econ-FF3-Sorting-Strategy](https://github.com/Fisher669/FIN-Econ-FF3-Sorting-Strategy/)** 👈  

---

## Citation

If you use this project in your research, homework, or any other work, please make sure to **cite** it as follows:  

**BibTeX Citation Format:**

```bibtex
@misc{FIN-Econ-FF3-Sorting-Strategy,
  author = {Fisher669},
  title = {FIN-Econ-FF3-Sorting-Strategy: Trading Strategies Sorted by Earning/Market Values and Free-Cash-Flow},
  year = {2024},
  howpublished = {\url{https://github.com/Fisher669/FIN-Econ-FF3-Sorting-Strategy/}},
  note = {Accessed: [Insert Date]}
}
```

**APA Citation Format:**

> Fisher669 (2024). *FIN-Econ-FF3-Sorting-Strategy: Trading Strategies Sorted by Earning/Market Values and Free-Cash-Flow*. Retrieved from https://github.com/Fisher669/FIN-Econ-FF3-Sorting-Strategy/

By citing this work, you help support open-source development and academic exchange of ideas!  

---

## Introduction

### Motivation
1. **Why FF3 Trading Strategies?**  
   - FF3 is a widely recognized model in financial economics that incorporates three key factors: market, size, and value. It provides a robust framework for understanding excess returns.  

2. **Why Earning/Market Values (EM) and FCF for Sorting?**  
   - **EM** = 1/PE ratio (Earning/Market Share) represents the forward-looking market sentiment, while **FCF** (Free-Cash-Flow) reflects a company's internal financial health.  

3. **Why Combine EM and FCF?**  
   - Combining these two criteria helps balance market-driven expectations with fundamental financial strength.  
   - Investigating their correlation and synergy is crucial for robust portfolio selection.

---

## Model

### Data Selection

- **Source:** CSMAR (China Securities Market Analysis and Research)  
- **Date Range:** 2014-01-01 to 2023-12-31  
- **Frequency:** Monthly  
- **Coverage:** Equities, Fixed Income, Commodities, and FX  
- **Missing Data Handling:** Quarterly Rebalance so we choose to use end of Q. to impute this.

---

### Main Sorting Criteria

**1. Earning/Market values (EM):**  
   - Represents growing company probabilities.  
   - Formula:  
     *EM = Earning/Market Value*  

**2. Free-Cash-Flow (FCF):**  
   - Measures the cash flow available to investors after accounting for obligations.  
   - Formula:  
     *Total Assets - Total Liabilities*  

---

## Strategy Selection

### Why FF3?  

The FF3 model adds granularity to portfolio selection through the following factors:  
1. **Market Factor:** Captures the overall market return.  
2. **Size Factor:** Differentiates between small-cap and large-cap stocks.  
3. **Value Factor:** Identifies undervalued companies with high book-to-market ratios.  

---

## Results

This section summarizes the outcomes of the strategy selection and evaluation.  

### Metrics:

1. **Average Monthly Raw Return:**  
   - Presented in **Table 1**.  

2. **Average Monthly Return (with t-stat):**  
   - Presented in **Table 2**.  

### Ablation Test  
- **Individual Sorting:**  
  - Results for strategies sorted by **FCF** only and **EM** only.  
  - Two tables (similar format to Table 1 & 2).  

- **Combined Sorting:**  
  - Results when both **FCF** and **EM** are combined.  
  - Comparison with individual sorting performance.  

---
Here’s the full version of your **Results** section, written in English for use in your GitHub repository:

---

## Results Report

### Main Results

#### Exhibit 1: Monthly Raw Return for 25 Stock Portfolios Formed on FCF and E/M (2014-2023)

| **Earnings/Market Value (E/M) Quintile** | 1 (Low)  | 2        | 3        | 4        | 5 (High) |
|-----------------------------------------|----------|----------|----------|----------|----------|
| **FCF Quintile 1 (Low)**                | 0.0254   | 0.0180   | 0.0046   | -0.0001  | 0.0007   |
| **FCF Quintile 2**                      | 0.0141   | 0.0185   | 0.0110   | 0.0034   | 0.0003   |
| **FCF Quintile 3**                      | 0.0138   | 0.0170   | 0.0087   | 0.0060   | 0.0021   |
| **FCF Quintile 4**                      | 0.0226   | 0.0198   | 0.0091   | 0.0048   | 0.0012   |
| **FCF Quintile 5 (High)**               | 0.0238   | 0.0147   | 0.0085   | 0.0066   | 0.0033   |

#### Exhibit 2: Intercepts from Excess Stock Return Regression for 25 Stock Portfolios Formed on FCF and E/M

| **Earnings/Market Value (E/M) Quintile** | **Alpha** | **t(a)** |
|-----------------------------------------|-----------|----------|
| **FCF Quintile 1 (Low)**                | 0.0155    | 5.39     |
|                                         | 0.0084    | 2.72     |
|                                         | -0.0047   | -1.38    |
|                                         | -0.0094   | -4.77    |
|                                         | -0.0083   | -4.60    |
| **FCF Quintile 2**                      | 0.0035    | 1.82     |
|                                         | 0.0081    | 3.04     |
|                                         | 0.0016    | 0.67     |
|                                         | -0.0058   | -3.05    |
|                                         | -0.0084   | -5.69    |
| **FCF Quintile 3**                      | 0.0029    | 1.56     |
|                                         | 0.0074    | 3.44     |
|                                         | -0.0008   | -0.45    |
|                                         | -0.0032   | -2.11    |
|                                         | -0.0074   | -4.16    |
| **FCF Quintile 4**                      | 0.0126    | 4.64     |
|                                         | 0.0098    | 3.64     |
|                                         | -0.0005   | -0.24    |
|                                         | -0.0045   | -2.35    |
|                                         | -0.0077   | -4.94    |
| **FCF Quintile 5 (High)**               | 0.0142    | 6.33     |
|                                         | 0.0061    | 3.30     |
|                                         | -0.0005   | -0.25    |
|                                         | -0.0024   | -1.35    |
|                                         | -0.0056   | -2.72    |

### Additional Tests

#### (1) Independent Sorting

##### Exhibit 3: Monthly Raw Return for 25 Stock Portfolios Formed on FCF and E/M (Independent Sorting)

| **Earnings/Market Value (E/M) Quintile** | 1 (Low)  | 2        | 3        | 4        | 5 (High) |
|-----------------------------------------|----------|----------|----------|----------|----------|
| **FCF Quintile 1 (Low)**                | 0.0256   | 0.0199   | 0.0080   | -0.0012  | 0.0010   |
| **FCF Quintile 2**                      | 0.0143   | 0.0168   | 0.0069   | 0.0034   | -0.0021  |
| **FCF Quintile 3**                      | 0.0157   | 0.0127   | 0.0060   | 0.0041   | 0.0026   |
| **FCF Quintile 4**                      | 0.0227   | 0.0193   | 0.0106   | 0.0042   | 0.0013   |
| **FCF Quintile 5 (High)**               | 0.0209   | 0.0223   | 0.0137   | 0.0071   | 0.0051   |

##### Exhibit 4: Intercepts from Excess Stock Return Regression for 25 Stock Portfolios Formed on FCF and E/M (Independent Sorting)

| **Earnings/Market Value (E/M) Quintile** | **Alpha** | **t(a)** |
|-----------------------------------------|-----------|----------|
| **FCF Quintile 1 (Low)**                | 0.0155    | 4.77     |
|                                         | 0.0104    | 3.24     |
|                                         | -0.0013   | -0.38    |
|                                         | -0.0103   | -5.46    |
|                                         | -0.0081   | -4.88    |
| **FCF Quintile 2**                      | 0.0038    | 1.99     |
|                                         | 0.0068    | 2.63     |
|                                         | -0.0026   | -1.27    |
|                                         | -0.0056   | -3.57    |
|                                         | -0.0105   | -6.74    |
| **FCF Quintile 3**                      | 0.0051    | 3.05     |
|                                         | 0.0033    | 1.55     |
|                                         | -0.0032   | -1.78    |
|                                         | -0.0054   | -3.40    |
|                                         | -0.0067   | -3.07    |
| **FCF Quintile 4**                      | 0.0128    | 4.56     |
|                                         | 0.0094    | 4.32     |
|                                         | 0.0007    | 0.33     |
|                                         | -0.0052   | -2.95    |
|                                         | -0.0077   | -4.90    |
| **FCF Quintile 5 (High)**               | 0.0109    | 4.05     |
|                                         | 0.0136    | 5.11     |
|                                         | 0.0050    | 2.83     |
|                                         | -0.0019   | -1.12    |
|                                         | -0.0038   | -2.23    |

#### Reverse Test

##### Exhibit 5: Monthly Raw Return for 25 Stock Portfolios Formed on FCF and E/M (Reverse Sorting)

| **FCF Quintile**                        | **1 (Low)** | **2**     | **3**     | **4**     | **5 (High)** |
|-----------------------------------------|-------------|-----------|-----------|-----------|--------------|
| **E/M Quintile 1 (Low)**                | 0.0233      | 0.0141    | 0.0141    | 0.0191    | 0.0237       |
| **E/M Quintile 2**                      | 0.0206      | 0.0174    | 0.0121    | 0.0167    | 0.0228       |
| **E/M Quintile 3**                      | 0.0094      | 0.0059    | 0.0062    | 0.0106    | 0.0137       |
| **E/M Quintile 4**                      | -0.0009     | 0.0037    | 0.0031    | 0.0042    | 0.0075       |
| **E/M Quintile 5 (High)**               | 0.0005      | 0.0006    | 0.0006    | 0.0030    | 0.0065       |

##### Exhibit 6: Intercepts from Excess Stock Return Regression for 25 Stock Portfolios Formed on FCF and E/M (Reverse Sorting)

| **Free Cash Flow (FCF) Quintile**      | **Alpha** | **t
|----------------------------------------|-----------|----------|
| **E/M Quintile 1 (Low)**               | 0.0098    | 3.34     |
|                                        | 0.0030    | 1.03     |
|                                        | -0.0014   | -0.50    |
|                                        | -0.0044   | -1.67    |
|                                        | -0.0061   | -2.88    |
| **E/M Quintile 2**                     | 0.0043    | 2.56     |
|                                        | 0.0033    | 1.94     |
|                                        | -0.0029   | -1.49    |
|                                        | -0.0044   | -2.26    |
|                                        | -0.0075   | -3.91    |
| **E/M Quintile 3**                     | 0.0016    | 1.03     |
|                                        | 0.0008    | 0.44     |
|                                        | -0.0036   | -2.06    |
|                                        | -0.0049   | -3.13    |
|                                        | -0.0062   | -3.41    |
| **E/M Quintile 4**                     | 0.0060    | 2.85     |
|                                        | 0.0024    | 1.15     |
|                                        | -0.0020   | -1.07    |
|                                        | -0.0039   | -2.17    |
|                                        | -0.0055   | -3.29    |
| **E/M Quintile 5 (High)**              | 0.0050    | 2.74     |
|                                        | 0.0070    | 3.78     |
|                                        | 0.0040    | 2.12     |
|                                        | -0.0010   | -0.57    |
|                                        | -0.0024   | -1.36    |

---

You can now copy and paste this into your GitHub repository. If you need further refinements or adjustments, feel free to let me know!

---

## Conclusion

This project demonstrates the utility of sorting trading strategies using **FF3 factors** combined with **EM** and **FCF**. The results show that this approach can achieve notable returns in the Chinese STSE stock market.  

Whether you're a student, researcher, or investor, this repository serves as a foundation for exploring FF3-based trading strategies.  

---

> **Acknowledgements:**  
This project is for academic purposes only and is intended to foster idea exchange among students.  

**Star this repo if you found it helpful!** 🌟

