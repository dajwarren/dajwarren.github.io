---
layout: post
title:  "Testing things"
date:   2016-09-12
categories: testing
---
Let's just get to grips with Markdown (kramdown) for a moment.
## This is title

# This is also title

### As is this

##### Also this

> Now for blockquotes
>> Which can be nested?

Now we have lists:
+ A list
* Well, part of one
- Now this is silly

1. yes
2. no
3. maybe?

### Tables?

|-----------------+------------+-----------------+----------------|
| Default aligned |Left aligned| Center aligned  | Right aligned  |
|-----------------|:-----------|:---------------:|---------------:|
| First body part |Second cell | Third cell      | fourth cell    |
| Second line     |foo         | **strong**      | baz            |
| Third line      |quux        | baz             | bar            |
|-----------------+------------+-----------------+----------------|
| Second body     |            |                 |                |
| 2 line          |            |                 |                |
|=================+============+=================+================|
| Footer row      |            |                 |                |
|-----------------+------------+-----------------+----------------|  

Well, it's technically a table. It just looks awful <.< I'll fix it eventually

### Code blocks:

``` R
data$fol_seg <- 'SHORT'
data[data$svlr == 'no' & data$VE == 'yes' & data$svlr2=='short', ]$fol_seg <- 'VE-LONG'
data[data$svlr == 'yes' & data$VE == 'yes' & data$svlr2 == 'phono', ]$fol_seg <- 'SVLR-LONG'
data$fol_seg <- factor(data$fol_seg)
##recoding
```


### Abbreviations
I study the SVLR

### IPA

How does the inline IPA look?

ɪt lʉks faen ʌi hoːp

*[SVLR]: Scottish Vowel Length Rule
*[IPA]: International Phonetic Alphabet
