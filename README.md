# Bayesian Analysis of Supervision Effects in Resistance Training

## Project Overview

This project applies Bayesian statistical modeling to analyze resistance training and evaulate whether supervision plays a role in training performance. The study was completed as part of an independent study focused on Bayesian statistics and focuses on applying probabilistic modeling analysis to real-world training data.

The goal of the analysis was to determine the effect of supervised and unsupervised training using Bayesian inference while accounting for variation across individuals and environments.

The project uses hierarchical Bayesian mmodels and Markov Chain Monte Carlo (MCMC) sampling to estimate posterior distributions for the measured training metrics in the study.

## Data Description

### Historical Dataset
- ~11,500 observations
- Data from multiple clinics
- used to establish prior distirbutiions for the experimental study

The historical dataset was used to develop informative prior distributions for the Bayesian model. These priors were then applied to the experimental dataset to develop improved posterior distributions, resulting in more precision in the evaluation of the effect of supervision on training performance.

### Experimental Dataset
- ~270 observations
- 45 members across strength clinics
- used to develop posterior distributions evaluating the supervision effect

The experimental dataset was used to evaluate the effect of supervision on training perfomance across sessions by analyzing the posterior distributions after the Markov Chain Monte Carlo sampling.

### Metrics of Measurement 
The study focused on three primary measures to determine the potential positive or negative influence that supervision could have on training performance.

- Time Under Load (TUL) : Represents the total duration under stress a trainee maintained their working muscle for the given set.
- Rating of Perceived Effort (RPE) : A subjective scale measuring the intensity a trainee would exert on a given set.
- Rating of Perceived Discomfort (RPD) : A subjective scale measuring discomfort a trainee experienced on a given set.

## Statistical Methods

The study implements a Bayesian hierarchical modeling framework to estimate performance variation between supervised and unsupervised training.

### Bayesian Inference
Model Parameters are estimated as probability distributions as opposed to fixed values. Posterior distributions represent the uncertainty around these parameter estimates using credible intervals.

### Hierarchical Modeling
Model accounts for variation across individual members, training machines, and clininc locations, allowing the model to capture the natural variability in real-world training performance. 

### Student-t likelihood
A Student-t distribution was used to model performance outcomes due to its robustness to outliers.

### Hurdle Model
A hurdle model was used to model the probability of trainees stopping exactly at the 120s TUL reccomended cap regardless of achieving muscular failure.

### Markov Chain Monte Carlo (MCMC)
Posterior distributions were estimated using Hamiltonian Monte Carlo sampling with adequate chains and iterations to ensure convergence and stability in results.

## Key Findings
Evaluation of the historical dataset showed minimal differences between supervised and unsupervised training. The differences in estimated TUL values were close enough to zero; practically suggesting to difference, whilst also the credible intervals contained zero, further suggesting no clear effect.

However, evaluation of the experimental dataset suggested that TUL had improved by ~20 seconds on average under supervision. A possible reason for this difference between the historical and experimetal data could be an underlying behavioral effect in the experimental trainees given they knew they were part of a study, leading to overall greater perfomance. 

## Tools
- R
- Bayesian Statistical Modeling
- Markov Chain Monte Carlo
- Data visualizations for prior and posterior distributions

## Purpose
This project was developed to gain practical experience implementing Bayesian statistical techniques on real-world performance data. The study ultimately shows how probailistic Bayesian modeling techniques can be implemented to quantify uncertainty, use prior information, and analyze training performance.
As complementary to its statistical focus, the project also reflects a personal interest in fitness performance, motivating the application of data science methods to domains in fitness analytics and exercise science.


## Full Report
The complete independent project containing all detailed process, analysis, model specification, visualizations, and reslts can be found in the report.
