# Venice High App Data

The following are explanations for each of the fields used for the app data. It's best to edit the JSON files directly for small changes, and only edit and create a CSV file for a larger number of edits.

## Buildings
* name - Name of the building.
* latitude - Latitude coordinate from iOS map data.
* longitude - Longitude coordinate from iOS map data.

## Dates
* yy - Four digit year.
* mm - One or two digit month. Don't include 0 for single-digit months.
* dd - One or two digit day. Don't include 0 for single-digit days.
* s - Schedule number. 1=professional, 2=minimum, 3=no school

## Rooms
* number - Room number. Use abbreviation for longer names (e.g. EGYM for east gym).
* building - Must exactly match one building from the buildings list.
* floor - Floor number, either blank, 1, or 2.
* altid - Longer room name, used for shops and rooms without a number.

## Staff
* id - First two letters of first name and last name.
* prefix - Mr., Ms., or Dr.
* firstName - Staff's first name.
* lastName - Staff's last name.
* email - Staff's full email address.
* link - Right click on a staff's link to get group id.
* mata, sma, wlgs, alps, stemm - Status of magnet membership.
* p0, p1, p2, p3, p4, p5, p6, p7 - Must exactly match a room, or be CONF, /, WASC, UTLA, or RSP.

## Times 

* schedule - Regular, professional, or minimum. All lower-case.
* times - Array of time objects, described below.
* id - Periods should be p and the number. Nutrition=n and lunch=l. Passing period should be pp and the number of the upcoming period.
* sh - Starting hour. Should not start with a 0.
* sm - Starting minute. Should not start with a 0, but can be 0.
* eh - Ending hour. Should not start with a 0.
* em - Ending minute. Should not start with a 0, but can be 0.
* title - Title shown in the widget. Should be name of period or passing message.

*No CSV file as the array of objects can't be converted. Edit the JSON directly.

## CSV to JSON
[Convert CSV to JSON](http://www.convertcsv.com/csv-to-json.htm)

Use the following link to convert edited CSV files into JSON. Once converted, the files should be checked for null values. Any occurrences of null should be replaced with an empty set of double quotes (""). Commit the uploaded file to [GitHub](https://github.com/steets250/Venice-High-App-Data), and then the app will use the new data the next time that it is run.
