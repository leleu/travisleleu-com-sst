---
layout: post
title: "Data Source for Financial Analyses"
excerpt: "A catalog of data sources potentially relevant to analyses for financial firms"
categories: articles
tags: [data-source, finance]
modified: 2018-01-04T18:17:50-07:00
published: true
---
I've been spending a lot of time looking at different raw data sources, especially focused on economic and financial data.  Here is some information that other people might find useful.

# Government Data

## SEC Data from EDGAR
EDGAR is a database of documents filed with the SEC per regulatory requirements.  Huge amounts of data -- up to 1 TB uncompressed.  There appear to be issues with the data quality that even Congress is aware of.  Contains firmographic, geographic, and lots of accounting and legal data.  Some of it is structured

Special shoutout: 13F and 10-K/Q forms.   The former are ledgers showing positions for institutional investors, while the latter contains accounting information for publicly traded companies.

Cautions
* lots of different formats (XML, XBRL, HTML tables, csv, txt, natural language)
* concerns over data accuracy
* takes a long time to acquire and collate

For more information, please see my series of [posts on EDGAR](https://travisleleu.com/blog/edgar-sec-data-series-index/), starting with the ["Introduction to EDGAR" article.](https://travisleleu.com/blog/edgar-sec-database-part-i-introducing-edgar/)

## Social Media
A lot of smart people believe they can tease a tradable signal out of publicly expressed sentiment.  I have my reservations -- sentiment influences market, but I'm not sure anyone's attenuated an actual signal instead of a false positive.

There are lots of companies that analyze twitter sentiment for signal.  It would be interesting to incorporate sentiment into another analysis, but I suspect it's something that sounds better in theory than practice.
<!-- 

<figure>
	<a href="/images/restart-run-all.png"><img src="/images/restart-run-all.png" alt="Restart & Run All Cell"></a>
	<figcaption>Make sure our code structure isn't too far out of bounds</figcaption>
</figure>
 -->