# Week1: Excel Basics

## Intro to Excel and Cleaning Data
### Why Excel?
  * Everyone everywhere uses it in business. 
  * It’s a great tool for exploratory data analysis
  * You can use it to make CSV files for other tools, and use in Python/R/Javascript apps
  * It has some powerful capabilities including charts,formulae, stats, filters, etc
  * It can be used for reporting, analysis, charts, 2 interactivity...

### Data Analysis Skills
http://www.datascienceweekly.org/articles/you-can-be-a-data-analyst-without-doing-heavy-math
https://www.quora.com/What-Excel-skills-and-formulas-does-a-business-analyst-need

This course is not much about math, and more about data organization, cleaning, and tools available to you to save you a lot of time.
   
### Good practices and bad: multiple tables on one sheet is bad.
![Good_bad_practices](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/good_bad.png)



survey_data_spreadsheet_messy.xlsx 

### Separating data, analysis and presentation
> One of the most important concepts in a data model is the separation of data, analyis and presentation. The fundamental idea is that you don't want your data to become too tied into any one particular way of presenting that data. 
>
> To get your mind around this concept think about an invoice. When you receive an invoice, you do'nt assume the financial data on that invoice is the true source of your data. It's merely a presentation of data that's actually stored ins ome database. That data can be analyzed and presented yo you in many other manners: in charts, in tables, or even on Web sites. This sounds obvious, but Exce users often fuse data, analysis, and presentation together.
>
>For instance, I've seen Excel workbooks that contain 12 tabs, each reprensenting a month. On each tab, data for that month is listed along with formulas, pivot tables, and summaries. Now what happens when you're asked to provide summary by quarter? Do you add more formuas and tabs to consolidate the data on each of the month tabs ? the fundamental problem in this scenario is that the tabs actually represent data values that are fused into the presentation of your analysis

  *– Excel 2007 Dashboards and Reports for Dummies –*

**3 Worksheets to separate your concerns:**

1. Raw data is just rows and columns.
2. Analysis: color, tables, formula referring to data sheet,... 
3. Charts 

![Data](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/Data.png) 


### A few “bad” things for raw data sheets
  * Color coded cells without clear data column values (why were they colored?) Merged cells
  * Header rows that aren’t at the top of the data
  * Multiple tables on one sheet
  * Too many tabs...
  * Metadata about the data on the same sheet Spaces in column headers
  * Bad “null” values
  * Multiple pieces of info in the same cell

More: http://www.datacarpentry.org/spreadsheet-ecology-lesson/02-common-mistak7es.html

### Presentation is different from raw data
  * “raw data” is the number, values, columns, rows... in plain format
  * Cells that are colored, highlighted, footnoted, graphs etc — are presentation and analysis tools, not the raw data.
  * The stuff that is saved in CSV files (plain text) is the raw data.




## Excel UI Tools

#### Windows looks very different.  (It’s actually better, too.)

Filter is on home tab   
![Home_tab_Windows](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/home_tab.png)

Insert Tab has charts/pivots on it....  
![Insert_tab_Windows](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/inster_tab_W.png)

The Data tab....   
![Data_tab_Windows](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/Data_tab_W.png)


#### Mac Excel is different
Right click on top toolbar to customize it...   
![Toolbar_mac](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/Toolbar_mac.png)

The Data Tab has filters, Pivots, Text to Columns, etc...  
![Data_tab_mac](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/Data_tab_mac.png)

**Make sure all your tabs are showing.**

  * Excel Preferences.... 
(under File **menu on Windows**, or the **main app menu on Mac**)

  * Click on Ribbon   
  ![Ribbon](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/Ribbon.png)

  * Be sure to scroll this window and check all of them.  
  ![check_tabs](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/check_tabs.png)

### Key UI Tools You Must Understand
 * Sorting
 * Filtering columns
 * Text-to-columns (used to split one column into many columns using some separator like a comma)
 * Pivot tables (tables croisées) 
 * Paste-Special (paste as values)




## Loading and Cleaning Data

### Data is Often “Messy”
 * Missing data
 * “Bad” values for missing data (e.g., a string code)
 * Non-normalized (names not upper case, “Street” vs “St.”)
 * Misspellings (or inconsistent spellings)
 * Dates aren’t of type “date” but of type “text” or “general” 
 * Merged fields — entire address in one cell, etc

***Recent Example***
Gene study errors blamed on Excel types.  
http://www.bbc.com/news/technology-37176926
 
### Basic Approach to Cleaning

>The basic steps for cleaning data are as follows:
>
>1. Import the data from an external data source.
>2. Create a backup copy of the original data in a separate workbook
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

***More Articles***

https://breakingintowallstreet.com/biws/cleaning-up-data-in-excel/   
(strong reference sheets for keyboard shortcuts)   
http://trumpexcel.com/2014/08/clean-data-in-excel/   
Extensive tutorial:  
http://schoolofdata.org/handbook/recipes/cleaning-data-with-spreadsheets/   





## Things I Do All the Time For Data Import, Analysis, and Cleaning
  * Filtering & sorting (goes without saying)
  * Split Data to More Columns (& Remove Duplicates)
  * Paste Values, Transpose... (especially working with formulae)
  * Pivot Tables (invaluable) - we’ll do them next week — they help you clean too, by showing you counts
  * Conditional Formatting during exploration (we’ll skip for now)

### Split Column (Text-To-Columns)
It is very common for a raw data set to be in a text format, not excel. Usually it will be in “CSV” or “TSV” format — “comma separated values” or “tab separated values.”

The difference is the character that separates the columns of data — for instance, this is CSV data with 2 columns (and no “header” title on the first row):

![csv_data](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/csv_data.png)


#### Let’s try the dialog that splits data by a separator value.

1. Click on File menu, then “Import....” and make sure this dialog says CSV:

![import_menu](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/import_menu.png)

2. If it is “tab separated”, you would choose text.
 
![delimiter1](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/delimiter1.png)

![delimiter2](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/delimiter2.png)
  
3. The “Types” Dialog:


You can also change your data types after importing, but there is one important issue here: **decimal number format**.  

![dialog_types](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/dialog_types.png)

Click on “Advanced...”

This issue caused a lot of difficulty to students last semester.  
![comma_issue](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/comma_issues.png)

:zap: :zap:  **All of my data files use international formatting for decimals: “point” or “dot”, not “comma.”** :zap: :zap:   
Make sure you change this to match my settings when you import text data with numbers.

4. The last dialog - if you are in a blank new workbook, use $A$1:
 
![import_data](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/import_data.png)

#### alternatively... some Excel versions can open CSV files for you:

In a blank workbook, click File menu, choose Open.... and change the dialog to show or enable “All files”:  

![all_files](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/all_files.png)

Navigate to and click on **ChiCrimes_Chicago2008.csv** to open it.   
Hopefully it will understand the csv format and load it correctly for you:
 
![Chicago_csv](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/Chicago_csv.png)

###### If it does not... all of it will be in one column, with no headers.

Then you can split the single column using the same dialogs, accessible from the “text to columns” button (under Data in Mac Excel, maybe home on Windows?)
 
![txt_col](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/txt_col.png)


### For Homework,   
You need to split this column into two.   
Create two columns from one, using a bunch of tools:

![location](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/location.png)

*How could we split this into Latitude and Longitude?*

#### Hints
  * Use text-to-column (split by comma)
  * Select each resulting column and replace the “)” or “(“ by nothing 
  * Label the new columns


### Text Replacements

![price](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/price.png)

These are not numbers.  
We can clean by hand and/or using formula or find/replace.

***See section 4 of this: http://schoolofdata.org/handbook/recipes/cleaning-data-with-spreadsheets/***





 
## Date/Time types

The data type is very importantin Excel.

Put your mouse in a column, and check the type in this dropdown.  
![types](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/types.png)
  
### Dates - Beware: 
When we import from CSV (or other text formats), Excel may guess “wrong” for the date/time fields.

> **A common problem**  
> One issue people frequently run into is that Excel occasionally misinterprets text fiels as dates.  
> An example is here :  
> ![Excel](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/Excel.png)  
> Be careful when entering dates, especially if you are importing from other data sources, to make sure that you "Jan-13" is being stored as January 13, 2013 !
***- http://www.exceltactics.com/definitive-guide-using-dates-times-excel/ -***
 
### Field Types - Especially Dates

![format_cells](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/format_cells.png)

### Formating Times as Custom...

![time_format](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/time_format.png)

Choose the time format you prefer from the Custom dialog.  
Try this with me on the Dates tab in the **ChiCrimes** file. 
Change the time to show am/pm.   
You must select the entire column, not just a single cell!  
Do that by clicking the C on top.  
Then choose “Custom...”
 
![custom_format](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/custom_format.png)

You should have a date option that includes AM/PM in the time.

![am_pm_dates](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/Dam_pm_dates.png)
 

###### What if we wanted the date and time in different columns?
Hint: Copy the Date column to 2 new columns. Reformat them.  
Rename the original col to “date-time” and the other 2 to “Date” and “Time”
Work on doing this now...   
![date](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/date.png)  
Notice that when you mouse in a cell, you see the full info.
 

### Now save this edited data as CSV. Call it “chi2.csv”.
  * Save As...  
  * Pick format CSV  
  * Give it the name “chi2.csv” 
 ![chi_csv](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/chi_csv.png)   
*Note: you are going to upload this file, so make sure you do this and work in it now.*
 
Now open that new file you made.

##### What do you see about the new “Date” and “Time” columns now?

**This is why we kept the original column with both...**  
Excel format saves more info than csv. Csv is a text format that preserves **only the text visible** in the cells.   
That’s why format types matter so much in the display in the cell. Make sure you have your data formatted with the info you need.

### More Advice for Dates
  * http://www.datacarpentry.org/spreadsheet-ecology-lesson/03-dates-as-data.html
  * Store your day, month, year separately (allows some special analysis by each) &/or
  * Be sure text fields are interpreted as date types correctly






## FILTERS (AND SORTING)! 
:zap: **YOU MUST MASTER THIS.** :zap:   


### Filters – One of the Most Important Tools

On Windows, over on the right side of Home. (Select all your columns first.)  
![windows_filter](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/windows_filter.png)  

Mac - the DATA tab.
![mac_filter](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/mac_filter.png)  

**You should be sure you select ALL the Columns before you pick the Filter icon.**


1. Click this triangle, it will highlight all of them.
2. THEN select the filter icon (it will be on Data tab or Home).
3. You should see the little sorting arrows on each column if you did it right.
![filter_step](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/filter_step.png) 

###### Exercises
Import the CSV version of ChiCrimes data (Chicago crime data).
Open ChiCrimes data and try filters:

![filter_chicrimes](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/filter_chicrimes.png) 

*A nice feature in recent Excels – saves you time and helps you troubleshoot your data:
![bottom_toolbart](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/bottom_toolbart.png) 
On Mac, you can pick one to show - sum is default, I think. Change to count.*

### Filters can be combined with sorting to get answers to questions.
1. Filter to show only Primary Type Burglary.
2. Then sort by Date, Ascending.
This puts the earliest date/time for the burglaries first, and the latest last.

![bulgary_filter](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/bulgary_filter.png) 

*What is the last burglary in this data?*

###### Exercises
 So, Using Filters, Tell Me... ln the Chicago crimes:  
  * What dates does this data cover?
  * How many offenses occurred at Animal Hospitals?
  * Did they occur at the same one?
  * What about at Airports? Did they occur at the same one?
  * Find all offenses that occurred anywhere on Whipple Street:   
  (Hint : Use a search or text filter.) 
    * How many where there? 
    * How many Whipple locations are there?
  * Look at just Sexual Offenses. Can you see anything interesting here?

*Warning: Don’t forget you might have filters in action and not see your whole data set. To turn off all the filters, just hit the filter button again:*
 ![filter_button](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/filter_button.png) 



### Useful for counting: Remove Duplicates
  
![duplicates](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/duplicates.png) 





## Formulae

### Text and Data Formulae to Clean 
(sadly, you must find the french versions)

Trim removes whitespace!
Proper makes title case.  

![formulae](/https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/formulae.png) 

> See video in https://breakingintowallstreet.com/biws/cleaning-up-data-in-excel/ 
 
### Reminder about formulae cell references

![references](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/references.png)  
A2 : relative reference  
$A2 : fixed column, relative 2   
$A$2 : fixed col and cell!  

> http://www.gcflearnfree.org/excel2013/relative-and-absolute-cell-references/2/ 

  
### Use a formula
Let’s try to split up the data on the street address for Chicago crimes.  
Copy the block column onto a new sheet. Enter this formula (but the french version, probablytrouver(‘ ‘;A2)... in b2:  

![find](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/find.png) 
 
### Paste As Values
After you finish your formula and get your results, it’s very important to copy the data and paste it as values — because leaving a formula in a cell can cause bad problems.
 
![paste](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/paste.png) 

### Problem with Formulas

  * They are not obvious to a reader of the sheet - you have to put your mouse in a cell to see them
  * If you move a column or cell, you can destroy the formula without noticing it. (The references will break)
  * It is easy to “mess up” your formula with an accidental click in a cell containing one, and then you have lost important data

After doing this operation...  
![street_col](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/street_col.png)   
You should have both columns - the original, and the new derived column (pasted as values, no formula in the cell!)
 
### Saving as csv: Remember Format

![save](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/save.png)   
Then you must say “continue” to the dialogs afterwards.... 

**WARNINGS**

  * When you save as CSV - make sure there are no filters applied.
  * If you save a filtered data table, it will save only the visible rows.
  * Save with a new filename, so you don’t overwrite the original data!