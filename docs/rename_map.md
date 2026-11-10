# Rename map

In 2021 the files had Indonesian names. In 2026 they were renamed to
English and moved into folders. Every move used `git mv`, and the renames are in
commits of their own, so the earlier history is still there. To see it:

```
git log --follow -- notebooks/wheat_imports.ipynb
```

Apart from the renames, the only edit to the notebooks is to the file paths in
the code cells. Saved outputs were not changed. See
[original_readme.md](original_readme.md) for the README as it was in 2021.

## Folder names

| Indonesian | English |
|---|---|
| Gandum | wheat |
| Tepung | flour |
| Mesin | machinery |
| Otomotif / Mobil | automotive (cars) |
| Kelapa Sawit | palm oil |
| Krustasea | crustaceans |
| Komoditas | commodities |
| Ekspor / Impor | exports / imports |

## Files

| Old path | New path |
|---|---|
| `Otomotif.ipynb` | `notebooks/automotive_exports.ipynb` |
| `Data BPS.ipynb` | `notebooks/bps_trade_structure_aug2021.ipynb` |
| `Data SIC.ipynb` | `notebooks/coffee_imports_exploration.ipynb` |
| `Tepung.ipynb` | `notebooks/flour_exports_v1.ipynb` |
| `Tepung v.2.ipynb` | `notebooks/flour_exports_v2.ipynb` |
| `Mesin.ipynb` | `notebooks/machinery_imports.ipynb` |
| `Komoditas.ipynb` | `notebooks/palm_oil_crustacean_coffee_exports.ipynb` |
| `Pasta.ipynb` | `notebooks/pasta_exports_v1.ipynb` |
| `Pasta v.2.ipynb` | `notebooks/pasta_exports_v2.ipynb` |
| `Gandum.ipynb` | `notebooks/wheat_imports.ipynb` |
| `SVG files/ekspor tepung.svg` | `figures/flour_exports.svg` |
| `Infographics.png` | `figures/infographic.png` |
| `SVG files/impor mesin.svg` | `figures/machinery_imports.svg` |
| `SVG files/ekspor pasta dan tepung.svg` | `figures/pasta_and_flour_exports.svg` |
| `SVG files/ekspor pasta.svg` | `figures/pasta_exports.svg` |
| `SVG files/impor gandum .svg` | `figures/wheat_imports.svg` |
| `Datasets/Mobil/2016-2020.csv` | `data/raw/automotive/by_partner_2016_2020.csv` |
| `Datasets/Krustasea/2016-2020.csv` | `data/raw/crustaceans/by_partner_2016_2020.csv` |
| `Datasets/Tepung/2001 - 2005.csv` | `data/raw/flour/by_partner_2001_2005.csv` |
| `Datasets/Tepung/2006 - 2010.csv` | `data/raw/flour/by_partner_2006_2010.csv` |
| `Datasets/Tepung/2011 - 2015.csv` | `data/raw/flour/by_partner_2011_2015.csv` |
| `Datasets/Tepung/2016 - 2020.csv` | `data/raw/flour/by_partner_2016_2020.csv` |
| `Datasets/TEPUNG WORLD/comtrade (40).csv` | `data/raw/flour/world_2001_2005.csv` |
| `Datasets/TEPUNG WORLD/comtrade (41).csv` | `data/raw/flour/world_2006_2010.csv` |
| `Datasets/TEPUNG WORLD/comtrade (42).csv` | `data/raw/flour/world_2011_2015.csv` |
| `Datasets/TEPUNG WORLD/comtrade (43).csv` | `data/raw/flour/world_2016_2020.csv` |
| `Datasets/Mesin/2001-2005.csv` | `data/raw/machinery/by_partner_2001_2005.csv` |
| `Datasets/Mesin/2006-2010.csv` | `data/raw/machinery/by_partner_2006_2010.csv` |
| `Datasets/Mesin/2011-2015.csv` | `data/raw/machinery/by_partner_2011_2015.csv` |
| `Datasets/Mesin/2016-2020.csv` | `data/raw/machinery/by_partner_2016_2020.csv` |
| `Datasets/Mesin/comtrade.csv` | `data/raw/machinery/world_2001_2005.csv` |
| `Datasets/Mesin/comtrade (1).csv` | `data/raw/machinery/world_2006_2010.csv` |
| `Datasets/Mesin/comtrade (2).csv` | `data/raw/machinery/world_2011_2015.csv` |
| `Datasets/Mesin/comtrade (3).csv` | `data/raw/machinery/world_2016_2020.csv` |
| `Datasets/Kelapa Sawit/2001-2005.csv` | `data/raw/palm_oil/by_partner_2001_2005.csv` |
| `Datasets/Kelapa Sawit/2006-2010.csv` | `data/raw/palm_oil/by_partner_2006_2010.csv` |
| `Datasets/Kelapa Sawit/2011-2015.csv` | `data/raw/palm_oil/by_partner_2011_2015.csv` |
| `Datasets/Kelapa Sawit/2016-2020.csv` | `data/raw/palm_oil/by_partner_2016_2020.csv` |
| `Datasets/Pasta/2001-2005.csv` | `data/raw/pasta/by_partner_2001_2005.csv` |
| `Datasets/Pasta/2006-2010.csv` | `data/raw/pasta/by_partner_2006_2010.csv` |
| `Datasets/Pasta/2011-2015.csv` | `data/raw/pasta/by_partner_2011_2015.csv` |
| `Datasets/Pasta/2016-2020.csv` | `data/raw/pasta/by_partner_2016_2020.csv` |
| `Datasets/PASTA WORLD/1-5.csv` | `data/raw/pasta/world_2001_2005.csv` |
| `Datasets/PASTA WORLD/6-10.csv` | `data/raw/pasta/world_2006_2010.csv` |
| `Datasets/PASTA WORLD/11-15.csv` | `data/raw/pasta/world_2011_2015.csv` |
| `Datasets/PASTA WORLD/16-20.csv` | `data/raw/pasta/world_2016_2020.csv` |
| `Datasets/Pasta/comtrade (34).csv` | `data/raw/pasta/world_2016_2020_duplicate.csv` |
| `Datasets/Gandum/2001-2005.csv` | `data/raw/wheat/by_partner_2001_2005.csv` |
| `Datasets/Gandum/2006-2010.csv` | `data/raw/wheat/by_partner_2006_2010.csv` |
| `Datasets/Gandum/2011-2015.csv` | `data/raw/wheat/by_partner_2011_2015.csv` |
| `Datasets/Gandum/2016-2020.csv` | `data/raw/wheat/by_partner_2016_2020.csv` |
| `Datasets/Gandum/comtrade.csv` | `data/raw/wheat/world_2001_2005.csv` |
| `Datasets/Gandum/comtrade (1).csv` | `data/raw/wheat/world_2006_2010.csv` |
| `Datasets/Gandum/comtrade (2).csv` | `data/raw/wheat/world_2011_2015.csv` |
| `Datasets/Gandum/comtrade (3).csv` | `data/raw/wheat/world_2016_2020.csv` |
| `README.md` | `docs/original_readme.md` |

## Data file naming

- `by_partner_YYYY_YYYY.csv`: Indonesia's trade with its main partner
  countries over that period.
- `world_YYYY_YYYY.csv`: Indonesia's trade with the world as a whole
  (Partner = World).
- `pasta/world_2016_2020_duplicate.csv`: an exact copy of `pasta/world_2016_2020.csv`.
  It is kept because both files were in the original upload.

Each period in a file name was checked against that file's `Year` column.

## Notebook paths changed

The notebooks used to read from Google Drive (`/content/drive/MyDrive/...`) or a local
Windows path. They now read from `../data/raw/...`, which is relative to `notebooks/`.
Some input files were never committed. Their paths now point to `../data/raw/not_in_repo/...`
and do not exist:

- `Kopi/comtrade (3).csv` (palm_oil_crustacean_coffee_exports)
- `tepung2/tepung3.csv`, `tepung2/tepung4.csv` (pasta_exports_v1)
- `tepung2/comtrade (26)–(29).csv` (flour_exports_v2)
- `comtrade.csv` (coffee_imports_exploration)
