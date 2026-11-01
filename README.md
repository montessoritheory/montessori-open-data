![Montessori Open Data, by Montessori Theory](banner.png)

# Montessori Open Data

**Free, documented datasets on Montessori schools and early childhood, checked against their official sources.**

Every dataset has its own repository with a cover, a data dictionary, a method, its known limits and a citation. The same data is on Kaggle, with a starter notebook, and on Hugging Face, ready for the `datasets` library. They come from the research behind [Montessori Theory](https://www.montessori-theory.com/), a site about Montessori at home.

## 🏫 Montessori Schools

| Dataset | GitHub | Kaggle | Hugging Face | DOI |
|---|---|---|---|---|
| 2,070 Montessori private schools in 2023-24, and 37,543 school-year records from 18 NCES survey waves since 1989, by state, city and county | [us-montessori-private-schools](https://github.com/montessoritheory/us-montessori-private-schools) | [Kaggle](https://www.kaggle.com/datasets/mariamontessori/us-montessori-private-schools) | [Dataset](https://huggingface.co/datasets/montessoritheory/us-montessori-private-schools) | [Zenodo](https://doi.org/10.5281/zenodo.23871758) |

A research note built on this dataset, *How Many Montessori Private Schools Are There in the United States?*, is archived at [doi.org/10.5281/zenodo.23871815](https://doi.org/10.5281/zenodo.23871815).

More datasets on child development and early education will be added here as they are released.

## How The Data Is Checked

Each dataset is rebuilt from its official source, here the NCES Private School Universe Survey, then compared with the figures the source publishes. For the US Montessori schools, the weighted estimate matches the NCES figure of 2,441 Montessori schools for 2021-22, and the total of all private schools matches the NCES national totals for every wave from 1997-98 to 2015-16. The checks are listed in each README under Checked Against The Source.

## Quick Start

```python
import pandas as pd

base = "https://raw.githubusercontent.com/montessoritheory"
schools = pd.read_csv(f"{base}/us-montessori-private-schools/main/data/montessori_private_schools_2023_24.csv")
schools.groupby("state").size().sort_values(ascending=False).head(10)
```

## License

All datasets are CC BY 4.0. Each repository has its own LICENSE and CITATION.cff. Please credit Montessori Theory, with a link to [montessori-theory.com](https://www.montessori-theory.com/), and the original source when you reuse them.

## Version Française

**Des jeux de données ouverts et documentés sur les écoles Montessori et la petite enfance, vérifiés à la source.** Chaque jeu existe sur GitHub, Kaggle et Hugging Face, sous licence CC BY 4.0, avec un dictionnaire des colonnes, la méthode et les limites. Le premier recense les 2 070 écoles Montessori privées des États-Unis en 2023-24, d'après l'enquête officielle NCES.
