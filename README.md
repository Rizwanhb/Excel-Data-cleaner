# Excel Data Cleaner 🧹

A Python-based data cleaning tool built in Jupyter Notebook that takes messy Excel or CSV files and outputs a clean, analysis-ready file — automatically.

---

## What It Does

Real-world Excel files are messy. This tool handles all of it:

- Removes duplicate rows
- Drops completely empty rows and columns
- Fixes inconsistent column names (spaces, symbols, mixed case)
- Strips hidden whitespace from cells
- Handles missing values (mean, median, mode, forward fill, or drop)
- Converts number-looking strings into actual numbers
- Removes constant columns that add no value
- Outputs a clean `.xlsx` or `.csv` file ready for analysis

---

## Before & After

| | Before | After |
|---|---|---|
| Rows | 1000 | 964 |
| Duplicate rows | 36 | 0 |
| Missing values | 112 | 0 |
| Column names | `"First Name "`, `"SALARY"` | `first_name`, `salary` |
| Number stored as text | `"50,000"` | `50000` |

---

## Built With

- Python 3
- pandas
- openpyxl
- Jupyter Notebook

---

## Getting Started

**1. Clone the repository**
```bash
git clone https://github.com/Rizwanhb/excel-data-cleaner.git
cd excel-data-cleaner
```

**2. Install dependencies**
```bash
pip install pandas openpyxl
```

**3. Add your file**

Place your messy `.xlsx` or `.csv` file in the same folder as the notebook.

**4. Open the notebook**
```bash
jupyter notebook Data-Cleaner.ipynb
```



**6. Run All Cells**

`Kernel` → `Restart & Run All` — done.

---

## Fill Method Options

| Option | What it does |
|---|---|
| `mean` | Fills missing numbers with column average |
| `median` | Fills missing numbers with column middle value |
| `mode` | Fills missing values with most frequent value |
| `ffill` | Fills using the previous row's value |
| `bfill` | Fills using the next row's value |
| `drop` | Removes any row with a missing value |
| `keep` | Leaves missing values as-is |

---

## Project Structure

```
excel-data-cleaner/
│
├── Excel_Data_Cleaner.ipynb   # main notebook
├── README.md                  # this file
├── warehouse_messy.xlsx       # sample messy input file
└── warehouse_clean.xlsx       # cleaned output (generated after running)
```

---

## Use Cases

This tool works well for:

- E-commerce order exports with duplicate entries
- Financial reports with inconsistent formatting
- Survey exports with blank rows and mixed data types
- Any Excel file that needs to be cleaned before analysis

---

## Author

**Rizwan**
BBA Finance | Aspiring Quant Developer
[GitHub](https://github.com/Rizwanhb) · [LinkedIn](https://linkedin.com/in/rizwan-khuharo)

---

## License

MIT License — free to use, modify, and distribute.
