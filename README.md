## 📚 Background & Acknowledgments

This repository is built upon the foundational code examples provided in *Using R for Item Response Theory Model Applications* (Paek & Cole, 2019). The original scripts have been extensively refactored and extended to optimize performance and include new functionalities suited for modern analysis workflows.

### 📖 Recommended Reading
For those interested in the theoretical underpinnings and technical documentation of the methods used in this repository:

* **Official Documentation:** For comprehensive details on function arguments and package capabilities, strictly refer to the [mirt package documentation on CRAN](https://cran.r-project.org/web/packages/mirt/index.html).
* **Estimation Methods (CML vs. MML):** For a detailed comparison between Conditional Maximum Likelihood (CML) and Marginal Maximum Likelihood (MML) estimators, please refer to Bartolucci & Scrucca (2010).
* **General IRT Framework:** Chapter 4 of *Modern Psychometrics with R* (Mair, 2018) provides an excellent overview of Item Response Theory applications in R.

### 🧩 Scalability to Advanced Models (Chapter 4)

The architecture of these scripts is designed to be modular. While the templates focus on Unidimensional Polytomous/Dichotomous models, the workflow can be easily adapted for the advanced applications described in **Chapter 4** of Paek & Cole (2019), such as:
* **Mixed-Format Data** (Dichotomous + Polytomous items).
* **Multiple-Group Analysis** (DIF & Equating).
* **Fixed Item Parameter Calibration (FIPC).**
* **Latent Regression.**

**Note:** For these cases, the primary adjustment required is within the **Model Specification & Estimation** step (e.g., defining `model` syntax or grouping variables). The subsequent diagnostics, fit statistics, and plotting pipelines remain largely applicable. For detailed theoretical guidance on these specific configurations, please refer directly to Chapter 4 of the book.


### 🌐 Multidimensional IRT Modeling (Chapter 5)

The analysis pipeline is fully compatible with Multidimensional Item Response Theory (MIRT), assuming that more than one latent trait underlies the item responses. Following the framework in **Chapter 5**, the code supports:

* **Between-Item Multidimensionality (Simple Structure):** Where items cluster to measure specific dimensions (e.g., items 1-10 measure Dimension A, items 11-20 measure Dimension B).
* **Within-Item Multidimensionality (Cross-loading):** Where specific items are indicators for more than one trait simultaneously.
* **High-Dimensional Data:** Scalable applications to complex constructs (e.g., 8+ dimensions) using both dichotomous (Rasch, 2PL, 3PL) and polytomous (PCM, GPCM, GRM) models.

**Note:** Transitioning to multidimensional models primarily requires updating the **Model Specification** syntax (e.g., specifying `F1 = 1-10`, `F2 = 11-20`, `COV = F1*F2`). The core estimation engine (`mirt`) and the majority of the diagnostic plots provided in these scripts remain applicable and effective.
---

### 🔗 References

* **Bartolucci, F., & Scrucca, L. (2010).** Point Estimation Methods with Applications to Item Response Theory Models. *Computational Statistics & Data Analysis*. [DOI: 10.1016/B978-0-08-044894-7.01376-2](https://doi.org/10.1016/B978-0-08-044894-7.01376-2)
* **Chalmers, R. P. (2012).** mirt: A Multidimensional Item Response Theory Package for the R Environment. *Journal of Statistical Software*, 48(6), 1–29. [DOI: 10.18637/jss.v048.i06](https://doi.org/10.18637/jss.v048.i06)
* **Mair, P. (2018).** Item Response Theory. In: *Modern Psychometrics with R*. Use R!. Springer, Cham. [DOI: 10.1007/978-3-319-93177-7_4](https://doi.org/10.1007/978-3-319-93177-7_4)
* **Paek, I., & Cole, K. (2019).** *Using R for Item Response Theory Model Applications* (1st ed.). Routledge. [DOI: 10.4324/9781351008167](https://doi.org/10.4324/9781351008167)
