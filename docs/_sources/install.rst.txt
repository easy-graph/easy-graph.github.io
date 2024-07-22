
Installation
============

For Windows, MacOSX, and Linux users, we recommend using Python's 
package management system, `pip <https://pip.pypa.io/en/stable>`_ .
You can find EasyGraph on PyPI `here <https://pypi.org/project/Python-EasyGraph/>`_.

**Installation with** ``pip``
::

    $ pip install Python-EasyGraph

The package is no longer under maintenance on conda.
If you've previously installed EasyGraph, please uninstall it with conda and reinstall with pip.
If prebuilt EasyGraph wheels are not supported on your platform (OS / CPU arch, check here), you can build it locally as follows:

**Example installation with** ``conda``
::
    $ git clone https://github.com/easy-graph/Easy-Graph && cd Easy-Graph && git checkout pybind11
    $ pip install pybind11
    $ python3 setup.py build_ext
    $ python3 setup.py install

.. hint::
    EasyGraph uses `PyTorch <https://pytorch.org/get-started/locally/>`_ (version 1.12.1 to below 2.0) for machine
    learning functions.
    Note that this does not prevent you from running non-machine learning functions 
    if PyTorch is not installed in your environment.
    However, you will receive warnings indicating the unavailability of certain modules that depend on PyTorch.

    
    
