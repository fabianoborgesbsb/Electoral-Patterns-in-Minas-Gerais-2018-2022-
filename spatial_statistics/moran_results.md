# Global Moran's I Results

## Spatial Autocorrelation Analysis

To evaluate whether voting patterns exhibited spatial dependence, the Global Moran's I statistic was computed using a Queen contiguity weights matrix.

Statistical significance was assessed using a Monte Carlo permutation test with 999 random permutations.

Under the null hypothesis (**H₀**), the spatial distribution of municipal vote shares is random.

---

## Results

| Year | Candidate         | Party | Moran's I | Expected I | z-score | p-value |
| ---: | ----------------- | ----- | --------: | ---------: | ------: | ------: |
| 2018 | Fernando Pimentel | PT    |    0.7484 |    -0.0012 |  35.614 |  0.0010 |
| 2018 | Romeu Zema        | NOVO  |    0.7051 |    -0.0012 |  33.556 |  0.0010 |
| 2018 | Antonio Anastasia | PSDB  |    0.3639 |    -0.0012 |  17.347 |  0.0010 |
| 2022 | Alexandre Kalil   | PSD   |    0.6768 |    -0.0012 |  32.214 |  0.0010 |
| 2022 | Romeu Zema        | NOVO  |    0.6638 |    -0.0012 |  31.596 |  0.0010 |
| 2022 | Carlos Viana      | PL    |    0.1718 |    -0.0012 |   8.220 |  0.0010 |


---

## Interpretation

The Global Moran's I statistic measures the degree of spatial autocorrelation in electoral results.

- Values close to **+1** indicate strong positive spatial autocorrelation, meaning neighboring municipalities tend to exhibit similar vote shares.
- Values close to **0** indicate spatial randomness.
- Negative values indicate spatial dispersion, where neighboring municipalities tend to exhibit dissimilar voting patterns.

All estimated statistics were statistically significant (**p = 0.001**), providing strong evidence that voting patterns were not randomly distributed across municipalities.

The estimated Moran's I values ranged from **0.1718** to **0.7484**, revealing substantial differences in the spatial organization of electoral support among candidates.

Fernando Pimentel exhibited the strongest spatial autocorrelation (**I = 0.7484**), followed by Romeu Zema in both elections (**I = 0.7051** in 2018 and **I = 0.6638** in 2022). Alexandre Kalil also presented a highly structured spatial voting pattern (**I = 0.6768**). Antonio Anastasia (**I = 0.3639**) and Carlos Viana (**I = 0.1718**) exhibited comparatively weaker spatial dependence, indicating a more heterogeneous territorial distribution of votes.

Although Romeu Zema remained highly spatially clustered in both elections, the slight reduction in Moran's I between 2018 and 2022 suggests a modest decrease in the spatial dependence of his electoral support, while preserving a strongly structured territorial pattern. These results demonstrate that electoral support in Minas Gerais exhibited clear territorial organization, although the intensity of spatial clustering varied considerably across candidates and election years.

---

## Statistical Note

A high Moran's I is **not** a violation of statistical assumptions in this context.

Unlike ordinary least squares (OLS) regression, where spatial autocorrelation may bias statistical inference if ignored, the purpose of the Global Moran's I statistic is precisely to test whether spatial dependence exists.

Therefore, the significant values reported here provide statistical evidence that voting patterns exhibit meaningful spatial structure rather than random geographic variation.

---

## Methodological Workflow

The analysis followed the workflow below:

1. Municipal election results obtained from the Brazilian Superior Electoral Court (TSE).
2. Official 2021 Minas Gerais municipal boundaries.
3. Construction of a Queen contiguity spatial weights matrix.
4. Estimation of Global Moran's I.
5. Statistical significance assessed using a Monte Carlo permutation test with **999 permutations**.

---

## References

Anselin, L. (1995). Local indicators of spatial association—LISA. Geographical Analysis, 27(2), 93–115. https://doi.org/10.1111/j.1538-4632.1995.tb00338.x

Cliff, A. D., & Ord, J. K. (1984). Spatial Processes: Models and Applications. Journal of the Royal Statistical Society. Series A (General), 147(3), 515. https://doi.org/10.2307/2981590

Moran, P. A. P. (1950). Notes on Continuous Stochastic Phenomena. Biometrika, 37(1–2), 17–23. https://doi.org/10.1093/biomet/37.1-2.17

Rey, S. J., & Anselin, L. (2007). PySAL: A Python Library of Spatial Analytical Methods. Review of Regional Studies, 37, 5–27. https://doi.org/10.52324/001c.8285


