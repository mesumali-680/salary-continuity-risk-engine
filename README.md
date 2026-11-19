# Salary Continuity Risk Engine
 
A prototype risk-scoring engine for salary-linked lending. For any customer wallet at any point in time, it predicts the probability that **salary keeps arriving on the wallet for each of the next 1–6 months (M1–M6)**, assigns a **risk bucket**, and gives a **reason code** for high-risk cases.
 
Built as a technical assessment of my capabilities during my internship, and shared with permission. The notebook was reviewed by an AI engineer at the company and revised based on their feedback. It was **not used in production**, the project was a test of my machine learning engineering skills.
 
All data is **synthetic**: it mirrors the structure of production payroll and card tables but contains no real customers, employers or wallets.
 
---
 
## Summary
 
The loans in scope are repaid from salary landing on the customer's wallet, so the key risk is **whether that salary keeps arriving**. The objective was to:
 
- Predict salary continuity for each of the next 1–6 months, with consistent probabilities across horizons.
- Explain high risk with a reason category (employer disruption, employment stop, diversion, visa/EID issues).
- Handle cold-start cases (new employers and new employees).
- Validate the model on historical data before any go-live decision.
  
A historical repayment simulation was out of scope for this phase.
