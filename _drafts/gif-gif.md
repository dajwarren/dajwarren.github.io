---
layout: post
title: '/gɪf/ or /d͡ʒɪf/?'
---
*Disclaimer: nothing in this post should be taken overly seriously, especially everything in 'the longest answer'. I got bored and this is what resulted, nothing more and nothing less.*

The file format ```.gif``` seems to be the cause of a lot of disagreement. Sometimes rather passionate disagreement. But which pronunciation is correct?

## The short answer
It's pronounced 'gif'. Heh, aren't I amusing?

## The slightly longer answer
Some people use one pronunciation, others use a different one. This is fine.

## The longest answer
Imagine that you were coming across the word written down for the first time. You had never heard it spoken aloud.

## The technically-correct answer
The question is poorly formed.

~~~python
'''
Each line of the CMU Pronouncing Dictionary begins with the orthographic transciption, followed by two spaces, then the first phone, followed by a space, then the second phone and so on.

This script takes the input format and returns the dictionary as a tab-delimited text file.
'''
import re

def format_dict(cmu_dict, csv_dict):
    dictionary = open(cmu_dict, 'rU')
    lines = dictionary.readlines()
    output_dict = open(csv_dict, 'w')
    for line in lines:
        line = line.rstrip()
        lines = re.sub('  ', ',', line)
        output_dict.write(lines+'\n')
    dictionary.close()
    output_dict.close()

cmu_dict = '/home/david/FAVE/FAVE-align/model/dict'
csv_dict = '/home/david/Desktop/csv_dict.txt'
format_dict(cmu_dict, csv_dict)
~~~
