---
layout: page
title: Documentation Samples
author: Isaac Williams
---

Here are some samples of my technical documentation. The first is documentation for the web archiving software Archive-It. The second is documentation I created for the Center for the Study of Political Graphics about updating a project in Google Maps.

---

# CSPG Digital Mapping Documentation

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

Give it a few minutes, and the map will be visible on the CSPG site.

---

# Archive-It documentation

This is technical documentation I wrote in support of UCLA’s web archiving initiatives. Few librarians at UCLA have experience using Archive-It, the software we use to archive web content, and I wrote this documentation to help librarians better understand how it functions. This documentation is currently hosted on Confluence, the website the UCLA Library uses to host its documentation.

To begin, sign into Archive-It at https://archive-it.org. You will be redirected to the UCLA Library account overview page, which shows a list of all collections being archived by UCLA using Archive-It. You can navigate to the collection you would like to work with by clicking on the collection name, or you can create a new collection by clicking the blue "Create a Collection" button above the list.

## Creating a new collection

From the account overview (landing) page, click the blue "Create a Collection" button above the list of active collections.

In the window that appears, name your collection.

You will be redirected to the landing page for your new collection. From this page, you can take a tour of the collection area, add seeds, or delete the collection. You can also toggle between making your collection private or public, and active or inactive. Later, you will be able to see your scheduled crawls on this page.

## Adding seeds

You can add seeds to a new collection from the collection's landing page. For an existing collection, you can add seeds by navigating to the "Seeds" tab and clicking the blue "Add Seeds" button above the seed list on the right side.
When inputting seed URLs, you must pay attention to how the URLs are formatted. Usually, you can copy and paste the URL as it appears in your browser, and it will be properly formatted. However, there are two primary considerations:
- You may need ``/`` at the end of the seed URL.
- Anything that comes after ``#`` in a seed URL will be ignored by the crawler.

Scope

The scope setting determines what the crawler archives. You can change or refine the scope by blocking URLs or using regular expressions. Seeds' default crawling scope will be determined by how you format their URLs when you add them to the collection. For most seeds, embedded content such as videos will be archived (including embedded content not hosted on the same site as the seed), but linked content will not (unless you specify otherwise).

You can also change the scope at the seed level.

Here is information about how the crawler determines scope, and here are instructions for modifying a collection's scope.

## Running crawls
To run a crawl and record content, select the crawl from the "Seeds" tab and click the "Run Crawl" button above the seed list. From this page, you can set parameters for your crawl and whether it is a crawl or a test crawl. You can limit documents, data, and time archived. You also have the ability to crawl only PDFs.

## Test crawls
Web archiving can be expensive, and it is important to stay within your budget. Because it is possible to archive more data than intended while running crawls, be sure to first run a free test crawl. Test crawls are a great way to see which parts of your intended crawl and scope need improvement without paying for collected data. If your test crawl is satisfactory, you can purchase (save) your test crawl and add it to your collection as a normal crawl.

Run the test crawl with the domains first, and then check for issues such as:
- redirects, malicious or not. You may elect to disable a seed if the URL has changed or there are other reasons for excessive redirects. Check that most documents for each seed come from the same domain as the seed; if not, this is an unwanted redirect and you should consider disabling the seed.
- unusually high amount of documents. UT Austin's guidelines say that any amount over 30,000 documents is worrisome. High amounts of documents could be due to a site re-launching, a seed directing to a malicious site, or crawler traps.

If the test crawl has no issues, you can save it. If the test crawl has issues, add host constraints and then run another test crawl. Repeat until you are satisfied with the results of the crawl.
## Crawler traps

A crawler trap is a series of web pages that create an infinite amount of URLs for crawlers to find. In other words, if our crawler stumbles into one of these traps, it could continue running forever. While Archive-It's crawlers have maximum crawl duration times, a lot of data can be archived prior to this cut-off, so avoiding these traps is imperative.

Unusually high amounts of "queued" URLs can indicate that a seed has a crawler trap. Archive-It has a list of suspicious patterns on its page "Identify and avoid crawler traps."

To prevent traps from being crawled, it is necessary to limit the scope of your crawls. This is possible by identifying a string of text that appears in trap URLs and blocking it from future crawls. You may also use regular expressions to limit scope. Refer to the "Scope" section of this page for more information about how to limit scope.

## Archiving Facebook
A few guidelines will help streamline Facebook archiving:
- Be sure to only archive specific portions of Facebook, and not the entirety of the site. Be sure to add an ending slash to your seed URL.
- Use HTTPS instead of HTTP in your seed URL–Facebook only uses HTTPS.
- See if you can view the seed on the live web. Many pages on Facebook are only visible to specific users. Archive-It has instructions for how to crawl password-protected pages.
- Limit the scope of each seed to archive at least 1GB of data. Many Facebook pages will take more than 1GB to capture properly.
- Either change the collection-level scoping rules to ignore robots exclusions on three hosts (`www.facebook.com`, `fbcdn.net`, and `akamaihd.net`) OR ignore robots.txt for each seed at the seed level.
- You can also limit the scope of your crawls so that they only archive English language content (or other languages), or that they exclude personal information or segmented video files. Archive-It has more detailed guidelines.
- Archived Facebook pages will appear the same as they do on the live web, but you will be unable to expand comments sections to see comments beyond what the crawlers saw, and you will not be able to see the names of individual Facebook users who have "liked" archived posts (although you will be able to see the number of people who "liked" it).

## Archiving Twitter

There are three main rules to follow when archiving Twitter:
- Avoid adding www to your seed URL, as Twitter URLs do not have a www and www.twitter.com is blocked by a robots exclusion.
- You must add an ending slash to your seed URL. If you do not do this, you will archive all of Twitter instead of just the feed you want.
- You should also be sure to exclude additional languages. Each tweet is captured in all languages Twitter supports. To avoid capturing more than what you need, you should limit the scope of your collection or seed to block URLs that match the regular expression ``^.*lang=(?!en).*$``
