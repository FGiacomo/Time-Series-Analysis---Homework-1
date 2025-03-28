# 📈 Time Series Analysis – Homework #1

**Date:** 2025-03-28  
**Student:** *Giacomo Fantato* - 16958

**Course:** Time Series Analysis - UW WNE  
**Assignment:** Homework #1

---

## 📂 Dataset Description

- **Source:** `CDR["Close"]["CDR.WA"]`
- **Frequency:** Business Days (`freq='B'`)
- **Period:** `[Start Date]` to `[End Date]`
- **Target Variable:** Daily closing price of CDR.WA

---

## 🧼 1. Data Preprocessing

- Converted index to `DatetimeIndex`
- Checked and handled missing values
- Ensured frequency consistency

```python
# Example
series = CDR["Close"]["CDR.WA"]
series.index = pd.DatetimeIndex(series.index)
series.index.freq = pd.infer_freq(series.index)

