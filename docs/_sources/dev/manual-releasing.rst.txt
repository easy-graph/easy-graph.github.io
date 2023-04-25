(Mostly) Manually Building and Releasing python-easygraph
=========================================================

.. raw:: html

   <!-- Author: [Teddy Xinyuan Chen](https://github.com/tddschn) -->

We choose to build Linux wheels on GitHub Actions because it’s reliable.
For other platforms, we build manually on our machines, because we’ve
yet to find a way to make it work on GitHub Actions.

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

After the workflow finishes, download the artifacts from the workflow
run page.

The artifact contains the built wheel file for Linux x86_64.

Unzip the artifact and remove anything but the ``.tgz`` source
distribution and ``.whl`` wheel files with ``linux`` in the name (if
applicable).

Build for other platforms
-------------------------

Do it manually on your machines:

.. code:: bash

   python3.{7..10} setup.py build_ext # expand the command yourself, to python3.10 etc

Locate find the built ``.whl`` files.

Put all the wheel files and source distribution in a directory and upload to PyPI
---------------------------------------------------------------------------------

Put all the wheel files and source distribution built in the previous 2
steps in a directory ``<your_directory>``, and run

::

   python3 -m twine upload <your_directory>/*