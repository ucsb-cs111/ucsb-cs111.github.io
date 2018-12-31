---
topic: "LaTeX Tutorial"
desc: "A formatting language for Mathematical documents"
---


# Resources


These resources will be useful for almost everything outside
of the small scope of this tutorial. Thus, they are displayed
prominently at the top.


* [<i class="far fa-file-pdf"></i> The Not So Short Introduction to LaTeX2e](http://tobi.oetiker.ch/lshort/lshort.pdf) - Great introduction to LaTeX
* [LaTeX Wikibook](http://en.wikibooks.org/wiki/LaTeX) - Full of detailed examples for just about anything
* [Comprehensive list of symbols](http://www.ctan.org/tex-archive/info/symbols/comprehensive/symbols-a4.pdf) - Don't know
   how to make that symbol that was used in class? Look it up in this
   massive PDF (try searching the closest english you know, or look
   through the index at the end).


# Prerequisites

First and foremost, you will need access to a copy of LaTeX.
You should be able to install a LaTeX distribution for nearly any operating system:



* [Windows](http://miktex.org/)
* [Mac OS X](http://mactex-wiki.tug.org/wiki/index.php/Main_Page)
* [Linux](http://tug.org/texlive/)


You could also use SSHFS, SSH and your CSIL account, rather
than install these rather large distributions.

Alternatively, something like [LyX](http://www.lyx.org/) is a great
all-in-one solution.
	    
Finally, we will need a favorite text editor and a copy of MATLAB.
		


# Template directory
		
The template files are in the following github repo:

* <i class="fab fa-github"></i><https://github.com/ucsb-cs111/latex-template>

Here is a summary of the files:
			   

| File             | Explanation |
|------------------|-------------|
| `latex_tut.tex`  | LaTeX source file. **Read through this carefully** |
| `Makefile`       | Runs `pdflatex latex_tut` 3 times&mdash;just to be safe. |
| `finitefern.m`   | Matlab code used to generate figure. |
| `finitefern.pdf` | PDF version of the figure generated in Matlab.
| `placeins.sty`   | LaTeX package that is included so the `FloatBarrier` command can be used. |

Run `make` in the `template` directory.

If your machine doesn't have `make`, run `pdflatex latex_tut` (you may need to run this 3 times).

If you have some time, [rubber](https://launchpad.net/rubber) is a *much*
better alternative to `make` or the by-hand method.

# Create a Matlab figure

The instructions to duplicate the figure (or replace it with your own)
included in the template directory are simple.  I used
`finitefern` to generate my figure.  Run the code and a figure
should appear.  Then save the figure as a PDF.  Place the code that
generated the figure and the PDF in the same directory as your LaTeX
code.

# Credits

This file was authored by Jeff Tyson, and refomatted for Markdown by P. Conrad
