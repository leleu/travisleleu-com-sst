---
layout: post
title: "Algorithms are Obsolete."
excerpt: "Mike Judge's hit tv show Silicon Valley gets it wrong.  Algorithms are obsolete; it's about the data.."
categories: analyses
tags: [ai, analyses]
modified: 2017-12-015T12:17:50-07:00
published: true
---
# Algorithms are Obsolete 
AI/ML/DL is focused on strategies for finding an acceptable/nearly optimal algorithm for a given set of data.  It uses a fitness function to evaluate those algorithms, then adjust the parameters accordingly.

This general purpose strategy for finding good solutions means that generalized algorithms are becoming obsolete.  We use A* search for pathfinding in general because it does pretty well in general.  But Deep Learning and the other trendy acronyms can create an algorithm that is customized for the specific data and heuristic for each problem.  Specialization wins, as usual.

## They're Giving it Away 
The major players give away AI algorithms -- convolutional neural nets, recursive networks, GANs, etc -- for free.  Google has put a ton of marketing effort behind it's AI library, [TensorFlow](https://en.wikipedia.org/wiki/TensorFlow).  Facebook, MS, and even Apple have all joined the open source tactic.  This benefits them because it gets bright minds contributing to their core technologies, while they hold back the secret sauce: the data they have collected over the years.  (And the infrastructure they developed to run these massive systems.)

## Post-Hype AI 
2017 was AI hype central.  We're now post-peak, which doesn't mean AI winter 2.0 is back, but that it's not a buzzworthy.  (This is a good thing.)  Moving forward, here's what I see: 
* commoditization of the algorithms
* commoditization of the infrastructure
* data remains secret sauce

Nothing groundbreaking there.  However, I do see GANs or data augmentation using computer models becoming a great equalizer in some fields.  Google can train itself to recognize Coke cans in images because of their massive db, but anyone can find a 3d model of a coke can, render it and insert into different scenarios.

AI will accelerate that.  You've already seen the cool stylistic transfer stuff coming out of AI labs -- turn a picture into an impressionist painting, and add in a couple of people in the same style.  Imagine applying that network so you can realistically insert visually different (yet generated) models of Coke cans into pictures, then train the Coke can identifier on the images with "artificially inserted" cans.

It works better than you'd think.  So while Google may have 100mm images of Coke cans, others can catch up (at least partway) through democratizing techniques.

## Modifying the title 
OK, it's about the algorithms.  But I think it's more about the algorithms that generate data than it is about the algorithms that process data.