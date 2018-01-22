---
layout: post
title: "Simulating Optionality"
excerpt: "As uncertainty increase, it becomes more important to increase the number of available options to make it more likely you're getting close to the optimal outcome"
categories: data
tags: [optimization, growth, options]
modified: 2018-01-19T18:17:50-07:00
published: true
---
# Options
Options are alternate ways of doing something.  The simulations below show the value of creating optionality when making decisions under uncertainty, e.g., doing something new.

You can change the assumptions, but the values I used were fairly conservative from my experience.

## Optimizing via Optionality
Suppose you have an outcome you want to optimize -- we shall consider a company's visit-to-signup conversion rate.  We'd like to optimize our signup screen to increase that metric, driving more users into our service's onboarding flow.

## Estimate scale
* Assume 100 conversions per day at a 5% conversion rate (2,000 sessions/day)
* Assume cLTV at $100
* 20% lift is 20 more signups per day, $2000 additional dollars per day, $60,000 per month

<figure>
	<img src="images/situation-3-optionality.png" alt="">
	<figcaption>In a highly uncertain environment, it may be valuable to run more tests with fewer options, bounded by the number of tests you can think to run</figcaption>
</figure>



You can see why companies in growth stages are so excited about split testing.  For the right situation, it can print money.

Check out the (Jupyter notebook hosted at github)[https://github.com/leleu/travisleleu-com-sst/blob/master/notebooks/split%2Btesting%2Boptionality%2Bsimulation.ipynb] for the code, embedded graphs, and other insight.  The takeaway: the greater the uncertainty in any decision, the more important it is to explore options.