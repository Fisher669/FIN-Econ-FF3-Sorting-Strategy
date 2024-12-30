# FIN-Econ-FF3-Sorting-Strategy

## Overview

**FIN-Econ FF3 Chinese Sorting Trading Strategies To Select Portfolios**  

This program is part of a course project for **FIN ECON**, demonstrating a trading strategy that leverages the **Fama-French three-factor model (FF3)**, sorted by **Expected Market Return (EM)** and **Free-Cash-Flow (FCF)**.  

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
  title = {FIN-Econ-FF3-Sorting-Strategy: Trading Strategies Sorted by EM and Free-Cash-Flow},
  year = {2024},
  howpublished = {\url{https://github.com/Fisher669/FIN-Econ-FF3-Sorting-Strategy/}},
  note = {Accessed: [Insert Date]}
}
```

**APA Citation Format:**

> Fisher669 (2024). *FIN-Econ-FF3-Sorting-Strategy: Trading Strategies Sorted by EM and Free-Cash-Flow*. Retrieved from https://github.com/Fisher669/FIN-Econ-FF3-Sorting-Strategy/

By citing this work, you help support open-source development and academic exchange of ideas!  

---

## Introduction

### Motivation
1. **Why FF3 Trading Strategies?**  
   - FF3 is a widely recognized model in financial economics that incorporates three key factors: market, size, and value. It provides a robust framework for understanding excess returns.  

2. **Why EM and FCF for Sorting?**  
   - EM (Expected Market Return) represents the forward-looking market sentiment, while FCF (Free-Cash-Flow) reflects a company's internal financial health.  

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
- **Missing Data Handling:** Imputed with a dynamic interpolation strategy  

---

### Main Sorting Criteria

**1. EM (Expected Market Return):**  
   - Represents the weighted sum of expected returns for all assets in the market portfolio.  
   - Formula:  
     *Market Return × Total Market Capitalization*  

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

## Strategy Workflow

Here are the main steps of the program:  

1. **Data Preprocessing:**  
   - Clean and standardize raw financial data.  
   - Handle missing values and outliers.  

2. **Strategy Selection:**  
   - Implement FF3 factor-based portfolio sorting.  
   - Sort by **EM**, **FCF**, or a combination.  

3. **Strategy Evaluation:**  
   - Measure performance using historical data.  

4. **Strategy Backtesting:**  
   - Simulate historical performance to validate the strategy.  

5. **Strategy Optimization:**  
   - Fine-tune parameters for improved returns.  

6. **Strategy Deployment:**  
   - Deploy and monitor the strategy in real-time.  

---

## Conclusion

This project demonstrates the utility of sorting trading strategies using **FF3 factors** combined with **EM** and **FCF**. The results show that this approach can achieve notable returns in the Chinese STSE stock market.  

Whether you're a student, researcher, or investor, this repository serves as a foundation for exploring FF3-based trading strategies.  

---

> **Acknowledgements:**  
This project is for academic purposes only and is intended to foster idea exchange among students.  

**Star this repo if you found it helpful!** 🌟
