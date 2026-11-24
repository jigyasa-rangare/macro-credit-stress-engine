# Second-Line (2LoD) Macro-to-Credit Risk Transmission & Stress-Testing Engine

**Live Interactive Stress Simulator:** https://macro-credit-stress-engine.streamlit.app/  
**Data Sources:** Reserve Bank of India (RBI DBIE Sectoral Credit Deployment & Index of Industrial Production, 2007–2026)

---

### Executive Risk Summary
* **Causal Policy Impact (Difference-in-Differences):** Evaluated the RBI's November 2023 risk-weight tightening (+25% risk weight on unsecured retail loans & NBFCs) against secured housing loans (`2022–2026`). Identified a **-6.57 percentage point** causal slowdown in unsecured credit expansion ($p = 0.028$ with HC3 robust errors; $p = 0.182$ under Newey-West HAC accounting for overlapping YoY autocorrelation).
* **Segment Risk Heterogeneity (Panel Fixed Effects):** Across 20 years of longitudinal RBI data (`2007–2026`), Credit Card Outstanding exhibited the highest pro-cyclical expansion (**23.19% mean YoY growth**, $\sigma = 10.94\%$) compared to secured Housing Loans (**16.50%**, $\sigma = 7.22\%$).
* **Second-Line (2LoD) Monte Carlo Stress Engine:** Built a 2,000-path Monte Carlo Expected Loss ($EL = PD \times LGD \times EAD$) simulator with automated **Red/Amber/Green Key Risk Indicators (KRIs)** tied to Risk Appetite Framework (RAF) boundaries.

---

### Repository Structure
* `app.py` — Interactive Streamlit Second-Line Stress-Testing & KRI Dashboard.
* `requirements.txt` — Python dependencies for Streamlit Community Cloud deployment.
* `01_RBI_Data_Cleaning.ipynb` — Longitudinal ETL pipeline, Panel Fixed-Effects Distributed Lag model, DiD policy evaluation, and Newey-West HAC diagnostics.
