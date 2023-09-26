# Evaluating Collaborative Forecasting in Non-Horizontal Federated Learning
## Abstract
Federated Learning (FL) is a privacy-preserving and decentralized machine learning approach that requires attention in collaborative forecasting problems when parties do not share the same input feature space. Computing a global AI model by joining parties' models that differ in architecture and input space prompts us to consider evaluating the predictive variability in collaborative forecasting.  In collaborative prognostics, where multiple condition monitoring systems enhance the machinery's useful lifetime forecast, our approach begins by partitioning turbofan engine sensor signals from the C-MAPSS dataset among different parties. Utilizing  Vertical Asynchronous Federated Learning (VAFL) algorithm, we successfully address the Federated Learning experiment through two architectures: Multilayer Perceptron followed by a Kalman Filter (MLP-KF) and Functional Multilayer Perceptron (FMLP). In the final step, we assessed multiple models per party by repeating the experiment for each architecture and used appropriate key metrics to compare prediction variability among parties and experiments. The evaluation revealed that FMLP outperformed MLP-KF, providing more stable and reproducible predictions.

## How to use
This repository contains the code to reproduce the results of using Functional Multilayer Perceptron (FMLP) and Multilayer Perceptron followed by a Kalman Filter (MLP-KF) in estimating the Remaining Useful Life (RUL) of turbofan engines. This RUL estimation is performed in a Federated Learning scenario with vertical data partitioning. 

Since each party aims to improve the RUL estimation collaboratively, the RUL prediction error is evaluated globally and locally. Metrics such as Mean Absolute Error (MAE) and Roor Mean Squared Error (RMSE) are used to evaluate the RUL estimation performed by global AI models. On the other hand, metrics such as Overall Average Bias (OAB), Overall Average Variability (OAV) and Reproducibility are used to evaluate the Health Indicator (normalized RUL) estimation among the parties models. 

We refer to multiple global AI models because the federated optimization problem was repeated ten times. The predictions of these federated experiments were saved in the Predictions.xlsx file of the data/predictions folder for FMLP and MLP-KL architectures. 

This Predictions.xlsx file has to be loaded in the Calculate Experimental Results.mlx Matlab Live Script to reproduce the estimation error of these experiments. 

To reproduce the federated optimization problem using FMLP and MLP-KF architectures, the following Lives Scripts must be reproduced:
VFL - FMLP.mlx
VFL - MLP-KF.mlx
It will save a .xlsx file with the estimation results. 
