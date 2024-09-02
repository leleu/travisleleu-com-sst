---
layout: post
title: "MLB Injury Database Research"
excerpt: "If you are looking for what I learned in building an injury database, this may be of us."
categories: baseball
tags: [baseball, injuries, datasets]
modified: 2018-01-04T18:17:50-07:00
published: false
---

# MLB Injury Datasets

## HITS
MLB has their own injury database, run in collabortion with [Johns Hopkins Public Health](http://c.ymcdn.com/sites/www.cste.org/resource/resmgr/weston/2016WESTON/18.Pollack_WestOn_Sept_2016_.pdf.  It's called HITS, it looks like the gold standard, and there is no way they're gonna make that public.  Bummer.

## Other structured databases
I only looked for a half hour or so, but didn't find anything except [this Jeff Zimmerman article](https://www.fangraphs.com/tht/2016-disabled-list-information-and-the-future-of-injury-analysis/) from Dec '16, bemoaning the lack of a structured dataset out there.

### Crap.  OK, we'll do this ourselves
Fortunately, transactions are readily available on a number of different websites.  I'll start with the easiest, then try to grab a couple other datasets to compare.

## Constraint: 2 hours
1:54:39 remaining.

We use python because it can do anything.  It does great when scraping websites, as long as they aren't loading the data via javascript.  MLB.com's official transaction page uses javascript, but we have a trick to deal with that.

OK , no more time to waste.  Let's start on [ProSportsTransactions.com](http://www.prosportstransactions.com/baseball/Search/SearchResults.php?Player=&Team=&BeginDate=&EndDate=&DLChkBx=yes&submit=Search&start=0)

* <50 records / page
* 828 pages
* ~40k transactions, going way back, but most of the data is after 1998.

We could use a very basic script -- like handspun python, aye -- but I'm going to use the scrapy library for one simple reason: with a couple config lines, you have a cached copy of the pages you develop against.  This is so freaking useful, because the lag between their server and your scraper is the most frustrating thing ever.

### 1:30 remaining
Some software installed, a few settings updated, and about 40 lines of python to trigger this thing.  Let's turn it on, will take a bit to acquire all the data.  scrapy is amazing.

### 1:26 remaining
With 828 pages to scrape, 1-5s/page, we could be looking at a few minutes to acquire the data.  Good time to scheme what's next.

It'd be nice to know more about what I've got.  To do that, I can either put it into a SQL database or a pandas DataFrame.  I'm going to use Pandas because of the dataframe size.  Maybe I can normalize a few things to cleanup for csv export, then host the data file for Jeff Z.

With 83 minutes to go, the scrape is complete.  No errors, and best of all, if there is a mistake, I've got everything cached on my computer.  So I can re-run the scrape for these same data without needing to contact their servers.

Now to the pandas.  I use Jupyter notebook for my interactive data exporatory tool.

<figure>
	<a href="/images/prosportsinjurydata-summary.png"><img src="/images/prosportsinjurydata-summary.png" alt=""></a>
	<figcaption>Josh Beckett was the most acquired and reqlinquished player.  Acquired 18 times, relinquished 21.</figcaption>
</figure>

Let's compute some fields that will be useful
1. Days on the DL
1. Cap "Days on DL" if they go past end of season
1. extract any terms that indicate type of injury or body part
1. Publish!

### 8 minutes remaining
For the past hour, I've been going through the data structure, trying to figure out what makes sense.  I needed to match up start of a stint with the end of a stint, but account across years.

With 8 minutes left, I acknowledge that I'm not getting this done in these 2 hours.  Time for a break, we'll return shortly.

