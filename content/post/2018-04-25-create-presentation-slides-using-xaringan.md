---
title: Create Presentation Slides using xaringan through R Markdown
author: Guiyuan Lei
date: 2018-04-25
publishdate: 2018-04-26
lastmod: 2018-04-28
categories:
  - R
tags:
  - R Markdown
  - xaringan
  - Presentation
---


Sometimes it takes quite a lot time to grasp one new method (such as machine learning); on the other hand, you may just need less than half an hour to learn one skill. R Markdown is the latter one but change your way of working. 

My experience of using R Markdown since 2006 for statistical analysis and reporting mainly focused on exploratory analysis. The reports generated were word/pdf/html documents. I have not worked on a real example of slides format yet (except simple demo with one or two slides). But this year I was thinking of using R Markdown more in work, for example, to create presentation slides for periodic reporting since it is really tedious to copy and paste numbers into PowerPoint slides repeatedly.


After some research, I decided I want to try [xaringan](https://github.com/yihui/xaringan), an R package for creating slideshows with remark.js through R Markdown. The slides I saw from the author of the package ([Yihui Xie](https://yihui.name/)) and other people look very professional, the syntax also seems not difficult (at least for the basics). Recently one colleague asked me if I would be willing to re-create “R Markdown” training slides (which I did for "Stats Software Initiative Training –-- R Markdown" in Feb 2018) using xaringan for PD (Product Development) wide R workshops.  I was not sure how much time needed, but since I had half a day free, I decided to have a go. I did learn the package and re-create the R Markdown training slides in HTML5 format!

 

Yihui Xie said that xaringan is designed for ninja. If you are a beginner of HTML/CSS, you may have to stick with the default CSS (which is not bad). The more you know about CSS, the more you can achieve with this package. The sky is your limit. The resulted slides are in HTML5 format. You can use "presenter mode" by pressing `p` on keyboard! It is a great way for you to view your presentation with your speaker notes on one computer (your laptop, for example), while the audience views the notes-free presentation on a different monitor. You can even [embed a live video of yourself through your camera in HTML5 slides](https://yihui.name/en/2017/12/html5-camera/)!

 

I only used the basic features since I don't know much about CSS; I think it is sufficient for now. The slides I created with xaringan are better than the one I created in PowerPoint. All features I used in PowerPoint can be achieved, including the incremental slide. One advantage is for training type of slides, I can show the code in left and the output (automatically generated by R Markdown) in right. For slides presenting analysis results, all numbers/plots/tables can be displayed automatically. 

 

If you want to learn xaringan, you can read Yihui Xie’s [“Presentation Ninja”](https://slides.yihui.name/xaringan/). Here I just summarize some basics/tips:

* Install the xaringan package from Github:

```r
devtools::install_github("yihui/xaringan")
```

* The easiest way to create a new R Markdown document is to use a template and modify it. In Rstudio, from the menu `File -> New File -> R Markdown -> From Template -> Ninja Presentation`

* Use the RStudio Addin "Infinite Moon Reader" to live preview the slides (every time you update and save the Rmd document, the slides will be automatically reloaded in RStudio Viewer).

* For dividing slides, use three dashes `---` (see an example from the template above)

* To create incremental slide (show the content in one slide incrementally), use two dashes `-- `

* For speaker note, use `???`

* You can split one slide into left and right using `.pull-left[]` and `.pull-right[]`

* You can add footnote with `.footnote[]`

* For lists, fonts, link, images, equations etc, the syntax is same as R Markdown. If you use local images (those not generated by R code or not on the internet), put image files in the same location as your .Rmd file 

* If you want to show/display R Markdown code/text (don’t want R Markdown to evaluate/execute the code), wrap the R codes/text as below

```r
 ````markdown
       R codes
 ````
```

For inline R code, use 

```r
`` `r knitr::inline_expr("expression")` ``
```

which produces 

```r
`r expression`
```


I hope you have a chance to try this package and enjoy using it!