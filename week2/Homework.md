
# Homework Week2

Install a plain text editor if you don't have one. You need to be able to look at files and save them without introducing non-text characters like formatting symbols.  You can also verify that your CSV files are correct in a text editor.  (Several people had a problem with their formats and junk characters at the bottom of the file.  This is especially important when we get to SQL.)

Windows:
* Notepad++ is great. Notepad is ok too.

Mac:
* If you use TextEdit, you need to be sure to edit in Plain Text Format. This is very important. [Here are directions](https://www.tekrevue.com/tip/textedit-plain-text-mode/).
* There are other plain text editor options for writing code: Atom, Sublime Text, BBEdit...

Clean up the file in survey_data_spreadsheet_messy.xlsx following the principles in the [TidyData](TidyData.md) section.  Turn in a CSV file of your tidy data. Here are the requirements:

* Make the data long, not wide. (Do it with copy/paste, not a tool.)
* Put it on one tab, not multiple tabs, using long/tidy techniques. One table!
* Fix the date formats to be in the format of YYYY-MM-DD. ( AAAA-MM-JJ en francais). Fix any errors you think you see.
* Fix the measurements to be numeric values only.
* No color/annotations or notes outside of the data columns.
* Decide what to do about “bad data” including weird dates; fix them. Leave rows with some blank data — don’t delete them.
* Save as a csv file “species_clean.csv” and upload.

Upload your Paris Pivots file. It should have these tabs at least:

* raw_data (source for your pivots)
* annual_sum
* annual_avg
* by_month
* century_totals
* mean_winter
* a histogram of the month of May rainfall values (all years)
