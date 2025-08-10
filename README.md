# 🌤 CSV Weather Data Processing & Report Generation System

**In one sentence:**
I help you **turn your raw CSV city data into complete weather-enriched reports with cleaned data, trend charts, and PDF summaries** — fully automated, processing many files at once.

---

## 🚀 What You Get

* **Batch processing** – handle multiple files in one run, saving hours of manual work
* **Automatic weather data fetching** – from a real API or demo/mock data (no API limits during testing)
* **Data cleaning** – remove invalid rows, unify temperature & wind speed units
* **Local database storage** – keeps processed data for future analysis
* **Automatic chart creation** – clear temperature trend charts (PNG format)
* **PDF reports** – charts + key summaries in one shareable file
* **Fully automated workflow** – drop your CSVs in, run one command, and you’re done

---

## 📂 Project Structure (Simple View)

```
cities/           ← Put your input CSV files here
outputs/          ← Processed results (CSV, DB, charts)
outputs/reports/  ← PDF reports are saved here
src/              ← Main program code
tests/            ← Automated test scripts
config.yaml       ← Easy settings (edit to match your needs)
```

---

## 📥 Input Format

Each CSV only needs two columns:

```
city,date
London,2025-06-01
London,2025-06-02
...
```

You provide **city name** and **date** — the system does the rest.

---

## 📤 Output for Each City

* Cleaned CSV file with weather data
* SQLite database file containing all processed records
* Temperature trend chart (PNG)
* PDF report combining chart + summary statistics

---

## ⚙️ Configuration (No Tech Skills Needed)

Edit `config.yaml`:

```yaml
input_folder: cities          # Input folder for CSV files
output_folder: outputs        # Output folder for results
report_folder: outputs/reports
use_mock_data: true           # true = demo data, false = real API
max_threads: 8                # Speed boost: how many files processed in parallel
```

If you have a real weather API key, just put it into `.env` and switch `use_mock_data` to `false` to fetch live data.

---

## ▶️ How to Run

**Batch Mode (process all CSVs at once):**

```bash
python -m src.main
```

The program will:

1. Detect all CSV files in `cities/`
2. Add weather data
3. Clean & save to a database
4. Generate charts
5. Create PDF reports
6. Save everything to `outputs/`

---

## 🧪 Reliable & Tested

The project includes automated tests (`pytest`) to verify all functions work as expected — ensuring accurate, stable results.

---

## 💡 Why This Works for You

* No technical knowledge required — just give me your CSV files
* Perfect for business reports, client presentations, or analytics
* Flexible setup for different industries (logistics, travel, energy, etc.)

---

If needed, I can also set up **daily automatic runs** so reports are updated without you lifting a finger.

---
