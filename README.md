# IPyPublish

A program for creating and editing publication ready scientific reports and presentations,
from one or more Jupyter Notebooks.

**Documentation**: [ipypublish.readthedocs.io](http://ipypublish.readthedocs.io)

[![CI Status](https://github.com/chrisjsewell/ipypublish/workflows/continuous-integration/badge.svg)](https://github.com/chrisjsewell/ipypublish/actions)
[![Coverage Status](https://codecov.io/gh/chrisjsewell/ipypublish/branch/develop/graph/badge.svg)](https://codecov.io/gh/chrisjsewell/ipypublish)
[![PyPI](https://img.shields.io/pypi/v/ipypublish.svg)](https://pypi.python.org/pypi/ipypublish/)
[![DOI](https://zenodo.org/badge/96322423.svg)](https://zenodo.org/badge/latestdoi/96322423)
[![Conda](https://anaconda.org/conda-forge/ipypublish/badges/version.svg)](https://anaconda.org/conda-forge/ipypublish)
[![Code Style](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/ambv/black)
<!-- [![Codacy Badge](https://api.codacy.com/project/badge/Grade/243d0038a2f543e7a9c47a781ca3cbf5)](https://www.codacy.com/app/chrisj_sewell/ipypublish?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=chrisjsewell/ipypublish&amp;utm_campaign=Badge_Grade) -->

>**Attention**:
This package is still maintained, but it is envisaged that it will eventually be superceeded by the [Executable Book Project toolchain](https://executablebooks.org/en/latest/tools.html). So definitely also check that out, and feedback any improvement suggestions! 😀

![Conversion Process](/docs/source/_static/main_image.png)

For an example of the potential input/output, see:
[Example.ipynb](example/notebooks/Example.ipynb),
[Example.pdf](https://chrisjsewell.github.io/ipypublish/Example.view_pdf.html),
[Example.html](https://chrisjsewell.github.io/ipypublish/Example.html) and
[Example.slides.html](https://chrisjsewell.github.io/ipypublish/Example.slides.html#/).

Or, for a practical example of the ipypublish capability, see these documents on Atomic 3D Visualisation:
[Notebook](https://github.com/chrisjsewell/chrisjsewell.github.io/blob/master/3d_atomic/3D%20Atomic%20Visualisation.ipynb),
[PDF](https://chrisjsewell.github.io/3d_atomic/converted/3D%20Atomic%20Visualisation.view_pdf.html),
[HTML](https://chrisjsewell.github.io/3d_atomic/converted/3D%20Atomic%20Visualisation.html) or
[Reveal.JS slideshow](https://chrisjsewell.github.io/3d_atomic/converted/3D%20Atomic%20Visualisation.slides.html).

## Design Philosophy

In essence, the dream is to have the ultimate hybrid of Jupyter Notebook, WYSIWYG editor (e.g. MS Word) and document preparation system (e.g. [TexMaker](http://www.xm1math.net/texmaker/)), being able to:

- Dynamically (and reproducibly) explore data, run code and output the results
- Dynamically edit and visualise the basic components of the document (text, math, figures, tables, references, citations, etc).
- Have precise control over what elements are output to the final document and how they are layed out and typeset.
  - Also be able to output the same source document to different layouts and formats (pdf, html,presentation slides, etc).

## Workflow

1. Create a notebook with some content!
2. optionally create a .bib file and external images
3. Adjust the notebook and cell metadata.
4. install ipypublish and run the `nbpublish` for either the specific notebook, or a folder containing multiple notebooks.
5. A converted folder will be created, into which final `.tex` `.pdf` and `.html` files will be output, named by the notebook or folder input

The default latex template outputs all markdown cells (unless tagged `latex_ignore`), and then only code and output cells with [latex metadata tags](#latex-metadata-tags).
See [Example.ipynb](https://github.com/chrisjsewell/ipypublish/blob/master/example/notebooks/Example.ipynb), [Example.pdf](https://chrisjsewell.github.io/ipypublish/Example.view_pdf.html),
[Example.html](https://chrisjsewell.github.io/ipypublish/Example.html) and [Example.slides.html](https://chrisjsewell.github.io/ipypublish/Example.slides.html#/) for examples of the potential input and output.

![WorkFlow Example](/example_workflow.gif)

**See the project site for more info!**

## Acknowledgements

IPyPublish is built as an extension to [nbconvert](https://nbconvert.readthedocs.io).

I also took strong influence from:

- [Julius Schulz](http://blog.juliusschulz.de/blog/ultimate-ipython-notebook)
- [Dan Mackinlay](https://livingthing.danmackinlay.name/jupyter.html)
- Notebook concatination was adapted from [nbconvert issue#253](https://github.com/jupyter/nbconvert/issues/253)
