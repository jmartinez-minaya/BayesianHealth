BayesianHealth: Bayesian Inference for health using JAGS, brms and INLA
==============
This is a 15-hour course designed for students, researchers, and professionals in the field of statistics who want to begin their journey into Bayesian inference and deepen their understanding of its application to healthcare-related problems. Using advanced tools like R-INLA and inlabru, the course provides a solid foundation in Bayesian hierarchical modeling and culminates with comprehensive applications in spatial statistics, including disease mapping and geostatistical modeling.

# Course Structure (15 Hours)

## Part I: Bayesian Inference. An introduction and applications in health

### Unit 1: An introduction to Bayesian inference

- **1. A bit of history**: Introduction to the origins of Bayesian inference, including key developments and notable contributors. Examples such as the United Kingdom aviation case and the transatlantic flight. Application in evaluating diagnostic tests.
- **2. Bayesian approach**: Overview of the Bayesian paradigm, focusing on prior beliefs, posterior distributions, and how data updates beliefs.
  - Examples/S1-BI_beta_binomial: beta-binomial conjugate prior. An application to intracerebral hemorrhage.
- **3. Predictions**: How Bayesian inference is used for making predictions, including predictive distributions and uncertainty quantification.

---

## Part II: Bayesian GLMs and Hierarchical Models using MCMC methods and INLA

### Unit 2: Bayesian Computation and Mixed models

- **1. Bayesian computation. MCMC methods**: Introduction to Markov Chain Monte Carlo (MCMC) methods, focusing on their role in Bayesian computation, and discussing key algorithms like Metropolis-Hastings.
- **2. Bayesian Software**: Overview of popular software for implementing MCMC methods, including JAGS and Stan, with a focus on practical considerations and healthcare applications.
  - Examples/S2-JAGS-heart_attack: JAGS for logistic regression models. The case of heart attacks.
  - Examples/S2-brms-heart_attack: brms for logistic regression models. The case of heart attacks.
  - Exercises/S2-diabetes: Exercise for studying diabetes using JAGS and brms.
- **3. Hierarchical Bayesian Models for Mixed Models**: Introduction to hierarchical Bayesian models, focusing on their application in mixed models for healthcare data. Examples include random intercepts and slopes, as well as variability across hierarchical levels.
  - Exercises/S1-diabetes: Exercise for studying diabetes using brms and including random effects.



### Unit 3: Hierarchical Bayesian Models and INLA Methodology

- **1. Hierarchical Bayesian Models with INLA**
  - Overview of hierarchical Bayesian models.
  - Advantages of INLA over MCMC for efficiency and accuracy.

- **2. Elements to understand how INLA works**


- **3. Putting all the pieces together: INLA**
  - Key steps of the INLA methodology.
  - Efficient posterior approximation for latent Gaussian models.

- **4. Implementation in `R-INLA`**


- **5. Model Selection**
  - Using DIC and WAIC for model comparison.

- **6. Examples**
  - Examples/S2-INLA-rain
  - Examples/S2-INLA-measurement_agreement_COPD

---

## Part III: INLA Methodology and Spatial Statistics 

### Unit 4: Bayesian Spatial Statistics 

- **Introduction to Spatial statistics**
- **Types of Spatial Data**
- **Disease mapping**
  - Examples/S3-INLA-disease-mapping: an example of disease mapping in oral cancer in the Valencian Region.
- **Geostatistics**
  - Examples/S3-inlabru-geostatistics: an example of malaria prevalence in Mozambique.
- **PC-priors**


---


# Bibliography
1. Bachl, F. E., Lindgren, F., Borchers, D. L., & Illian, J. B. (2019). *inlabru: An R package for Bayesian spatial modelling from ecological survey data*. Methods in Ecology and Evolution, 10(6), 760-766. DOI: 10.1111/2041-210X.13168.
2. Blangiardo, M., & Cameletti, M. (2015). *Spatial and Spatio-temporal Bayesian Models with R-INLA*. Wiley.
3. Broemeling, L. D. (2013). *Bayesian Methods in Epidemiology*. Chapman and Hall/CRC.
4. Gelman, A., Carlin, J. B., Stern, H. S., Dunson, D. B., Vehtari, A., & Rubin, D. B. (2013). *Bayesian Data Analysis* (3rd ed.). Chapman and Hall/CRC.
5. Gómez-Rubio, V. (2020). *Bayesian Inference with INLA*. CRC Press.
6. Krainski, E., Gómez-Rubio, V., Bakka, H., Lenzi, A., Rue, H., & Lindgren, F. (2019). *Advanced Spatial Modeling with Stochastic Partial Differential Equations Using R and INLA*. Chapman and Hall/CRC.
7. Lawson, A. B. (2018). *Bayesian Disease Mapping: Hierarchical Modeling in Spatial Epidemiology* (3rd ed.). CRC Press.
8. Lesaffre, E., & Lawson, A. B. (2012). *Bayesian Biostatistics*. Chapman & Hall/CRC Biostatistics Series.
9. Martínez-Beneito, M. A., & Botella-Rocamora, P. (2019). *Disease Mapping: From Foundations to Multidimensional Modeling*. CRC Press.
10. Moraga, P. (2019). *Geospatial Health Data: Modeling and Visualization with R-INLA and Shiny*. Chapman and Hall/CRC.
11. Moraga, P. (2021). *Handbook of Spatial Epidemiology and Disease Modeling: Applications with R*. CRC Press.
12. Rue, H., Martino, S., & Chopin, N. (2009). *Approximate Bayesian Inference for Latent Gaussian Models by Using Integrated Nested Laplace Approximations*. Journal of the Royal Statistical Society: Series B (Statistical Methodology), 71(2), 319-392.

# Software

To take full advantage of the course, it is necessary that everyone has the following programs installed:

- version 4.4.1 of [R](https://www.r-project.org/) or posterior, and
- [RStudio](https://www.rstudio.com/products/rstudio/download/), or
- [Quarto](https://quarto.org/docs/get-started/), or
- [Visual Studio Code](https://code.visualstudio.com/download)
- [JAGS](https://mcmc-jags.sourceforge.io/)


# R packages

This will be the packages required for the course

```r
install.packages(pkgs = c("sf", "spdep", "lattice", "latticeExtra", "viridis", 
                          "gridExtra", "RColorBrewer", "INLA", "ggthemes", 
                          "leaflet", "ggplot2", "dplyr", "inlabru", "rnaturalearth", 
                          "patchwork", "runjags", "brms", "inlabru"))

```

The R-INLA package can be downloaded directly from the webpage https://www.r-inla.org/download-install

```r
### --- INLA --- ###
install.packages("INLA",repos=c(getOption("repos"),INLA="https://inla.r-inla-download.org/R/stable"), dep=TRUE)
```

Also, other packages from Bioconductor
```r
BiocManager::install(c("graph", "Rgraphviz"), dep=TRUE)
```



