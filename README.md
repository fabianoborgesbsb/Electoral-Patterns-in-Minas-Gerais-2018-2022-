## Data

This project is based on official electoral results published by the Brazilian Superior Electoral Court (TSE).

The original datasets are available from the TSE Electoral Results Portal:

https://sig.tse.jus.br/ords/dwapr/seai/r/sig-eleicao-resultados/resultado-consolidado

Municipal boundaries were obtained from the official 2021 Minas Gerais municipal shapefile provided by the Brazilian Institute of Geography and Statistics (IBGE).

---

## Data Preparation

The original TSE datasets were processed specifically for this project prior to the spatial analyses.

The preprocessing workflow included:

- aggregation of municipal-level election results;
- computation of candidate vote shares (%);
- standardization of municipal identifiers (`CD_MUN`);
- integration with municipal boundaries;
- preparation of datasets for spatial interpolation and spatial autocorrelation analyses.

The processed datasets included in this repository are:

- `MG_DADOS_ELEICAO_2018.csv`
- `MG_DADOS_ELEICAO_2022.csv`

These files were derived from the official TSE data and prepared exclusively for the analyses presented in this repository.

---

## Spatial Analysis

Spatial interpolation was performed using the Inverse Distance Weighting (IDW) method to produce continuous electoral surfaces.

As a complementary analysis, global and local spatial autocorrelation were evaluated using Moran's I and Local Indicators of Spatial Association (LISA) based on first-order Queen contiguity weights with 999 Monte Carlo permutations.

## Spatial Statistics

Additional spatial statistics are available in the `spatial_statistics/` directory, including:

- Global Moran's I results;
- Local Indicators of Spatial Association (LISA);
- Moran scatterplots;
- LISA cluster maps for all gubernatorial candidates analyzed.

These analyses complement the IDW interpolation presented in the main notebook.
