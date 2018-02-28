
# Advanced Work with Tableau

Tableau needs LONG data (unpivoted).

Remember how we unpivoted data?  You need it to be long data, not summarized by columns.
Paris Rainfall unpivoted: Load that into Tableau.

Make this:

<img src="assets/TableauTips-d107d.png">


### Adding Annotations on Outliers

Make this a habit. It is good design.

Right click on the dot:

<img src="assets/TableauTips-d260d.png">

## Exploratory Charts - Examine Your Data

Always do counts on your data, using histograms and/or boxplots to see distributions.

 <img src="assets/TableauTips-89072.png">

 <img src="assets/TableauTips-29ffe.png">

 Make this:

 <img src="assets/TableauTips-19791.png">

 What about this:

 <img src="assets/TableauTips-895c9.png">

 ## Boxplots

 You need to uncheck "Aggregate Measures" again.

 <img src="assets/TableauTips-225bc.png">

 <img src="assets/TableauTips-9e04c.png">

 ### Calculated Fields

 Right-click on the background of "Dimensions" on the left to create a Calculated Field.  Enter this:

 <img src="assets/TableauTips-d0f19.png">

 [See the Help Docs link on calculated fields](http://kb.tableau.com/articles/knowledgebase/creating-groups-using-calculated-fields)

You can also copy-paste this:

````
If ([Month] = "Dec" or [Month] = "Jan" or [Month] = "Feb") then "Winter"
ELSEIF ([Month] = "Mar" or [Month] = "Apr" or [Month] = "May") then "Spring"
ELSEIF ([Month] = "Jun" or [Month] = "Jul" or [Month] = "Aug") then "Summer"
ELSEIF ([Month] = "Sep" or [Month] = "Oct" or [Month] = "Nov") then "Fall"
END
````

Then you can use it like other dimensions!

<img src="assets/TableauTips-f3c0e.png">

Seasonal Trends using this:

<img src="assets/TableauTips-78810.png">

You should be able to drag the reorder the seasons.





### Worksheet Setup

<img src="assets/TableauTips-ef06c.png">



### Another Map

Try the Wisconsin Shootings Excel file now.

<img src="assets/TableauTips-585ae.png">

<img src="assets/TableauTips-73060.png">

<img src="assets/TableauTips-cdf87.png">

<img src="assets/TableauTips-485e2.png">

Edit the Alias:

<img src="assets/TableauTips-9fa5e.png">

Group:

<img src="assets/TableauTips-19601.png">

Then fix colors:

<img src="assets/TableauTips-92344.png">

Cases by year:

<img src="assets/TableauTips-a1b05.png">

<img src="assets/TableauTips-35c52.png">


### Filtering

Right click on "Unknown" and exclude it for now:

<img src="assets/TableauTips-649bc.png">

Then make a filter for top 10.  Drag an item into "filters".

<img src="assets/TableauTips-73067.png">

### Labeling Things Properly

Good visualization design also means good text use.

* Changing your Axis labels or making aliases for data point labels for clarity
* Making a good title for the chart
* Adding text annotations and explanations


### Reminder: Copy Image to save it

For reporting with Tableau, use the Copy > Image option
and paste into your PPT/Word doc.
(You saw how bad the PDF export is.)

<img src="assets/TableauTips-b239e.png">
