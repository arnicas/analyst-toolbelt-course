# VLOOKUP and HW

##  Lookup formulas

In place of SQL joins, in Excel we have **lookups** — where we use one table to “look up” another value to add a column to a table

**VLOOKUP** and **HLOOKUP** are the usual examples.
VLOOKUP is more common (vertical look up) FRENCH: **RECHERCHEV**

### Tutorials

* http://www.gcflearnfree.org/excel-tips/how-to-use-excels-vlookup-function/1/
* https://support.office.com/en-us/article/VLOOKUP-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1
* You can search for more - very common question.

#### Examples

In your files, *VLOOKUP_Examples.xlsx*

First is a one sheet example, then there are 2 sheets plus some IF statements.


### Handling errors

If there’s no match in the lookup table, you get an error #NA in Excel.  
You can put an **IFERROR** test here and return “NONE” if you have an error!

### Reminder about Formula references

 *A2 vs $A2 vs $A$2*  
Be careful to use absolute references ($A$2) in your VLOOKUP second argument, because you don’t want the lookup range to change.
