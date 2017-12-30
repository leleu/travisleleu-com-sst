---
layout: post
title: "EDGAR: Acquiring the SEC Data (Part II: ETL)"
excerpt: "EDGAR is the SEC's huge database of public filings.  In this post, we acquire and load EDGAR data."
categories: blog
tags: [public-data,edgar,sec]
modified: 2017-12-30T14:17:50-07:00
published: true
---
EDGAR is the SEC documents registration system.  This post is part of a series on the EDGAR data, how to acquire it, analyze it, and use it for greater powers.  See the [series index](/blog/edgar-sec-data-series-index/)

### In this post
* Explore EDGAR data structure and associated documents/attributes
* Develop strategy to sample data to home computer managable
* Acquire the data

## Before the Start
EDGAR exports are large, like really big: 120GB for Q32017.  We're going to have to sample this dataset in order to explore it.  Before we sample it, we need to take a look at it.

### Django App - django_sec
I like using [chrisspen's django_sec fork of pysec](https://github.com/chrisspen/django-sec) because it bootstraps the process.  You can acquire data pretty easily, explore the structure and relationships (what kind of attributes are available?), and basically just poke around.

### Cautions
* EDGAR serves 429 form types; some of the data are in a nice XML derivative called XBRL.
* django_sec parses some of the data but has a lot of limitations we'll update.
* EDGAR submissions are not vetted or reviewed by officials, so misformatting is probable.

## Data Structure
* Companies are a central entity.  `cik` is the primary key.  Companies can be downloaded from quarterly indexes and processed using django_sec.  Can get forms/documents easily via cik.
* Each company has 1+ submission.  This is a bundle of documents associated with  regulatory requirements for a given industry/company in a given quarter.
* Each document can be XBRL or subclassed XML.  Each document can contain multiple records like a list of holdings [(Form 13F-HR for institutional investors)](https://www.sec.gov/divisions/investment/13ffaq.htm) or [unaudited financial reportings for publicly traded companies (Form 10-Q)](https://en.wikipedia.org/wiki/Form_10-Q)
* Each form will need a custom parser and data model developed.  django_sec can only parse attributes from 10-Q and 10-K, we'll be updating that later.


<figure>
	<a href="/images/django-sec-cli-build-company-index.png"><img src="/images/django-sec-cli-build-company-index.png" alt=""></a>
	<figcaption>Importing the company index with django-sec</figcaption>
</figure>
---
<pre style="font-size: 1.1em">What to do: Install django_sec and import the company data.
(This may take up to 10 hours)</pre>
---


<figure>
	<a href="/images/edgar-sec-sqlite-schema.png"><img src="/images/edgar-sec-sqlite-schema.png" alt=""></a>
	<figcaption>Our first glimpse at (someone's) take on the EDGAR schema</figcaption>
</figure>


The primary entities are company, index, and attribute.  Company and index are populated by running `python manage.py sec_import_index --start-year=2007 --end-year=2018`.


<figure>
	<a href="/images/edgar-index-of-documents-data-example.png"><img src="/images/edgar-index-of-documents-data-example.png" alt=""></a>
	<figcaption>django-sec parses a list of filings for all companies</figcaption>
</figure>
The attributes table provides a lot of flexibility, at the cost of ease of calculations.  As best I can tell, `django-sec` only populates around 50 fields from each company's 10-K/Q forms (these fields were identified by a corporate accountant, so they're likely a pretty good first approximation.)

<figure>
	<a href="/images/edgar-edgar-attrbutes-django-sec.png"><img src="/images/edgar-attrbutes-django-sec.png" alt=""></a>
	<figcaption>only parsed if you turn on load attribute for some companies & run `manage.py sec_import_attr`</figcaption>
</figure>


## What We've Got
* Starting point -- a list of companies and their EDGAR submissions.
* Parsed accounting data for publicly traded companies

## Problems We're Facing
* Current processing limited (django-sec) 
  * Not all form types are being processed 
  * Not all fields from 10-K/Q processed
  * No company demographic information
* Data not structured for analysis
* Entire dataset is still pretty big

# Getting More Data

We've got a 5GB database of companies and an index of associated documents, 2007-2017.  I want demographic data (available on the company profile page in EDGAR), and develop a schema made for analysis of the 10-Q filings.

<blockquote>I will continue this in Part 2 of Part II, once my company index download-and-process finishes.  Make sure to leave plenty of time for data acquisition!</blockquote>

