
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
 