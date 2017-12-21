---
layout: post
title: "Let's Apply Benford's Law to San Diego City Budgets"
excerpt: "Did you know that 30% of the leading digits 'should' be 1?"
categories: blog
tags: [sandiego,opendata,fraud-detection]
modified: 2017-12-16T12:17:50-07:00
published: true
---
[Benford's Law](https://en.wikipedia.org/wiki/Benford%27s_law) is an observation that certain real-world datasets have unbalanced distribution of leading digits.  It is applied by [forensic](https://www.journalofaccountancy.com/issues/2017/apr/excel-and-benfords-law-to-detect-fraud.html) [accountants](http://www.acfe.com/Benfords/) and is [formally studied by accountants](https://www.isaca.org/Journal/archives/2011/Volume-3/Pages/Understanding-and-Applying-Benfords-Law.aspx); it has been used to [identify possibly forged data in science experiments](https://www.ncbi.nlm.nih.gov/pubmed/28653153).

Let's explore the San Diego City Budgets from 2011-2018 to see if they appear artificial.

<figure style="opacity: 1 !important">
	<img src="/images/sd_benford_2011.png" alt="FY2011 San Diego Budget">
	<figcaption>FY2011 San Diego Budget</figcaption>
</figure>

### Data
[San Diego City Budgets, 2011-2018](https://data.sandiego.gov/datasets/operating-budget/)

### Code 
[Jupyter Notebook](https://github.com/leleu/travisleleu-com-sst/blob/master/notebooks/Benford's%20Law%20-%20San%20Diego%20City%20Budgets.ipynb)

### Results
Individual Year Graphs all pretty much look like the ideal distribution.  For example, here's FY2015:


<figure style="opacity: 1 !important">
	<img src="/images/sdcity_benford_fy15.png" alt="FY2015 San Diego Budget">
	<figcaption>FY2015 San Diego Budget</figcaption>
</figure>

And FY2018:
<figure style="opacity: 1 !important">
	<img src="/images/sdcity_benford_fy18.png" alt="FY2018 San Diego Budget (Projected)">
	<figcaption>FY2018 San Diego Budget (Projected)</figcaption>
</figure>


## Conclusions
The San Diego City Budgets all match the expected distribution very closely, for each individual year as well as cumulatively.

<figure style="opacity: 1 !important">
	<img src="/images/sdcity_benford_total.png" alt="FY11-18 San Diego Budget (Projected)">
	<figcaption>2011-2018 San Diego Budget Data</figcaption>
</figure>
