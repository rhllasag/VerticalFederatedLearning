# Evaluating Collaborative Forecasting in Non-Horizontal Federated Learning
Federated Learning (FL) is a privacy-preserving and decentralized Machine Learning (ML) approach that typically faces forecasting challenges when parties share the same input space. In a centralized FL configuration, horizontal data partitioning enables evaluating a local model with an overall testing dataset. However, vertical or hybrid data partitioning settings require careful evaluation of collaborative forecasting, mainly when researchers aim to adopt an ML architecture that better fits the forecasting problem. It is because federated beneficiaries' data differ in feature space and models are updated using parts of the global model.  This work constructed a collaborative forecasting problem in the context of the Remaining Useful Life (RUL) estimation of turbofan engines by dividing sensor signals from the C-MAPSS dataset into multiple parties. Using the Vertical Asynchrouns Federated Learning (VAFL) algorithm, this problem was solved using two ML architectures: Multilayer Perceptron followed by a Kalman Filter (MLP-KF) and Functional Multilayer Perceptron (FMLP). In a federated network comprising four parties, we obtained 80 local models by performing federated optimization ten times using MLP-KL and FMLP, respectively. To compare the prediction performance of both ML architectures, we evaluated those local models using three key metrics: Overall Average Bias (OAB), Overall Average Variability (OAV), and Reproducibility (Rep). The evaluation showed that FMLP outperformed MLP-KL, delivering more stable and reproducible predictions.
