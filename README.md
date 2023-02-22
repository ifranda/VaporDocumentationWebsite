# VaporDocumentationWebsite
This repository holds the html files that are used to host [Vapor's documentation github page](https://github.com/NCAR/VaporDocumentationWebsite).

We use the Sphinx documentation generator to produce the html for the website.

To reproduce this documentation locally, we recommend setting up a conda environment with the five dependencies listed below.  Once installed, the .rst files located in the docs/ directory can be edited to produce new html.

    $ conda env export --from-history
    name: VaporDocumentationWebsite
    channels:
      - conda-forge
      - ncar-vapor
      - defaults
    dependencies:
      - sphinx
      - sphinx-rtd-theme
      - sphinx-gallery
      - sphinx-book-theme
      - python=3.9
      - vapor

Once this conda environtment has been configured, the html can be generated with the following steps.

1) git clone https://github.com/NCAR/VaporDocumentationWebsite.git 
2) cd VaporDocumentationWebsite/docs
3) make html
4) cp -r html/* ../

Note that step 4 moves the html files from VaporDocumentationWebsite/docs/html to the root directory, VaporDocumentationWebsite.  Without this step, github pages will not host the the html files.
