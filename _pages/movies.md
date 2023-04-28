---
layout: archive
title: "IMDb Data Analyzer"
permalink: /imdb/
author_profile: true
---

{% include base_path %}

***

I love movies.

There was a time when IMDb provided some user statistics within our own profile. Not anymore...

I've decided to code a basic (and far from good) Python script to bring those and more statistics back to life.

If you have some suggestions for the code/statistics, please let me know.

You can check the code [here](https://github.com/joelreis/imdb-data-analyzer)

***

To the best of my knowledge, Github pages, Jekyll and Jupyter Notebooks do not play along very well.

In order to display the notebook seen below, I used the Anaconda Prompt to obtain a markdown file by running the following command:

> jupyter nbconvert --to markdown  < file name >.ipynb 

Between this and converting the notebook to html, I prefer the former.

***

{% include imdbanalyzer.md %}


