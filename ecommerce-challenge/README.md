# eCommerce - Sales Data Analysis

Analysis of the [C1 Github](https://github.com/CapitalOneRecruiting/DA-E-Commerce-Data-Challenge) data in Python and SQL.

## How to view or run

- **Just read:** click any notebook below. GitHub shows the code and all results, so nothing needs to run.
- **Run it yourself:** click **Open in Colab**, then choose **Runtime → Run all**. Each notebook downloads the data from this repo automatically, so you don't need to sign in to Drive or upload anything.
  - If Colab warns *"This notebook was not authored by Google"*, click **Run anyway**.

## Notebooks

| # | Question | Run |
|---|---|---|
| 00 | [Data cleaning: how the raw files were prepared](ecommerce-challenge/notebooks/00_data_cleaning.ipynb) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/VizDataWorks/CapitalOne_DataAnalysis/blob/main/ecommerce-challenge/notebooks/00_data_cleaning.ipynb) |
| 01 | [Order volume by hour: is 24/7 staffing needed?](ecommerce-challenge/notebooks/01_order_volume_by_hour.ipynb) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/VizDataWorks/CapitalOne_DataAnalysis/blob/main/ecommerce-challenge/notebooks/01_order_volume_by_hour.ipynb) |
| 02 | [Average profit per order by quarter and customer segment](ecommerce-challenge/notebooks/02_profit_per_order_by_quarter.ipynb) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/VizDataWorks/CapitalOne_DataAnalysis/blob/main/ecommerce-challenge/notebooks/02_profit_per_order_by_quarter.ipynb) |
| 03 | [Revenue lost to the referral program](ecommerce-challenge/notebooks/03_referral_program.ipynb) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/VizDataWorks/CapitalOne_DataAnalysis/blob/main/ecommerce-challenge/notebooks/03_referral_program.ipynb) |
| 04 | [Black Friday's impact on annual sales by segment](ecommerce-challenge/notebooks/04_black_friday_impact.ipynb) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/VizDataWorks/CapitalOne_DataAnalysis/blob/main/ecommerce-challenge/notebooks/04_black_friday_impact.ipynb) |
| 05 | [Our best customer base, and KPIs to grow it](ecommerce-challenge/notebooks/05_best_customer_base.ipynb) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/VizDataWorks/CapitalOne_DataAnalysis/blob/main/ecommerce-challenge/notebooks/05_best_customer_base.ipynb) |

Start with **00** to see how the data was cleaned. Notebooks 01–05 each run on their own, so you can open any of them directly.

## Folder layout

```
ecommerce-challenge/
├── data/
│   ├── raw/      original challenge files (never edited)
│   │   ├── buyer.csv, sales.csv.gz, metadata.pdf
│   │   └── vendors/   11 product files, one per vendor
│   └── clean/    written by notebook 00
│       ├── customers.csv         47,500 rows, one per buyer
│       ├── products.csv           1,037 rows, one per SKU
│       ├── sales.csv.gz         348,905 rows, one per order line
│       └── data_quality_log.csv  every cleaning step and the rows it affected
└── notebooks/    00–05 above
```
