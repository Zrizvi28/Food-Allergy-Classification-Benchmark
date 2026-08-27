# Food Allergy Classification Benchmark

Evaluating an immune transcriptomic foundation model for food allergy classification against conventional machine-learning baselines.

## Research Question:
Can EVA, a pretrained immune bulk RNA-seq foundation model, improve food allergy classification compared with conventional transcriptomic pipelines?

## Approach:
Using public bulk RNA-seq data, this project compares
- EVA foundation-model embeddings
- conventional expression-based features
- LASSO feature selection
- pathway-informed features
- PCA
- linear classifiers and SVMs

## Results:
The classical SelectKBest + PCA + Logistic Regression baseline was the only approach to produce a statistically significant result, with an AUC of approximately 0.69–0.75 and p ≈ 0.01–0.02.
Other approaches were non-significant, including EVA, hybrid, ssGSEA, LASSO, and DESeq2 + SVM.
A properly cross-validated model using the nine DESeq2-significant genes performed at approximately AUC = 0.495, near chance.
These results do not demonstrate that EVA improves food allergy classification over conventional methods in this dataset.

## Takeaway:
A pretrained immune foundation model did not provide a clear advantage over a simple classical baseline in this small food allergy classification task. Possible contributing factors include a weak allergy signal (considering this project evaluated rna-seq data from naive CD4 cells for a disease that is particularly heterogenous and lacks prominent biomarkers) and the small cohort size (n=48). The result illustrates why foundation models should be evaluated against strong conventional baselines rather than assumed to improve performance because of their complexity, specifically when it comes to food allergy or similar diseases and small cohorts.

## Status:
Completed exploratory benchmark

Author: Zamin Abbas Rizvi
