[README.md](https://github.com/user-attachments/files/34305767/README.md)
# E-Commerce Data Challenge

Analysis of the [DA E-Commerce Data Challenge](https://github.com/CapitalOneRecruiting/DA-E-Commerce-Data-Challenge) in Python (pandas) on Google Colab.

## How to view or run

- **Read:** click a notebook below. GitHub shows the code and all results; nothing needs to run.
- **Run:** click **Open in Colab**, then **Runtime → Run all**. Each notebook downloads the data from this repo, so no sign-in or upload is needed. If Colab warns *"This notebook was not authored by Google"*, click **Run anyway**.

## Questions and answers

| # | Question | Answer | Run |
|---|---|---|---|
| 01 | [Order volume by hour: is 24/7 staffing needed?](/notebooks/01_order_volume_by_hour.ipynb) | **No.** 91.4% of orders arrive 6 AM–midnight CT; an average night brings about 27 orders. | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/VizDataWorks/ecommerce_data_analysis/blob/main/notebooks/01_order_volume_by_hour.ipynb) |
| 02 | [Average profit per order by quarter and segment](notebooks/02_profit_per_order_by_quarter.ipynb) | Tech Enthusiasts lead every quarter (\$85.88 per order vs \$24–32). Q4 2024 peaked; 2025 was flat. | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/VizDataWorks/ecommerce_data_analysis/blob/main/notebooks/02_profit_per_order_by_quarter.ipynb) |
| 03 | [Revenue lost to the referral program](ecommerce-challenge/notebooks/03_referral_program.ipynb) | \$21,325 net over two years, about \$6 per referred customer. **Keep it:** referred customers are as valuable as others. | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/VizDataWorks/ecommerce_data_analysis/blob/main/notebooks/03_referral_program.ipynb) |
| 04 | [Black Friday's impact on annual sales by segment](ecommerce-challenge/notebooks/04_black_friday_impact.ipynb) | About 4× a normal day's orders, but only about 1% of the year's orders and revenue. Revenue fell 24% in 2025. | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/VizDataWorks/ecommerce_data_analysis/blob/main/notebooks/04_black_friday_impact.ipynb) |
| 05 | [Our best customer base, and KPIs to grow it](ecommerce-challenge/notebooks/05_best_customer_base.ipynb) | Tech Enthusiasts: 12.6% of customers, 30.8% of profit (\$404 each). Track CAC (under about \$135), activation and electronics stock. | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/VizDataWorks/ecommerce_data_analysis/blob/main/notebooks/05_best_customer_base.ipynb) |

## Data cleaning

[Notebook 00](notebooks/00_data_cleaning.ipynb) [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/VizDataWorks/ecommerce_data_analysis/blob/main/notebooks/00_data_cleaning.ipynb) turns the raw files into three clean tables. Notebooks 01–05 read those tables, so each runs on its own.

| Table | Raw rows | Clean rows | Main fixes |
|---|---|---|---|
| Customers | 52,500 | 47,500 | Duplicates and blank IDs removed; region and time zone filled from state |
| Products | 1,037 (11 vendor files) | 1,037 | Column names aligned; percentage margins converted to fractions; `$` removed from prices; new `sku_id` key |
| Sales | 376,004 | 348,905 | Duplicates removed; mixed date formats parsed; typos fixed; bad quantities flagged; order time converted to company time (Central) |

## Key definitions

- **Revenue:** delivered orders only, after Black Friday (20%) and referral (10%) discounts.
- **Profit per order:** item profit − discounts + shipping charged − \$4.99 carrier fee.
- **Company time:** Central (`America/Chicago`). Orders are converted from the buyer's local time zone.

## Folder layout

```
ecommerce-challenge/
├── data/
│   ├── raw/      original challenge files (never edited)
│   └── clean/    customers.csv, products.csv, sales.csv.gz (written by notebook 00)
└── notebooks/    00–05
```
