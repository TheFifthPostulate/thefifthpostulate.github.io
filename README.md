# Applied Decision Science Portfolio  
### Uncertainty-Aware Modeling and Human-in-the-Loop Systems

## Overview

I am an applied decision scientist building uncertainty-aware forecasting and decision support systems for high-stakes, data-scarce environments. I specialize in Bayesian modeling and human-in-the-loop workflows across regulated domains such as biotech and healthcare.

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
- Methods Note (PDF): [https://thefifthpostulate.github.io/projects/stochastic-forecasting.html](https://thefifthpostulate.github.io/projects/stochastic-forecasting.html)  
- Analysis Notebook: [https://thefifthpostulate.github.io/Stochastic-Consumption-Forecasting/InventoryProject.html](https://thefifthpostulate.github.io/Stochastic-Consumption-Forecasting/InventoryProject.html)
- Source Code: Available upon request 

**Key takeaway:**  
Uncertainty modeling revealed the true complexity of the consumption process. Assumptions about the stochastic process and decision rule were insufficient to consistently provide decision-grade forecasts, making expert oversight more reliable than fully automated inventory control.

## Project 2 — Evidence Geometry  

### An Interpretable Evidence-Based Risk Modeling Framework  

Evidence Geometry is an experimental framework for interpretable risk modeling in classification problems.
Instead of producing a single probability score, it decomposes model predictions into structured evidence signals that reveal how risk emerges in the data.

The framework transforms heterogeneous features into a **unified log-likelihood ratio evidence space, allowing risk to be analyzed geometrically**.

**Repository**  

**GitHub Repo**  
[https://github.com/TheFifthPostulate/evidence-geometry/tree/main](https://github.com/TheFifthPostulate/evidence-geometry/tree/main)
  
**Example Notebooks**  
  
**Breast Cancer Wisconsin**  
[https://thefifthpostulate.github.io/evidence-geometry/bcw_analysis.html](https://thefifthpostulate.github.io/evidence-geometry/bcw_analysis.html)
  
**Cleveland Heart Disease**  
[https://thefifthpostulate.github.io/evidence-geometry/heartdisease_analysis.html](https://thefifthpostulate.github.io/evidence-geometry/heartdisease_analysis.html)
  
### Core Idea

Each feature contributes log-likelihood ratio evidence:

log p(x_i \| positive class) − log p(x_i \| negative class)  
  
Stacking these contributions forms an evidence vector for each observation.

Working in this space provides several advantages:  

- heterogeneous features become comparable
- evidence accumulates additively
- population structure becomes analyzable
- case-level risk can be decomposed

This connects the framework to **classical likelihood ratio testing and Bayesian evidence accumulation**.  

### Interpretable Risk Signals

For each case, the framework computes three complementary signals in the evidence space.  

#### **Distance Contrast** (`d_dist`)  

Difference in Mahalanobis distance to the learned class manifolds.  

Measures which class distribution better explains the case.  
  
#### **Drift Projection** (`proj`)  

Projection of evidence deviations from negative class manifold onto the mean class separation direction.  

Captures net accumulation of evidence toward the positive class.  
  
#### **Eigenmode Bundle Energy** (`E_pos`)  

Energy along dominant covariance eigenmodes (principal component axes) of the positive class.  
  
Detects activation of correlated pathological feature bundles.  

### Current Status

**Prototype v0.1**  
  
Current work focuses on:  

- extending the framework to large clinical datasets (MIMIC-IV / eICU)
- exploring temporal risk signal evolution
- integrating triage policies based on evidence structure
  
## Contact

Jithakrishna Prakash  
📧 [jprakashoff@gmail.com](mailto:jprakashoff@gmail.com)  
🔗 LinkedIn: [https://linkedin.com/in/jithakrishna-prakash](https://linkedin.com/in/jithakrishna-prakash)  
💻 GitHub: [https://github.com/TheFifthPostulate](https://github.com/TheFifthPostulate)
