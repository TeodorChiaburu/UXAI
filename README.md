# Uncertainty Propagation in XAI: A Comparison of Analytical and Empirical Estimators

This repository contains the code and experiments from our paper:  
**Uncertainty Propagation in XAI: A Comparison of Analytical and Empirical Estimators** (under review)

## Overview 

Understanding Uncertainty in Explainable AI (UXAI) is essential for assessing the reliability of explanations provided by machine learning models. 
Many widely used XAI methods produce explanations that are **non-robust, unfaithful, and sensitive to perturbations**, raising concerns about their trustworthiness 
in real-world applications. This repository provides a **systematic framework for quantifying and analyzing uncertainty in explanations**, focusing on how 
perturbations in input and model parameters propagate through different XAI methods.  

We compare two fundamental approaches:  
1. **Empirical uncertainty estimation** via **Monte Carlo sampling**, where multiple perturbed explanations are generated and their covariance is computed.  
2. **Analytical uncertainty estimation** via **first-order uncertainty propagation**, using finite difference approximations of Jacobians to quantify explanation variance.  

## Key Findings 

Our experiments reveal three distinct uncertainty propagation behaviors:  
- Case 1: **Linear dependence on perturbation scale**: Some XAI methods exhibit uncertainty that scales proportionally with input noise and align well with first-order analytical approximations.  
- Case 2: **Near-zero empirical uncertainty for small perturbations**: Some methods fail to reflect small-scale variations, leading to misleadingly stable explanations.  
- Case 3: **Uncertainty plateaus below a threshold**: For certain methods, empirical uncertainty saturates below a specific noise level.  