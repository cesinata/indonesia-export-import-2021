# Indonesia's Primary Commodity Exports and Imports (Satria Data 2021)

## What this is

Our team made this analysis for **Satria Data 2021**. Satria Data
(Statistika Ria dan Festival Sains Data) is a national statistics and data
science competition for university students in Indonesia, held every year by
Puspresnas, part of the Ministry of Education. The 2021 edition was held online.
Our team was selected to represent **Universitas Brawijaya**.

The analysis asks whether imports and exports of primary commodities could
support each other in Indonesia's recovery from COVID-19. One example is
importing wheat and food-processing machinery and exporting wheat flour and
pasta. We used UN Comtrade trade data for 2001–2020 and BPS export and import
figures for August 2021, and the final output was an infographic
([figures/infographic.png](figures/infographic.png)). The project name and
background, as written in 2021, are in
[docs/original_readme.md](docs/original_readme.md).

The original working folders were labelled "SIC". In Satria Data 2021 this most likely
means the Statistics Infographic Competition category. [TO CONFIRM: competition category]

This repository is kept mostly as it was in 2021. In 2026 the files were renamed
to English and moved into folders. Nothing else in the analysis was changed.

## Team

- Cesilia Natasya Nainggolan
- [Femi Novia Lina](https://www.linkedin.com/in/feminovialina/)
- [Alya Fitri Nurhaliza](https://www.linkedin.com/in/alyafitrin/)

My role: [TO CONFIRM]

## Result

[TO CONFIRM]

## Data sources

**UN Comtrade.** Every CSV in `data/raw/` is a download from UN Comtrade in its
legacy (pre-2023) format. Each file has 35 columns. The useful ones are:

| Column | Meaning |
|---|---|
| `Year` | Calendar year of the trade |
| `Trade Flow` | `Import` or `Export`, as Indonesia reports it. Two files show `X` (Trade Flow Code 0). See Limitations |
| `Reporter` | Always Indonesia |
| `Partner` | The partner country, or `World` for Indonesia's total trade |
| `Commodity Code` / `Commodity` | Harmonized System (HS) code and its description |
| `Classification` | HS edition used for that year (H1–H5) |
| `Trade Value (US$)` | The value the notebooks analyse |
| `Netweight (kg)`, `Qty` | Quantity fields. Often empty |

Commodities in the data:

| Folder | HS code | Description | Flow |
|---|---|---|---|
| `wheat/` | 1001 | Wheat and meslin | Import |
| `machinery/` | 843880 | Machinery for industrial food preparation (HS 8438.80) | Import |
| `flour/` | 1101 / 110100 | Wheat or meslin flour | Export |
| `pasta/` | 1902 | Pasta | Export |
| `palm_oil/` | 1511 | Palm oil and its fractions | Export |
| `crustaceans/` | 0306 | Crustaceans | Export |
| `automotive/` | 8703 | Motor cars | Shown as `X` in the file |

**BPS (Badan Pusat Statistik).** `bps_trade_structure_aug2021.ipynb` charts the
make-up of Indonesia's exports and imports in August 2021. The BPS figures are
typed directly into the notebook. There is no source file for them.

Raw trade data comes from UN Comtrade and BPS. It is still subject to their
terms of use.

## Folder guide

```
notebooks/   Jupyter notebooks from 2021 (originally run in Google Colab)
data/raw/    UN Comtrade CSVs, one folder per commodity
             by_partner_YYYY_YYYY.csv  main partner countries for that period
             world_YYYY_YYYY.csv       totals against the world
figures/     Competition infographic and SVG charts
docs/        Original README and the old-to-new rename map
```

| Notebook | What it does |
|---|---|
| `wheat_imports` | Wheat imports from the world, 2001–2020 |
| `machinery_imports` | Food-processing machinery imports from the world, 2001–2020 |
| `flour_exports_v1` | Wheat flour exports by partner country, 2001–2020 |
| `flour_exports_v2` | Wheat flour exports to the world, compared with pasta |
| `pasta_exports_v1` | Early pasta export charts (input files not in repo) |
| `pasta_exports_v2` | Pasta exports by partner country, 2001–2020 |
| `palm_oil_crustacean_coffee_exports` | Palm oil, crustacean and coffee exports |
| `automotive_exports` | Car trade by partner country, 2016–2020 |
| `bps_trade_structure_aug2021` | Donut charts of the BPS export and import structure, August 2021 |
| `coffee_imports_exploration` | Early exploration of coffee imports (input file not in repo) |

The full mapping from the original Indonesian names is in
[docs/rename_map.md](docs/rename_map.md).

## How to run the notebooks

The notebooks import these packages:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `google.colab` (Colab only)

```
pip install pandas numpy matplotlib seaborn jupyter
cd notebooks
jupyter notebook
```

To run them outside Colab, skip the `from google.colab import drive` /
`drive.mount(...)` cell. Data paths are relative to `notebooks/`.

These notebooks were written in 2021 for an older pandas. Several of them call
`DataFrame.append`, which pandas 2.0 removed. To run those, use pandas 1.x, or
replace the call with `pd.concat` in your own copy.

## Limitations

- **Legacy data format.** The CSVs use UN Comtrade's old export format. The current
  Comtrade API has different column names.
- **Unclear trade flow in two files.** `automotive/by_partner_2016_2020.csv` and
  `flour/by_partner_2016_2020.csv` record `Trade Flow` as `X`, not
  `Export`.
- **Missing inputs.** Some notebooks read files that were never committed. Those
  paths point to `data/raw/not_in_repo/` and will fail.
- **No pipeline.** These are separate exploratory notebooks. Nothing connects
  them, and there are no tests.
- **Not re-run as a whole.** In 2026 copies of the notebooks were run with
  pandas 3.1 to check that the file paths work. Every data file the code
  points to loaded. Only `bps_trade_structure_aug2021` ran start to finish. The others stopped
  at the Colab cell, `DataFrame.append`, or a missing input. The saved outputs
  are still the 2021 ones.
- **Mixed languages.** Notebook headings and chart labels are still in
  Indonesian.

## AI assistance

In 2026 an AI assistant (Claude) helped write this README and rename the files
and folders. The analysis, notebooks, data selection and infographic are the
original 2021 team work.

## Licence

The notebooks, documentation and figures are released under the [MIT License](LICENSE).
The trade data in `data/raw/` is not covered. It remains subject to UN Comtrade's terms.
