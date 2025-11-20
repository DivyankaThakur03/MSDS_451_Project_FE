# NVIDIA Directional Timing Strategy

**Author:** Divyanka Thakur  
**Institution:** Northwestern University  
**Date:** November 2025

---

## Project Summary

This project evaluates whether a machine learning-based directional timing strategy for NVIDIA (NVDA) stock is commercially viable as an active ETF fund.

**Conclusion:** The strategy is **NOT viable** and should NOT be launched. It consistently underperformed buy-and-hold across all validation methods.

---

## Key Results

| Validation Method | Result | Status |
|-------------------|--------|--------|
| Historical Test (2020-2024) | Captured 23% of buy-hold returns | FAIL |
| Monte Carlo (500 scenarios) | 38.8% win rate | FAIL |
| Walk-Forward (14 folds) | 14.3% win rate, Sharpe -0.058 | FAIL |

**Bottom Line:** Strategy failed all 5 viability criteria. Market timing destroys value for high-growth stocks.

---

## Repository Structure

```
├── README.md                          # This file
├── term_paper.md                      # Final term paper
├── checkpoints/
│   ├── checkpoint_a/                  # Baseline development
│   ├── checkpoint_b/                  # Feature enhancement
│   └── checkpoint_c/                  # Validation (Monte Carlo, Walk-Forward)
├── presentation/
│   ├── slides.pdf
│   └── recording.mp4
```

---

## Methodology

**Model:** XGBoost classifier with 9 features (technical indicators + macro context: VIX, S&P 500, Treasury yields)

**Trading Rule:** If predict UP → 100% NVDA; If predict DOWN → 100% T-Bills (2%)

**Validation:**
1. **Checkpoint A:** Baseline model, identified class imbalance
2. **Checkpoint B:** Added features, tested binary allocation (2020-2024)
3. **Checkpoint C:** Monte Carlo (500 scenarios) + Walk-Forward (14 folds)

---

## Why It Failed

1. **Regime adaptation failure** - Model trained on crashes (2000-2019) couldn't anticipate AI boom (2023-2024)
2. **Binary switching too extreme** - Missing rallies more costly than avoiding crashes
3. **Fundamental asymmetry** - For growth stocks, cost of being out >> benefit of being defensive

---

## Management Recommendation

**Launch Decision:** NO - Do not pursue this business opportunity

**Personal Investment:** $0 - Would buy-and-hold NVDA instead

**Employment:** Would only work as researcher to improve strategy, not as fund manager

**Wealth Building:** Use passive strategies, not this fund

---

## Technical Stack

**Language:** Python 3.8+  
**Key Libraries:** pandas, numpy, scikit-learn, xgboost, imblearn, matplotlib, seaborn  
**Data:** Yahoo Finance (NVDA, SPY, VIX, TNX) 2000-2025

---

## GenAI Tools

**Tool:** Claude 3.5 Sonnet (Anthropic)

**Usage:**
- Report writing assistance (structure and synthesis)

**What GenAI did NOT do:**
- Design trading strategy
- Run simulations or generate results
- Make business decisions

All research design, analysis, and recommendations are human-authored.

---

## Key References

- Grinold & Kahn (2000) - *Active Portfolio Management*
- Lo (2019) - *Adaptive Markets*
- López de Prado (2018) - *Advances in Financial Machine Learning*


---

**Last Updated:** November 2025 | **Status:** Final Submission ✅
