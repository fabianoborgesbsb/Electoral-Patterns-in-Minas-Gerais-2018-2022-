## Data

This project is based on official electoral results published by the Brazilian Superior Electoral Court (TSE).

The original datasets can be obtained from the **TSE Electoral Results Portal**:

https://sig.tse.jus.br/ords/dwapr/seai/r/sig-eleicao-resultados/resultado-consolidado

Municipal boundaries correspond to the official 2021 Minas Gerais municipal shapefile.

---

## Data Preparation

The original TSE datasets were processed specifically for this project before spatial interpolation.

The preprocessing workflow included:

- aggregation of municipal-level election results;
- computation of candidate vote shares (%);
- standardization of municipal identifiers (`CD_MUN`);
- preparation of datasets for spatial interpolation.

The processed datasets included in this repository are:

- `MG_DADOS_ELEICAO_2018.csv`
- `MG_DADOS_ELEICAO_2022.csv`

These files are derived from the official TSE data and were prepared exclusively for the analyses presented in this repository.