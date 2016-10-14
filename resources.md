---
layout: page
title: Resources
permalink: /resources/
---
This is a list of the software I use, or no longer use but would still recommend, during my time as a linguistics undergraduate and now as a PhD candidate specialising in (socio)phonetics.

While perhaps not everything here is strictly-speaking the best tool for the job, they're what I've come to prefer. There's also the added bonus that everything here is free, and many are open-source too.

## Audio software

#### Recording
**[Audacity]():** Right now I'm using headset mics connected to a designated digital audio recorder. As a result, I don't generally use any software day-to-day for making recordings. The times I've needed to, I've used Audacity after it was recommended by a lecturer a couple of years back. It seems pretty good, and better than Praat's recording option.

#### Conversion & manipulation
**[SoX](http://sox.sourceforge.net):** While Audacity seems perfectly capable when it comes to audio conversion, downsampling and channel splitting, I much prefer command line utilities, especially for tasks that are often repetitive and therefore should be automated. That's why I generally use SoX.

## Forced Alignment
**[FAVE (Forced Alignment and Vowel Extraction)](https://github.com/JoFrhwld/FAVE):** FAVE is built upon P2FA. Although trained on a corpus of American English, FAVE [performs considerably better](http://personalpages.manchester.ac.uk/staff/laurel.mackenzie/files/MacKenzie_Turton_NWAV42_slides.pdf) than both PLA and SPPAS when aligning varieties of British English if provided with a British pronunciation dictionary. I've also had generally good results with Scottish English and Scots.

## IPA keyboards

#### Local
**[UCL IPA keyboard](http://www.phon.ucl.ac.uk/resource/phonetics/):** Before I switched to Ubuntu from Windows I used this keyboard layout. I tried several, and this one felt most intuitive, with the added ability of being able to type without having to take time to select symbols.

Unfortunately, I can't use it anymore. I tried others, but they didn't work out for me. The end result was that I made my own version, and expanded it to add almost the entirety of the IPA characterset. When I get round to sharing it, I'll update this.

<!-- #### Web-based
**[Chomskey](http://sci1.uk/Chomskey/#ucl-ipa):** I had the horrible experience of teaching in a room with only a projector and a screen. This meant making do with an inevitably-clunky and unfamiliar web-based keyboard if I need to type any IPA unplanned. Apparently I complained enough at home that this was made for me. It lets you type IPA just like a keyboard layout, and is therefore awesome. Also the name. -->

## Speech analysis
**[Praat](http://www.fon.hum.uva.nl/praat/):** If you're in the phonetic sciences, you'll almost certainly know Praat. It's amazing. You can do both acoustic measurement and speech manipulation for perceptual work. It also has its own scripting system that, while perhaps a little quirky in places, is incredibly useful for automating work. Best of all, the entire thing is free. Seriously, go use Praat.

## Statistics
**[R](https://www.r-project.org/):** R is a programming language and environment for doing statistics, data manipulation, data plotting, machine learning and more. And you should be using it. Yes, there is a learning curve, but the benefits hugely outweigh the time taken to learn it.

One of the major benefits is the easy of reproducing results. Give your  R code and data to someone, and, in a few keystrokes, they can reproduce your analysis exactly. What if you make a minor error when coding your data?--correct it then run the code and all your tests, models and plots will be updated automatically.

R also has a huge range of libraries for pretty much anything you'd want to do, and if you can't find what you need, you can write the packages and functions yourself. This means you get access to cutting-edge methods that haven't yet been included in the commercial statistics packages.

Here's a list of the packages I use most often:
- ```dplyr```: makes basic data tidying and manipulation so. much. easier. than it normally is in R. It's fantastic and should be learned and used by everyone.
- ```ggplot2```: almost certainly the best way of producing plots and graphs in R. Relatively easy to use (and with excellent documentation) and the results are beautiful.
- ```lme4```: used for building and running mixed effects regression models.
- ```phonR```: lots of people swear by the ```vowels``` package for creating vowel plots, but I've never been overly fond of their output and the requirement that the input data be structured a specific way annoys me. ```phonR``` produces much nicer plots, has all the normalisation methods included in ```vowels``` and has fewer requirements about data structure (it can, thankfully, accept input straight from FAVE-extract!).

#### IDE
**[RStudio](https://www.rstudio.com/):** RStudio is an IDE for R.
<!-- TODO: finish writing about RStudio -->

## Text editors
**[Atom](https://atom.io/):** Currently my favourite text editor. It's what I write my thesis in, manage my website with, and many other things. It's hugely customisable via plugins (and you can make your own). It will also probably get a blog post.

**[Vim](http://www.vim.org/):** An incredibly powerful editor, though doesn't exactly score highly on immediate user-friendliness. One day I will learn it properly.

**[Texmaker](http://www.xm1math.net/texmaker/):** Okay, so it isn't a text editor, but it's going in the section because if all you're doing is writing LaTeX and want a UI for it then I really like Texmaker. Before discovering Atom it was my preferred editor and the ability to compile from the GUI is useful even if you're not using most of the other features. It's also cross-platform.
