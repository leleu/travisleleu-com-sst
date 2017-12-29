---
layout: post
title: "Book Notes: The Effective Engineer"
excerpt: "Strategies for Effective Work"
categories: blog
tags: [optimization]
modified: 2017-12-27T12:17:50-07:00
published: true
---
Related: a great article about [how to run an effective engineering organization](https://minnenratta.wordpress.com/2017/01/25/things-i-have-learnt-as-the-software-engineering-lead-of-a-multinational/) popped up this morning on HN.

# The Effective Engineer
* Optimize for Learning
* Invest in tools that save time
* Shorten OODA (debugging) loop
* Marathons aren't for sprinting
* Recovery over prevention (builds anti-fragile systems)
* Automate mechanics/ops so you can focus on decision making
* Batch processes should be repeatably (no global state)

## Project Oxygen

Google studies everything they do relentlessly, including employee productivity.  They ran an internal project, called Project Oxygen, to study what characteristics made employees more productive.  What they found: soft skills are what matter, especially for technical people.

<blockquote>
	Project Oxygen shocked everyone by concluding that, among the eight most important qualities of Google’s top employees, STEM expertise comes in dead last. The seven top characteristics of success at Google are all soft skills: being a good coach; communicating and listening well; possessing insights into others (including others different values and points of view); having empathy toward and being supportive of one’s colleagues; being a good critical thinker and problem solver; and being able to make connections across complex ideas.
	<br />
	<a href="https://www.washingtonpost.com/news/answer-sheet/wp/2017/12/20/the-surprising-thing-google-learned-about-its-employees-and-what-it-means-for-todays-students/">WaPo article on Project Oxygen</a>
</blockquote>

Cribbed from <a href="http://www.effectiveengineer.com/">"The Effective Engineer", by Edmond Lau.</a>

This book is primarily about designing and developing a mindset that has a positive ROI, so to speak.  How to focus on what matters so you can make yourself better in your profession.

* Focus on high leverage activities with higher payoff potentials -- Pareto Principle
* Optimize for Learning -- learning is like compound interest for your life
* Adopt a growth mindset -- from Dweck's book: believe you can cultivate and grow your own intelligence and skills through effort.  Own your own story.
* Invest in learning, prioritize it over profitability.  Time is always the biggest constraint, so invest it in activities with the highest learning rate.  (Hint: these will be the most challenging tasks/environments.  The opportunity cost of working somewhere unchallenging is higher than any actual costs could be.)
* On the job: go outside your comfort zone & get inspired by other people's brilliance.

## Prioritization
Prioritization is usually a high leverage activity.  You spend 2 hours in review and prioritization, that enables you to work on a higher payoff/leverage idea instead of wasting 2 weeks on something else.
* Working on the wrong idea can set things back by years (opportunity cost of time)
* Prioritize based on ROI, focus on what directly produces value because that's measurable and manageable (rather than vague or abstract concepts)

## Speed
* automate mechanics of doing things so you have better control over decisions
* invest in tools and skills that save time
* speed enables faster iteration, which reduces the costs of mistakes and is a smart strategy for learning to optimize

## Measure to Manage
* developing your good metric is a High Leverage activity
* Have to measure things to manage them.  Need a good true north metric:
** good metric frames decisions: will it improve or reduce this number?
** good metric will limit damage from mistakes / incorrect decisions
** bad metric can incentivze / lead to bad behavior (don't measure hours worked, measure productivity)
** actionable -- tied into the efforts of the team
* internalize most useful numbers, so you have a gut feel for when something is off

## Get out of the building
* Not validating = wasted efforts, is only caused by psychological discomfort.  By validating early, we reduce waste and put ourselves into the growth mindset.
* small batches / low effort ways to validate.  make it easier and it'll be done more often.

## Estimation Skills
* Improving estimation skills a High Leverage activity
* Project Management = risk management.  reduce the biggest risks first.  Allow buffer for the unknown unknowns.

## Shipping
* Balancing quality with pragmatism, but make sure to know risks and downsides

## Reduce Operational Complexity
* High Leverage Activity
* stay simple in tech stack and architecture.
* simpler architectures have lower ops burden

## Fail Fast
* false positives / uncertain results do not optimize for fast learning.  Failing fast does
* High Leverage Activity

## Automation
* automate mechanics (operations) so you can spend more time on decision making
* speed up recovery -- respond and recovery quickly makes it less risky to leap before you look
* make batch processes idempotent (not dependent/affecting state of the overall system)
