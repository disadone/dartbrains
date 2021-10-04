![alt text](https://github.com/ljchang/dartbrains/blob/master/images/logo/dartbrains_logo_square_transparent.png)
[![DOI](https://zenodo.org/badge/171529794.svg)](https://zenodo.org/badge/latestdoi/171529794)
[![deploy-book](https://github.com/ljchang/dartbrains/actions/workflows/deploy-book.yml/badge.svg?branch=master)](https://github.com/ljchang/dartbrains/actions/workflows/deploy-book.yml)

# DartBrains
DartBrains.org is an open access online educational resource that provides an introduction to functional neuroimaging analysis methods using Python. DartBrains is built using Jupyter-Book and provides interactive tutorials for introducing the basics of neuroimaging data analysis. This includes the basics of programming, signal processing, preprocessing, univariate analyses using the general linear model, functional connectivity, and multivariate analytic techniques (e.g., prediction/classification and representational similarity analysis). The tutorials focus on practical applications using open access data, short open access video lectures, and interactive Jupyter notebooks. All of the tutorials use open source packages from the python scientific computing community (e.g.,  numpy, pandas, scipy, matplotlib, scikit-learn, networkx, nibabel, nilearn, fmriprep, and nltools). The course is designed to be useful for varying levels of experience, including individuals with minimal experience with programming, Python, and statistics.

# Contributing
One of the wonderful aspects of both the neuroimaging and Python scientific computing communities is the strong commitment to developing and sharing knowledge and tools within the broader community. The goal of the dartbrains project is to build on this work and provide a resource for people to learn about how to analyze neuroimaging data. We try to incorporate as much open content as we can find that contributes to this goal. Please let us know if we have inadvertently ommitted credit for any content generated by others. Though this project is based on a neuroimaging analysis course taught at Dartmouth College, we welcome contributions from anyone in the broader imaging community.

# Getting Started
The DartBrains project is hosted on [github](https://github.com/ljchang/dartbrains). If you have any questions, comments, or suggestions, please open an issue.

If you notice any mistakes or have idea for new content, please either open an issue or submit a pull request for us to review.

The website is built using [jupyter book](https://jupyter.org/jupyter-book/intro.html), which creates a jekyll website from markdown and jupyter notebooks. Please read their materials to learn more about this neat resource.

# Updating Book
To update the book, you will need to build it locally using [jupyter-book build](https://jupyterbook.org/start/build.html) and then push it to github. We are syncing the code to master and the deployed website to the gh-pages branch. I recommend using [ghp-import](https://github.com/c-w/ghp-import) to make this easier. We are using the new version of jupyter-book, so make sure this package is up to date. You will also need to install `ghp-import`. I think we can probably set this up to autobuild on travis or circelci at some point if anyone wants to help with that.

1. **Install packages**

`pip install jupyter-book ghp-import`

2. **Build website locally**. The new version of jupyter-book will run the notebooks to generate the figures by default. I find it helpful to keep 1-2 subjects in `~/Github/dartbrains/data/localizer`, which is in .gitignore so it will not get pushed to github.

`jupyter-book build dartbrains`

3. **Push updated book to github**. This will sync the updated book to gh-pages branch of our github repository. Don't forget to submit a pull request or push the code to the master repository as well.

`ghp-import -n -p -f -c dartbrains.org _build/html` 

4. **Add domain name to settings**. Everytime we update the website, we need to tell github that we are using a custom domain name. This is annoying and should be an easy fix. I think it just has something to do with properly specifying the URL in the CNAME file. Until this is fixed, after syncing gh-pages branch, you will need to go into settings and add `dartbrains.org` as URL name.



# License for this book
All content in this book is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0) license.

# Acknowledgments
Dartbrains was created by Luke Chang and supported by an NSF CAREER Award 1848370.

Our jupyterhub server was built and maintained by the Research Computing staff at Dartmouth. Special thanks to Arnold Song, William Hamblen, Christian Darabos, and John Hudson.

