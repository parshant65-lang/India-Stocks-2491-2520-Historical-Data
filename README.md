# India-Stocks-2491-2520-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2491 to 2520)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2491-2520-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2491 to 2520)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2491 | `UTKARSHBNK` | Utkarsh Small Finance Bank Limited | `UTKARSHBNK.NS` |
| 2492 | `UTLSOLAR` | Fujiyama Power Systems Limited | `UTLSOLAR.NS` |
| 2493 | `UTTAMSUGAR` | Uttam Sugar Mills Limited | `UTTAMSUGAR.NS` |
| 2494 | `UYFINCORP` | U. Y. Fincorp Limited | `UYFINCORP.NS` |
| 2495 | `V2RETAIL` | V2 Retail Limited | `V2RETAIL.NS` |
| 2496 | `VADILALIND` | Vadilal Industries Limited | `VADILALIND.NS` |
| 2497 | `VADILENT` | Vadilal Enterprises Limited | `VADILENT.NS` |
| 2498 | `VAIBHAVGBL` | Vaibhav Global Limited | `VAIBHAVGBL.NS` |
| 2499 | `VAISHALI` | Vaishali Pharma Limited | `VAISHALI.NS` |
| 2500 | `VAKRANGEE` | Vakrangee Limited | `VAKRANGEE.NS` |
| 2501 | `VALIANTLAB` | Valiant Laboratories Limited | `VALIANTLAB.NS` |
| 2502 | `VALIANTORG` | Valiant Organics Limited | `VALIANTORG.NS` |
| 2503 | `VARDHACRLC` | Vardhman Acrylics Limited | `VARDHACRLC.NS` |
| 2504 | `VARDMNPOLY` | Vardhman Polytex Limited | `VARDMNPOLY.NS` |
| 2505 | `VARMORA` | Varmora Granito Limited | `VARMORA.NS` |
| 2506 | `VARROC` | Varroc Engineering Limited | `VARROC.NS` |
| 2507 | `VASCONEQ` | Vascon Engineers Limited | `VASCONEQ.NS` |
| 2508 | `VASUPRADA` | Shri Vasuprada Plantations Limited | `VASUPRADA.NS` |
| 2509 | `VASWANI` | Vaswani Industries Limited | `VASWANI.NS` |
| 2510 | `VCL` | Vaxtex Cotfab Limited | `VCL.NS` |
| 2511 | `VEDAVAAG` | VEDAVAAG Systems Limited | `VEDAVAAG.NS` |
| 2512 | `VEEDOL` | Veedol Corporation Limited | `VEEDOL.NS` |
| 2513 | `VEEGALAND` | Veegaland Developers Limited | `VEEGALAND.NS` |
| 2514 | `VELJAN` | Veljan Denison Limited | `VELJAN.NS` |
| 2515 | `VENKEYS` | Venky's (India) Limited | `VENKEYS.NS` |
| 2516 | `VENTIVE` | Ventive Hospitality Limited | `VENTIVE.NS` |
| 2517 | `VENUSPIPES` | Venus Pipes & Tubes Limited | `VENUSPIPES.NS` |
| 2518 | `VENUSREM` | Venus Remedies Limited | `VENUSREM.NS` |
| 2519 | `VERANDA` | Veranda Learning Solutions Limited | `VERANDA.NS` |
| 2520 | `VERTOZ` | Vertoz Limited | `VERTOZ.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream UTKARSHBNK 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2491-2520-Historical-Data/main/UTKARSHBNK/1m/2026/10/UTKARSHBNK_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
