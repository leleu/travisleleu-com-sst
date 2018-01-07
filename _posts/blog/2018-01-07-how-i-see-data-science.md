---
layout: post
title: "So You Wanna Do 'Data Science'?"
excerpt: "What the heck is it, anyhow?"
categories: blog
tags: [data-science]
modified: 2018-01-07T18:17:50-07:00
published: true
---
A friend recently mentioned he was picking up Python, in an effort to dip his toes into the data science career path.  He's got a very strong theoretical grasp of programming, even if his preferred tools are JS and PHP.

I've been thinking about what he should learn, or be aware of.  Now we're all on the same page.
---
<figure>
	<a href="/images/drew-conway-data-science-venn-diagram.png"><img src="/images/drew-conway-data-science-venn-diagram.png" alt="Data Science Diagram"></a>
	<figcaption>Drew Conway's famous Venn Diagram of the field</figcaption>
</figure>

The common view of d.s. is the intersection of statistics, coding skills, and substantive expertise.  Personally, I see it more as the intersection of coding skills, risk awareness (instead of Statistics), and Intellectual Curiosity (instead of domain knowledge).

Statistical knowledge is certainly important, but you don't need to be an expert.  You just need to be aware of the risks and tradeoffs of the techniques you use.  Most of the time, the statistical work is fairly minimal, but the data discipline / risk awareness is important.

Substantive Expertise is fraught with biases and peril.  In "traditional" ML, you needed an expert to engineer the features you'd build into models -- you need someone to tell you what's significant in the field of study.  Not so much anymore, a point I'll elaborate on later.

## OK, what should I learn then?
How to acquire and clean data for analysis.  Seriously, that's >80% of the work to building useable models for fun and profit.

## Skills Needed
* Data scraping skills.  Javascript and Python are great options.
* CSV skills.  That's the data lingua franca for most datasets (JSON is verbose, XML is old and enterprisey)
* Summarization skills.  What variables do you have, can you develop a feel for how frequently the column is empty?  What are the range of values?  What's the histogram look like, and percentiles?
* Statistical software.  In python, that's the pandas library
* SQL skills.  Most data you acquire won't be in SQL, but I like to store my data there.  Maybe that's just because I'm more comfortable doing SQL queries than pandas summarization, or maybe it's because relational databases are great at storing data safely.
* Hack factor.  You found the perfect data on someone's website, but they have anti-scraping protections.  How are you gonna get it?
* A desire to prove yourself wrong.  The biggest danger with this stuff, why that diagram considers Statistics so important.  So many people look for evidence they're right in the data.  That is just flat out wrong.  The Scientific Method is your friend; do not psychologically incent yourself to be correct.

## How to get these skills
Start hacking.  Find some data you want, scrape it.  Summarize it.  Try to do a regression, then a prediction.  Write about it.

Classes are de rigeur for many newbies, but I question whether they'll have the toughness to produce valid results.  Do your own analyses, try a few of the demo Kaggle competitions.  Once you have a couple hundred hours of practical experience on several datasets, then dive into the theory.

## Conclusion
Get your hands dirty.  This field isn't a white glove, at a distance, theory based one.  The way to learn is to do.

If you need any project ideas, I've got a million that I will never get around to building.

Other Concepts (possible future posts):
* Confusion Matrix
* Data Acquisition
* Transforming data (ETL)
* Setting up an analysis
* Coding the analysis
* Communicating the results
* Discipline
* Psychological Biases
* Artificial Intelligence
