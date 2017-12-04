---
layout: post
title: "Jupyter Tip: Enable Extensions"
excerpt: "Jupyter Notebook has an extension platform that is fairly easy to enable."
categories: blog
tags: [notes, jupyter, jupyter-tips]
modified: 2017-12-03T14:17:50-07:00
published: true
---

The awesome Jupyter Notebook has many tricks up its sleeve.  Once you get comfortable with the [keyboard shortcuts](https://www.cheatography.com/weidadeyue/cheat-sheets/jupyter-notebook/), you may want to explore the extension library.

This brief guide will show you how to install the notebook extensions feature, and how to enable an extension [ExecuteTime](http://jupyter-contrib-nbextensions.readthedocs.io/en/latest/nbextensions/execute_time/readme.html) that will append cell execution time into your notebooks.

## Installation
You need to install a pip package called `jupyter_contrib_nbextensions` with pip.
```pip install jupyter_contrib_nbextensions```

Then install javascript and css files for the exntesions
```jupyter contrib nbextension install --user```

Now let's add a tab to the web UI to manage these, with [jupyter_nbextensions_configurator](https://github.com/Jupyter-contrib/jupyter_nbextensions_configurator)
```pip install jupyter_nbextensions_configurator
jupyter nbextensions_configurator enable --user
```

Now restart your jupyter server, relogin, and you will se a tab across the top titled NbExtensions.  Check the box next to ExecuteTime to enable timings embedded in your notebooks.

<figure>
	<a href="/images/nbextensions-executetime.png"><img src="/images/nbextensions-executetime.png" alt="Jupyter Enable ExecuteTime"></a>
	<figcaption>Check to enable ExecuteTime</figcaption>
</figure>
