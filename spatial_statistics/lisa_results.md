# Local Indicators of Spatial Association (LISA)

## Spatial clustering analysis

To complement the Global Moran's I analysis, Local Indicators of Spatial Association (LISA) were computed for the three most voted candidates in each gubernatorial election.

While the Global Moran's I summarizes the overall degree of spatial autocorrelation across Minas Gerais, the Local Moran statistic (LISA) identifies where statistically significant spatial clusters and local spatial outliers occur.

Statistical significance was assessed using a Monte Carlo permutation test with **999 random permutations** and a significance level of **α = 0.05**.

---

## Cluster Types

The Local Moran statistic classifies municipalities into four categories.

| Cluster | Interpretation |
|----------|----------------|
| **High–High (HH)** | High vote share surrounded by municipalities with high vote shares. |
| **Low–Low (LL)** | Low vote share surrounded by municipalities with low vote shares. |
| **High–Low (HL)** | High vote share surrounded by municipalities with low vote shares (spatial outlier). |
| **Low–High (LH)** | Low vote share surrounded by municipalities with high vote shares (spatial outlier). |

Only statistically significant municipalities (p < 0.05) are assigned to one of these four categories. Remaining municipalities are classified as **Not Significant**.

---

## Significant LISA Clusters

| Year | Candidate | Party | High–High | Low–Low | High–Low | Low–High | Not Significant |
|-----:|---------------------|:-----:|----------:|---------:|----------:|----------:|----------------:|
| 2018 | Fernando Pimentel   | PT    | 181 | 236 | 5 | 5 | 426 |
| 2018 | Antonio Anastasia   | PSDB  | 80 | 113 | 20 | 13 | 627 |
| 2018 | Romeu Zema          | NOVO  | 165 | 163 | 10 | 10 | 505 |
| 2022 | Romeu Zema          | NOVO  | 202 | 179 | 13 | 8 | 451 |
| 2022 | Alexandre Kalil     | PSD   | 177 | 208 | 11 | 14 | 443 |
| 2022 | Carlos Viana        | PL    | 55 | 108 | 9 | 17 | 664 |

---

## Interpretation

The Local Moran statistics reinforce the results obtained from the Global Moran's I analysis.

Candidates exhibiting higher Global Moran's I values also presented larger numbers of **High–High** and **Low–Low** municipalities, indicating broad and spatially cohesive electoral regions where neighboring municipalities tended to display similar voting patterns.

Fernando Pimentel (2018) showed the largest concentration of significant clusters, with **181 High–High** and **236 Low–Low** municipalities, consistent with the highest Global Moran's I observed in the study (I = 0.7484).

Romeu Zema also exhibited extensive High–High and Low–Low clusters in both elections, confirming the strong spatial organization of his electoral support.

Conversely, Antonio Anastasia and Carlos Viana presented substantially fewer significant clusters and larger numbers of municipalities without significant local spatial association, reflecting weaker territorial cohesion and lower Global Moran's I values.

Spatial outliers (High–Low and Low–High) represented only a small proportion of municipalities for all candidates, indicating that abrupt local changes in voting behavior were relatively uncommon across Minas Gerais.

Overall, the Local Moran analysis confirms that the spatial dependence detected by the Global Moran's I was primarily driven by contiguous territorial clusters rather than isolated municipalities.

---

## Methodological Workflow

The local spatial analysis followed the workflow below.

1. Municipal election results obtained from the Brazilian Superior Electoral Court (TSE).
2. Municipal boundaries from the official 2021 Minas Gerais municipal shapefile.
3. Queen contiguity spatial weights matrix.
4. Local Moran's I estimation.
5. Monte Carlo significance test (999 permutations).
6. Classification of statistically significant municipalities into High–High, Low–Low, High–Low and Low–High clusters.

---

## References

Anselin, L. (1995). Local indicators of spatial association—LISA. Geographical Analysis, 27(2), 93–115. https://doi.org/10.1111/j.1538-4632.1995.tb00338.x

PySAL Development Team. PySAL Documentation. https://pysal.org/

Rey, S. J., Anselin, L., & Li, W. (2020). Open Geospatial Data Science with PySAL. https://geographicdata.science/