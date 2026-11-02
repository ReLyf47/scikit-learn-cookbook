# 🚀 Scikit-Learn Mastery: A Learning Journey

This repository is a hands-on learning archive built around the scikit-learn cookbook. Instead of treating the examples as a one-to-one copy, each notebook is reframed as a guided learning module: the code is adjusted, the terminology is clarified, and each section ends with reflection notes to reinforce understanding.

The goal is simple: move from "I can run the example" to "I understand why the model works, how the parameters affect behavior, and how the workflow fits into a real ML pipeline."

## 📚 Naming convention

To make the project easier to navigate, each notebook follows a consistent naming pattern:

`chapter_XX_<topic>.ipynb`

This keeps the structure clear and makes it easier to browse the learning path in order.

## 🧭 Learning path

| Standardized module | Repository file | Topic | Focus |
|---|---|---|---|
| `chapter_01_api_foundations.ipynb` | `Chapter_01_sklearn_api.ipynb` | API Foundations | Core scikit-learn API, estimator patterns, and model workflows |
| `chapter_02_preprocessing.ipynb` | `Chapter_02_preprocessing.ipynb` | Data Cleaning & Preprocessing | Missing values, scaling, encoding, and feature preparation |
| `chapter_03_dimensionality_reduction.ipynb` | `Chapter_03_Dimensionality_Reduction.ipynb` | Feature Compression | PCA and dimensionality reduction strategies |
| `chapter_04_distance_metrics_knn.ipynb` | `Chapter_04_Distance_Metrics_KNN.ipynb` | Similarity-Based Models | KNN, distance metrics, and neighborhood behavior |
| `chapter_05_linear_models_regularization.ipynb` | `Chapter_05_Linear_Models_Regularization.ipynb` | Linear Regression & Regularization | Ridge, Lasso, and regularization trade-offs |
| `chapter_06_logistic_regression.ipynb` | `Chapter_06_Logistic_Regression.ipynb` | Advanced Logistic Regression | Classification foundations and model interpretation |
| `chapter_07_svm_kernel_methods.ipynb` | `Chapter_07_SVM_Kernel_Methods.ipynb` | SVM & Kernel Tricks | Support vectors, kernels, and margin maximization |
| `chapter_08_tree_based_algorithms.ipynb` | `Chapter_08_tree_based_algorithms.ipynb` | Tree-Based Ensembles | Decision trees, random forests, and boosting intuition |

> The repository currently includes these notebooks in the main project root. The table above reflects the intended uniform naming convention for future cleanup and organization.

## 🧪 How to use this repository

1. Start with `chapter_01_api_foundations.ipynb` and work through the notebooks in order.
2. Read the narrative sections before running code cells, especially when a new concept is introduced.
3. Re-run experiments with modified hyperparameters to observe how model behavior changes.
4. Use the reflection sections to summarize what the algorithm is doing and why it matters.
5. Treat this repo as a guided study path rather than a simple example dump.

## 🎯 What makes this repo different

This is not a direct copy of the original cookbook. Each notebook was intentionally adapted to support deeper learning:

1. **Variable refactoring**: Standard textbook labels like `X` and `y` were replaced with more expressive names such as `features` and `target`.
2. **Hyperparameter variation**: Parameters such as `random_state`, `test_size`, and `k_neighbors` were changed to encourage experimentation.
3. **API modernization**: Where appropriate, notebook code uses `make_pipeline()` and other idiomatic scikit-learn patterns.
4. **Reflective structure**: Each notebook integrates theory spotlights and final reflections to promote synthesis rather than memorization.
5. **Learning-first organization**: The sequence is designed to build intuition incrementally from foundational concepts to more advanced models.

## 📌 Suggested next steps

- Add missing notebooks to complete the full cookbook journey.
- Standardize all filenames to the `chapter_XX_<topic>.ipynb` convention.
- Add a short summary section inside each notebook explaining the concept, expected output, and key takeaways.
- Include a small project roadmap or checklist for learners who want to track progress.

This repository is best used as a structured study path for understanding scikit-learn through experimentation, reflection, and concept-building.
