# Automatic Data Quality Assessment Dashboard

This dashboard is an interactive tool designed to evaluate the quality of datasets stored in local data repositories. Built using Plotly Dash, it supports various file types and provides rich visual and statistical insights to assist users in identifying data issues such as incompleteness, duplicates, outliers, and distribution anomalies.

## Features

### 🗂️ 1. Loading and Analyzing Data Repositories

#### 📁 Repository Setup
Two local data repositories were simulated using a diverse set of file types including `.csv`, `.tsv`, `.json`, `.jsonl`, and `.txt`. This simulates a real-world data lake environment.

#### 📊 Repository Overview
Upon loading, users see a summary of:
- Repository name
- Size
- Number of files

This initial context helps users understand the data's scale and complexity before diving deeper into quality analysis.

---

### 📋 2. Data Repository Summary Table

A central table summarizes key metrics per file:
- File size (MB)
- Volume (rows × columns)
- Completeness score
- Uniqueness score
- Outlier percentage
- Aggregated data quality score
- Quality-based file ranking

#### Interactive Features:
- **Sorting** by any column
- **Filtering** based on attributes like file size, extension, or quality scores

Users can select any file from this table to view a detailed, column-wise breakdown of its data quality.

---

### 📂 3. Detailed File Analysis

#### 🧭 Navigation
After selecting a file, a detailed view provides:
- File summary (name, size)
- Sidebar with column names for attribute-level analysis

#### 📈 Attribute Analysis
Each column's characteristics are dynamically analyzed:

- **Index Detection**: Determines if a column is a potential index or candidate key.
- **Distribution Visualization**:
  - **Numeric Columns**: Histogram
  - **Categorical Columns**: Pie chart (if uniqueness ≤ 10%)

##### 🔍 Interactive Visualization
- Zoom, pan, and sliders for fine-grained analysis

#### 📉 Statistical Summary
Each attribute also displays key metrics:
- Mean, median, min, max
- Standard deviation, count (non-null)
- Mean/median imbalance (skewness indicator)
- Skewness & kurtosis (shape of distribution)

---

### 🚨 Outlier Detection

Outliers are identified based on column type:
- **Categorical**: Low-frequency values flagged
- **Numeric**: IQR-based method  
  \[
  \text{Outlier if: } x < Q1 - 1.5 \times IQR \text{ or } x > Q3 + 1.5 \times IQR
  \]

Outlier table includes:
- Column name
- Expected value (mean or mode)
- Row index for locating issues

#### ➕ Column Extension Technique
Inspired by Pit-Claudel et al. (2020), this enriches each column with derived features (e.g., day of week for date fields) to improve anomaly detection in both numeric and categorical data.

---

## 📂 Dataset Compatibility

- Accepts `.csv`, `.tsv`, `.json`, `.jsonl`, `.txt` formats.
- Designed for real-world repositories with heterogeneous file structures.

---

## 🖼️ Visualization Stack

- Plotly Dash for UI and interactivity
- Histograms, pie charts, heatmaps, and bar plots
- Interactive filtering, zoom, sliders

---

## 🧪 Preprocessing Techniques

- Type inference and casting
- Null value analysis
- Frequency analysis
- Outlier detection using IQR and frequency-based logic
- Column enrichment for better semantic understanding

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

---

## 🙏 Acknowledgments

- [Plotly Dash](https://dash.plotly.com/)
- [Pandas](https://pandas.pydata.org/)
- [NumPy](https://numpy.org/)
- [Seaborn](https://seaborn.pydata.org/)
- [Matplotlib](https://matplotlib.org/)
- Outlier Detection inspired by [Pit-Claudel et al., 2020](https://dl.acm.org/doi/10.1145/3318464.3380592)

---

Feel free to contribute or raise an issue if you'd like to suggest improvements or extensions!
