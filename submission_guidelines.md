# HW/Lab Submission FAQ

- Screenshots of code are never accepted
- Never submit code as a plain text file (e.g., without syntax highlighting or fixed-width fonts) because it is too hard to read

### General

**Gradescope** has a [submission
guide](https://gradescope-static-assets.s3.amazonaws.com/help/submitting_hw_guide.pdf)
that recommends software for your phone to take pictures of written
homework and convert it to a PDF (your final submission to Gradescope
must be a PDF).

Note: the links in the PDFs will not work if you view the PDF on
github, but if you open the PDF in its own tab, or download it, all
the links should work.

**Canvas**: For lab submissions to Canvas, we will allow PDF as
submission formats.

**Collaboration**: Collaboration with your fellow students is OK and in fact recommended, although direct copying is not allowed.

**Internet**: The internet is allowed for basic tasks (e.g., looking up definitions on wikipedia, or documentation, or following basic tutorials) but it is
not permissible to search for answers to exact problems or to post requests for help on forums such as [math.stackexchange.com](http://math.stackexchange.com/)
or to look at solution manuals.

See also our [AI policy](./policies.md)

#### Merging multiple PDF files

**Mac** You can use the Preview software that comes with Mac, and drag-and-drop in the Thumbnail view, or follow these [instructions](https://support.apple.com/en-us/HT202945).

**Linux** install `pdftk` (e.g., `apt-get install pdftk`), and the on the command line, it's just `pdftk inputFile1.pdf inputFile2.pdf cat output outputFileName.pdf`.  This works on Mac and Windows too (on Mac, the exact command line works; on Windows, I'm not sure).

**Windows** there are [lists of free web- and desktop-based software](https://superuser.com/a/34294), including [i-love-pdf](https://www.ilovepdf.com/merge_pdf), but [PDFtk](https://www.pdflabs.com/tools/pdftk-the-pdf-toolkit/) is one of the most classic and respected (no viruses). I haven't used PDFtk on Windows, but the website claims they have a GUI; or if you don't like their GUI, try a [3rd party GUI that uses PDFtk](https://www.pdflabs.com/tools/pdftk-the-pdf-toolkit/).

### Python
For overall Python, and numpy in particular, Matlab users might like [NumPy for Matlab users](https://numpy.org/doc/stable/user/numpy-for-matlab-users.html).

For **plotting** in Python using Matplotlib, try these [plotting cheatsheets](https://github.com/matplotlib/cheatsheets) and [controlling figure aesthetics](https://seaborn.pydata.org/tutorial/aesthetics.html) with seaborn. Export figures to PDF (rather than a raster format like png or jpeg) when possible since it will retain the nice fonts.


#### Jupyter

Tips for exporting jupyter notebook code to a PDF:

- From Colab, you can select "Print" and then "Print to PDF". This isn't the most beautiful method but it's good enough for the class.

- You can try this [Notebook to PDF conversion website](https://htmtopdf.herokuapp.com/ipynbviewer/) that some of our students have had good luck with

- Or try `nbconvert` which requires [`pandoc`](https://pandoc.org/installing.html). You can do this on [Colab](https://colab.research.google.com/), following the [instructions here](https://stackoverflow.com/a/54191922) (but note that you may need to add a backslash before any white space when you run commands, e.g., change a command like

`!cp drive/My Drive/Colab Notebooks/Untitled.ipynb ./`
to
``!cp drive/My\ Drive/Colab\ Notebooks/Untitled.ipynb ./``
)

Note that if you include latex in the jupyter notebook, when you run `nbconvert`, you cannot have any whitespace near the `\$` symbols for math due to a requirement of `pandoc` (see [here](https://pandoc.org/MANUAL.html#extension-tex_math_dollars)).  So, ``$ f(x) = 3x^2 $`` will not work, but `$f(x) = 3x^2$` will be OK.

The downside of `nbconvert` is that images are saved as png, not pdf, so fonts don't come through, but that's not a big deal for homework.

Tips for locally exporting a jupyter notebook to pdf

- You will likely need some sort of a local installation of LaTeX to export to PDF directly.
  
- If you run jupyter locally, you might be able to run `nbconvert` without using the command line; go to "Download" the "PDF via LaTeX".
  
- A similar method can be down for exporting to HTML, without the need for a local LaTeX installation.

- A workaround for exporting a jupyter notebook to a pdf, is to export it to HTML first, then open the HTML file in a browser and print to pdf. Warning, this can cut off some of the outputs of your code/the code itself, so make sure all of your code and its outputs are included in the pdf. This can be done by either changing the scale when printing to pdf or formatting your code to have line breaks.


#### Python source code (not Jupyter), or really any kind of source code
The *unacceptable* ways are
- screenshot of your code editor (not so nice since it's an image not text);
- export from a standard **text editor** to PDF (not so nice if you don't get syntax color highlighting). It's not nice to the graders to submit code without syntax color highlighting!

Acceptable: from a code editor, print to a PDF. This retains color syntax highlighting.

Better ways: it depends on your system and editor, but there are many ways. For example, this [stackoverflow 'printing python code to PDF'](https://stackoverflow.com/q/20412038) offers several suggestions. For example, since I already use `vim` and its setup with syntax highlighting, I can do [this answer](https://stackoverflow.com/a/20412421) and do `vim abc.py -c ":hardcopy > abc.ps" -c ":q"` followed by `ps2pdf abc.ps abc.pdf` -- no extra software needed!

Another way is to use the `minted` package with LaTeX. A tutorial on this from overleaf is [here](https://www.overleaf.com/learn/latex/Code_Highlighting_with_minted). Make sure that it has proper syntax highlighting and formatting before you submit.
