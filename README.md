# American Guest House Convention Guest Analysis

This code analyzes convention names and corresponding check-in dates from multiple CSV files. The analysis focuses on identifying similar convention names and understanding the time difference between the booking date and the check-in date.

## Tools and Libraries Used

- **Pandas**: Used for data manipulation and analysis.
- **Pathlib**: Used for working with file paths.
- **NumPy**: Used for numerical operations.
- **Fuzzywuzzy**: Used for fuzzy string matching.
- **Datetime**: Used for working with date and time.
- **Dateutil.parser**: Used for parsing date strings.

## Data Loading and Cleaning

The script loads convention name data from three CSV files corresponding to different years (2018-2019, 2020-2021, 2022-2023). The data is concatenated into a single DataFrame for further analysis. Convention names are converted to lowercase and stripped of leading/trailing whitespaces for consistency.

## Similar Convention Name Detection

The script identifies similar convention names by considering both string similarity and check-in date proximity. Acronyms in convention names are also taken into account. The results are stored in a dictionary (`similar_values_dict`) where each unique convention name is mapped to a list of similar names.

## Similar Convention Name Counting

The script counts the occurrences of similar convention names and stores the counts in a dictionary (`similar_values_count`). The counts are then sorted in descending order.

## Time Difference Analysis

The script calculates the time difference (in days) between the booking date and check-in date for convention names. The results are added to the DataFrame, and the DataFrame is sorted based on the time difference.

## Data Output

Three DataFrames are generated during the analysis:
1. `similar_values_df`: Contains counts and unique check-in dates for similar convention names.
2. `sorted_by_most_common_names`: Contains convention names filtered to the most common ones, sorted by convention name.
3. `sorted_by_days_reserved_before_checkin_date_df`: Contains convention names sorted by the time difference between booking and check-in dates.

The script prints these DataFrames for visual inspection and can save them to CSV files for further use.

Note: The final output DataFrames can be saved to CSV files using the provided code in the comments.
