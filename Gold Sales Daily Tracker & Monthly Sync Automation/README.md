# Gold Sales Daily Tracker & Monthly Sync Automation

## Overview

This project provides a streamlined Google Sheets solution to track daily gold sales with automatic date and time stamping and aggregate daily sales data into monthly summary sheets.

Using Google Apps Script, this system automates:

- Real-time logging of individual sales entries with date & time.
- Daily aggregation of sales data into monthly sheets with totals, averages, and profit calculations.
- Easy end-of-day synchronization with a single button click.
- Automatic clearing of daily logs while preserving necessary formulas for the next day.

## Features

- **Automatic date/time stamping** on sales entry.
- **Daily sales aggregation** for accurate reporting.
- **Monthly sheets** pre-populated with dates for easy data sync.
- **Custom timezone support** (default set to `Asia/Jerusalem`).
- **User-friendly UI** with a custom menu in Google Sheets.

## Setup Instructions

1. **Prepare your sheets:**

   - Create a `Sale Log` sheet for daily sales input.
   - Create monthly sheets (`January`, `February`, etc.) with column A containing every date of the month (`dd/MM/yyyy`).

2. **Add the Apps Script:**

   - Open your Google Sheet.
   - Navigate to `Extensions → Apps Script`.
   - Remove any existing code and paste the provided automation script.
   - Save and authorize the script.

3. **Usage:**

   - As you enter sales (grams sold), the date and time automatically fill in.
   - At the end of the day, click the custom menu `Daily Sync → Send to Monthly Sheet`.
   - The day's data aggregates into the matching monthly sheet, and the sale log is cleared for the next day.

## Important Notes

- The script timezone is set by default to `"Asia/Jerusalem"`. Adjust the timezone variable in the script to match your location for accurate timestamps.
- This setup can be reused yearly by updating the starting year in the monthly sheets and reapplying the process.
- You may optionally skip daily logging and input only the final daily data if desired.

## License

This project is open-source and free to use.

---

*Happy tracking!*
