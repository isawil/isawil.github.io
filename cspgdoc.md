---
layout: narrative
title: Transferring data from Mimsy XG to Google Maps
author: Isaac Williams, for the Center for the Study of Political Graphics
---

## Background

When I worked at the Center for the Study of Political Graphics, I created a digital map that showed the location of origin for over 4,000 digitized collections items. Because creating the map was complicated at times, I created documentation showing permanent staff how to update the project when my internship was complete.

---

## Exporting data from Mimsy XG

To create a map, you first need a file that has collections information. Specifically, you need a spreadsheet that has data from Mimsy XG. Follow these steps to export this spreadsheet:

1. Open Mimsy XG and log in using your user credentials.
2. Navigate to the “search” tab and perform a “basic search.” Check the box for “digitized” to retrieve the list of all digitized items. Click the yellow lightning bolt icon to perform the search.
3. Navigate to the “tools” tab, and click “toggle grid/form view.” This will open a new screen showing all records in a grid. Select all of the records you want to map by highlighting records.
4. To select all records, click the first record at the top, hold down the shift key, and click the last record at the bottom. This will highlight every poster in the search results.
5. To select only specific records, click the first record you want to include, hold down `ctrl`, and individually select each additional record.
6. Then go to the “file” tab and click “export data.” Name the file, and export it in either comma-delimited export (CSV) or tab-delimited export (TSV) form.
7. You’ll be able to open this file in Microsoft Excel, Google Sheets, OpenRefine, or any program that can open spreadsheets.

## Editing the spreadsheet

Unfortunately, this spreadsheet is unusable in its current form. While it will open in Google My Maps, it’s not “clean” enough for it to be helpful. To make it usable, you will need to delete confidential information and information that is not immediately helpful to the user.

To do this, open the spreadsheet in a program such as Google Sheets or Microsoft Excel.

Remove columns that have inward-facing or confidential information, like in-house notes, so users cannot see it.

Delete these columns:
- Wall text
- Measurements
- Category
- Lot number
- Exhibition annotations
- In-house notes

When you’re done with your spreadsheet(s), export them (if created on Google Sheets), or save them (if you used Excel). Export or save each spreadsheet as an xlsx, or Excel, file. If you export or save them as a CSV or TSV file, Google My Maps will display far fewer posters than there actually are.

## Uploading to Google My Maps as a new map

Log into Google My Maps, and click “create new map.” If you do not already have a Google account, you will need to create a new account.

Upload each spreadsheet by clicking “import” under each layer. Google My Maps will ask you to select the columns that have location information, and which you would like to use as titles. Use “place made” for location, and “title” for title.

Check to make sure everything looks correct.

## Uploading to Google My Maps as additions to existing map

Adding new records to the existing map is similar to adding them as a new map. Instead of clicking “create a new map,” you will navigate to the edit page of the existing map.

Click “import” to import a new spreadsheet to the map. When prompted, select columns with location information and title information. Check to make sure everything looks correct.

There’s no need to save--Google saves changes automatically.

## Geolocating posters

For the map to display locations correctly, it has to recognize the locations in the spreadsheet. Google My Maps will recognize most location names that come from Mimsy XG, and will place these accurately.

However, a minority of locations will not be recognized, due to Mimsy’s formatting. Google My Maps will alert you when some locations are not recognized.

When this happens, click “open data table” under the spreadsheet you want to edit. Unrecognized locations will be highlighted in red. Edit these locations by hand, and they will display correctly.

## Adding metadata

You can add a title and description to the map. To do this, click on the title or description while in edit view. You will then be able to edit or add text. Click “save” to save your changes.

## Making the map public and embedding it

To put the map on the CSPG website, you do not need to have any experience with coding, and do not need to write any code of your own. Google generates an embed code that you can then paste into CSPG site files.

1. From the edit view, click on the three dots next to the map’s title.
2. Click on “embed on my site.”
3. A window will appear that has some code written in HTML. Copy the code.
4. Navigate to the folder that contains your site HTML.
5. Decide on which page you want the map to appear, and open the HTML file for that page (usually `index.html`).
6. Paste the code into the HTML file where you would like the map to appear.
7. Save the file, and send your changes to the site.

In a few minutes, the map will be visible on the site.

<!-- Default Statcounter code for Isawil.github.io
https://isawil.github.io -->
<script type="text/javascript">
var sc_project=11863955;
var sc_invisible=1;
var sc_security="f1c0a47a";
</script>
<script type="text/javascript"
src="https://www.statcounter.com/counter/counter.js"
async></script>
<noscript><div class="statcounter"><a title="Web Analytics
Made Easy - StatCounter" href="https://statcounter.com/"
target="_blank"><img class="statcounter"
src="https://c.statcounter.com/11863955/0/f1c0a47a/1/"
alt="Web Analytics Made Easy -
StatCounter"></a></div></noscript>
<!-- End of Statcounter Code -->
