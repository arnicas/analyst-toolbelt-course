
Homework

Turn in your .sql or .txt files (no Word or RTF files) with ";" at the end of each query. Use comments to identify which query is which homework question. (Look at last week's instructions for how to do comments in SQL files.)  Again, we will run them!  They must run for us.

"Use Chinook;" for these:

1. How many tracks does each playlist contain? order by playlist id ascending.
2. What playlist has no tracks?
3. What tracks are in the playlists that have only one song in them? Use a join and get the track names.
4. Count the genres of the tracks in each playlist. Order by count desc and show count and playlist columns.
5. What are the 10 most frequent artists appearing in the playlists? (Get names and counts as columns.)
6. Get the count, average price, and avg length (in SECONDS, this means math!) of all the mediatypes in tracks. Also return the name of the media types.
7. What are the 10 longest (time duration) MPEG audio mediatype tracks?

Use the movies database.  Put "Use Movies;" in your file and execute it.

1.  Find the top 10 tags that were used the most. Sort descending by count.
2.  Find the userid’s of the top 10 people who created the most tags and how many they each created. We need the id's and the counts for each.
3.  Find the 10 movies with the highest avg rating (return the title, rating count, and avg rating) - but limit it to movies with more than 4 ratings only (i.e., not 4, but 5 or more)! order by rating value, descending.
4.  Report the avg. rating and count of movie titles with genres that include “Action”.
