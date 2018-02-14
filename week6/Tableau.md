
# Tableau Training


### Required for the Homework

http://www.tableau.com/fr-fr/learn/training

Use this data: http://www.tableau.com/sites/default/files/getting-started_data-sets_fr-fr.zip

Watch “Demarrage” and “L’Interface de Tableau.”  
For HW, you will recreate the charts in the “Demarrage” video.

https://www.tableau.com/fr-fr/learn/tutorials/on-demand/getting-started?reg-delay=6c7a19ee163152f99a781d669f828213

### In Class

Connect a datasource and choose "Excel."  Use Superstore.xlsx.

<img src="assets/Tableau-53032.png" height="200">

Drag the data sheet you want into the upper area.  Pick "Orders."

<img src="assets/Tableau-26a88.png">

Joins:  Drag "returns" up there too.

<img src="assets/Tableau-53b85.png">

You get an inner join by default.
Click on the join icon and change it to a Left Join.
What is the difference?

As soon as you have data visible, you can make a visualization sheet. Lower left corner:

<img src="assets/Tableau-a0633.png">

#### Dimensions and Measures

<img src="assets/Tableau-90823.png">

Categories, on upper left, are Text items, often discreet, ways to split your data numbers.

Measures, on the bottom left, are generally numbers.  Quantitative.

Read: http://www.datablick.com/blog/2017/2/24/tableau-padawan-data-types-vs-display-formats

In the upper right corner, click on "Show Me."  Click on a dimension or measure and watch it change.  It shows charts that may work with that kind of data.

<img src="assets/Tableau-44324.png">

Command-Click (on mac)
or CRTL-click on multiple
measures and/or dimensions to
see what is suggested for these variables.  Combined data elements are more interesting to chart.

Link: https://onlinehelp.tableau.com/current/pro/desktop/en-us/buildauto_showme.html

For example, click on these to see this:

<img src="assets/Tableau-1aae7.png">   <img src="assets/Tableau-191e8.png">

If you click on the bar chart in Show Me, you will get:

<img src="assets/Tableau-59fc6.png">

Just like in a pivot table, you can change your aggregation method for the bars:

<img src="assets/Tableau-b6087.png">

You can stack up rows and columns in your chart, using Drag and Drop. Start from Province and Product Category and then drag the others in:

<img src="assets/Tableau-6429a.png">

Timeseries are easy:

<img src="assets/Tableau-59a74.png" height="200">

Use the + in the Years Pill to get breakdowns:

<img src="assets/Tableau-1f2f5.png">

Keep clicking the + to expand:

<img src="assets/Tableau-a0f3a.png">

Now try dragging Product Category into a Row.  It will re-order for you:

<img src="assets/Tableau-dcf8b.png" height="150">

Now drag Product Category onto COLOR in the marks menu.

Use Show Me to put them all on the same axes (the one on the left):

<img src="assets/Tableau-d9b87.png">

Then change "Sum" to "Avg(sales)" in your rows:

<img src="assets/Tableau-f1e42.png">

You can customize the info tooltip ("infoboule") to add items, like Sum of Sales.

<img src="assets/Tableau-ef941.png">

### Histograms

Make a histogram of count of sales.  Click on sales and Show me:

<img src="assets/Tableau-2e292.png" height="150">

Gets you:

<img src="assets/Tableau-d0168.png">

Right click on the x axis, select "edit axis", and change the limits.

Edit the bins for the histogram using the created Dimension item:

<img src="assets/Tableau-4a512.png" height="150">

<img src="assets/Tableau-66862.png" height="150">

### Adding Annotations

Change to sum(sales) in your Row now:

<img src="assets/Tableau-982cc.png">

Add an Annotation for the Average to your chart -- drag it:

<img src="assets/Tableau-acf78.png">

### Inspect the Data

Right click on a bar, and click "view data":

<img src="assets/Tableau-01de9.png" height="150">

The binned data will show the current bins, but you have a tab on bottom for "full datat":

<img src="assets/Tableau-a91eb.png" height="200">

### Heatmap in tableau

Use this on in Show Me:

<img src="assets/Tableau-a72ec.png">

To get:

<img src="assets/Tableau-d4a21.png">

Add a Highlight/Sousligner to it:

<img src="assets/Tableau-dc3d4.png" height="150">

Change the color palette by clicking on Color, Edit Colors...

<img src="assets/Tableau-8c996.png" height="150">


### Maps

Control-click on two items, one a measure (quantitative) and one geographical. In Show Me, pick one of two maps:

<img src="assets/Tableau-889a9.png">

The one with the shaded countries (NOT the dots) is called a "Choropleth map."

Maps sometimes need location help in Tableau. If nothing appears, or if only some items appear,
you have to "Edit the Locations" to help Tableau identity them.  Click the small gray bullet in the lower right corner if it's visible.

<img src="assets/Tableau-36d84.png" height="300">

The country should be "Canada."

<img src="assets/Tableau-8367a.png" height="150">

Fix Saskatchewan spelling by hand:

<img src="assets/Tableau-e2701.png" height="150">

This shaded map is a "choropleth map."

<img src="assets/Tableau-3ceac.png">

The other type of map uses symbols (circles) sized relative to the amount of the quantity and placed at the location.  This works best for City or other local data. You will make something like this in the Getting Started Video, but I have added transparency to make it look better:

<img src="assets/Tableau-32316.png">


### Hierarchies in dimensions

You can drag items under other items to create nested hierarchy.

<img src="assets/Tableau-c041e.png" height="150">

Just like dates, hierarchies allow you to "drill down" into category levels:

<img src="assets/Tableau-9b724.png">

<img src="assets/Tableau-c6751.png">

### Scatterplots

There are a couple methods to make scatterplots in Tableau.  One is to just show all your marks, un-aggregated.  The default is for Tableau to aggregate and you will see only a single dot:

<img src="assets/Tableau-6ce49.png" height="200">

This is a hidden control on a menu:

<img src="assets/Tableau-0d06d.png" height="150">

Now you can see all your dots:
<img src="assets/Tableau-ab6d1.png">

You could add a trendline from the Analytics tab:

<img src="assets/Tableau-cb2a4.png">

To deal with the overlap of dots, the best solution is to use transparency.  Do it in the Color marks menu:

<img src="assets/Tableau-f5c6a.png" height="150">

You'll have colored trendlines if you break out your marks by a dimension like category or segment:

<img src="assets/Tableau-47324.png">

Another option for a Scatterplot is to use aggregration on the dots, using the "detail" menu item.  Here I've set the Category to both Color and Detail, which makes for 3 SUM aggregated dots:

<img src="assets/Tableau-c386f.png">

### Dashboards

Dashboards are created using existing Sheets in your workbook. You must have created the views you want to add to you Dashboard in advance.  You will see them in the Getting Started video.  There is a "Live Filter" in this one.

<img src="assets/Tableau-a83bc.png">

### Save as PDF

You can save the whole workbook as PDF for the Homework. It will not look good, but that's ok for the review.

<img src="assets/Tableau-31d20.png" height="200">

### Save a Single Chart Image

Right click on the background of a sheet, select "Copy," then Image...

<img src="assets/Tableau-2bfd0.png" height="200">

Then you can paste into a PPT or email for a client.

### Required for the Homework

http://www.tableau.com/fr-fr/learn/training

Use this data: http://www.tableau.com/sites/default/files/getting-started_data-sets_fr-fr.zip

Watch “Demarrage” and “L’Interface de Tableau.”  
For HW, you will recreate the charts in the “Demarrage” video.

https://www.tableau.com/fr-fr/learn/tutorials/on-demand/getting-started?reg-delay=6c7a19ee163152f99a781d669f828213
