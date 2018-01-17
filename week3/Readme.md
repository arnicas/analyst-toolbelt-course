# Week3 Analyst Toolbelt : Excel Charts and Graphs

### Data files used for this session :
  * Paris Rainfall.csv
  * Examples_Charts.xlsx
  * Superstore Sales

# Analysis tools

## Statistics
*Anscombe’s Quartet:http://en.wikipedia.org/wiki/Anscombe's_quartet *

Seeing Patterns  
*N.Yau, Data Points*

 The Data-Ink Ratio

 > “A visualization is more effective than another if the information is more easily perceived in it than in the other.”  

*Paraphrase of Jock Mackinlay, from full quote in A. Kirk’s*

## Visualizing Data

Leverage our amazing perceptual system....  

 *Slide from Noah Iliinsky*


 Bar charts are safe for almost everything, but....
>“There’s a strand of the data viz world that argues that everything could be a bar chart. That’s possibly true but also possibly a world without joy.”

*Amanda Cox, NYT (paraphrased)
http://freakalytics.com/blog/2013/05/10/joyful-circle-charts-or-informative-bar-charts-best-practices-in-visual-analytics/*

##### Example:
  * Political Exaggeration: Puerto Rican Crime Drop

*http://esolutionspr.com/DataVisualization/CrimeStatsChartAsPublished.png   
10 redesign by Alberto Cairo*

**Bar Charts always start their Y axis at 0!**  
Otherwise they are lying.  
:zap: *This will be on your quiz.* :zap:

## Encodings

*N.Yau, Data Points*

Recommended!  
*The Wall Street Journal Guide to Information Graphics – The Dos and Don′ts of Presenting Data, Facts, and Figures ; from Dona M. Wong*

## The Problem with Pie Charts

*Wikipedia entry on pie charts*

 3d Distortion
*From A.Kirk’s _ Data Visualization *

*Fig 6-11,from Iliinsky & Steele _ Designing Data Visualizations*

Pie Chart Rule:
>Don’t use them if you have more than 3-6 wedges, and label your wedges with the values. Avoid if you can, especially if any of the wedges are really Iny and hard to tell apart.

Design Process Tips
*N.Yau, Data Points*

## Making a Chart With Defaults
1. Select some data column(s)
2. Click the chart tab
3. Pick a chart type!

*Examples_Charts.xlsx*

## Parts of a Chart  

  * Title and Legend


  * Data Labels and Axes

## General Design Tips
* Only color sparingly - use a different one for the
* Remove or reduce saturation of grids/axes and ticks (especially remove ticks)
* Add annotation or label on “interesting” points
* Have useful titles and axes labels

We made a chart with defaults...
 1. some data column(s)  
 2. Click the chart tab  
 3. Pick a chart type!  

Now customize it.  
Click on the chart,  
Go to Chart Layout >> Format.   
Click in the Title Field on the Chart to Change it...

 Many more things you can customize...  

Click on parts of the graph, and then RIGHT CLICK, you will get menus to format:  
  * Axes
  * Gridlines
  * Legend
  * Text
  * data series
  * labels...

Highlights and Annotations

 Let’s go thru the first tab in *Examples_Charts File*

1. Custom Colors and Formatting   
  *(in Examples_Charts.xlsx)*  

 * Click once on a data element to select the whole series
 * Click a second Ime to select on data element
 * RIGHT-CLICK for this dialog and select Format Data:  
  Btw, avoid 3-D, glow, etc.

2. Add the Labels / Annotations

 * One click for all data bars, 2 clicks for a single bar,
 * then right-click, pick Add Data Label(s)
 * Default label is the value- But you can click inside it to edit the text as you like!

3. Format Data Labels

 * Right-click on the label(s) you want to adjust (color, $ sign, etc.).

Try it once or twice to get the right ones selected before you choose the menu item.

 4. Formatting the Axis: Number Type, Display, Ticks...

 * Right-click on chart element to get these menus.

**Important Under-the-Hood...**

 * Understanding Data Series in a Chart  
When you click on a chart, you’ll see the data fields in the spreadsheet outlined. Those outlines are draggable/resizable.

 * Even more importantly, the data series dialog:  
Click on the chart, and then the Select icon in the Charts tab.This dialog is how you add series, change labels, etc.

 * Tip: Inserting Text Boxes in Charts (on a Mac)  
With the chart **NOT** selected, use the Insert menu. Move the text box to where you want it on the chart.

## Excel Makeovers

###### 1. Cole Nussbaumer’s Students

Student Makeover examples:  
  - by BriSney Younger
  - by Marianne Siblini

*http://www.storytellingwithdata.com/2013/11/intro-to-information-visualization.html*

###### 2. Jon Schwabish Excel Remakes

 - Redoing a Bureau of Labor Statistics employment graph  
http://thewhyaxis.info/defaults/

 - Redoing a Gender Gap graph from NYT Economix blog: http://thewhyaxis.info/gap-remake/

## Fun Chart Types

- Stephanie Evergreen:
http://stephanieevergreen.com/how-to-make-dumbbell-dot-plots-in-excel/

- Slope Graphs: http://peltiertech.com/slope-graphs-in-excel/

- Small Multiples / Cycle Plots: Examples1 file

- Dot Plots with a helper tool  
Using PelIer Chart UIlity plugin
(http://peltiertech.com/UIlity20/), with customization.   
See Examples1 file.

- More Date Grouping power  
*Paris Rainfall - Year (Centuries)*

- Adding Trendlines
*Paris_Rainfall_graphs.xlsm*

## Conditional Formatting & Sparklines
### 1. Conditional Formatting:

 *Hunting Deaths file*
 Heatmaps in the media:  
http://graphics.wsj.com/infectious-diseases-and-vaccines/

### 2. Highlighting Cells

 Highlighting duplicates is very useful for comparing  overlaps or finding uniques.   
 Shoot injuries, for instance.

 You can go to town on formatting...

### 3. Sparklines  

 *In data set Paris Rainfall...*

  - In a cell, a tiny chart   
(concept from Tufe: http://www.edwardtufe.com/bboard/q-and-a-fetch-msg?msg_id=0001OR)

  - Insert or Chart tab:  
  - Add to the right of the months.  


### 4. Advanced Maneuver: “Interactive” Charts

The Developer Tab is added via the Preferences, Ribbon.

 These are a powerful way to deliver a report or explore yourself.... or build a simple prototype for an interactive project!

 *See Chapter 11, M. Alexander book file, or my tweaked copy in InteracIveExcel.xlsx*

## A Few Excel Charting Resources

* Excel Charting Do’s And Don’ts (Jon Peltier)  
http://peltiertech.com/WordPress/excel-charting-dos-and-donts/

* Jon Schwabish tutorial: Making Excel Graphs Better  
 http://www.slideshare.net/jschwabish/making-excel-graphs-better

* Book: Michael Alexander’s Excel 2007 Dashboards and Peltier Chart utility   
http://peltiertech.com/Utility20/
