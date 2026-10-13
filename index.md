---
layout: default
title: He Zhuoyan | Data Science Portfolio
---

# Hi, I'm He Zhuoyan

**Aspiring Data Analyst | Data Science & Business Analytics | Data Visualization**

I have a background in accounting and business, and I am developing skills in data science and analytics. I enjoy turning complex data into clear, meaningful stories, investigating patterns, and exploring how models perform beyond their training datasets.

## About Me

My interests include predictive modeling, exploratory data analysis, data visualization, and the intersection of business questions and technical methods. I value reproducible analysis and transparent communication of model limitations.

## Technical Skills

| Area | Tools & Techniques |
| --- | --- |
| Programming | Python, SQL |
| Data analysis | Pandas, NumPy, exploratory data analysis |
| Machine learning | scikit-learn, linear regression, model evaluation |
| Visualization | Matplotlib, data storytelling |
| Other | Excel, GitHub, Jupyter Notebook |

## Featured Project

### House Price Prediction: Model Performance and Residual Diagnostics

**Why compare these models?** More complex models can capture nonlinear relationships, but added flexibility can also make them fit patterns that do not hold for new observations. Comparing a simple baseline with a polynomial model shows why predictive performance must be judged on unseen data—not training fit alone.

**Research question:** How accurately can basic housing attributes predict house prices, and what can held-out prediction errors reveal about model limitations? Does a more complex polynomial Ridge model generalize better than linear regression?

**Project status:** Ongoing — reproducible demonstration with **synthetic housing data**.

### Key results at a glance

| Model | Training R² | Test R² ↑ | Test MAE ↓ |
| --- | ---: | ---: | ---: |
| Linear regression (baseline) | 0.881 | **0.885** | **$71,992** |
| Polynomial Ridge (degree 3) | **0.897** | 0.870 | $75,581 |

*Metrics are from one train/test split of 600 synthetic homes. MAE is the average absolute prediction error in US dollars; higher test R² and lower test MAE indicate better performance.*

**Main finding:** Although the polynomial Ridge model fits the training data more closely, the simpler linear regression performs better on the held-out test set. In this demonstration, **greater complexity does not translate into better generalization**. This is consistent with an overfitting concern, although the results of one split do not establish how every future dataset would behave.

### Visual evidence

<div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,280px),1fr));gap:1.25rem;align-items:start;margin:1rem 0 1.5rem;">
  <div style="min-width:0;border:1px solid #d6e0e8;border-radius:12px;padding:12px;background:#f8fafc;">
    <img src="images/actual_vs_predicted.png" alt="Actual versus predicted house prices for linear regression and polynomial Ridge models on synthetic test data" style="display:block;width:100%;height:auto;border-radius:6px;" />
    <p style="font-size:0.92rem;margin:0.8rem 0 0;"><strong>Figure 1 — Actual vs. predicted.</strong> Compare each model's predicted prices against the observed synthetic prices. Greater distance from the ideal prediction line means larger prediction errors.</p>
  </div>
  <div style="min-width:0;border:1px solid #d6e0e8;border-radius:12px;padding:12px;background:#f8fafc;">
    <img src="images/residual_diagnostics.png" alt="Residuals against predicted prices for linear regression and polynomial Ridge models on synthetic test data" style="display:block;width:100%;height:auto;border-radius:6px;" />
    <p style="font-size:0.92rem;margin:0.8rem 0 0;"><strong>Figure 2 — Residual diagnostics.</strong> Residuals reveal where prediction errors vary with fitted prices, helping assess whether a model may be less reliable for some price ranges.</p>
  </div>
</div>

### Limitations and next steps

**Key limitation:** This project uses artificially generated data (**600 synthetic homes**), not actual property transactions. The findings **cannot be generalized to real housing markets**. Important real-world factors such as geographic location, school quality, and changes in market conditions are not represented.

**[View the project repository on GitHub](https://github.com/ZorinaHo/Data-science-project)**

## What's Next

- Explore model behavior across different price ranges.
- Investigate additional features and validation strategies.
- Replace synthetic data with an appropriately licensed real-world dataset if available.

---

*Thanks for visiting my portfolio!*
