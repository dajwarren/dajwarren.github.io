---
title: Research
layout: page
thumbnail: graduation-cap
---
## Thesis
### The Scottish Vowel Length Rule
I am currently examining the impact of coda consonant voicing on vowel timing in language varieties spoken in the North East of Scotland. The primary focus is on the Scottish Vowel Length Rule (Aitken's Law), the name given to a phenomenon across much of Scotland and the very north of England in which a vowel is realised with a greater duration if it precedes any voiced fricative, the rhotic phoneme, or a morpheme boundary.


{% for post in site.posts %}
  {% if post.categories contains "SVLR"%}
  <h2 id="{{ category | first }}-ref">{{ category | first }}</h2>
  <ul>
        <li>
          <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
          <small class="hidden-xs">{{ post.date | date: "%B %-d, %Y" }}</small>
        </li>
    </ul>
  {% endif %}
{% endfor %}

## Conferences
- Warren, David A. J. *forthcoming*\. Vowel timing and coda stop voicing: the ‘Voicing Effect’ in North East Scotland. *Poster presentation*, UKLVC11: Cardiff.
- Warren, David A. J. *forthcoming*\. Phonetic preaspiration of word-final voiceless fricatives in North East Scotland. *Poster presentation*, Linguistics and English Language Postgraduate Conference: University of Edinburgh.
- **Warren, David A. J.** & Barras, Will. 2015\. The Scottish Vowel Length Rule in North East Scotland. *Poster presentation*, UKLVC10: York.

## Talks
- *forthcoming*. Vowel timing in North East Scotland. Centre for Linguistic Research: University of Aberdeen.
- 2015\. The Scottish Vowel Length Rule in North East Scotland. Glasgow University Laboratory of Phonetics (GULP): University of Glasgow.
