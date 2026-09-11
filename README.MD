# BTC Market Analysis

Analisis faktor-faktor (macro, micro, siklus halving) yang mempengaruhi pergerakan harga Bitcoin. Tujuan project ini adalah memahami pola pergerakan pasar BTC — bukan memprediksi harga secara presisi, karena price prediction untuk aset likuid pada dasarnya sangat noisy dan sulit dilakukan secara reliable.

## Status
🚧 Work in progress — tahap pengumpulan data.

## Struktur Project

btc-analysis/
├── data/ # dataset (di-ignore git, hasil download API)
├── notebooks/ # notebook eksplorasi & analisis
├── .env # API keys (di-ignore git)
└── requirements.txt # dependencies


## Data Sources
- **Harga BTC**: Yahoo Finance via `yfinance` (harian, 2014–sekarang)
- **Suku Bunga Fed**: FRED API (Federal Funds Effective Rate)

## Setup
```bash
python -m venv venv
.\venv\Scripts\Activate.ps1  # Windows
pip install -r requirements.txt
```
Buat file `.env` berisi `FRED_API_KEY=your_key_here` (daftar gratis di fred.stlouisfed.org).

## Roadmap
- [x] Data harga BTC + feature siklus halving
- [x] Data macro: Fed Funds Rate
- [ ] Data macro tambahan (DXY, CPI)
- [ ] Exploratory Data Analysis
- [ ] Modeling: regime classification (bullish/bearish/sideways)