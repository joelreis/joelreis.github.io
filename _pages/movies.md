---
layout: archive
title: "IMDb Data Analyzer"
permalink: /imdb/
author_profile: true
---

{% include base_path %}

***

I love movies too!

There was a time when IMDb provided user statistics within our profiles, but unfortunately, that's no longer the case.

So, I've decided to code a basic (and far from perfect) Python script to bring those statistics back to life, along with some additional ones.

If you have any suggestions for the code or the types of statistics to include, please let me know.

You can check out the code [here](https://github.com/joelreis/imdb-data-analyzer)

***

To the best of my knowledge, GitHub Pages, Jekyll, and Jupyter Notebooks do not integrate seamlessly.

To display the notebook shown below, I used the Anaconda Prompt to generate a markdown file by running the following command:

> jupyter nbconvert \-\-to markdown  < file name >.ipynb 

Between this method and converting the notebook to HTML, I prefer the former.

***

{% include imdbanalyzer.md %}
