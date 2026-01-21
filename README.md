# Fundamental Machine Learning – Research Projects

This repository contains small-scale, hypothesis-driven experiments focused on fundamental properties of deep learning models. The projects emphasize understanding model behavior, representation structure, and failure patterns rather than optimizing benchmark performance.

## Projects

### 1. Representation Stability under Input Perturbations
Study of how convolutional representations change under controlled Gaussian noise. Representation drift is analyzed across network depth using cosine similarity to understand robustness and sensitivity to input perturbations.

### 2. Pooling-Induced Information Loss
Controlled comparison of max pooling and average pooling to analyze their effect on feature variance and information preservation. The study highlights invariance–information trade-offs introduced by architectural design choices.

### 3. Failure Mode Analysis of Vision Models
Systematic analysis of misclassifications in a pretrained vision model to identify structured and recurring failure modes. Errors are manually categorized into dominant causes such as scale-related effects, background bias, and occlusion, revealing non-random model weaknesses beyond aggregate accuracy metrics.

Each project is implemented as a self-contained notebook with accompanying analysis, explicit assumptions, and documented limitations.
