# Netflix Movies and TV Shows — Data Cleaning Task

## Dataset
- **Source:** Netflix Movies and TV Shows Dataset from Kaggle
- **Tool Used:** Microsoft Excel(Power Query), Notepad++

---

## Cleaning & Preprocessing Steps

1. **Removed Duplicates**  
   - Removed duplicate entries based on the `show_id` column using Excel’s `Remove Duplicates` tool.

2. **Renamed Headers**  
   - Changed eg:-`show_id` to `Show_Id` for better readability and uniform formatting across columns.

3. **Fixed File Format Issue with Notepad++**  
   - Resolved a format-breaking issue in the `Show_Id` column caused by extra quotes (e.g., `Flying Fortress`) using Notepad++.
   - Cleaned delimiters and ensured the CSV opens correctly in Excel.

4. **Handled Missing Values**  
   - Filled missing values in `Director` and `Country` columns with **"Unknown"**.
   - Replaced blanks in `Cast` column with **"No Cast Info"** for clarity and consistency.

5. **Split Duration Column**  
  - Used `Text to Columns` in Excel to split the `Duration` column into:
     - `Duration_Value` (numeric)
     - `Duration_Unit` (e.g., "min", "Seasons")

6. **Lowercased Description Column**  
   - Converted all text in the `description` column to lowercase to maintain consistency in formatting and text analysis readiness.
   - [Reason: Converting descriptions to lowercase ensures consistency and avoids case-based mismatches during text processing or future filtering/searching tasks]

7. **Created a Duplicate Sheet for Category Mapping**  
   - Created a new sheet `Category Mapping` with only `Show_Id` and `listed_in` columns.
   - Split `listed_in` values (which had multiple genres per show) into **multiple rows**, and trimmed extra spaces for clean categorization.
   - [Reason: Creating a separate sheet for category mapping helps in genre-wise analysis by separating multiple categories per show into individual rows. This makes it easier to filter, group, or count shows by individual genres]




