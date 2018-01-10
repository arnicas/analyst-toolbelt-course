# Homework

##Your Chicago Crimes data has been modified:

* Has a separate “date” and “time” column
* Has a column for Street, derived from the Block column. You must separate the 2 columns somehow and put the street name in its own column.
* Has new columns for Latitude and Longitude (as well as
the original column for location) with no parentheses or comma.
* Is sorted by the original “date-time” column in ascending
order, after you answer the quiz questions about it.  (This means earliest data/time first.  Make sure you have the month and date in the right order.)

Save the cleaned data as chi2.csv (in CSV format).

##Facebook ads data:

Import the csv file.

* Make a copy of the data on another spreadsheet tab. (You should always copy it when you modify it to clean it.) 
* Clean it by removing the rows that do not have numeric data in “audience_size”. 
* Remove also the bad row you can find by inspecting the identifiers and looking for non-numeric data in audience_size.
* Copy the path field to another column right beside path, and split that column into parts called path1, path2, path3, using the / as delimiter. (you must use text-to-columns).
* Use filtering and sorting to answer the questions on the quiz.
* Sort the file by Identifier, Ascending.
* Upload the new fixed data tab as a csv file called “fb_clean.csv”.
