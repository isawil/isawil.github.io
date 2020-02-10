---
layout: narrative
title: Archive-It for Web Archiving
author: Isaac Williams, for UCLA Digital Library Program
---

# Background

This is technical documentation I wrote in support of UCLA’s web archiving initiatives. Few librarians at UCLA have experience using Archive-It, the software we use to archive web content, and I wrote this documentation to help librarians better understand how it functions. This documentation is currently hosted on Confluence, the website the UCLA Library uses to host its documentation.

---

## Getting started

To begin, sign into Archive-It at https://archive-it.org. You will be redirected to the UCLA Library account overview page, which shows a list of all collections being archived by UCLA.

Navigate to the collection you would like to work with by clicking on the collection name. You can also create a new collection by clicking the blue "Create a Collection" button at the top of the account overview page.

## Creating a new collection

From the account overview page, click the blue "Create a Collection" button above the list of active collections.

In the window that appears, name your collection. Choose a name that reflects what you are archiving.

After naming your collection, you will be redirected to the landing page for your new collection. From this page, you can take a tour of the collection area, add seeds, or delete the collection. You can also toggle between making your collection private or public, and active or inactive. Later, you will be able to see your scheduled crawls on this page.

## Adding seeds

You can add seeds to a new collection from the collection's landing page. For an existing collection, add seeds by navigating to the "Seeds" tab and clicking the blue "Add Seeds" button above the seed list on the right side.

When inputting seed URLs, pay attention to how the URLs are formatted. Usually, you can copy and paste the URL as it appears in your browser, and it will be properly formatted.

However, there are two primary considerations:
1. You may need ``/`` at the end of the seed URL.
2. Anything that comes after ``#`` in a seed URL will be ignored by the crawler.

## Scope

The scope setting determines what the crawler archives. You can change or refine the scope by blocking URLs or using regular expressions.

Seeds' default crawling scopes will be determined by how you format their URLs when you add them to the collection.

For most seeds, embedded content such as videos will be archived. This includes embedded content not hosted on the same site as the seed, such as a YouTube video embedded on a different website. However, linked content will not, unless you specify otherwise.

You can also change the scope at the seed level.

## Running crawls

To run a crawl and record content, navigate to the "Seeds" tab and click the "Run Crawl" button above the seed list.

From the "Run Crawl" page, you can set parameters for your crawl and determine whether it is a crawl or a test crawl. You can limit documents, data, and time archived. You also have the ability to crawl only PDFs.

## Test crawls

Web archiving can be expensive, and it is important to stay within your budget. Because it is possible to archive more data than intended while running crawls, be sure to first run a free test crawl.

Test crawls enable you to see which parts of your intended crawl and scope need improvement without paying for collected data. If your test crawl is satisfactory, you can purchase (save) your test crawl and add it to your collection as a normal crawl.

Run a test crawl first, and then check for issues such as:

- Redirects, malicious or not. You may choose to disable a seed if the URL has changed or there are other reasons for excessive redirects. Check that most documents for each seed come from the same domain as the seed; if not, this is an unwanted redirect and you should consider disabling the seed.
- Unusually high amount of documents. UT Austin's guidelines say that any amount over 30,000 documents is worrisome. High amounts of documents could be due to a site re-launching, a seed directing to a malicious site, or crawler traps.

If the test crawl has no issues, you can save it. If the test crawl has issues, add or change host constraints and run another test crawl. Repeat until you are satisfied with the results of the crawl.

## Crawler traps

A crawler trap is a series of web pages that create an infinite amount of URLs for crawlers to find. In other words, if your crawler stumbles into one of these traps, it could continue running forever.

While Archive-It's crawlers have maximum crawl duration times, a lot of data can be archived prior to this cut-off, so avoiding these traps is imperative.

Unusually high amounts of "queued" URLs can indicate that a seed has a crawler trap.

To prevent traps from being crawled, it is necessary to limit the scope of your crawls. You can do this by identifying a string of text that appears in trap URLs and blocking it from future crawls.

You can also use regular expressions to limit scope. Refer to the "Scope" section of this page for more information about how to limit scope.

## Archiving Facebook

A few guidelines will help streamline Facebook archiving:

- Add an ending slash to your seed URL to only archive specific portions of Facebook, and not the entire site.
- Use `HTTPS` instead of `HTTP` in your seed URL.
- See if you can view the seed on the live web. Many pages on Facebook are only visible to users with permissions to view them.
- Limit the scope of each seed to archive at least 1GB of data. Many Facebook pages will take more than 1GB to fully capture.
- Either change the collection-level scoping rules to ignore robots exclusions on three hosts (`www.facebook.com`, `fbcdn.net`, and `akamaihd.net`) OR ignore `robots.txt` for each seed at the seed level.
- You can also limit the scope of your crawls so that they only archive English language content (or other languages), or that they exclude personal information or segmented video files.
- Archived Facebook pages will appear the same as they do on the live web, but you will be unable to expand comments sections to see comments beyond what the crawlers saw, and you will not be able to see the names of individual Facebook users who have "liked" archived posts (although you will be able to see the number of people who "liked" it).

## Archiving Twitter

There are three main rules to follow when archiving Twitter:

1. Avoid adding `www` to your seed URL, as Twitter URLs do not have `www` and `www.twitter.com` is blocked by a robots exclusion.
2. Add an ending slash to your seed URL. If you do not do this, you will archive all of Twitter instead of just the feed you want.
3. Exclude additional or unwanted languages. Each tweet is captured in all languages Twitter supports. To avoid capturing more than what you need, you should limit the scope of your collection or seed to block URLs that match the regular expression ``^.*lang=(?!en).*$``

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
