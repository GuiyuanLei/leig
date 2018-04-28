---
title: Create a Website Using Blogdown
author: Guiyuan Lei
date: 2018-04-27
categories:
  - R
tags:
  - R Markdown
  - Netlify
  - blogdown
  - github
---


To build a website via [Blowdown](https://github.com/rstudio/blogdown), an easy way is to let [Netlify](https://www.netlify.com/) to build an initial website for you once you have [Github account](https://github.com). 

1. For example, if you use "Academic" theme website, go to [Install Academic with Netlify](https://app.netlify.com/start/deploy?repository=https://github.com/sourcethemes/academic-kickstart). Nelify will create a repository *academic-kickstart* (you can change the name) under your Github account and provide you with a customizable URL to access your new site. 

1. On GitHub, go to your newly created repository and edit config.toml to personalize your site. Shortly after saving the file, your site will automatically be updated

Usually you will want to write post in markdown (.md or .rmd) and pre-view in your local repository. So clone the repository from Github to your Rstudio, install blogdown and hugo to do it. The repository created by Netlify does not physically put the theme into your repository. You will have to download the theme into your local repository (put the files under folder "theme", don't need to commit those files) so that you can pre-view the website in your local laptop.

There are other ways to build a website, please read the book ["blogdown: Creating Websites with R Markdown"](https://bookdown.org/yihui/blogdown/). Alison ([https://alison.rbind.io]) has also wrote a nice post ["Up and running with blogdown"](https://alison.rbind.io/post/up-and-running-with-blogdown/). 