
Installation
============

For users of Windows, MacOSX, and Linux, we recommend using Python's 
package management system, `pip <https://pip.pypa.io/en/stable>`_ .
EasyGraph's site on PyPI - `Link <https://pypi.org/project/Python-EasyGraph/>`_

**Installation with** ``pip``
::

    $ pip install Python-EasyGraph

The conda package is no longer updated or maintained.
If you've installed easygraph this way before, please uninstall it with conda and install it with pip.
If prebuilt easygraph wheels are not supported for your platform (OS / CPU arch, check here), you can build it locally this way:

**Example installation with** ``conda``
::
    $ git clone https://github.com/easy-graph/Easy-Graph && cd Easy-Graph && git checkout pybind11
    $ pip install pybind11
    $ python3 setup.py install

.. hint::
    EasyGraph uses `tensorflow 2 <https://www.tensorflow.org/install>`_ for machine 
    learning functions. If cuda settings for GPU are not well deployed in your PC, you will
    get similar warning messages as the followings when using tensorflow-based methods
    (e.g. easygraph.functions.graph_embedding.line.LINE):
    ::
        2020-11-09 13:40:31.453228: W tensorflow/stream_executor/platform/default/dso_loader.cc:59] Could not load dynamic library 'cudart64_101.dll'; dlerror: cudart64_101.dll not found
        2020-11-09 13:40:31.456194: I tensorflow/stream_executor/cuda/cudart_stub.cc:29] Ignore above cudart dlerror if you do not have a GPU set up on your machine. 

    Note that this does not prevent the codes from running normally, because tensorflow will
    leverage CPU in case GPU cannot be used. If you want to use GPU, this `link <https://www.tensorflow.org/install/gpu>`_ might be
    helpful for GPU settings.
    
    
