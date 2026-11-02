# Capital One E-Commerce Data Challenge

## Folder layout

```
ecommerce-challenge/
├── data/
│   ├── raw/        original files from the challenge repo (never edited)
│   │   ├── buyer.csv, sales.csv, metadata.pdf
│   │   └── vendors/   11 product files, one per vendor
│   └── clean/      written by notebooks/00_data_cleaning.ipynb
│       ├── customers_clean.csv   47,500 rows, one per buyer_id
│       ├── products_clean.csv     1,037 rows, one per sku_id
│       ├── sales_clean.csv      348,905 rows, one per order + sku
│       └── data_quality_log.csv  every cleaning step and rows affected
└── notebooks/
    └── 00_data_cleaning.ipynb
```

## Run it in Google Colab

1. Upload the whole `ecommerce-challenge` folder to **My Drive**.
2. Open `notebooks/00_data_cleaning.ipynb` with Google Colab.
3. In the first code cell set `USE_DRIVE = True`, then **Runtime → Run all**.

The notebook finds the raw files in `data/raw/` and rewrites `data/clean/`. Opened on its own (without the folder), it downloads the raw files from the [challenge repo](https://github.com/CapitalOneRecruiting/DA-E-Commerce-Data-Challenge) instead.

Source data: https://github.com/CapitalOneRecruiting/DA-E-Commerce-Data-Challenge
