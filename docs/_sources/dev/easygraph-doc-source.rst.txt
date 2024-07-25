Scripts and guides for generating documentation for EasyGraph
=============================================================

.. raw:: html

   <!-- Author: [Teddy Xinyuan Chen](https://github.com/tddschn) -->

Repository:
`easygraph-doc-source <https://github.com/easy-graph/easygraph-doc-source>`__

-  `Scripts and guides for generating documentation for
   EasyGraph <#scripts-and-guides-for-generating-documentation-for-easygraph>`__

   -  `Prerequisites <#prerequisites>`__
   -  `Update ``rst`` files <#update-rst-files>`__

      -  `Edit manually created ``rst``
         files <#edit-manually-created-rst-files>`__
      -  `Generate ``rst`` files from docstrings as
         references <#generate-rst-files-from-docstrings-as-references>`__

   -  `Build HTML from ``rst`` files <#build-html-from-rst-files>`__
   -  `Deploy to easy-graph.github.io <#deploy-to-easy-graphgithubio>`__
   -  `Troubleshooting <#troubleshooting>`__

      -  `Reference built but not correctly displayed on the
         website <#reference-built-but-not-correctly-displayed-on-the-website>`__

Prerequisites
-------------

It is recommended to have conda/miniconda/anaconda installed on your machine. 
Clone these repositories and put them inside the same directory:

.. code:: bash

   REPOS=('Easy-Graph' 'easy-graph.github.io' 'easygraph-doc-source')
   for i in "${REPOS[@]}"; do
       echo "Cloning: $i"
       git clone "https://github.com/easy-graph/$i"
   done

Update ``rst`` files
--------------------

Edit manually created ``rst`` files
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Go to ``easygraph-doc-source/docs_using_sphinx``, and hand-edit / remove
/ add any ``rst`` files outside of ``reference``.

Generate ``rst`` files from docstrings as references
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code:: bash

   cd easygraph-doc-source/docs_using_sphinx
   make gen-rst
   # generated rst files in reference dir

Build HTML from ``rst`` files
-----------------------------

.. raw:: html

   <!-- 1. Update the `.rst` file in `docs_using_sphinx`
   2. Run terminal, changing work directory to `docs_using_sphinx`
   3. run `python3 -m venv .env` for the virtual environment
   4. run `source .env/bin/activate` to activate
   5. run `pip install -r requirements.txt` to install dependencies -->

-  Install dependencies in ``requirements.txt`` with the following command: ``pip install -r requirements.txt``.
-  Run ``make html``. The updated pages locate in ``./_build/html``.

Deploy to easy-graph.github.io
------------------------------

-  Sync all the files under ``./_build/html`` to repository
   ``easy-graph.github.io``:

.. code:: bash

   cd easygraph-doc-source
   make sync-doc-pub-repo

-  Push the changes of these two repository to their remotes

Troubleshooting
---------------

Reference built but not correctly displayed on the website
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Check the ``toctree`` of ``reference.rst``, you may need to manually
   update the section to reflect the built references.
-  Make sure the html files you generated are inside ``easygraph-doc-source/docs_using_sphinx/_build/html`` 
   if you intend to take a look.
