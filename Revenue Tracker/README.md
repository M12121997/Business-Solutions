
# Financial Ledger - 2025

## Overview

The **Financial Ledger** is a simple yet efficient yearly financial tracker designed to help individuals or businesses track their daily financial transactions for the year 2025. It enables users to maintain detailed records of their **credit** and **cash** transactions, with a dynamically updated **total** for each month. The tool creates an Excel workbook with separate sheets for each month, a full year data sheet, and a summary sheet to visualize the financial information.

This project provides:
- Monthly financial tracking.
- A summary sheet that consolidates monthly data.
- A **stacked bar chart** for each month, as well as a yearly summary chart for visual analysis.
- Formatting for easy readability and dynamic calculations for monthly totals.

## Features
- Monthly breakdown of financial data (Credit, Cash, and Total).
- A full-year data sheet that dynamically pulls data from all months.
- Currency formatting (in NIS - New Israeli Shekel).
- Summary sheet that aggregates monthly data with a yearly total.
- Stacked bar charts for each month and a yearly breakdown.

## How It Works

1. **Data Generation**: 
   The code generates monthly financial records for 2025, including the date, day of the week, credit, cash, and total columns.
   
2. **Excel File Creation**:
   An Excel file, `Financial_Ledger_2025.xlsx`, is created with:
   - Monthly sheets (January - December 2025)
   - A Full Year Data sheet (consolidated data from all months)
   - A Summary sheet (monthly totals and a stacked bar chart)

3. **Dynamic Updates**:
   - The totals for each month and year are calculated automatically in Excel.
   - The currency format for the credit, cash, and total columns is set to NIS.
   
4. **Charts**:
   - A stacked bar chart is created for each month and placed on its respective sheet.
   - A summary chart is placed in the Summary sheet to visualize the yearly breakdown.

---

## Customizing for the Current Year (2026)

If you'd like to use this project for the year 2026 (or any other year), you can easily adjust the code. Here’s how:

1. **Update the `generate_month_data` function**:
   In the function where we generate the data (`generate_month_data`), update the year to 2026 instead of 2025:
   ```python
   data_2026 = generate_month_data(2026)
   ```

2. **Change the Output File Name**:
   Update the output file name from `Bookkeeping_Journal_2025.xlsx` to `Bookkeeping_Journal_2026.xlsx` to reflect the new year:
   ```python
   save_path = os.path.expanduser('~/Documents/untitled folder/Bookkeeping_Journal_2026.xlsx')
   ```

3. **Adjust Sheet Names**:
   If you want the sheet names to reflect the new year, you can modify the title format inside the loop where the months are being added:
   ```python
   month_year = f'{month_name[:3]}-26'  # Change '25' to '26'
   ```

4. **Review and Re-run**:
   After making these changes, re-run the script, and it will generate an Excel file for 2026.

---

## How to Run

1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/yourusername/financial-ledger.git
   ```

2. Install required dependencies:
   ```bash
   pip install pandas openpyxl
   ```

3. Run the Python script:
   ```bash
   python financial_ledger.py
   ```

4. The Excel file, `Financial_Ledger_2025.xlsx`, will be generated in the specified path.

---

## Example Output

The generated Excel file will contain the following:
- 12 sheets (one for each month of the year).
- A Full Year Data sheet consolidating the monthly data.
- A Summary sheet showing monthly totals and including a stacked bar chart.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
