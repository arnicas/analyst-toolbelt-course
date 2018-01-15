# Week2 Analyst Toolbelt : Pivot Tables

## Goals
  * Making a pivot table with rows
  * sorting
  * top 10
  * Columns and Rows
  * Nesting
  * calculations other than count
  * time groupings

### Pivot Tables like Tall, Raw Data   
***Hunting Accidents file...***

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/1.png" width="900" height="425">  

 Pivot Input data is as on the right...
“Wide” data
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/2.png" width="600" height="410">  
                                                    “Tall” or “Long” data   

This is actually a tabular summary on the left. Pivots want the right side of this pic. (Pic from Spreadsheet page link below.)

## Finding the Pivot Table Command  

1. Find and Click the PivotTable (“Table Croisée”) on the ribbon toolbar or menu.  
2. *On Windows,* check the “Insert” Ribbon Tab.   
	*On Mac,* the “Data” Ribbon Tab.  
3. Also look at the menus (check Insert and Data menus).  

You should get the dialog:  
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/3.png" width="600" height="461">   
 *Note: Every column needs a label for it to work!*

4. Click OK (after making sure it shows your selection.)  

On Mac, it makes a “default” pivot table.   
It should show the “Builder” open. The command to open it is on top on the ribbon (in case you lose it/close it).
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/4.png" width="600" height="439">   

If you have items in your builder, drag them “out” to empty it. Goal is to start from empty:

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/5.png" width="600" height="445">   

The parts of the builder dialog:

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/6.png" width="400" height="415">   

5. Do this: Drag “Primary Type” into both Rows and Values:

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/7.png" width="600" height="559">   

By default, it produces a Count of each Primary Value.  
And the row labels are alphabetic.  

**A quick pivot can reveal a need to clean... Keep an eye on the results you see!**

This is another data set: *Hunting Injury Data – VictimACTIVITY (Victim Activity) by Count of WOUNDs*  

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/8.png" width="600" height="676">   

Might decide to group these – by fixing the label in a copy of the raw data.

6. You can change the sort order
On Windows, right click inside a cell in Values  
On Mac, click the Sort button in the Data tab.  

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/9.png" width="600" height="644">   

###### Example 1- show the top primary crimes in order, descending

 Let’s do that with chi2.csv, our Chicago dataset.

*Result:*   
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/10.png" width="250" height="551">   

  * Top 10... on Windows:
Right click on first column item, and you’ll see Filter > Top 10...
(or filter by other options!)  
Get the top 10 crime types.   

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/11.png" width="400" height="556">   


  * Top 10 on Mac:  
Pick Menu on Row Labels, Choose the menu beside “By Value”...

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/12.png">   

https://www.techonthenet.com/excel/pivottbls/top10_2011.php

###### Exercise 1- Do the same operations with Streets now (your created field)  
1. *What is the street with the most crimes? What are the top 10?*


Now Add “Arrest” to columns   
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/13.png">   

2. *What if we wanted to find out which crimes had the most arrests?*

Make Arrests your columns, and the primary type the rows. Sort by Arrests, True.

*Result:*
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/14.png" width="300" height="337">   


### Filters
If you want to dig into a particular type of data, you can make a filter.   
Drag “Primary Type” into the filters area — it will appear above the pivot results —


<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/15.png" width="282" height="450">   

and set it to Narcotics.   
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/16.png" width="200" height="93">   

### Nested Rows
If you want to learn more about each ROW (or column) of data, you can add another variable to the same group.       
Try adding Location Description to the Rows under “Street”:  
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/17.png" width="400" height="618">   

**Feel free to change the filter!**

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/18.png" width="400" height="307">   

 Now try...

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/19.png" width="400" height="436">   

 What’s interesting there?


## Pivots with Quantitative Data

:zap: **This file is due for homework.** :zap:

*What if we want a calculation or combination of quantitative numbers, instead of Count of qualitative data?*
For instance, if you have numeric data like Sales figures over time, or rainfall per month.

**Open Paris_Rainfall_Unpivoted.csv** in a tab.   

1. Create a pivot table on a new tab (empty all the Builder fields).
2. Set it up this way... Year and Value:
  * click on the option for Values and edit it to be SUM instead
  * With numeric data, you can summarize by other calculations than count.

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/20.png">   

3. Now sort by Values, descending.
Call this tab “annual_sum”
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/21.png" width="200" height="403">     


4. Now do average per year:
If you sort descending by Total, what’s the top year?  
Call this tab “annual_avg"
<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/22.png" width="200" height="280">   

5. How would we get to the original data we “unpivoted”?
Call this tab “by_month”

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/23.png">

## Grouping & Dates

We can “group” numeric data to make a manual histogram or to handle date ranges.  

On Mac: If you have years in your row labels, with your mouse on one date,
right click to open the group option.

On Windows: try the menu above

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/24.png" width="400" height="404">

1. Group Years by Centuries
Call this tab century_totals

<img src="https://github.com/arnicas/analyst-toolbelt-course/blob/master/week2/week2_pic/25.png" width="800" height="417">

2. Now filter by months...
Set the filter to Jan, Feb, and Dec.   
Set your Aggregation to Mean.   

Call this tab “mean_winter”   

***Your file should have these tabs:***
  * annual_sum
  * annual_avg
  * by_month
  * century_totals
  * mean_winter

> Video recap of pivot functionality - for Windows,but the same principles:
> https://www.youtube.com/watch?v=Vx-Fuw46VbY
