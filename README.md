# DA-Internship-Task1

Initial Dataset Info
Original rows: 8,809

Columns: 26

Common issues: missing values, inconsistent formatting, and duplicates.

 Cleaning Steps Performed
1. Fixed Encoding Issue
The original file had non-UTF-8 characters.

Loaded using ISO-8859-1 encoding to handle special characters correctly.

2. Removed Duplicate Records
Used drop_duplicates() to remove exact duplicate rows.

This helps avoid overcounting entries.

3. Handled Missing Values
Filled missing values in key descriptive columns with "Unknown":

country, director, cast

Dropped rows where date_added or rating was missing:

These are important for time-based and content-type analysis.

4. Standardized Text Fields
Removed leading/trailing whitespaces in:

title, director, cast, country, rating, listed_in

Ensures consistent grouping and filtering.

5. Parsed Dates Correctly
Converted the date_added column to proper datetime format.

Dropped rows where the date couldn't be parsed.

6. Reset the Index
After dropping rows, the DataFrame index was reset for consistency.

 Final Result
Cleaned rows: 8,795

Saved to: netflix_titles_cleaned.csv

Data is now:

Consistently formatted

Free from duplicates

Missing-critical fields handled

Date fields ready for analysis

