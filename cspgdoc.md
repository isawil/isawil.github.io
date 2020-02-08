---
layout: narrative
title: Documentation Samples
---

### CSPG Digital Mapping Documentation

## Summary

The Center for the Study of Political Graphics has a digital map of its digitized collections items. The map shows the location of origin for over 4,000 posters, and redirects users to catalog records for any posters they are interested in. The map is hosted on Google Maps, and uses collections data from Mimsy XG to generate locations.

This documentation describes how to update the map with new collections items and locations.

## Exporting data from Mimsy XG

To create a map, you first need a file that has collections information. Specifically, you need a spreadsheet that has data from Mimsy XG. Luckily, Mimsy allows users to export collections data. Here’s how:

- Open Mimsy XG and log in using your user credentials.
- Navigate to the “search” tab and perform a “basic search.” Check the box for “digitized” to retrieve the list of all digitized items. Click the yellow lightning bolt to perform the search.
- Navigate to the “tools” tab, and click “toggle grid/form view.” This will open a new screen showing all records in a grid. Select all of the records you want to map by highlighting records.
- If you want to map every result, you can click the first record at the top, hold down the shift key, and click the last record at the bottom. This will highlight every poster in the search results.
- If you only want to map certain results, you’ll need to select each record individually. Click the first record you want to include, hold down the ctrl key, and individually select each additional record.
- Then go to the “file” tab and click “export data.” Name the file, and export it in either comma-delimited export (CSV) or tab-delimited export (TSV) form.
- You’ll be able to open this file in Microsoft Excel, Google Sheets, OpenRefine, or any program that can open spreadsheets.

## Editing the spreadsheet

Unfortunately, this spreadsheet isn’t usable in its current form. While it will open in Google My Maps, it’s not “clean” enough for it to be helpful. We’ll need to delete some confidential information, and information that isn’t immediately useful to the user.

To do this, open the spreadsheet in a program such as Google Sheets or Microsoft Excel.

Remove columns that have inward-facing or confidential information, like in-house notes, so that users can’t see it.

Delete these columns:
- Wall text
- Measurements
- Category
- Lot number
- Exhibition annotations
- In-house notes

This information is important! But it doesn’t need to be in the map. If we include every column, the map will become unwieldy and less user-friendly. If a user finds a poster of interest, and wants to know the measurements, they can always contact CSPG or check the CSPG collections site.

When you’re done with your spreadsheet(s), it’s time to export them (if created on Google Sheets), or save them (if you used Excel). Export or save each spreadsheet as an xlsx, or Excel, file. If you export or save them as CSVs, Google My Maps may not recognize each item, and will display far fewer posters than there really are.

## Uploading to Google My Maps as a new map

With your spreadsheets ready, it’s time to plug them into Google My Maps! Log into Google My Maps, and click “create new map.” If you do not already have a Google account, you will need to create a new account.

Upload each spreadsheet by clicking “import” under each layer. Google My Maps will ask you to select the columns that have location information, and which you would like to use as titles. Use “place made” for location, and “title” for title.

Check to make sure everything looks correct.

## Uploading to Google My Maps as additions to existing map

Adding new records to the existing map is similar to adding them as a new map. Instead of clicking “create a new map,” you will navigate to the edit page of the existing map. Click “import” to import a new spreadsheet to the map. When prompted, select columns with location information and title information. Check to make sure everything looks correct. There’s no need to save--Google saves changes automatically.

## Geolocating posters

For the map to display locations correctly, it has to recognize the locations in the spreadsheet. Luckily, Google My Maps will recognize most location names that come from Mimsy XG, and will place these accurately.

However, this is not always the case. A minority of locations will not be recognized, due to Mimsy’s formatting. Google My Maps will alert you when some locations are not recognized. When this happens, click “open data table” under the spreadsheet you want to edit. Unrecognized locations will be highlighted in red. Edit these locations by hand, and they will display correctly.

## Adding metadata

You can add a title and description to the map. To do this, click on the title or description while in edit view. You will then be able to edit or add text. Click “save” to save your changes.

## Providing internal access

You’ll want to allow CSPG staff and volunteers to access the map if they are working on it. You will also need to set the map to be publicly viewable to include it on the CSPG site.

To change access permissions, click on the “share” button. Change the access settings so they say “Public on the web -- Anyone on the Internet can find and view.” Ensure that it is “find and view” and not “find and edit.” Only CSPG staff and volunteers should be able to edit the map. You can add CSPG staff and volunteers individually by either sending them a link, or by adding them by email.

## Making the map public and embedding it

To put the map on the CSPG website, you do not need to have any experience with coding, and do not need to write any code of your own. Google generates an embed code that you can then paste into CSPG site files.

- From the edit view, click on the three dots next to the map’s title.
- Click on “embed on my site.”
- A window will appear that has some code written in HTML. Copy it.
- Navigate to the folder that has the CSPG site HTML.
- Decide on which page you want the map to appear, and open the HTML file for that page (such as “index.html,” or something similar).
- Paste the code into the HTML file where you would like the map to appear.
- Save the file, and send your changes to the site.

Give it a few minutes, but the map should now be visible on the CSPG site!
