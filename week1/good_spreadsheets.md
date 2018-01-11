

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
