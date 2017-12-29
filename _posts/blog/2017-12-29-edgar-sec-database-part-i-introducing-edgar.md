---
layout: post
title: "EDGAR: SEC Data (Part I: Introduction)"
excerpt: "EDGAR is the SEC database for many types of registrations.  It's also a humungous dataset."
categories: blog
tags: [public-data,edgar,sec]
modified: 2017-12-29T14:17:50-07:00
published: true
---
The US SEC operates EDGAR (Electronic Data Gathering, Analysis, and Retrieval) a system where companies electronically file required paperwork.

It is also  public, and really really big.  There have been [concerns about data quality](http://oversight.house.gov/wp-content/uploads/2013/09/2013-09-10-DEI-to-White-re-Interactive-Data-Rule.pdf) in the past, although some of the evidence cited is from a nonprofit who sells software to help compliance.

In this introductory post, I will introduce some of the basics of EDGAR.  I'd like to answer the following questions:
* What is EDGAR?
* What kind of data does EDGAR have?
* Why should I care?

## print('Hello, EDGAR')
* [Wikipedia link to EDGAR](https://en.wikipedia.org/wiki/EDGAR)
* [EDGAR web search (official)](https://www.sec.gov/edgar/searchedgar/webusers.htm)
* [SEC Strategic Plan for EDGAR](https://www.sec.gov/about/sec-strategic-plan-2014-2018-draft.pdf)
* [Company or Entity Lookup](https://www.sec.gov/edgar/searchedgar/cik.htm)

EDGAR hosts over 21 million documents (many in standard machine readable formats).  Each quarter of data (e.g. QTR3 2017) has daily exports of the documents filed that day.

It's big.  Q3 of 2017, for example, is 32GB compressed / ~120GB uncompressed.  Each year requires about a terabyte of disk space to uncompress, and data goes back over 20 years.  It's also in XML, text, and html, which has a lot of repetitive tags.

### What kind of documents?
Financial documents for all publicly traded companies.  Holdings for private groups that invest other people's money.  Mutual funds reporting requirements.  Over 420 form types are in the database, including Form 4 (ownership changes), 8-Ks, 10-Q (most financials of publicly traded companies), and 13F-HR (holdings summaries).

In part 2, I'll cover how to acquire and load the data.  Some ETL skills and the data will be much smaller when it's normalized and stored in a SQLite database.

## What's in here?
* From 2016-2017 sampled data
** 429 form types
** 1.7 million documents, associated with 166,817 companies

Also included: Thousands of parsed attributes like RepaymentsOfNotesPayable, OperatingIncomeLoss, EarningsPerShareBasicAndDiluted, Depreciation, etc., allow you to quickly paint a picture of what a company does.  And (hopefully!) just how healthy that company is, relative to their peers.


## Why should I care?
Finance nerds can tell a lot about a company with just a table of numbers.  Data nerds can tell a lot more about a company based on how it compares to other companies, what people are saying about it, and other metadata.  Beyond that, investors can run anti-fraud heuristics, or track changes over time to infer to trajectory of key metrics.

Investment groups can use this information to see what other key groups are buying and selling.  Later on, we'll explore using a K-Means cluster to identify competition by market, geography, or shared stocks.  Perhaps at the end, we'll build a "Netflix recommendation algorithm" using collaborative filtering.

Later in this series we'll explore some anti-fraud heuristics, quantifying public sentiment using social media and other textual data, and identify competition using a few different techniques.

Ultimately, I hope you walk away with an understanding of a massive public resource that has been historically underutilized due to data size, quality, and a paucity of research and introductory articles.