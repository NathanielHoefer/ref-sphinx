
Documentation Workflow
======================

This page lists my personal workflow for incorporating Sphinx into my documentation.

.. _ref-workflow:

Reference Workflow
------------------

In order to maintain an organized structure of reference material for all of the software engineering concepts I encounter on a daily basis,
I've decided to implement reference repositories to separate all of the information into modules.
Below are the steps that I implement to support consistency.

#. Create new repository on GitHub labelled 'ref-<name>'
#. Clone repo to PC
#. Copy ``.gitignore`` file into base of directory
#. Within the repo, execute ``sphinx quick-start``
#. Install `sphinx-rtd-theme <http://sphinx-rtd-theme.readthedocs.io/en/latest/installing.html>`_ into the directory following their instructions.
#. Create and ``.rst`` files and add them to ``index.rst``
#. Commit and push to GitHub
#. In the master repository, add the new repository as a submodule using the following command in ``docs/``::

    git submodule add <repo> [<path>]

#. If cloning the master repo with submodules, execute the following command::

    git submodule init

#. If needing to update all the submodules in the master repository, execute the following command::

    git submodule update --recursive --remote

#. Add the submodule index to the master ``index.rst``
#. Ensure that the webhook for ReadTheDocs on the master repo is correctly set up
#. Commit and push master repo updates to GitHub, and the changes should be reflected on ReadTheDocs

 .. note::

    Any git submodules must use HTTPS rather than SSH to be properly interpreted by ReadTheDocs

