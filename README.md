# Applied Decision Science Portfolio  
### Uncertainty-Aware Modeling and Human-in-the-Loop Systems

## Overview

I am an applied decision scientist building uncertainty-aware forecasting and decision support systems for high-stakes, data-scarce environments. I specialize in Bayesian modeling, inventory analytics, and human-in-the-loop workflows across regulated domains such as biotech and healthcare.

My work emphasizes principled modeling, honest failure analysis, and designing analytical systems that make automated inference workflows reliable under uncertainity.

## Design Philosophy

Most data science portfolios optimize for predictive accuracy in static benchmark settings. My work instead focuses on **decision-grade reliability** in real operational environments characterized by sparse data, nonstationarity, and asymmetric failure costs.

Across projects, I design systems that:
- Explicitly model uncertainty rather than collapsing it into point predictions
- Encode operational constraints into decision rules
- Intentionally throttle automation when model confidence is insufficient
- Integrate human oversight as a first-class component of the system
- Treat model failure as a diagnostic signal about system structure, not a defect to be hidden

This perspective is informed by experience in regulated domains where false confidence, silent failure, and automation bias carry real-world consequences.

## Project 1 — Decision-Aware Stochastic Consumption Forecasting

This project explores stochastic inventory forecasting under severe covariate scarcity using Poisson–Gamma conjugacy and a waste-constrained restocking policy.

It demonstrates both a principled Bayesian modeling approach and the structural limits of automated forecasting in nonstationary, human-driven consumption systems.

**Key contributions:**
- Exposure-normalized Poisson–Gamma modeling of consumption rates  
- Closed-form posterior predictive forecasting via Negative Binomial distributions  
- Monte Carlo decision policy optimizing reorder quantities under waste constraints  
- Rolling-origin evaluation under regime shifts  
- Formal falsification of automation viability under nonstationarity  

**Artifacts:**
- 📄 Methods Note (PDF): [https://thefifthpostulate.github.io/projects/stochastic-forecasting.html](https://thefifthpostulate.github.io/projects/stochastic-forecasting.html)  
- 📊 Analysis Notebook: [https://thefifthpostulate.github.io/Stochastic-Consumption-Forecasting/InventoryProject.html](https://thefifthpostulate.github.io/Stochastic-Consumption-Forecasting/InventoryProject.html)
- 💻 Source Code: Available upon request 

**Key takeaway:**  
Uncertainty modeling revealed the true complexity of the consumption process. Assumptions about the stochastic process and decision rule were insufficient to consistently provide decision-grade forecasts, making expert oversight more reliable than fully automated inventory control.

## Project 2 — Geometry-Based Risk Modeling for Safe ML Inference in Medical Diagnostic Triage

This project develops a safety-aware diagnostic inference system on the Breast Cancer Wisconsin dataset that explicitly models and intercepts failure modes in probabilistic classifiers.
Rather than optimizing for overall accuracy, the system introduces a **post-classification reliability layer** that detects high-risk predictions using geometry-derived signals and routes them to human review, enforcing a **zero–false-negative constraint** in clinically ambiguous regions.
The core contribution is a selective inference control system that extracts additional risk signals from the information geometry of class-conditional feature manifolds, enabling reliable automation in the presence of deep class overlap and overconfident model failures.

**Key contributions:**
- Geometry-derived risk signals that expose hidden false-negative failure modes beyond model probabilities
- Selective inference policy that enforces zero false negatives via principled abstention
- Reliability layer decoupled from the base classifier, enabling controllable human-in-the-loop deployment
- Bootstrap-validated decision thresholds for stability under retraining and sampling uncertainty
- Quantitative analysis of automation–review tradeoffs in safety-critical inference

**Artifacts:**
- 📄 Methods Note (PDF): (link)
- 📊 Analysis Notebook / Demo: [https://thefifthpostulate.github.io/Geometric-Risk-Modeling/geometric_risk_modeling.html](https://thefifthpostulate.github.io/Geometric-Risk-Modeling/geometric_risk_modeling.html)
- 💻 Source Code: Available upon request

**Key takeaway:**
By explicitly modeling geometric failure modes and enforcing selective abstention, this system transforms a high-performance classifier into a controllable decision system with principled human oversight, illustrating a general framework for deploying machine learning safely in high-stakes environments.

## Contact

Jithakrishna Prakash  
📧 [jprakashoff@gmail.com](mailto:jprakashoff@gmail.com)  
🔗 LinkedIn: [https://linkedin.com/in/jithakrishna-prakash](https://linkedin.com/in/jithakrishna-prakash)  
💻 GitHub: [https://github.com/TheFifthPostulate](https://github.com/TheFifthPostulate)
