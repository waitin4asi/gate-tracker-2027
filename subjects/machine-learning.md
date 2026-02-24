# 🤖 Machine Learning (DA Paper)

![Weightage](https://img.shields.io/badge/Weightage-8–12%20marks%20(DA)-red)
![Priority](https://img.shields.io/badge/Priority-Very%20High%20(DA)-red)

---

## 📋 Topic Checklist

### 🔷 Foundations
- [ ] Types of ML: supervised, unsupervised, semi-supervised, reinforcement learning
- [ ] Training, validation, and test sets
- [ ] Bias-variance tradeoff
- [ ] Overfitting and underfitting
- [ ] Regularization: L1 (Lasso), L2 (Ridge), Elastic Net
- [ ] Cross-validation: k-fold, leave-one-out (LOOCV)
- [ ] Feature engineering and feature selection

### 🔷 Supervised Learning — Regression
- [ ] Linear regression — least squares estimation
- [ ] Multiple linear regression
- [ ] Polynomial regression
- [ ] Ridge and Lasso regression
- [ ] Logistic regression — sigmoid function, binary and multi-class
- [ ] Maximum Likelihood Estimation (MLE)

### 🔷 Supervised Learning — Classification
- [ ] Decision trees — entropy, information gain, Gini impurity
- [ ] Random forests — bagging
- [ ] Naive Bayes classifier — Bayes theorem, class conditional independence
- [ ] k-Nearest Neighbors (k-NN)
- [ ] Support Vector Machines (SVM) — hyperplane, margin, kernel trick
  - [ ] Hard margin vs soft margin
  - [ ] Kernel functions: linear, polynomial, RBF/Gaussian
- [ ] Perceptron learning rule
- [ ] Multi-layer perceptron (MLP)

### 🔷 Unsupervised Learning
- [ ] k-Means clustering — algorithm, convergence, limitations
- [ ] Hierarchical clustering — agglomerative, divisive
- [ ] DBSCAN (density-based)
- [ ] Gaussian Mixture Models (GMM) and EM algorithm
- [ ] Principal Component Analysis (PCA) — dimensionality reduction
- [ ] Singular Value Decomposition (SVD)
- [ ] Autoencoders (basics)

### 🔷 Neural Networks
- [ ] Neuron model — activation function, weights, bias
- [ ] Activation functions: Sigmoid, Tanh, ReLU, Leaky ReLU, Softmax
- [ ] Feedforward neural networks
- [ ] Backpropagation — chain rule for gradients
- [ ] Gradient descent variants: Batch, SGD, Mini-batch
- [ ] Optimizers: Momentum, RMSProp, Adam
- [ ] Vanishing/exploding gradient problem
- [ ] Batch normalization, Dropout
- [ ] Convolutional Neural Networks (CNNs) — convolution, pooling, filters
- [ ] Recurrent Neural Networks (RNNs) — sequence modeling, LSTM, GRU

### 🔷 Evaluation Metrics
- [ ] Confusion matrix: TP, TN, FP, FN
- [ ] Accuracy, Precision, Recall, F1-score
- [ ] ROC curve and AUC
- [ ] Mean Squared Error (MSE), RMSE, MAE
- [ ] R² (coefficient of determination)
- [ ] Log loss / cross-entropy loss

### 🔷 Optimization
- [ ] Gradient descent — learning rate, convergence
- [ ] Convex and non-convex optimization
- [ ] Local vs global minima
- [ ] Stochastic vs batch optimization

### 🔷 Model Selection & Validation
- [ ] Bias-variance decomposition
- [ ] Learning curves
- [ ] Hyperparameter tuning: grid search, random search, Bayesian optimization
- [ ] Ensemble methods: bagging, boosting, stacking
- [ ] AdaBoost, Gradient Boosting, XGBoost (conceptual)

---

## ⚡ Key Formulas

### Linear Regression
```
ŷ = Xβ
β = (X^T X)⁻¹ X^T y   (Ordinary Least Squares)

MSE = (1/n) Σ (yᵢ − ŷᵢ)²
```

### Logistic Regression
```
σ(z) = 1 / (1 + e^(-z))   (sigmoid)
P(y=1|x) = σ(w^T x + b)

Loss (binary cross-entropy): -[y log(ŷ) + (1-y) log(1-ŷ)]
```

### Decision Tree Entropy
```
Entropy: H(S) = -Σ pᵢ log₂(pᵢ)
Information Gain: IG(S,A) = H(S) - Σ (|Sᵥ|/|S|) H(Sᵥ)
Gini Impurity: G(S) = 1 - Σ pᵢ²
```

### Naive Bayes
```
P(C|x) ∝ P(C) × Π P(xᵢ|C)
```

### SVM
```
Decision boundary: w^T x + b = 0
Margin = 2/||w||
Maximize margin ↔ Minimize ||w||²/2 subject to yᵢ(w^T xᵢ + b) ≥ 1
```

### PCA
```
1. Center the data (subtract mean)
2. Compute covariance matrix Σ
3. Compute eigenvectors and eigenvalues of Σ
4. Project data onto top-k eigenvectors (principal components)
Variance explained by component = λᵢ / Σλ
```

### Evaluation Metrics
```
Accuracy = (TP + TN) / (TP + TN + FP + FN)
Precision = TP / (TP + FP)
Recall = TP / (TP + FN)
F1 = 2 × (Precision × Recall) / (Precision + Recall)
```

### Bias-Variance Tradeoff
```
Expected error = Bias² + Variance + Irreducible noise

High bias → underfitting (model too simple)
High variance → overfitting (model too complex)
```

---

## ❌ Common Mistakes

| Mistake | Correct Understanding |
|---|---|
| High accuracy = good model | Consider class imbalance — use F1, AUC instead |
| More features = better | Feature selection prevents overfitting |
| Gradient descent always converges | Only guaranteed for convex functions; use adaptive LR |
| Cross-entropy = MSE | Cross-entropy for classification; MSE for regression |
| SVM only for linear separation | Kernel trick enables non-linear boundaries |
| k-NN requires training phase | k-NN is lazy learner — no explicit training |

---

## 📊 PYQ Frequency Analysis (GATE DA)

| Topic | Frequency | Marks Range |
|---|:---:|:---:|
| Supervised learning (regression/classification) | Very High | 2–4 |
| Neural networks / backpropagation | High | 2–3 |
| Evaluation metrics | High | 1–2 |
| Clustering algorithms | High | 1–2 |
| PCA / dimensionality reduction | Medium | 1–2 |
| SVM | Medium | 1–2 |
| Bayes / Naive Bayes | High | 1–2 |

---

## 🎯 Confidence Tracker

| Topic | Confidence | Last Revised |
|---|:---:|---|
| Linear/Logistic Regression | ☐ Low / ☐ Med / ☐ High | |
| Decision Trees / Random Forest | ☐ Low / ☐ Med / ☐ High | |
| SVM | ☐ Low / ☐ Med / ☐ High | |
| Neural Networks | ☐ Low / ☐ Med / ☐ High | |
| Clustering | ☐ Low / ☐ Med / ☐ High | |
| PCA / Dimensionality Reduction | ☐ Low / ☐ Med / ☐ High | |
| Evaluation Metrics | ☐ Low / ☐ Med / ☐ High | |
