
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

Version Control
---------------

Sphinx and reStructuredText is compatible with version control systems, however be sure to omit
``_build/`` since it contains information not needed for versioning.

Themes
------

A theme can be changed via the ``conf.py`` file.
The themes available can be found online or within the source directory of sphinx.::

    ~/<path>/lib/python2.7/site-packages/sphinx/themes/

Additional Comments
-------------------

* Every sentence/thought, break lines to improve version control modifications and editability.

`Sphinx Directives Documentation <http://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html?highlight=code-block#directive-code-block>`_
