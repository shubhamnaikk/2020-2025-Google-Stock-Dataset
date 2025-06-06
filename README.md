# GOOGL 5-Year Stock EDAweweqweqwe

![GOOGL 5-Year Stock EDA](image.jpeg)

This repository contains everything needed to perform Exploratory Data Analysis (EDA) on a 5-year historical stock price dataset for Google LLC (Ticker: GOOGL). The analysis is provided as a Jupyter notebook, with instructions to run it in Visual Studio Code (VS Code).

---

## 📂 Repository Structure

```
googl_eda_project/
├── google_5yr_one.csv       # The CSV file containing 5 years of GOOGL daily prices
├── googl_eda.ipynb          # Jupyter notebook performing the full EDA (tables & visualizations)
└── requirements.txt         # Python dependencies required to run the notebook
```

---

## 🛠 Prerequisites

1. **Python 3.8+** installed on your machine.
2. **Visual Studio Code (VS Code)** with the **Python** and **Jupyter** extensions enabled.
3. A working internet connection (only for installing packages; no external data download is needed).

---

## ⚙️ Installation & Setup

1. **Clone (or download) this repository** and navigate into it:

   ```bash
   git clone <repository-url>
   cd googl_eda_project
   ```

2. **Create and activate a virtual environment** (highly recommended to isolate dependencies):

   * macOS / Linux:

     ```bash
     python3 -m venv .venv
     source .venv/bin/activate
     ```
   * Windows (PowerShell):

     ```powershell
     python -m venv .venv
     .venv\Scripts\Activate.ps1
     ```
   * Windows (CMD):

     ```cmd
     python -m venv .venv
     .venv\Scripts\activate.bat
     ```

3. **Install the required Python packages** listed in `requirements.txt`:

   ```bash
   pip install -r requirements.txt
   ```

   The key dependencies are:

   * pandas
   * matplotlib
   * notebook

---

## 🚀 Running the Notebook in VS Code

1. **Open VS Code** and select **File → Open Folder…**, then choose the project folder (`googl_eda_project`).

2. **Activate the virtual environment** in VS Code’s integrated terminal:

   ```bash
   cd /path/to/googl_eda_project
   source .venv/bin/activate    # or the Windows equivalent
   ```

3. **Open the notebook file** `googl_eda.ipynb` in the VS Code editor. VS Code will detect it as a Jupyter notebook.

   * Select the Python interpreter inside `.venv` when prompted.

4. **Run the cells** in order:

   * The initial cells load the data, convert price and volume columns to numeric types, and inspect the structure.
   * Later cells compute summary tables for price, returns, and moving averages, then produce four visualizations:

     1. **Closing Price Over Time**
     2. **Closing Price + Moving Averages**
     3. **Histogram of Daily Returns**
     4. **Trading Volume Over Time**

5. **Review the outputs** directly in the notebook interface.

---

## 📑 Key Notebook Steps

1. **Data Loading & Conversion**

   * Load the CSV file and sort by date.
   * Convert `Open`, `High`, `Low`, `Close`, and `Volume` columns to numeric types, ensuring no string values remain.

2. **Data Inspection**

   * Display the first few rows to confirm column names and data types.
   * Generate summary statistics and check for any missing values.

3. **Calculate Derived Metrics**

   * Compute daily percentage returns based on closing price.
   * Calculate 50-day and 200-day moving averages of the closing price.

4. **Visualizations**

   * Plot the closing price over the entire 5-year period.
   * Overlay 50-day and 200-day moving averages on the closing price plot.
   * Create a histogram showing the distribution of daily returns.
   * Plot trading volume over time.

---

## 📝 Customization & Next Steps

* **Filter by date range**: Zoom in on specific periods (e.g., a single year) by subsetting the DataFrame before plotting.
* **Add more technical indicators**: Examples include Bollinger Bands, exponential moving averages, RSI, MACD, etc.
* **Time-series forecasting**: Use ARIMA, Facebook Prophet, or machine learning models on the closing price.
* **Volume-weighted metrics**: Calculate VWAP (Volume-Weighted Average Price) or other volume-based indicators.
* **Export results**: Save summary metrics to CSV or export plots to image files.

---

## 🔑 Troubleshooting

* **Non-numeric column errors**: Ensure price/volume columns are converted to numeric types. The notebook’s data-loading step enforces this conversion, with any invalid values becoming `NaN`. If unexpected `NaN`s appear, inspect those rows and either remove or correct them.
* **Missing data handling**: Drop or fill any rows where critical price information is unavailable.
* **Plots not rendering**: Confirm that the Jupyter extension is installed and that `%matplotlib inline` is enabled. Select the correct Python kernel in VS Code.

---

## 📄 License & Attribution

This repository is made available under the MIT License. The raw data originates from a publicly accessible Google (GOOGL) stock-price CSV covering the last five years. Feel free to use, modify, and share this analysis.

Thank you for exploring GOOGL’s historical performance!
