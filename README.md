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

## Contact

Jithakrishna Prakash  
📧 [jprakashoff@gmail.com](mailto:jprakashoff@gmail.com)  
🔗 LinkedIn: [https://linkedin.com/in/jithakrishna-prakash](https://linkedin.com/in/jithakrishna-prakash)  
💻 GitHub: [https://github.com/TheFifthPostulate](https://github.com/TheFifthPostulate)
