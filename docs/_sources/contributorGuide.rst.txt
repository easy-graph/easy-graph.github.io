Contributor Guide
=========================

.. Author: `Teddy Xinyuan Chen <https://github.com/tddschn>`__
.. Revised by: `Kun Cheng <https://www.linkedin.com/in/kun-cheng-080084291/>`

Thanks for taking time to contribute!

The following guidelines are intended to assist you in contributing to EasyGraph on GitHub. 
These guidelines should serve as suggestions rather than strict requirements. Please use your 
judgment and feel free to propose changes to this document by submitting a pull request.

Table of contents
^^^^^^^^^^^^^^^^^

`How to contribute <#how-to-contribute>`__

-  `Reporting bugs <#reporting-bugs>`__
-  `Suggesting enhancements <#suggesting-enhancements>`__
-  `Contributing to documentation <#contributing-to-documentation>`__
-  `Contributing to code <#contributing-to-code>`__
-  `Issue triage <#issue-triage>`__
-  `Git workflow <#git-workflow>`__

How to contribute
-----------------

Reporting bugs
~~~~~~~~~~~~~~

This section guides you through submitting a bug report for EasyGraph.
Adhering to these guidelines helps maintainers and the community 
understand your report, reproduce the behavior, and identify related
reports.

Before creating bug reports, please check the following `list 
<#before-submitting-a-bug-report>`__ to ensure that a new report is 
necessary. When you do create a bug report, please include as many details 
as possible and fill out the `required
template <https://github.com/easy-graph/Easy-Graph/blob/master/.github/ISSUE_TEMPLATE/---bug-report.md>`__,
as the information requested will assist maintainers in resolving the issue more quickly.

   **Note:** If you find a **Closed** issue that matches the one you encountered, open a new issue 
   and include a link to the original issue in your report.

Before submitting a bug report
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. raw:: html

   <!-- * **Check the [FAQs on the official website](https://python-EasyGraph.org/docs/faq)** for a list of common questions and problems. -->

-  **Check that your issue does not already exist in the **\ `issue
   tracker <https://github.com/easy-graph/Easy-Graph/issues>`__.

How do I submit a bug report?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Bugs are tracked on the `official issue
tracker <https://github.com/easy-graph/Easy-Graph/issues>`__ where you can create a new issue 
and provide the following information using the `template <https://github.com/easy-graph/Easy-Graph/blob/master/.github/ISSUE_TEMPLATE/---bug-report.md>`__.

Explain the problem and include additional details to help maintainers
reproduce the problem:

-  **Title**: Use a descriptive and specific title that summarizes the problem.
-  **Steps to Reproduce**: Outline the exact steps that lead to the issue. Include specific examples, links to relevant files or GitHub projects, and code snippets.
-  **Observed Behavior**: Detail what happens when the steps are followed and explain why this behavior is problematic.
-  **Expected Behavior**: Describe what you expected to happen instead and justify why this behavior is expected.

Provide more context by answering these questions:

-  **Did the issue start recently**, such as after 
   updating to a new version of EasyGraph, or has it always been a problem?
-  If the problem started happening recently, **can you reproduce the
   problem in an older version of EasyGraph?** What is the most recent 
   version in which the problem does not occur?
-  **Can you reliably reproduce the issue?** If not, provide details about the 
   frequency of the problem and the conditions under which it typically happens.

Include details about your configuration and environment:

-  **Which version of EasyGraph are you using?**
-  **Which Python version EasyGraph has been installed for?**
-  **What’s the name and version of the OS you’re using**?

Suggesting enhancements
~~~~~~~~~~~~~~~~~~~~~~~

This section guides you through submitting an enhancement suggestion for
EasyGraph, including completely new features and minor improvements to
existing functionality. Following these guidelines helps maintainers and
the community understand your suggestion and find related suggestions.

Before creating enhancement suggestions, please check `this
list <#before-submitting-an-enhancement-suggestion>`__ as you might find
out that you don’t need to create one. When you are creating an
enhancement suggestion, please `include as many details as
possible <#how-do-i-submit-an-enhancement-suggestion>`__. Fill in `the
template <https://github.com/easy-graph/Easy-Graph/blob/master/.github/ISSUE_TEMPLATE/---feature-request.md>`__,
including the steps that you imagine you would take if the feature
you're requesting existed.

Before submitting an enhancement suggestion
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. raw:: html

   <!-- * **Check the [FAQs on the official website](https://python-easygraph.org/docs/faq)** for a list of common questions and problems. -->

-  **Check that your issue does not already exist in the**\ `issue
   tracker <https://github.com/easy-graph/Easy-Graph/issues>`__.

How do I submit an Enhancement suggestion?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Enhancement suggestions are tracked on the `official issue
tracker <https://github.com/easy-graph/Easy-Graph/issues>`__ where you
can create a new one and provide the following information:

-  **Use a clear and descriptive title** for the issue to identify the
   suggestion.
-  **Provide a step-by-step description of the suggested enhancement**
   in as many details as possible.
-  **Provide specific examples to demonstrate the steps**..
-  **Describe the current behavior** and **explain which behavior you
   expected to see instead** and why.

Contributing to documentation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

One of the simplest ways to get started contributing to a project is
through improving documentation. EasyGraph is constantly evolving, this
means that sometimes our documentation has gaps. You can help by adding
missing sections, editing the existing content so it is more accessible
or creating new content (tutorials, FAQs, etc).

   **Note:** A great way to understand EasyGraph’s design and how it all
   fits together, is to add FAQ entries for commonly asked questions.
   EasyGraph members usually mark issues with
   `candidate/faq <https://github.com/easy-graph/Easy-Graph/issues?q=is%3Aissue+label%3Acandidate%2Ffaq+>`__
   to indicate that the issue either contains a response that explains
   how something works or might benefit from an entry in the FAQ.

Issues pertaining to the documentation are usually marked with the
`Documentation <https://github.com/easy-graph/Easy-Graph/labels/Documentation>`__
label.

Contributing to code
~~~~~~~~~~~~~~~~~~~~

Picking an issue
^^^^^^^^^^^^^^^^

   **Note:** If you are a first time contributor, and are looking for an
   issue to take on, you might want to look for `Good First
   Issue <https://github.com/easy-graph/Easy-Graph/issues?q=is%3Aopen+is%3Aissue+label%3A%22Good+First+Issue%22>`__
   labelled issues. We do our best to label such issues, however we
   might fall behind at times. So, ask us.

.. raw:: html

   <!-- If you would like to take on an issue, feel free to comment on the issue tagging `@python-easygraph/triage`. We are more than happy to discuss solutions on the issue. If you would like help with navigating -->

the code base, join us on our `Discord
Server <https://discord.gg/ppgcw2wUPg>`__.

Local development
^^^^^^^^^^^^^^^^^

To contribute to the EasyGraph codebase, you will need to set up EasyGraph locally. 
Refer to the official `documentation <https://easy-graph.github.io/>`__ to get 
started with EasyGraph.

   **Note:** Local development of EasyGraph requires Python 3.8 or
   newer.

First, clone the repository using git and navigate to its directory:

.. code:: bash

   git clone git@github.com:python-EasyGraph/EasyGraph.git
   cd EasyGraph

..

   **Note:** We recommend using a personal 
   `fork <https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/fork-a-repo>`__
   for this step. If you are new to GitHub collaboration, please refer
   to the `Forking Projects
   Guide <https://guides.github.com/activities/forking/>`__.

Next, install the required dependencies for EasyGraph and ensure 
that the current tests are passing on your machine:

.. code:: bash

   pytest

.. raw:: html

   <!-- EasyGraph uses [mypy](https://github.com/python/mypy) for typechecking, and the CI
   will fail if it finds any errors.  To run mypy locally:

   ```bash
   EasyGraph run mypy
   ``` -->

EasyGraph follows the `black <https://github.com/psf/black>`__ coding style
and it's essential to ensure that your code adheres to it. Failure to comply 
will cause the CI to fail, and your Pull Request will not be merged.



Similarly, the import statements are sorted with
`isort <https://github.com/timothycrosley/isort>`__, and it's crucial to 
adhere to this style. Failure to do so will cause the CI to fail.

To prevent accidental commits of code that does not adhere to the 
coding style, you can install a
`pre-commit <https://pre-commit.com/>`__ hook. This hook checks 
that everything is in order before committing:

.. code:: bash

   pre-commit install

You can also execute it at any time using the following command:

.. code:: bash

   pre-commit run --all-files

Your code must always be accompanied by corresponding tests. Code 
without accompanying tests will not be merged.


Run the Tests Locally
^^^^^^^^^^^^^^^^^^^^^

-  Install `tox <https://tox.readthedocs.io/>`__ and
   `pyenv <https://github.com/pyenv/pyenv>`__
-  Use pyenv to install python 3.6 to 3.10, and make sure that
   ``python3.6``, ``python3.7``, …, ``python3.10`` is in your ``$PATH``.
-  Run ``tox`` to run the tests across python 3.6 to 3.10.
-  To run tox only on python3.9 and 3.10, use the command ``tox -e py39,py310``.

Pull requests
^^^^^^^^^^^^^

-  Fill in `the required
   template <https://github.com/easy-graph/Easy-Graph/blob/master/.github/PULL_REQUEST_TEMPLATE.md>`__
-  Make sure that your pull request contains tests that cover the changed
   or added code.
-  If your changes warrant a documentation change, the pull request must
   also update the documentation.

..

   **Note:** Make sure your branch is
   `rebased <https://docs.github.com/en/free-pro-team@latest/github/using-git/about-git-rebase>`__
   against the latest main branch. A maintainer might ask you to ensure
   the branch is up-to-date prior to merging your Pull Request if 
   changes have conflicts.

All pull requests, unless otherwise instructed, must first be 
accepted into the main branch (``master``).

Issue triage
~~~~~~~~~~~~

.. raw:: html

   <!-- > **Note:** If you have an issue that hasn't had any attention, you can ping us `@python-EasyGraph/triage` on the issue. Please, give us reasonable time to get to your issue first, spamming us with messages
   > does not help anyone. -->

If you are helping with the triage of reported issues, this section
provides some useful information to assist you in your contribution.

Triage steps
^^^^^^^^^^^^

.. raw:: html

   <!-- 1. If `pyproject.toml` is missing or `-vvv` debug logs (with stack trace) is not provided and required, request that the issue author provides it. -->

1. Attempt to reproduce the issue with the reported EasyGraph version or
   request further clarification from the issue author.
2. Verify that the issue has not already been resolved. You can attempt to
   reproduce using the latest preview release and/or EasyGraph from the
   main branch.
3. If the issue cannot be reproduced,

   1. Seek clarification from the issue’s author,

4. If the issue can be reproduced,

   1. comment on the issue confirming so
   2. if possible, identify the root cause of the issue.
   3. Consider fixing the issue by submitting a pull request.

.. raw:: html

   <!-- #### Multiple versions

   Often times you would want to attempt to reproduce issues with multiple versions of `EasyGraph` at the same time. For these use cases, the [pipx project](https://pypa.github.io/pipx/) is useful.

   You can set your environment up like so.

   ```sh
   pipx install --suffix @1.0.10 'EasyGraph==1.0.10'
   pipx install --suffix @1.1.0rc1 'EasyGraph==1.1.0rc1'
   pipx install --suffix @master 'EasyGraph @ git+https://github.com/easy-graph/Easy-Graph'
   ```

   > **Hint:** Do not forget to update your `EasyGraph@master` installation in sync with upstream.

   For `@local` it is recommended that you do something similar to the following as editable installs are not supported for PEP 517 projects.

   ```sh
   # note this will not work for Windows, and we assume you have already run `EasyGraph install`
   cd /path/to/python-EasyGraph/EasyGraph
   ln -sf $(EasyGraph run which EasyGraph) ~/.local/bin/EasyGraph@local
   ```

   > **Hint:** This mechanism can also be used to test pull requests. -->

Git Workflow
~~~~~~~~~~~~

All development work is performed against EasyGraph’s main branch
(``master``). All changes are expected to be submitted and accepted to
this branch.

Release branch
^^^^^^^^^^^^^^

When a release is ready, the following steps are necessary before the release is
tagged.

1. A release branch with the prefix ``release-``, eg:
   ``release-1.1.0rc1``.
2. A pull request from the release branch to the main branch
   (``master``) if it’s a minor or major release. Otherwise, to the bug
   fix branch (eg: ``1.0``).

   1. The pull request description MUST include the change log
      corresponding to the release (eg:
      `#2971 <https://github.com/easy-graph/Easy-Graph/pull/2971>`__).
   2. The pull request must contain a commit that updates
      `CHANGELOG.md <CHANGELOG.md>`__ and bumps the project version (eg:
      `#2971 <https://github.com/easy-graph/Easy-Graph/pull/2971/commits/824e7b79defca435cf1d765bb633030b71b9a780>`__).
   3. The pull request must have the ``Release`` label specified.

.. raw:: html

   <!-- Once the branch pull-request is ready and approved, a member of `@python-EasyGraph/core` will, -->

1. Tag the branch with the version identifier (eg: ``1.1.0rc1``).
2. Merge the pull request once the release is created and assets are
   uploaded by the CI.

..

   **Note:** We prefer a merge commit over a squash or rebase merge in this case.

Bug fix branch
^^^^^^^^^^^^^^

Once a minor version (eg: ``1.1.0``) is released, a new branch for the
minor version (eg: ``1.1``) is created for the bug fix releases. Changes 
identified or approved by the EasyGraph team as needing a bug fix should 
be submitted as pull requests to this branch.

The following criteria must be met for an issue to be accepted into a 
bug fix branch (trivial fixes may be considered on a case-by-case basis):

1. The issue disrupts core functionality and/or is a critical
   regression.
2. The change set does not introduce a new feature or change 
   existing functionality.
3. A new minor release is not expected within a reasonable time frame.
4. If the issue affects the upcoming minor/major release, a corresponding
   fix must be accepted into the main branch.x

..

   **Note:** This is subject to the interpretation of a maintainer
   within the context of the issue.
