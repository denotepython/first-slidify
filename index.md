---
title: "learn slidify"
author: "rocket-liu"
highlighter: highlight.js
output: pdf_document
job: null
knit: slidify::knit2slides
mode: selfcontained
hitheme: tomorrow
subtitle: a simple introduction to slidify
framework: revealjs
widgets: [mathjax]
---

## framework  reveal.js  impress.js
framework   : revealjs
framework   : impressjs

## 3 basic points

1. Edit YAML front matter
2. Write using R Markdown,Rmd docments
3. Use an empty line followed by three dashes to separate slides!


--- .class #id 
## this is the second title
### this is the three title
you can test every markdown docment here
$$r_t=\beta a$$


---

## > mark
>test the result of mark ">"


---
## link
http://www.kaggle.com/c/amazon-employee-access-challenge 


---
### the table
Column Name | Description
---|---
ACTION | ACTION is 1 if the resource was approved, 0 if the resource was not
RESOURCE | An ID for each resource
MGR_ID | The EMPLOYEE ID of the manager of the current EMPLOYEE ID record
ROLE_ROLLUP_1 | Company role grouping category id 1 (e.g. US Engineering)

---
### use `` to highlight
`python` is  good

---
### code

```r
(t <- data.frame(true_label=c(0,0,0,0,1,1,1,1),
                   predict_1=c(1,2,3,4,5,6,7,8),
                   predict_2=c(1,2,3,6,5,4,7,8),
                   predict_3=c(1,7,6,4,5,3,2,8)))
```

```
##   true_label predict_1 predict_2 predict_3
## 1          0         1         1         1
## 2          0         2         2         7
## 3          0         3         3         6
## 4          0         4         6         4
## 5          1         5         5         5
## 6          1         6         4         3
## 7          1         7         7         2
## 8          1         8         8         8
```


---
### print code and result

```r
a <- c(1:10)
sum(a)
```

```
## [1] 55
```


---
### hide code print result

```
## [1] 55
```

---
### hide result print code

```r
a <- c(1:10)
sum(a)
```


---
*** up

```r
data.frame(true_label=t$true_label, 
           predict_2=t$predict_2, 
           predict_label=(t$predict_2>=6))
```

```
##   true_label predict_2 predict_label
## 1          0         1         FALSE
## 2          0         2         FALSE
## 3          0         3         FALSE
## 4          0         6          TRUE
## 5          1         5         FALSE
## 6          1         4         FALSE
## 7          1         7          TRUE
## 8          1         8          TRUE
```

*** down

```r
table(t$predict_2>=6, t$true_label)
```

```
##        
##         0 1
##   FALSE 3 2
##   TRUE  1 2
```


---
## Question 1
What is 1 + 1?
1. 1
2. 2
3. 3
4. 4
***.hint This is a hint
***.explanation This is an explanation



