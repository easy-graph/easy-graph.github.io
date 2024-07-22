(Mostly) Manually Building and Releasing python-easygraph
=========================================================

.. raw:: html

   <!-- Author: [Teddy Xinyuan Chen](https://github.com/tddschn) -->

We build Linux wheels on GitHub Actions due to its reliability. 
For other platforms, we manually build on our local machines, 
as we haven't yet found a way to automate this process on GitHub Actions.

-  `(Mostly) Manually Building and Releasing
   python-easygraph <#mostly-manually-building-and-releasing-python-easygraph>`__

   -  `Prerequisites <#prerequisites>`__

      -  `Install GitHub CLI <#install-github-cli>`__

   -  `Build for Linux x86_64 <#build-for-linux-x86_64>`__
   -  `Build for other platforms <#build-for-other-platforms>`__
   -  `Put all the wheel files and source distribution in a directory
      and upload to
      PyPI <#put-all-the-wheel-files-and-source-distribution-in-a-directory-and-upload-to-pypi>`__

Prerequisites
-------------

Install GitHub CLI
~~~~~~~~~~~~~~~~~~

Please refer to `GitHub CLI
documentation <https://cli.github.com/manual/installation>`__ for
installation instructions.

Build for Linux x86_64
----------------------

::

   gh workflow run release-cibuildwheel.yaml -F upload=none

Once the workflow completes, download the artifacts from the workflow
run page.

The artifact contains the built wheel file for Linux x86_64.

Unzip the artifact and retain only the ``.tgz`` source
distribution and ``.whl`` wheel files with ``linux`` in their names (if
applicable), discarding anything else.

Build for other platforms
-------------------------

Do it manually on your machines:

.. code:: bash

   python3.{7..10} setup.py build_ext # expand the command yourself, to python3.10 etc

Locate find the built ``.whl`` files.

Put all the wheel files and source distribution in a directory and upload to PyPI
---------------------------------------------------------------------------------

Place all the wheel files and source distributions generated in the previous two steps
in one directory ``<your_directory>`` and run

::

   python3 -m twine upload <your_directory>/*