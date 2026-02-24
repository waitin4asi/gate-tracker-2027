# 🧠 Machine Learning / Artificial Intelligence

> **Weightage (DA paper):** ~8–12% | **Avg Questions:** 5–8 | **Importance:** ⭐⭐⭐⭐⭐

---

## 📊 Overview

ML/AI is increasingly important for GATE DA and is gaining weight. The questions test conceptual understanding, not implementation. Focus on algorithms, assumptions, math behind models, and evaluation metrics.

---

## ✅ Topic-wise Checklist

### 📊 Supervised Learning

**Classification:**
- [ ] Decision Trees: ID3/C4.5, information gain, Gini impurity
- [ ] Naive Bayes: conditional independence assumption, Bayes' theorem application
- [ ] K-Nearest Neighbors (KNN): distance metrics, bias-variance in k
- [ ] Support Vector Machines (SVM): hyperplane, margin, kernel trick
- [ ] Logistic Regression: sigmoid function, cross-entropy loss
- [ ] Neural Networks: perceptron, multilayer, backpropagation (basics)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

**Regression:**
- [ ] Linear Regression: least squares, normal equation, gradient descent
- [ ] Polynomial Regression: overfitting with high degree
- [ ] Ridge (L2) and Lasso (L1) Regression: regularization effects
- [ ] Bias-Variance Tradeoff
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔍 Unsupervised Learning
- [ ] K-Means Clustering: algorithm, convergence, initialization (k-means++)
- [ ] Hierarchical Clustering: agglomerative, dendrogram
- [ ] DBSCAN: density-based, handles outliers
- [ ] Principal Component Analysis (PCA): dimensionality reduction, variance maximization
- [ ] Autoencoders (overview)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🧬 Neural Networks & Deep Learning
- [ ] Artificial Neuron: weights, bias, activation function
- [ ] Activation functions: sigmoid, tanh, ReLU, softmax
- [ ] Multilayer Perceptron (MLP)
- [ ] Backpropagation algorithm
- [ ] Gradient descent variants: batch, stochastic, mini-batch
- [ ] Overfitting prevention: dropout, batch normalization (conceptual)
- [ ] Convolutional Neural Networks (CNN): overview
- [ ] Recurrent Neural Networks (RNN): overview, LSTM concept
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 📏 Evaluation Metrics
- [ ] Confusion matrix: TP, TN, FP, FN
- [ ] Accuracy, Precision, Recall, F1-Score
- [ ] ROC curve and AUC
- [ ] Cross-validation: k-fold, leave-one-out
- [ ] Train/validation/test split
- [ ] Mean Squared Error (MSE), RMSE, MAE for regression
- [ ] R-squared (coefficient of determination)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🔧 Feature Engineering
- [ ] Feature scaling: normalization (min-max), standardization (z-score)
- [ ] Feature selection: filter, wrapper, embedded methods
- [ ] Handling missing values: imputation strategies
- [ ] Encoding categorical variables: one-hot, label encoding
- [ ] Dimensionality reduction: PCA, LDA
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

### 🤖 Artificial Intelligence
- [ ] Search algorithms: BFS, DFS, UCS, A*, greedy best-first
- [ ] Informed vs. uninformed search
- [ ] Heuristics, admissibility, consistency (A*)
- [ ] Game playing: minimax, alpha-beta pruning
- [ ] Constraint Satisfaction Problems (CSP)
- [ ] Markov Decision Processes (MDP): states, actions, rewards, policy
- [ ] Value iteration, policy iteration (DP methods)
- [ ] Q-Learning (reinforcement learning basics)
- **Confidence:** ⬜ Low | ⬜ Medium | ⬜ High

---

## 📋 Key Formulas

### Information Theory (for Decision Trees)
```
Entropy: H(S) = -Σ pᵢ log₂(pᵢ)
Information Gain: IG(S,A) = H(S) - Σ (|Sᵥ|/|S|) H(Sᵥ)
Gini Impurity: G(S) = 1 - Σ pᵢ²
```

### Regression
```
Linear regression: ŷ = Xβ, β = (XᵀX)⁻¹Xᵀy  [Normal equation]
MSE = (1/n) Σ(yᵢ - ŷᵢ)²
RMSE = √MSE
R² = 1 - SS_res/SS_tot = 1 - Σ(yᵢ-ŷᵢ)² / Σ(yᵢ-ȳ)²
Ridge: minimize ||y - Xβ||² + λ||β||²
Lasso: minimize ||y - Xβ||² + λ||β||₁
```

### Naive Bayes
```
P(C|x₁,...,xₙ) ∝ P(C) × Π P(xᵢ|C)
Classification: argmax_C P(C) × Π P(xᵢ|C)
```

### Evaluation Metrics
```
Accuracy = (TP + TN) / (TP + TN + FP + FN)
Precision = TP / (TP + FP)  [of predicted positives, how many are correct]
Recall = TP / (TP + FN)     [of actual positives, how many were found]
F1 = 2 × (Precision × Recall) / (Precision + Recall)
```

### K-Means
```
Algorithm:
1. Initialize k centroids (randomly or k-means++)
2. Assign each point to nearest centroid
3. Update centroids as mean of assigned points
4. Repeat 2-3 until convergence (assignments don't change)
```

---

## ⚠️ Common Mistakes

1. **Bias-Variance:** High bias = underfitting; High variance = overfitting. You want both low!
2. **Precision vs. Recall tradeoff:** Increasing threshold → higher precision, lower recall
3. **K-Means limitations:** Assumes spherical clusters; sensitive to initialization; need to specify k
4. **SVM kernel:** Kernel trick maps to higher dimension without explicit computation
5. **Overfitting indicators:** Training accuracy >> Test accuracy; very complex model
6. **L1 vs. L2 regularization:** L1 (Lasso) produces sparse models (some weights → 0); L2 (Ridge) doesn't
7. **A* admissibility:** h(n) must never overestimate actual cost to goal
8. **Gradient descent learning rate:** Too high → diverge; too low → slow convergence

---

## 📈 PYQ Frequency Analysis (GATE DA)

| Topic | Frequency |
|-------|-----------|
| Classification algorithms (Decision Tree, SVM) | Every year |
| Evaluation metrics | Every year |
| Linear/Logistic Regression | Most years |
| K-Means clustering | Most years |
| Neural Networks basics | Most years |
| Reinforcement Learning (MDP) | Increasing |

---

## 📚 Resources

- **Primary:** Hands-On Machine Learning — Aurélien Géron (Scikit-Learn + Keras)
- **Theory:** Pattern Recognition & ML — Bishop
- **Online:** Andrew Ng Machine Learning Specialization (Coursera, free audit)
- **AI:** Artificial Intelligence: A Modern Approach — Russell & Norvig
- **Video:** StatQuest (YouTube) — best ML explanations

---

## 📅 PYQ Progress Tracker

- [ ] GATE DA 2021 solved
- [ ] GATE DA 2022 solved
- [ ] GATE DA 2023 solved
- [ ] GATE DA 2024 solved
- [ ] GATE DA 2025 solved
- [ ] GATE DA 2026 solved

---

*Updated: ___ | Revision Count: ___*
