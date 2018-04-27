---
title: Create a Website Using Blogdown
author: Guiyuan Lei
date: '2018-04-27
categories:
  - R
tags:
  - R Markdown
  - Netlify
  - blogdown
  - github
---


To build a website via Blowdown, the quickest way is to let [Netlify](https://www.netlify.com/) to build an initial website for you once you have [Github account](https://github.com). 

1. For example, if you use "Academic" theme website, go to [Install Academic with Netlify](https://app.netlify.com/start/deploy?repository=https://github.com/sourcethemes/academic-kickstart). Nelify will provide you with a customizable URL to access your new site. 

1. On GitHub, go to your newly created *academic-kickstart* (you can change the name) repository and edit config.toml to personalize your site. Shortly after saving the file, your site will automatically update

If you want to build a website in your Rstudio by yourself, please read the post [Up and running with blogdown](https://alison.rbind.io/post/up-and-running-with-blogdown/). But I had problem with Hugo version at the step of "deploy".