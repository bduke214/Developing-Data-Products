---
title       : Body Mass Index (BMI) Calculator
subtitle    : RStudio Shiny application
author      : Srikanth Kamineni
date        : February 22, 2015
transition  : rotate
transition-speed: fast
job         : "Coursera - Developing Data Products"
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Introduction

This is an RStudio shiny application developed as a course project for Coursera's **Developing Data Products** course in the *Data Science Specialization* track.
The developed application is a **Body Mass Index (BMI) Calculator**.  

### Course project requirements
The course project requirements for this application are:
* Some form of input (widget: textbox, radio button, checkbox, ...)
* Some operation on the ui input in sever.R
* Some reactive output displayed as a result of server calculations
* You must also include enough documentation so that a novice user could use your application.
* The documentation should be at the Shiny website itself. Do not post to an external link.

--- .class #id 

## BMI Definition

> The body mass index (BMI), or Quetelet index, is a measure of relative 
> weight based on the mass and height of an individual.

BMI is a way to calculate whether an individual's weight is considered to be
in the normal range for their height.

## How does the BMI calculator help?

To assist with the calculation, we've created a Shiny app that takes 2 inputs:

- Height (in feet and inches)
- Weight (in lbs)

Given the height and weight, the app will calculate the BMI for that individual.

---

## Application - Operations and Output

Based on user inputs, and using the BMI calculation equation, the application displays:  
1. Inputs entered by the user  
2. Calculated BMI output value
3. Body Mass Index chart

The BMI calculation equation is:  
** bmi = mass / height^2 ** conversion_const

As an example, with an input height of 5 feet 7 inches and a weight of 155 lbs, the
app would perform the following calculation in R:


```r
inches <- (5 * 12) + 7
weight <- 155
conversion_const = 703
bmi <- (weight / (inches^2)) * conversion_const
bmi
```

```
## [1] 24.27378
```

---

## Application - Link and Code

In addition to calculating the BMI, the app includes a reference chart that tells
what cateogry the calculated BMI falls into.
It should be noted that not everybody agrees how BMI numbers should be classified.
In spite of its shortcomings, BMI calculations can still be a useful measurement.

Try out the application on the RStudio shinyapps.io website:  
http://srikanthkamineni.shinyapps.io/BMI_Calculator/

Try out Rstudio Presentation on gh-pages:      
http://srikanthkamineni.github.io/Developing-Data-Products/index.html

To see the code for the application, visit github website:  
http://github.com/srikanthkamineni/Developing-Data-Products

Useful files in repo:  
* ```server.R```
* ```ui.R```
