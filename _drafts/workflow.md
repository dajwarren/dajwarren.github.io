---
layout: post
title: Digital Workflow
---
As the work on writing and editing my PhD thesis picks up I've dedicated some time to improving my workflow. I've read several people's blog posts on the subject and decided to throw mine into the mix in the hope that someone, somewhere, will find it useful.

## Hardware and OS
<!--#TODO:0 correct this thing.-->
<!--#REVIEW:0 This isn't very good-->

I used to use Windows for everything, but a couple of years ago I took the plunge and moved all my academic work over to a separate partition on my desktop running Ubuntu. In addition to that I have an old iPhone 4 which I don't generally use for academic work and an even older laptop with a dodgy backlight that I also installed Ubuntu on and use whenever I don't have access to my desktop.

Long story short: desktop PC and Ubuntu.


## Data analysis / statistics

Years back when I was starting my PhD my supervisor strongly recommended that I use [R](https://www.r-project.org/), a programming language for statistics. I currently use [RStudio](https://www.rstudio.com/) as an IDE for all the things I do in R, but might move away from that soon as I'm not using the majority of the features anymore. That said, I would still recommend it as a way of making R somewhat more accessible, and the interface is fairly intuitive.

In terms of the R packages I use most often, ```dplyr``` and ```ggplot2``` are almost included by default now: the former because base R gets awkward to write for basic data manipulation tasks, and the latter because the graphs it produces are significantly nicer and more easily adjusted and customised. I use ```phonR``` for vowel normalisation and formant frequency plots as it offers more options and prettier outputs than ```vowels``` (the backend of the [Norm website](http://lingtools.uoregon.edu/norm/norm1.php)) and doesn't require a specific structure for the input data so I can use it directly with the output of FAVE-extract. Finally I use a combination of ```lme4``` and ```lmerTest``` for linear mixed effects regression models.

## Reference management

I don't know how I'd survive without a good way to manage the myriad papers, books and other resources (and their citation info) that I've accumulated over the past few years.

There are lots of software options out there, but I've settled on [Mendeley](https://www.mendeley.com/) for this. Because it has a built-in PDF reader with highlighting and annotation, I also use it for taking notes while reading, and usually write a basic summary of the main points in the Notes tab. Mendeley also allows folders to be shared with other Mendeley users for collaboration, so my supervisor has access to a folder containing the entire bibiography of my thesis and can add his own comments.

One of the other main draws was the free 2GB of online backup, and the ability to sync the entire library contents, PDFs included, to any device.

The list of citations is then outputted in a Bibtex-formatted file.

## Writing

I wrote my undergraduate Honours disseration (~8500 words) in MS Word 2010 and even with templates and styles it was a lot of hassle to bring everything together at the end. I felt like I was fighting the software and didn't want to experience that again with a document as large as a doctoral thesis. As it was, I discovered [LaTeX](https://www.latex-project.org/) about a month after submission and have used it for all my academic writing ever since, as well as for things like my CV. The markup even works on this blog: ```$$\textbf{LaTeX}$$``` = $$\textbf{LaTeX}$$.

If you haven't encountered it before, LaTeX is a 'document preparation system' and not a word processor. You write in plain text, denoting formatting (when needed) through use of markup tags. This is then compiled into an attractively-formatted PDF file by the TeX typesetting program. With the additional use of Sweave, R code can be executed within a LaTeX document during compilation, allowing the dynamic updating of graphs etc as more data is analysed or as the analysis changes. This is useful.

I used to use [Texmaker](http://www.xm1math.net/texmaker/) while working with LaTeX, but as with RStudio I didn't use the majority of the interface. I've now moved to using the text editor [Atom](https://atom.io/) with the ```language-latex``` package for syntax highlighting and ```latex-tools``` for compiling the PDF with a quick press of ```ctrl+shift+b```. If you have ```pdf-view``` installed, the compiled document will open in a separate pane within Atom. The downside to this is that I haven't yet found an easy way to compile the .Rnw file if I'm including R code: my solution right now is to use the ```atom-terminal``` package to open a terminal window in the directory of the currently-open file, run ```R CMD Sweave``` from the terminal, then return to Atom and compile the resulting .tex file as normal. Hopefully I'll solve that issue soon!

I probably haven't sold you on using Atom for your thesis yet. How about the ability to have multiple panes, so you can simultaneously show your current draft and an outline/notes page (or both)? Or the ```todo-show``` plugin, which displays a list of any time you've used a (customisable!) list of keywords, followed by the text immediately after them? You can then add comments in LaTeX with editing ideas and find them all easily. Or maybe the ability to have the entire folder containing your thesis documents open and searchable all the time? ...I think I'll end this here before it gets too long.

The other benefit to using plain text for writing is the ability to use ```git``` for version control and collaborative work. I now have a copy of my thesis in a private repository on Github, which also means it's available anywhere via a quick ```git clone```. The ability to see changes and revert to previous versions is going to prove more and more useful as I move from the first draft to the editing stage of writing.

## Backups and recovery

The last thing anyone wants to do is lose their work. Along with having my thesis hosted on Github, I use [Dropbox](http://dropbox.com/) for general backups. I also have local backups, both on a separate drive on my desktop and an external drive.

Of course, sometimes the worst still happens. I've twice had an SD card corrupt immediately upon removal from a digital recorder while doing fieldwork. The first time that happened my supervisor suggested [photorec](http://www.cgsecurity.org/wiki/PhotoRec), which despite its name can recover more than just pictures. You'll lose file names and folder structures, but it's both effective and free and having a messy collection of files to sort out is better than no files at all.
