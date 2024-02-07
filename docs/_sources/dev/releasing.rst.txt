Building and Releasing python-easygraph
=======================================

.. raw:: html

   <!-- Author: [Teddy Xinyuan Chen](https://github.com/tddschn) -->

-  `Building and Releasing
   python-easygraph <#building-and-releasing-python-easygraph>`__

   -  `Prerequisites <#prerequisites>`__

      -  `Install GitHub CLI <#install-github-cli>`__

   -  `Build and Release to PyPI <#build-and-release-to-pypi>`__
   -  `Build and Release to Test
      PyPI <#build-and-release-to-test-pypi>`__
   -  `Build only <#build-only>`__

Prerequisites
-------------

Install GitHub CLI
~~~~~~~~~~~~~~~~~~

Please refer to `GitHub CLI
documentation <https://cli.github.com/manual/installation>`__ for
installation instructions.

Build and Release to PyPI
-------------------------

::

   gh workflow run release-cibuildwheel.yaml -F upload=pypi

Build and Release to Test PyPI
------------------------------

::

   gh workflow run release-cibuildwheel.yaml -F upload=test_pypi

Build only
----------

Build artifacts will be uploaded to GitHub Actions artifacts available
for download and inspection.

::

   gh workflow run release-cibuildwheel.yaml -F upload=none
