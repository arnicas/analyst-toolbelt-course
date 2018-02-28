# Tableau with SQL

**Make sure you also have a SQL client, e.g : MySQL Workbench (both platforms) : https://www.mysql.fr/products/workbench/**


<img src="assets/TabSQL1.PNG" alt="Tableau" width="60%">

### Setting up the connection
Let's now add a connection. Our SQL host informations are :
* Server : analyst-toolbelt.cn119w37trlg.eu-west-1.rds.amazonaws.com
* Username : emlyon1 or emlyon2
* Password : student1 or student2

<img src="assets/TabSQL2.PNG" alt="setup" width="60%">

### Drivers download
You might need to install drivers.
You will get a link to download them - pick your
platform and choose your connection type.

<img src="assets/TabSQL3.PNG" alt="drivers" width="60%">


## Start working !
### Multiple Joins
Once you're connected, pick employees :

<img src="assets/TabSQL4.PNG" alt="dbemployee" width="50%">

<img src="assets/TabSQL5.PNG" alt="join" width="60%"/>

When you go to a sheet to make a chart, change employee number to a dimension. Since it's not a “value” but an id number, you can’t do math
on it.

Now perform the multiple joins :

<img src="assets/TabSQL6.PNG" width="60%">

Check out the rows carefully, what happened ? How can you handle that in your graphs ?

### Work on 'Titles'
First, make a chart showing how many employees have each title.

<img src="assets/TabSQL7.PNG" alt="count" width="60%">
Why is it cnt(emp no)?

Now duplicate that sheet and do avg(salary) by title.
<img src="assets/TabSQL8.PNG" alt="average" width="60%">

Right click under Measures and pick “Create Calculated Field”.
<img src="assets/TabSQL9.PNG" alt="calculated" width="50%">

### Working on Dates
Create a new measure for Date Differences in Tableau: http://kb.tableau.com/articles/knowledgebase/differencedates-one-date-field.

<img src="assets/TabSQL10.PNG" alt="function_date" width="50%">    
Now use a ShowMe histogram to check this data : On a blank sheet, open show me and click on your new Measure (“Time in Dept”).     

<img src="assets/TabSQL11.PNG" alt="histogram" width="50%">      
You must have this :

<img src="assets/TabSQL12.PNG" alt="histo_results" width="60%">   
Weird results. What’s going on? Go back to your original data.

Their “to_date” is impossible - it must mean “still employed.”     
<img src="assets/TabSQL13.PNG" alt="tofilter" width="60%">   
You might need to filter these values out.

### Adding a data source to a database
Let's add a data source for *movies*.    
<img src="assets/TabSQL14.PNG" alt="data_source" width="60%">

Pick movies.    
<img src="assets/TabSQL15.PNG" alt="movies" width="60%"/>    
But if you try to make a chart, it’s really slow :(

<img src="assets/TabSQL16.PNG" alt="query" width="60%">  
Make sure you preview your results before you hit ok.

### Back to queries
**Do a query for movies with the word “Action” in their Genres.**  
After it succeeds, join with Ratings (you need to fix Ratings so it's decimal !).  
Filter so that there are at least 5 ratings per movie in your chart.

 ***
Note that you can have multiple data connections
and queries in one workbook.
Use the menu by the disk on the right to connect to a new table/query/db. You might want to name it!

<img src="assets/TabSQL17.PNG" alt="note" width="50%">    
Tip: Use a SQL client while you use Tableau, so you can more easily understand what’s in your tables and how they related.
