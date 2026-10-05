# 🚀 Scikit-Learn Mastery: A Learning Journey

This repository is a comprehensive reproduction of the *scikit-learn Cookbook*, restructured as a series of learning modules. I have modified the original implementations to avoid direct duplication and to better understand the impact of different hyperparameters and variable structures.

## 🛠️ The Learning Path

### 🟦 Phase 1: The Foundations
- **Module 01: API Foundations** (Estimators & Pipelines)
- **Module 02: Data Cleaning** (Imputation & Scaling)
- **Module 03: Feature Compression** (PCA & LDA)

### 🟩 Phase 2: Supervised Learning
- **Module 04: Similarity Models** (KNN & Distance Metrics)
- **Module 05: Linear Tuning** (Ridge, Lasso, ElasticNet)
- **Module 06: Advanced Logistic** (Multi-label/Multiclass)
- **Module 07: SVM & Kernels** (Non-linear Separation)
- **Module 08: Tree Ensembles** (Random Forest & Boosting)

### 🟨 Phase 3: Specialized Domains & Unsupervised
- **Module 09: NLP Basics** (TF-IDF & Text Classifiers)
- **Module 10: Clustering** (K-Means, DBSCAN, GMM)
- **Module 11: Anomaly Detection** (Isolation Forest, One-Class SVM)

### 🟥 Phase 4: Validation & Production
- **Module 12: Evaluation Frameworks** (Nested CV & Diagnostics)
- **Module 13: MLOps & Deployment** (Serialization & Monitoring)

## 🎓 Methodology
To ensure this was a learning process and not just a copy, I implemented the following changes:
1. **Variable Refactoring**: renamed standard textbook variables (X, y) to more descriptive names (features, target).
2. **Hyperparameter Variation**: Modified `random_state`, `test_size`, and `k-neighbors` values across all modules.
3. **API Shifts**: Transitioned from `Pipeline()` constructors to `make_pipeline()` where appropriate.
4. **Structural Overhaul**: Added "Theory Spotlights" and "Final Reflections" to each notebook to synthesize the learning.
