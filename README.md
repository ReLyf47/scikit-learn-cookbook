# Scikit-learn Cookbook

A hands-on, chapter-by-chapter study guide to practical machine learning with
[scikit-learn](https://scikit-learn.org/). The repository contains 13 Jupyter
notebooks that move from the scikit-learn API and data preparation to model
selection, anomaly detection, and production deployment.

Each notebook combines explanations, runnable experiments, visualizations,
evaluation, and end-of-chapter takeaways. Most examples use familiar
scikit-learn datasets and carefully chosen synthetic datasets; the text
classification chapter additionally uses downloadable NLTK corpora.

## What you will learn

- How scikit-learn estimators, transformers, pipelines, and metadata work
- How to prepare numerical and categorical data without leakage
- How to reduce dimensionality and visualize high-dimensional data
- How distance metrics affect K-nearest-neighbor models
- How linear models, regularization, and logistic regression behave
- How kernels, support vectors, trees, and ensemble methods work
- How to represent and classify text with classical NLP techniques
- How to cluster data and detect outliers or novel observations
- How to use cross-validation, tuning, learning curves, and evaluation metrics
- How to serialize, validate, monitor, and deploy trained models

## Learning path

Work through the notebooks in order. Later chapters reuse ideas introduced
earlier, especially preprocessing, pipelines, scaling, and evaluation.

| Chapter | Notebook | Main topics |
|---|---|---|
| 1 | [`Chapter_01_sklearn_api.ipynb`](Chapter_01_sklearn_api.ipynb) | Estimators, `fit`/`predict`/`transform`, custom transformers, pipelines, estimator parameters, tags, and metadata routing |
| 2 | [`Chapter_02_preprocessing.ipynb`](Chapter_02_preprocessing.ipynb) | Missing values with `SimpleImputer`, `KNNImputer`, and `IterativeImputer`; scaling; encoding; `ColumnTransformer`; pipelines; polynomial features; feature selection |
| 3 | [`Chapter_03_Dimensionality_Reduction.ipynb`](Chapter_03_Dimensionality_Reduction.ipynb) | PCA, LDA, t-SNE, explained variance, scree plots, visualization, and the effect of compression on model performance |
| 4 | [`Chapter_04_Distance_Metrics_KNN.ipynb`](Chapter_04_Distance_Metrics_KNN.ipynb) | Euclidean, Manhattan, and Minkowski distance; KNN classification; decision boundaries; choosing `k`; grid search; learning curves |
| 5 | [`Chapter_05_Linear_Models_Regularization.ipynb`](Chapter_05_Linear_Models_Regularization.ipynb) | Ordinary least squares, multicollinearity, Ridge, Lasso, Elastic Net, coefficient paths, polynomial regression, and splines |
| 6 | [`Chapter_06_Logistic_Regression.ipynb`](Chapter_06_Logistic_Regression.ipynb) | Logistic probabilities and log-odds, binary and multiclass classification, One-vs-Rest, multilabel concepts, regularization, ROC curves, and classification metrics |
| 7 | [`Chapter_07_SVM_Kernel_Methods.ipynb`](Chapter_07_SVM_Kernel_Methods.ipynb) | Maximum-margin classification, support vectors, soft margins, linear/RBF/polynomial kernels, `C` and `gamma`, high-dimensional data, and SVM regression |
| 8 | [`Chapter_08_tree_based_algorithms.ipynb`](Chapter_08_tree_based_algorithms.ipynb) | Decision trees, Gini impurity, pruning and complexity control, random forests, bagging, gradient boosting, feature importance, and ensemble tuning |
| 9 | [`Chapter_09_Text_Processing_and_Multiclass_Classification.ipynb`](Chapter_09_Text_Processing_and_Multiclass_Classification.ipynb) | NLTK corpora, token counts, Bag of Words, TF-IDF, n-grams, POS tagging, Naive Bayes, logistic regression, SVM, One-vs-Rest, One-vs-One, and confusion matrices |
| 10 | [`Chapter_10_Clustering_Techniques.ipynb`](Chapter_10_Clustering_Techniques.ipynb) | K-Means and the elbow method, hierarchical clustering and dendrograms, DBSCAN and `eps` selection, cluster metrics, spectral clustering, and Gaussian mixtures |
| 11 | [`Chapter_11_novelty_outlier_detection.ipynb`](Chapter_11_novelty_outlier_detection.ipynb) | Outliers versus novelty, Isolation Forest, One-Class SVM, Local Outlier Factor, evaluation, and strategies for handling detected anomalies |
| 12 | [`Chapter_12_Cross_Validation_and_Model_Evaluation.ipynb`](Chapter_12_Cross_Validation_and_Model_Evaluation.ipynb) | K-fold and stratified validation, LOOCV, nested CV, `cross_val_score`, `cross_validate`, grid/randomized search, learning curves, and validation curves |
| 13 | [`Chapter_13_Deploying_sklearn_Models_in_Production.ipynb`](Chapter_13_Deploying_sklearn_Models_in_Production.ipynb) | Pickle and joblib persistence, batch versus single-sample inference, parallel validation, drift simulation, model metadata, versioned artifacts, pipelines, and CI/CD validation gates |

## Repository structure

All learning material currently lives in the repository root:

```text
.
├── Chapter_01_sklearn_api.ipynb
├── Chapter_02_preprocessing.ipynb
├── ...
├── Chapter_13_Deploying_sklearn_Models_in_Production.ipynb
└── README.md
```

The filenames intentionally preserve the chapter order. Names are not yet
uniform in capitalization or separators, so use the links in the learning
path rather than relying on a hypothetical renamed file.

## Getting started

### 1. Clone the repository

```bash
git clone https://github.com/ReLyf47/scikit-learn-cookbook.git
cd scikit-learn-cookbook
```

### 2. Create an environment

Python 3.10+ is recommended. The notebooks were authored with Python 3.10,
3.12, and 3.12.3 kernels, so small version-dependent differences may appear.

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
python -m pip install --upgrade pip
python -m pip install jupyterlab numpy pandas scipy scikit-learn matplotlib seaborn nltk joblib
```

### 3. Launch Jupyter

```bash
jupyter lab
```

Open `Chapter_01_sklearn_api.ipynb` and continue in chapter order. The
notebooks also include Google Colab badges where applicable.

### 4. Download the text corpora

Chapter 9 downloads the required NLTK resources in the notebook. If you want
to prepare them manually, run:

```python
import nltk

for resource in [
    "movie_reviews",
    "reuters",
    "brown",
    "punkt",
    "punkt_tab",
    "averaged_perceptron_tagger_eng",
    "stopwords",
]:
    nltk.download(resource)
```

## How to study with the notebooks

1. Read the explanation and stated learning goals before running the code.
2. Run cells from top to bottom so datasets, pipelines, and fitted models are
   created in the intended order.
3. Change one parameter at a time—such as `k`, `alpha`, `C`, `gamma`,
   `n_components`, or `n_clusters`—and compare the resulting metrics and
   visualizations.
4. Pay attention to train/test boundaries. Fit imputers, scalers, encoders,
   selectors, and dimensionality-reduction steps on training data only; use a
   pipeline when the transformation belongs with a model.
5. Finish each chapter's summary and key-learnings section, then revisit the
   earlier chapters when a later notebook introduces a connected concept.

## Important implementation notes

- Results can vary with package versions, random seeds, BLAS implementations,
  and platform-specific floating-point behavior.
- Chapter 2 demonstrates why preprocessing must be fitted only on training
  data to avoid leakage.
- Distance-based methods, SVMs, linear models, and many optimization
  procedures are sensitive to feature scale; the relevant notebooks compare
  scaled and unscaled workflows.
- t-SNE is primarily used here for visualization. Its coordinates are not
  intended to be a stable feature representation for production prediction.
- Text experiments depend on NLTK corpora and may take longer than the
  small tabular examples.
- Serialized models should only be loaded from trusted sources. Keep the
  training environment and dependency versions recorded alongside artifacts.
- The production chapter demonstrates deployment concepts locally; it does not
  provision a cloud service or web API.

## Datasets and techniques at a glance

The notebooks use built-in scikit-learn datasets such as Iris, Wine, Digits,
Breast Cancer, and Diabetes, plus generated classification, regression,
clustering, and anomaly-detection data. Chapter 9 additionally uses NLTK's
Movie Reviews, Reuters, and Brown corpora.

Across the full path, the repository demonstrates:

```text
Data preparation -> feature engineering -> dimensionality reduction
                 -> supervised and unsupervised learning
                 -> validation and tuning -> persistence and monitoring
```

## Contributing and experimenting

This is a learning-focused repository, so experimentation is encouraged:

- Add a short explanation when introducing a new technique.
- Keep examples reproducible with explicit random states where appropriate.
- Prefer pipelines when preprocessing and modeling must travel together.
- Report more than a single accuracy number when class imbalance or regression
  error makes another metric more informative.
- Preserve the chapter sequence and link new notebooks from this README.

## License and attribution

This repository is an adapted, learning-oriented collection of scikit-learn
cookbook material. See the upstream references and licensing information
associated with the original source material before redistributing notebook
content.
