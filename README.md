# ETL Extract Lab

**Name:** Bricole Asiachi  
**Student ID:** 670834

---

This project demonstrates a simple **ETL (Extract, Transform, Load)** process using synthetic sales data. The pipeline simulates full and incremental data extraction, followed by loading into SQLite (for full data) and Parquet format (for incremental data).

---

## Project Overview

The project mimics a real-world scenario where daily sales records are collected, tracked, and incrementally updated. The ETL process includes:

-  **Extraction** from a generated CSV file
- ⚙ **Transformation** (handling dates and updates)
-  **Loading** into:
  - SQLite database for full data
  - Parquet file for incremental updates

---

## ETL Phases

### 1. **Data Generation**
- Random synthetic data for 6 customers over a 60-day period
- Fields include: `id`, `customer`, `date`, `amount`, `last_updated`
- Output: `custom_data.csv`

### 2. **Full Extraction**
- Reads all data from `custom_data.csv`
- Parses `last_updated` field
- Saves the data for full loading

### 3. **Incremental Extraction**
- Reads `last_extraction.txt` for the last checkpoint
- Filters only records newer than the last checkpoint
- Updates the checkpoint after processing
- Output: filtered DataFrame (new or changed records)

### 4. **Loading**
- Full data is saved to **SQLite** (`full_data.db`)
- Incremental data is saved to **Parquet** (`incremental_data.parquet`)

---

## Tools Used

- **Python 3.8+**
- **Pandas** – for data manipulation
- **SQLite3** – for relational data storage
- **Apache Parquet** – for optimized storage of incremental data
- **PowerShell / Git** – for version control and updates

---

## How to Run the Project

### Step 1: Clone the Repository
```bash
git clone (https://github.com/Brciole/ETL_Extract_BricoleAsiachi_670834)
cd ETL_Extract_BricoleAsiachi_670834


