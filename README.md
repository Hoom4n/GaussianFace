# GaussianFace: Gaussian Mixture Models for Face Generation

Welcome to **GaussianFace**! This project investigates Gaussian Mixture Models (GMMs), blending theoretical exploration with practical applications to generate human-like faces using the Labeled Faces in the Wild (LFW) dataset. While the results don’t yet compete with state-of-the-art generative models like GANs, they provide meaningful insights into GMMs’ potential for creative tasks.

*Notice*: Due to GitHub's rendering limitations for large notebooks, you can view the notebook online via <a href="https://colab.research.google.com/github/hoom4n/GaussianFace/blob/main/GaussianFace.ipynb">Google Colab</a> or <a href="https://nbviewer.org/github/hoom4n/GaussianFace/blob/main/GaussianFace.ipynb"> NB Viewer</a>
---

## Project Overview
This repository features a detailed Jupyter notebook organized into three main sections:

1. **Theoretical Foundations of GMMs**  
   - Core concepts in probability and statistics, including likelihood estimation and multivariate Gaussian distributions.  
   - A clear explanation of the GMM algorithm, detailing latent variables, data likelihood, and the Expectation-Maximization (EM) process.  

2. **Practical Applications with Scikit-Learn**  
   - Implementation of GMMs on the Iris dataset, visualized in 2D using t-SNE, with a comparison of original and GMM-predicted labels.  
   - Analysis of model attributes like convergence and covariance structures.  
   - Examples of soft and hard clustering, plus strategies to simplify models with `covariance_type`.  
   - Anomaly detection via `score_samples()` and visualization of outliers.  
   - Evaluation of cluster counts using BIC and AIC metrics.  

3. **Face Generation with GMMs**  
   - Application of GMMs to the LFW dataset for generating artificial faces.  
   - Use of PCA for dimensionality reduction to streamline computation.  
   - Training on representative subsets identified by K-Means clustering.  
   - Experiments with GMMs to generate faces, exploring how number of gaussians affect overfitting and output quality.  
   - Improved results by focusing GMM training on clusters of similar faces from K-Means.  

---

## Key Findings
- Training GMMs on smaller, cohesive subsets of similar faces enhances image quality with fewer components.  
- Too many components (e.g., 100) can overfit, producing faces too close to the training set.  
- Training on similar faces with 25–50 components hit a sweet spot, yielding realistic yet original faces.  

---

## Motivation
This project stemmed from a curiosity to stretch GMMs beyond their usual scope and test their generative capabilities. By integrating theory with hands-on experimentation—using Linear Projection for efficiency and K-Means for data curation—I’ve uncovered both the strengths and limits of GMMs. The faces may not be flawless, but they mark an exciting step in probabilistic modeling.
