==================
Yummy Sphinx Theme
==================

.. image:: https://img.shields.io/pypi/v/yummy_sphinx_theme.svg
    :target: https://pypi.org/project/yummy_sphinx_theme/

.. image:: https://img.shields.io/github/release/TagnumElite/yummy_sphinx_theme/all.svg
    :target: https://github.com/TagnumElite/yummy_sphinx_theme

.. image:: https://img.shields.io/pypi/l/yummy_sphinx_theme.svg
    :target: https://pypi.org/project/yummy_sphinx_theme/

.. image:: https://img.shields.io/pypi/pyversions/yummy_sphinx_theme.svg
    :target: https://pypi.org/project/yummy_sphinx_theme/

.. image:: https://img.shields.io/github/issues-raw/TagnumElite/yummy_sphinx_theme.svg
    :target: https://github.com/TagnumElite/yummy_sphinx_theme

.. image:: https://img.shields.io/travis/TagnumElite/yummy_sphinx_theme/develop.svg
    :target: https://travis-ci.org/TagnumElite/yummy_sphinx_theme

The yummy_sphinx_theme is created from `DONGChuan's Yummy-Jekyll <https://github.com/DONGChuan/Yummy-Jekyll>`_

The niftools_sphinx_theme is a modification of the yummy_sphinx_theme for the niftools team.
If either has a complaint with what I have made, because I did do this without any legal knowledge.
Or proper creditation.

.. contents::

`Demo <http://tagnumelite.com/yummy_sphinx_theme>`_
=============================================================

Installation
============
There are two ways to install these themes

Via Python Package Interface
----------------------------

Download the package and add ``sphinx`` to your ``requirements.txt`` file:

.. code:: bash

    pip install yummy_sphinx_theme

In your ``conf.py`` file:

.. code:: python

    html_theme = "yummy_sphinx_theme"

Via git or download
-------------------

Download the ``yummy_sphinx_theme`` folder into your documentation at
``docs/_themes/`` then add the following two lines to your Sphinx
``conf.py`` file:

.. code:: python

    html_theme = "yummy_sphinx_theme"
    html_theme_path = ["_themes", ]

=========
Changelog
=========

Yummy
=====

0.1.0:
------
* Remove niftools_sphinx_theme
* Added option to disable geopattern
* Add background image fallback for jumbotron

0.0.6:
------
* Fix theme.css_t problem
* Add Home Name Config
* Remove Unwanted File
* Fix Version 0.0.5
* Add versions footholder

0.0.5:
------
* Fix Theme Problems
* Update Docs

0.0.4:
------
* Default Footer Icon
* Fix Table Of Contents
* Customizable Table Of Contents

0.0.3:
------
* More color customization
* `Customizable navbar icon <http://fontawesome.io/icons/>`_

0.0.2:
------
* Add Dedicated Documentation Page
* Add Disqus
* Add Content To Layout
* Made Navbar into Dictionary
* Made Navbar background color customisable in theme conf
* Use bowser to manage dependencies
* Add GitHub, GitLab, BitBucket and Canonical Urls
* Disable Octicons and Primer-Markdown
* Clean Layout.html
* Source Code footer Icon changes to the specified url
* Add the missing end html tag

0.0.1:
------
* Turn jekyll theme into sphinx theme
* Renamed project from niftools_sphinx_theme to yummy_sphinx_theme


