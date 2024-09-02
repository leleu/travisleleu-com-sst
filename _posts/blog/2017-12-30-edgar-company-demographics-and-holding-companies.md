---
layout: post
title: "EDGAR: More EDGAR data"
excerpt: "Acquiring demographic and institutional holdings data."
categories: blog
tags: [public-data,edgar,sec]
modified: 2017-12-30T14:17:50-07:00
published: true
---
EDGAR is the SEC documents registration system.  This post is part of a series on the EDGAR data, how to acquire it, analyze it, and use it for greater powers.  See the [series index](/blog/edgar-sec-data-series-index/)

# In this post
* Explore EDGAR data structure and associated documents/attributes
* Develop strategy to sample data to home computer managable
* Acquire the data

## What We've Got
* Starting point -- a list of companies and their EDGAR submissions.
* Parsed accounting data for publicly traded companies

## What's Next (Issues)
* Current processing limited (django-sec) 
  * Not all form types are being processed 
  * Not all fields from 10-K/Q processed
  * No company demographic information
* Data not structured for analysis
* Entire dataset is still pretty big

# Getting More Data

We've got a 5GB database of company names and an index of associated documents from 2007-2017.  I want demographic data from the company profile page, acquire and structure the 13F-HR filings (institutional investor holdings).

## Scrape EDGAR
We've got a nice website to scrape, and can dump a list of cik values from SQLite to parameterize the URLs to extract the data we want.  I use `scrapy` because it comes with a caching engine, making it super fast to rerun in the future.

```Next step: use scrapy to scrape company demographics into local csv files.```