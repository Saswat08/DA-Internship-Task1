# DA-Internship-Task1

Initial Dataset Info
Original rows: 8,809

Columns: 12

Common issues: missing values, inconsistent formatting, and duplicates.

 Cleaning Steps Performed

1. Removed Duplicate Records
Used drop_duplicates() to remove exact duplicate rows.

This helps avoid overcounting entries.

2. Handled Missing Values
Filled missing values in key descriptive columns with "Unknown":

country, director, cast

Dropped rows where date_added or rating was missing:

These are important for time-based and content-type analysis.

Unnamed columns were removed

3. Standardized Text Fields
Removed leading/trailing whitespaces in:

title, director, cast, country, rating, listed_in

Ensures consistent grouping and filtering.

4. Parsed Dates Correctly
Converted the date_added column to proper datetime format.

Dropped rows where the date couldn't be parsed.

5. Reset the Index
After dropping rows, the DataFrame index was reset for consistency.

 Final Result

Cleaned rows: 8,795

Data is now:

Consistently formatted

Free from duplicates

Missing-critical fields handled

Date fields ready for analysis

