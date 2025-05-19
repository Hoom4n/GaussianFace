# GaussianFace: Gaussian Mixture Models for Face Generation

Welcome to **GaussianFace**! This project investigates Gaussian Mixture Models (GMMs), blending theoretical exploration with practical applications to generate human-like faces using the Labeled Faces in the Wild (LFW) dataset. While the results don’t yet compete with state-of-the-art generative models like GANs, they provide meaningful insights into GMMs’ potential for creative tasks.

*Note:* If you experience issues viewing this notebook on GitHub, you can view it online via <a href="https://colab.research.google.com/github/hoom4n/GaussianFace/blob/main/GaussianFace.ipynb">Google Colab</a> or <a href="https://nbviewer.org/github/hoom4n/GaussianFace/blob/main/GaussianFace.ipynb"> NB Viewer</a>

---

## Project Overview
This repository features a detailed Jupyter notebook organized into three main sections:

1. **Theoretical Foundations of GMMs**  
   - Core concepts in probability and statistics, including likelihood estimation and multivariate Gaussian distributions.  
   - A clear explanation of the GMM algorithm, detailing latent variables, data likelihood, and the Expectation-Maximization (EM) process.  

2. **Practical Applications with Scikit-Learn**  
   - Implementation of GMMs on the Iris dataset, visualized in 2D using t-SNE, with a comparison of original and GMM-predicted labels.  
   - Analysis of model attributes like parameters, convergence and covariance structures.  
   - Soft and Hard clustering with GMM, plus strategies to simplify model with `covariance_type`.  
   - Anomaly detection via Density Estimation and visualization of outliers.  
   - Find the optimal number of clusters with BIC and AIC metrics.  

3. **Face Generation with GMMs**  
   - Application of GMMs to the LFW dataset for generating artificial faces.  
   - Use of PCA for dimensionality reduction to streamline computation.  
   - Training on representative subsets identified by K-Means clustering.  
   - Experiments with GMMs to generate faces, exploring how number of gaussians affect overfitting and output quality.  
   - Improved results by focusing GMM training on clusters of similar faces from K-Means.  

---

## Key Findings
- Training GMMs on smaller, cohesive subsets of similar faces enhances image quality with fewer components.  
- **Impact of Components**: Increasing the `n_components` hyperparameter adds more parameters, causing the model to learn finer details from the training set. This results in generated faces that resemble the source data too closely at high component counts.
- **LFW Challenges**: The LFW dataset’s variability—different lighting, exposures, backgrounds, and features like mustaches—complicates the identification of “similar images” for both GMMs and K-Means clustering.
- **GMM Limitations**: GMMs may not be ideal for image generation, as images often don’t align with the *mixture of Gaussians* assumption underlying the model.
- **Value of the Approach**: Despite these challenges, using statistical modeling like GMMs to synthesize faces is a compelling concept. It lays a foundation for understanding modern, state-of-the-art image generation techniques that build on similar probabilistic ideas.

---

## Motivation
This project stemmed from a curiosity to stretch GMMs beyond their usual scope and test their generative capabilities. By integrating theory with hands-on experimentation—using Linear Projection for efficiency and K-Means for data curation—I’ve uncovered both the strengths and limits of GMMs. The faces may not be flawless, but they mark an exciting step in probabilistic modeling.
