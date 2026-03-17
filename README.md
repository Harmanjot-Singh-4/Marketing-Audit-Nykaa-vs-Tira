💄 Marketing Performance Audit: Nykaa vs. Tira
Student’s T-Tests, James-Stein Estimators, & Monte Carlo Simulations

📌 Project Overview
This repository contains a comprehensive audit of 50,000+ marketing campaigns comparing two major beauty retailers: Nykaa and Tira. The project moves beyond basic descriptive statistics to answer a fundamental business question: Is one brand structurally outperforming the other, or is the observed difference merely statistical noise?

🛠️ Technical Stack
Data Manipulation: Pandas, NumPy

Statistical Analysis: SciPy (Hypothesis Testing)

Bayesian Modeling: James-Stein Estimators (Tango Method)

Simulation: Monte Carlo Random Walks (10,000 iterations)

Visualization: Matplotlib, Seaborn

🔬 Core Methodology
1. Hypothesis Testing (The Baseline)
Before diving into complex models, I established a statistical baseline.

Levene’s Test: Used to check for equal variance between the two brands.

Student’s T-Test: Since equal variance was confirmed, a standard T-test was applied to ROI.

Result: A p-value of 0.1487 was found, meaning we fail to reject the null hypothesis. The ROI difference is not statistically significant.

2. True Skill vs. Luck (Bayesian Shrinkage)
To rank the top 10 channel combinations, I used the James-Stein Estimator. This "shrinks" raw observed ROI toward the brand average to remove the impact of "lucky" high-performing outliers.

The Halo Effect: In the visualizations, the faint outer circles (Observed ROI) represent raw data, while the solid inner dots represent the "True Skill" level.

3. Monte Carlo Forecasting
I simulated 10,000 future scenarios to determine the probability of one brand dominating the other in CTR, ROI, and Conversions.

The results show a nearly 50/50 win probability, visually represented by "Simulation Branches" that track cumulative wins over time.

📊 Key Visualizations
CTR Comparison: A "zoomed-in" look at click-through rates.

Lead Waste Analysis: Identifying which brand is more efficient at converting leads.

Duration Optimization: Finding the "sweet spot" (e.g., 25s or 10s ads) for maximum performance.

Simulation Branches: A random walk visualization of 10,000 competitive scenarios.

🏃 How to Run
Clone the repo: git clone https://github.com/YOUR_USERNAME/Marketing-Audit-Nykaa-vs-Tira

Install dependencies: pip install pandas numpy scipy matplotlib seaborn

Run the Notebook: Open Project(Marketing Campaign Datasets).ipynb and run all cells.

🏁 Conclusion
The audit reveals that Nykaa and Tira are in a state of high-equilibrium competition. While raw numbers might suggest a leader, the Student's T-test and Monte Carlo simulations prove that neither brand has a statistically significant "moat" yet. The James-Stein analysis identifies specific channel mixes (like Email, YouTube, Facebook) as the most reliable drivers for long-term growth.
