---
layout: post
title: "Reproducible Analysis in Jupyter Notebooks"
excerpt: "Notes on Jake Vanderplas' video series on some best practices for using a Jupyter notebook.  Covers some practical tips as well as how he explores and visualizes datasets."
categories: blog
tags: [notes, jupyter]
modified: 2017-11-29T14:17:50-07:00
published: true
---
[GitHub Notebook from the video series](https://github.com/leleu/travisleleu-com-notebooks/blob/master/Reproducible%20Analysis%20with%20Jupyter%20Notebooks.ipynb)

Also check out Jake's awesome, free book: [Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/)

---

Jake Vanderplas has a great video series about [reproducible analysis in Jupyter Notebooks](https://www.youtube.com/watch?v=_ZEWDGpM-vM&list=PLYCpMb24GpOC704uO9svUrihl-HY1tTJJ).  His overall recommendation for using Jupyter:

{% twitter https://twitter.com/jakevdp/status/935187578881323008 %}

Before closing out of an analysis session, make sure you can run your notebook from a clean state.

<figure>
	<a href="/images/restart-run-all.png"><img src="/images/optimization-result.png" alt="Restart & Run All Cell"></a>
	<figcaption>Tests Notebook Linearity, an important part of reproducibility</figcaption>
</figure>

### Video Timelines and Notes
[video 1 [5min] - acquiring, loading, plotting data.](https://www.youtube.com/watch?v=_ZEWDGpM-vM&list=PLYCpMb24GpOC704uO9svUrihl-HY1tTJJ&index=1)
* Retrieve data from code; reproducible analysis starts with acquiring the data.
* Use [pandas](https://pandas.pydata.org/) to load data.
* Familiar libraries are often imported with nicknames common in the community
  * `import pandas as pd`


[video 2 [6min] - exploring data](https://www.youtube.com/watch?v=yUNBVzQfugg&index=2&list=PLYCpMb24GpOC704uO9svUrihl-HY1tTJJ)
* explore your data by graphing it from different angels
* matplotlib has built-in styles to prettify plots, including seaborn
* aggregate and groupby, data with pandas data wrangling
* pivot tables are very easy to run and output


<figure>
	<a href="/images/bikepath-usage.png"><img src="/images/bikepath-usage.png" alt="Bikepath usage"></a>
	<figcaption>Bikepath Usage by direction (time series)</figcaption>
</figure>

[video 3 [5min] - what should be saved](https://www.youtube.com/watch?v=J45NJ0pJXWQ&index=3&list=PLYCpMb24GpOC704uO9svUrihl-HY1tTJJ)
* Jupyter is great because we can explore data by jumping around in different code blocks (nonlinearity)
* before saving, linearize your notebook.  "Restart & Run All" is your friend

[video 4 [6min] - git and github](https://www.youtube.com/watch?v=VdLdfF_uuSQ&list=PLYCpMb24GpOC704uO9svUrihl-HY1tTJJ&index=4)
* don't check your data into version control (it should be acquired in code, if possible)

[video 5 [7min] - turn your code into a python package](https://www.youtube.com/watch?v=DjpCHNYQodY&list=PLYCpMb24GpOC704uO9svUrihl-HY1tTJJ&index=5)
* package useful bits of code so you don't have to c/p into other notebooks
* requires a few bits of code, but nothing complicated
  * create `__init__.py` file in directory that imports objects from w/in that same dir

[video 6 [6min] - test your code](https://www.youtube.com/watch?v=Pf1ADyUKOrE&list=PLYCpMb24GpOC704uO9svUrihl-HY1tTJJ&index=6)
* *unit tests* ensure the results of your methods do what they are supposed to
* is a positive signal to others that your code can be relied upon

[video 7 [6min] - refactoring for speed](https://www.youtube.com/watch?v=qMkhTo7sdHo&index=7&list=PLYCpMb24GpOC704uO9svUrihl-HY1tTJJ)
* if there's something common that can be optimized, pandas has a way to do it

<figure>
	<a href="/images/bikepath-usage.png"><img src="/images/optimization-result.png" alt="Speedup after an improved read_csv invocation"></a>
	<figcaption>From 22s to &lt;0.5s because we understood how pd works</figcaption>
</figure>

[video 8 [6min] - debugging](https://www.youtube.com/watch?v=jHjyUTQHjDg&list=PLYCpMb24GpOC704uO9svUrihl-HY1tTJJ&index=8)
* debugging is a learned art.  watch the videos to get better at it in your own code
* when you find a bug in your code, that's a good candidate for unit testing

[video 8.5 [8min] - finding, fixing, PR for scikit-learn bug](https://www.youtube.com/watch?v=1kA7oD7ftsM&index=9&list=PLYCpMb24GpOC704uO9svUrihl-HY1tTJJ)
* pretty neat - watch him find, fix, and submit a PR for a bug in a major library

[video 9 [8min] - more sophisticated analysis](https://www.youtube.com/watch?v=n1qKe0kkwyU&list=PLYCpMb24GpOC704uO9svUrihl-HY1tTJJ&index=10)

[video 10 [8min] - cleaning up the notebook](https://www.youtube.com/watch?v=GtvVpHP7CLs&list=PLYCpMb24GpOC704uO9svUrihl-HY1tTJJ&index=11)
* to go from a Jupyter notebook exploration to a Reproducible Result, and to share with other people, try to linearize your notebook.  Jake's tweet is pretty straightforward here:

{% twitter https://twitter.com/jakevdp/status/935178916490223616 %}

In short, think about how other people, including yourself at your next session, will likely approach your code.  It's great to explore in a non-linear fashion -- that's part of the power of this notebook IDE -- but try to tidy up after yourself, even if it's for your own sake.