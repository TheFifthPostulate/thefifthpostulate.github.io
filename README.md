## Overview

I am a data analyst focused on building interpretable, uncertainty-aware analytics systems using statistical modeling and machine learning.

My work involves transforming real-world data into structured, analysis-ready datasets and developing models that remain reliable under uncertainty and dataset variability. I primarily work in healthcare and operational analytics, with experience in real-world data (RWD), EHR-based modeling, and decision-oriented analytics.

## Design Philosophy

Most data systems optimize for predictive performance on static datasets. My work instead focuses on reliability in real-world settings, where data is sparse, noisy, and operational decisions carry asymmetric risks.

Across projects, I focus on:

- modeling uncertainty explicitly rather than relying on point predictions
- designing interpretable representations and decision signals
- evaluating model behavior under changing data conditions
- incorporating human oversight where automated decisions are uncertain

## Project 1 — Evidence Geometry  

### Likelihood-Based Feature Transformation for Tabular Data 

This project explores transforming heterogeneous features into a common, comparable representation using log-likelihood ratios.

Instead of relying solely on model outputs, the approach enables **analysis of feature-level contributions and data structure in a standardized space**.  
  
### Core Idea

Each feature contributes log-likelihood ratio evidence:  

`log p(x_i | positive class) − log p(x_i | negative class)` 
  
This produces a representation where:  

- heterogeneous features become comparable
- feature contributions can be aggregated
- samples can be analyzed relative to class-specific distributions

**Derived signals:**  
- `d_dist` — relative proximity to class distributions
- `proj` — directional accumulation of feature-level deviations 

### Links
- **GitHub Repo**: [https://github.com/TheFifthPostulate/evidence-geometry/tree/main](https://github.com/TheFifthPostulate/evidence-geometry/tree/main)  
- **Breast Cancer Wisconsin Notebook**: [https://thefifthpostulate.github.io/evidence-geometry/bcw_analysis.html](https://thefifthpostulate.github.io/evidence-geometry/bcw_analysis.html)  
- **Cleveland Heart Disease**: [https://thefifthpostulate.github.io/evidence-geometry/heartdisease_analysis.html](https://thefifthpostulate.github.io/evidence-geometry/heartdisease_analysis.html)

## Project 2 — Decision-Aware Stochastic Consumption Forecasting

This project explores inventory forecasting under limited and variable data using a Bayesian approach.

Key components:
- Poisson–Gamma modeling of consumption rates
- posterior predictive forecasting (Negative Binomial)
- simulation-based decision policies for restocking
- evaluation under non-stationary demand 
  
**Artifacts:**
- Methods Note (PDF): [https://thefifthpostulate.github.io/projects/stochastic-forecasting.html](https://thefifthpostulate.github.io/projects/stochastic-forecasting.html)  
- Analysis Notebook: [https://thefifthpostulate.github.io/Stochastic-Consumption-Forecasting/InventoryProject.html](https://thefifthpostulate.github.io/Stochastic-Consumption-Forecasting/InventoryProject.html)
- Source Code: Available upon request 
  
**Takeaway:**
Explicit uncertainty modeling revealed limitations of fully automated forecasting under non-stationary conditions, highlighting the importance of human-in-the-loop decision-making.  

