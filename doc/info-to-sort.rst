
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

Additional Comments
-------------------

* Every sentence/thought, break lines to improve version control modifications and editability.

