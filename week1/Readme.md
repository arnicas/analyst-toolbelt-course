# Week1: Excel Basics

## Intro to Excel and Cleaning Data
### Why Excel?


  * Everyone everywhere uses it in business. 
  * It’s a great tool for exploratory data analysis
  * You can use it to make CSV files for other tools, and use in Python/R/Javascript apps
  * It has some powerful capabilities including charts,formulae, stats, filters, etc
  * It can be used for reporting, analysis, charts, 2 interactivity...

### Data Analysis Skills

A couple background references on being a data analyst:
* [You Can Be a Data Analyst Without Doing Heavy Math](http://www.datascienceweekly.org/articles/you-can-be-a-data-analyst-without-doing-heavy-math)
* [What Excel Skills Does a Business Analyst Need - Quora](https://www.quora.com/What-Excel-skills-and-formulas-does-a-business-analyst-need)


This course is not much about math and stats, and more about data organization, cleaning, and tools needed for basic functional data analysis in the office. We start with important Excel skills that I find many people don't know, and then we move on to SQL (**the most important analyst skill**), and a visual analysis and reporting tool, Tableau.


## Good Spreadsheet Behavior

Most of you are used to pretty formatted tables in spreadsheets, and spend a lot of time making things look nice.  This course is not about that, and in fact, I frown hard at it. If you submit homework with pretty table formatting, I will give you a lower grade.

Your first job is to understand what the "data" is in a spreadsheet. And how to work with it. And how to save it for others to work with it.

Please read: [Data Organization in Spreadsheets, Broman & Woo](http://www.tandfonline.com/doi/full/10.1080/00031305.2017.1375989). This is on the quiz.



### Good practices and bad: multiple tables on one sheet is bad.
<img src="week1_pic/good_bad.png" width="600" height="291">


### Separating data, analysis and presentation
> One of the most important concepts in a data model is the separation of data, analyis and presentation. The fundamental idea is that you don't want your data to become too tied into any one particular way of presenting that data. 
>
> To get your mind around this concept think about an invoice. When you receive an invoice, you do'nt assume the financial data on that invoice is the true source of your data. It's merely a presentation of data that's actually stored ins ome database. That data can be analyzed and presented yo you in many other manners: in charts, in tables, or even on Web sites. This sounds obvious, but Exce users often fuse data, analysis, and presentation together.
>
>For instance, I've seen Excel workbooks that contain 12 tabs, each reprensenting a month. On each tab, data for that month is listed along with formulas, pivot tables, and summaries. Now what happens when you're asked to provide summary by quarter? Do you add more formuas and tabs to consolidate the data on each of the month tabs ? the fundamental problem in this scenario is that the tabs actually represent data values that are fused into the presentation of your analysis

  *– from the excellent [Excel 2007 Dashboards and Reports for Dummies](https://www.amazon.com/Excel-2007-Dashboards-Reports-Dummies/dp/0470228148/ref=sr_1_2?ie=UTF8&qid=1515603609&sr=8-2&keywords=excel+2007+dashboard) –*

**You Need Minimally 3 Worksheets to separate your concerns:**

1. Raw data is just text rows and columns. No colors, no formulas, no merged cells.  Single table.
2. Analysis: color, tables, formula referring to the data sheet,... 
3. Charts, again on another sheet.

<img src="week1_pic/Data.png" width="600" height="549">

### Common mistakes in data in spreadsheets:

  * Color coded cells without clear data column values (why were they colored?)
  * Merged cells
  * Header rows that aren’t at the top of the data 
  * Multiple tables on one sheet
  * Too many tabs...
  * Metadata about the data on the same sheet
  * Spaces in column headers
  * Bad “null” values (don't have empty cells)
  * Multiple pieces of info in the same cell

More: http://www.datacarpentry.org/spreadsheet-ecology-lesson/02-common-mistakes/

### Presentation is different from raw data
  * “raw data” is the number, values, columns, rows... in plain format
  * Cells that are colored, highlighted, footnoted, graphs etc — are presentation and analysis tools, not the raw data.
  * The stuff that is saved in CSV files (plain text) is the raw data.
 
 :zap: Questions about this are on the quiz. :zap:


### Why Does Raw Data Matter? 

* Raw data is useable in multiple types of analysis, including reading in code like Python, R, or inserting into a database.
* Well-formatted data can be used in Pivot tables in Excel -- data with "extras" like summary rows or merged columns can't be used in pivots easily.
* Raw data can be saved as a simple text format (like CSV or TSV) for exchanges with other programs/people.
* Data that is not "raw" contains things can produce errors, like formulas, or hides important information (hidden columns and rows, formatting).

**Raw data is as close to plain text form as possible.  If you have pretty table formatting, colors, etc, your data is NOT RAW.**

Please read: [Data Organization in Spreadsheets, Broman & Woo](http://www.tandfonline.com/doi/full/10.1080/00031305.2017.1375989)

Among their advice:

* write dates like YYYY-MM-DD, 
* don't leave any cells empty,
* put just one thing in a cell, 
* organize the data as a single rectangle (with subjects as rows and variables as columns, and with a single header row), 
* create a data dictionary, 
* don't include calculations in the raw data files, 
* don't use font color or highlighting as data, 
* choose good names for things,
* and save the data in plain text file (e.g., CSV or TSV format).


## Key UI Tools You Must Understand in Excel for Data Cleaning & Reporting

 * Sorting
 * Filtering columns
 * Find-and-Replace in Columns
 * Text-to-columns (used to split one column into many columns using some separator like a comma)
 * Formulas to clean data
 * Paste-Special (for paste as "values")
 * Pivot tables (tables croisées) -- we will do next week.


### Excel UI Tools

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
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/Ribbon.png" width="400" height="322">   

  * Be sure to scroll this window and check all of them.  

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/check_tabs.png" width="400" height="330">  


## CSV Data: Importing Text Data Into Excel

We need some data to start with.  A common "raw data" file format is CSV, or "comma separated values."  (In France it is usually ";" separated.)

Video: [Import CSV](https://youtu.be/7U5WgW_mQ8o)

It is very common for a raw data set to be in a text format, not excel. Usually it will be in “CSV” or “TSV” format — “comma separated values” or “tab separated values.”

The difference is the character that separates the columns of data — for instance, this is CSV data with 2 columns (and no “header” title on the first row):

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/csv_data.png" width="111" height="250">   


#### Importing steps:

1. Click on File menu, then “Import....” and make sure this dialog says CSV:

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/import_menu.png" width="500" height="353">   

2. If it is “tab separated”, you could choose text. But you can also use CSV for tab separated data.
 

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/delimiter1.png" width="500" height="355">

2.b. Here you specify what the character delimiter is between your data columns. You can type in a special one in "other".

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/delimiter2.png" width="500" height="355">   

  
3. The “Types” Dialog:


You can also change your data types after importing, but there is one important issue here: **decimal number format**.  


<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/dialog_types.png" width="500" height="440">   

Click on “Advanced...”

This issue caused a lot of difficulty to students last semester.  

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/comma_issues.png" width="304" height="200">  

:zap: :zap:  **All of my data files use international formatting for decimals: “point” or “dot”, not “comma.”** :zap: :zap:   
Make sure you change this to match my settings when you import text data with numbers.

4. The last dialog - if you are in a blank new workbook, use $A$1:
 
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/import_data.png" width="400" height="202">  


#### alternatively... some Excel versions can open CSV files for you:

In a blank workbook, click File menu, choose Open.... and change the dialog to show or enable “All files”:  

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/all_files.png" width="500" height="403">  


Navigate to and click on **ChiCrimes_Chicago2008.csv** to open it.   
Hopefully it will understand the csv format and load it correctly for you:
 
![Chicago_csv](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/Chicago_csv.png)

###### If it does not... all of it will be in one column, with no headers.

Then you can split the single column using the same dialogs, accessible from the “text to columns” button (under Data in Mac Excel, maybe home on Windows?)

Video: [Text to Columns](https://youtu.be/xs4QmuhFgSo)
 
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/txt_col.png" width="250" height="73">  


## FILTERS (AND SORTING)! 
:zap: **YOU MUST MASTER THIS.** :zap:   

[Filter and Sort video](https://youtu.be/Mdvu1EziwRM)
  
On Windows, over on the right side of Home. (Select all your columns first.)  
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/windows_filter.png" width="80" height="100">    

Mac - the DATA tab.
![mac_filter](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/mac_filter.png)   

**You should be sure you select ALL the Columns before you pick the Filter icon.**

1. Click this triangle, it will highlight all of them.
2. THEN select the filter icon (it will be on Data tab or Home).
3. You should see the little sorting arrows on each column if you did it right.
![filter_step](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/filter_step.png) 

###### Exercises
Import the CSV version of ChiCrimes data (Chicago crime data), if you haven't yet.

Open ChiCrimes data and try filters:

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/filter_chicrimes.png" width="250" height="367">   

*A nice feature in recent Excels – saves you time and helps you troubleshoot your data:*     
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/bottom_toolbart.png" width="300" height="454">    
*On Mac, you can pick one to show - sum is default, I think. Change to count.*

### Filters can be combined with sorting to get answers to questions.
1. Filter to show only Primary Type Burglary.
2. Then sort by Date, Ascending.
This puts the earliest date/time for the burglaries first, and the latest last.

 
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/bulgary_filter.png" width="300" height="368">

*What is the last burglary in this data?*

Reminder: [Filter and Sort video](https://youtu.be/Mdvu1EziwRM)

###### Exercises in Class:

 So, using filters, tell me... ln the Chicago crimes:  
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

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/filter_button.png" width="100" height="68">

## Verifying: Date/Time types

The data type is very important in Excel.

Put your mouse in a column, and check the type in this dropdown.  

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/types.png" width="350" height="225">  

### Dates - Beware: 
When we import from CSV (or other text formats), Excel may guess “wrong” for the date/time fields.

> **A common problem**  
> One issue people frequently run into is that Excel occasionally misinterprets text fiels as dates.  
> An example is here :  
> <img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/Excel.png" width="300" height="89">   
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
 
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/custom_format.png" width="600" height="371">   

You should have a date option that includes AM/PM in the time.

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/am_pm_dates.png" width="500" height="494">   

###### What if we wanted the date and time in different columns?
Hint: Copy the Date column to 2 new columns. Reformat them.  
Rename the original col to “date-time” and the other 2 to “Date” and “Time”. Or use formulae.
  
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/date.png" width="350" height="305">   
Notice that when you mouse in a cell, you see the full date information.

### Now save this edited data as CSV. Call it “chi2.csv”.
  * Save As...  
  * Pick format CSV  
  * Give it the name “chi2.csv”

Video: [Save as CSV](https://youtu.be/uJ_cSdF8hkk)

<img src="week1_pic/chi_csv.png" width="300" height="131">

*Note: you are going to upload this file after the exercises, so make sure you do this and work in it now.*
 
Now open that new file you made. What do you see about the new “Date” and “Time” columns now?

**This is why we kept the original column with both...**  

Excel format saves more info than csv. CSV is a text format that preserves **only the text visible** in the cells.   
That’s why format types matter so much in the display in the cell. Make sure you have your data formatted with the info you need.

### More Advice for Dates

  * The advice in Browman & Woo is to save your dates in the international standard YYYY-MM-DD.
  * Article: [Dates as Data](http://www.datacarpentry.org/spreadsheet-ecology-lesson/03-dates-as-data/)
  * Store your day, month, year separately (allows some special analysis by each) &/or
  * Be sure text fields are interpreted as date types correctly

### Useful for counting: Remove Duplicates

A useful trick - removing duplicates to see what your unique field values are.
  
![duplicates](https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/duplicates.png) 

Video: [Remove Duplicates](https://youtu.be/SRpAdtKNXSY)

## Cleaning Data

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

## Formulae

### Text and Data Formulae to Clean 

Trim removes whitespace!
Proper makes title case.  Example in this video of cleaning a column to fix the case to "proper." (In French, "nompropre".)

Site with formula translations: http://dolf.trieschnigg.nl/excel/index.php

Video: [Changing Text with Formula](https://youtu.be/RoWn9s-lo_M)

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/formulae.png" width="400" height="385">    

> Also see video in https://breakingintowallstreet.com/biws/cleaning-up-data-in-excel/ 
 
### Reminder about Formulae Cell References

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/references.png" width="400" height="132">

Remember: 
  * A2 : relative reference : both may change when you copy the formula.
  * A$2 : fixed row, relative column -- will change when you copy column.
  * $A2 : fixed column, relative row -- will change when you copy row.
  * $A$2 : fixed column and cell, will not change when you copy formula.

> http://www.gcflearnfree.org/excel2013/relative-and-absolute-cell-references/2/ 

  
### Use a Formula to Extract Text

Let’s try to split up the data on the street address for Chicago crimes.  
Copy the block column onto a new sheet. Enter this formula (but the french version, probably "trouve(‘ ‘;A2)"... in b2:  

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/find.png" width="300" height="79">

Then you can use another formula to get the right end of the string,

* RIGHT(text, number_of_chars) [French: DROITE]
* LEN(text)  [French: NBCAR]

How would you combine them?  In one formula. Work with me!

Read: https://spreadsheeto.com/text-functions/


### After Formula Use: Paste As Values  

After you finish your formula and get your results, it’s very important to copy the data and paste it as values — because leaving a formula in a cell can cause bad problems.
 

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/paste.png" width="300" height="368">  

### Problem with Formulas

Why is it bad to leave formulas in the workbook in your cleaned data?

  * They are not obvious to a reader of the sheet - you have to put your mouse in a cell to see them
  * If you move a column or cell, you can destroy the formula without noticing it. (The references will break)
  * It is easy to “mess up” your formula with an accidental click in a cell containing one, and then you have lost important data

After doing this operation...  
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/street_col.png" width="250" height="134">    
You should have both columns - the original, and the new derived column (pasted as values, no formula in the cell!)
 
## Saving as CSV: Remember Format

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week1/week1_pic/save.png" width="500" height="505">  
Then you must say “continue” to the dialogs afterwards.... 

**WARNINGS**

  * When you save as CSV - make sure there are no filters applied.
  * If you save a filtered data table, it will save only the visible rows.
  * You will save any date strings in the format that is visible. This means you may lose information (minutes, seconds) if you aren't showing enough precision.
  * Save with a new filename, so you don’t overwrite the original data!

Video: [Save as CSV](https://youtu.be/uJ_cSdF8hkk)

After you have saved in CSV format, your workbook is called filename.csv. You will want to save it as an Excel workbook too, to save all the tabs! 

Note: In France/Europe, the format is more commonly ";" delimited, not "," (virgule), because of number formatting.  This is ok too.
