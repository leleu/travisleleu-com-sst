---
layout: post
title: "Analysis Idea: Projecting Baseball Injuries"
excerpt: "Walk through a couple different ways to predict pitching injuries in Major League Baseball"
categories: analyses
tags: [baseball, injuries]
modified: 2017-12-04T23:17:50-07:00
published: true
---

# Analysis Idea
Build a classifier for injury predictions among baseball pitchers.  Try random forest, then try deep learning, compare the efforts.  Multiple posts, multiple sessions.

## Possibly cool explorations, time permitting
* main objective: predict DL days year to year
* secondary: predict TJS
* can i build a model of a healthy pitcher using pitchf/x data, then identify deviations to create an "identify an injury" in-season

# Data
* (all kinds of injury db links, probably focus 2010-2016 w/ TJS emphasis](http://www.baseballheatmaps.com/disabled-list-data/)
* MLB offers pitchfx data
* b-ref for precalculated/historical data
* [raw data - Lahman database for SQL](http://seanlahman.com/baseball-archive/statistics)
* retrosheet for play by play raw data

## Validation and Training Sets
* predict year to year injury rates
* predict inseason injury rates

### Additional Reading
* [How to find raw data from sabr.org](http://sabr.org/sabermetrics/data)
* [purchasable baseball datasets from fantasydata.com](https://fantasydata.com/products/historical-sports-data.aspx)
