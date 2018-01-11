
### Data is Often “Messy”.

 * Missing data
 * “Bad” values for missing data (e.g., a string code)
 * Non-normalized (names not upper case, “Street” vs “St.”)
 * Misspellings (or inconsistent spellings)
 * Dates aren’t of type “date” but of type “text” or “general” 
 * Merged fields — entire address in one cell, etc

***Recent Example***
Gene study errors blamed on Excel types.  
http://www.bbc.com/news/technology-37176926

We will "clean" it in the homework and now, using a copy of the data in a new tab.
 
### Basic Approach to Cleaning

>The basic steps for cleaning data are as follows:
>
>1. Import the data from an external data source.
>2. Create a backup copy of the original data in a separate workbook (or tab)
>3. Ensure that the data is in tabular format of rows and columns with: similar data in each column al columns and rows visible, and no blank rows within the range. For best resultats, use an Excel table.
>4. Do tasks that don't reaquire column manipulation first, such as spell-checking or using the Find and Replace dialog box.
>5. Next, do tasks that do require column manipulation. The general steps for manipulating a column are: 
>      * a. Insert a new column (B) next to the original colun (A) that needs cleaning.
>      * b. Add a formulat that will transform the data at the top of the new column (B).
>      * c. Fill down the formula that will transform the data at the top of the new column (B). In an Excel table, a calculated column is automatically created  with values filled down.
>      * d. Select the new column (B), copy it, and then paste as values into the new column (B).
>      * e. Remove the original column (A), which converts the new column from B to A.

*- https://support.office.com/en-us/article/Top-ten-ways-to-clean-your-data-2844b620-677c-47a7-ac3e-c2e157d1db19 -*

### Recap of that:
  * Copy raw data to a new tab/sheet or workbook. 
  * Work on that copy to clean it.
  * Use filters, do find/replace, etc on existing columns
  * Do things with formulae next: insert new column, copy formulae down, select and copy results, paste-as-vaues. Delete extra column.

Video examples: 
  * [Copy Data to new sheet](https://youtu.be/68onYmEcFdo)
  * [Data Cleaning with Find/Replace](https://youtu.be/hqP_3A1qcmI)
  * [Data Text Changes with a Formula](https://youtu.be/RoWn9s-lo_M)

***More Articles***

https://breakingintowallstreet.com/biws/cleaning-up-data-in-excel/   
(strong reference sheets for keyboard shortcuts)   
http://trumpexcel.com/2014/08/clean-data-in-excel/   
Extensive tutorial:  
http://schoolofdata.org/handbook/recipes/cleaning-data-with-spreadsheets/   


### Cleaning: Text Replacements

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/price.png" width="300" height="333"> 

These are not numbers. 
We can clean by hand and/or using formula or find/replace.

***See Problem 4 of this: http://schoolofdata.org/handbook/recipes/cleaning-data-with-spreadsheets/***

Also see video: [Clean column with replace](https://youtu.be/hqP_3A1qcmI)


### Cleaning: How to Split Columns by A Character (Text-To-Columns)

You usually want one item of data per column.  Sometimes you need to simplify the data you have loaded, and separate items.

For Homework, you need to split this column into two.   
Create two columns from one, using a bunch of tools:

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/location.png" width="374" height="400">  

*How could we split this into Latitude and Longitude?*

#### Hints
  * Work on a new tab with a copy of your data!
  * Use text-to-column (split by comma) See video above. 
  * Select each resulting column and replace the “)” or “(“ by nothing 
  * Label the new columns as requested.

See video: [Text to Columns](https://youtu.be/xs4QmuhFgSo)
