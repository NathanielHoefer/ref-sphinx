
Info to Sort
============

Creating a webpage
------------------

Execute the following command from ``doc/`` to generage an HTML webpage::

    // Execute from doc/
    make html

Test the code within the documentation
Code found within the documentation can be tested to ensure that it is correctly being displayed.
There are several methods to tag code for testing

Using paragraphs beginning with ``>>>``. Note, these paragraphs don't need to be indented::

    >>> print 'Hello World!'
    Hello World!

Using the ``testcode`` and ``testoutput`` directives::

    .. testcode::

        print 'Hello World!'

    .. testoutput::

        Hello World!

To execute the tests, run the following command::

    // Execute from doc/
    make doctest

Hosting Documentation
---------------------

Documentation can be hosted on a number of websites for free. The primary hosting service is
`ReadTheDocs.org`_ and is fairly straight forward to use. Simply create and account, supply the path to
your repository, then wait for your documentation to be built.

 .. _ReadTheDocs.org: https://readthedocs.org/

 .. note::

    In order to have the documentation automatically update when changes are pushed, to your repository,
    you will need to set up a hook within your repository settings.

Version Control
---------------

Sphinx and reStructuredText is compatible with version control systems, however be sure to omit
``_build/`` since it contains information not needed for versioning.

Themes
------

A theme can be changed via the ``conf.py`` file.
The themes available can be found online or within the source directory of sphinx.::

    ~/<path>/lib/python2.7/site-packages/sphinx/themes/

ReadTheDocs Sphinx Theme
~~~~~~~~~~~~~~~~~~~~~~~~

The ReadTheDocs Sphinx Theme can be found `here`_ along with the installation and examples

 .. _here: http://sphinx-rtd-theme.readthedocs.io/en/latest/#

Personal Documentation Workflow
-------------------------------

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

Additional Comments
-------------------

* Every sentence/thought, break lines to improve version control modifications and editability.

