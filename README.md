# E-Commerce-Sales-Data-Cleaning-Visualization

## Messy E-Commerce Data Cleaning-Visualization & Financial Analysis Pipeline

📌 Project Overview: In this project, I transformed a heavily corrupted e-commerce dataset into actionable business intelligence. The original data contained inconsistent dates, mixed currency formats (USD/TL/EUR), and text-based anomalies
🛠️ Technologies Used:

Python: Pandas, NumPy (For ETL processes) Logging

Data Visualization: Matplotlib, Seaborn

## 🔧 Techniques

**Anomaly Detection · Data Validation · Data Cleaning & Normalization**

- Normalized inconsistent date formats using controlled `datetime` parsing (`errors="coerce"`)
- Applied rule-based string cleaning for numeric fields without forcing regex-based solutions
- Separated numeric values from contextual metadata (currency)
- Verified price consistency using `UnitPrice × Quantity ≈ TotalPrice`
- Flagged invalid or ambiguous records rather than auto-correcting them

> Regex was intentionally avoided in the main pipeline to improve readability.  
> A minimal example is provided for demonstration purposes.

## Comprehensive Analysis 
![Display](Visualization%20Outputs/ecommerce_analysis_dashboard_v2.png)
(Instance , not in full form)

![Display](Visualization%20Outputs/order_status_distribution.png)

### The Solution (My Methodology): I engineered a robust cleaning script to automate the standardization process:
Algorithmic Formatting: Wrote a custom logic (visible in the portfolio images) to dynamically detect and convert decimal separators based on index positions, preserving the mathematical value of prices.

Robust Date Parsing: Standardized all temporal data into ISO 8601 format, handling errors and missing values gracefully.
Data Validation: Implemented checks to ensure no data was lost during the transformation from "Before" to "After."
