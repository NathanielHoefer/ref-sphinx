RST Quick Reference
===================

Sections
--------
Syntax::

    Title:

    <Title Name>
    ============

    Subtitle:

    <Subtitle Name>
    ---------------

    Subsection:

    <Subsection Name>
    ~~~~~~~~~~~~~~~~~


Emphasis
--------
Syntax::

    *Italic*
    **bold**
    ``variable name``
    ``function()``
    ``expression = 3 + 3``

Examples:

    | *Italic*
    | **bold**
    | ``variable name``
    | ``function()``
    | ``expression = 3 + 3``

Paragraph
---------
Syntax::

    Paragraph:
    A paragraph is one or more lines of un-indented text, separated
    from the material above and below by blank lines.

    Block Quotes:
        “Block quotes look like paragraphs, but are indented with
        one or more spaces.”

    Line Separations:
    | Because of the pipe characters, this will become one line,
    | And this will become another line, like in poetry.

    Terms and Definition:
    term
        Definition for the “term”, indented beneath it.
    another term
        And its definition; any of these definitions can continue on for
        several lines by -- you guessed it! -- being similarly indented.

    Lists:
    * Each item in a list starts with an asterisk (or “1.”, “a.”, etc).
    * List items can go on for several lines as long as you remember to
      keep the rest of the list item indented.

    Code Blocks:
    Code blocks are introduced by a double-colon and are indented::

       import docutils
       print help(docutils)

    Doctests:
        >>> print 'But doctests start with ">>>" and need no indentation.'

Examples:




Info to Sort
------------


Make an HTML webpage::

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
~~~~~~~~~~~~~~~~~~~~~

Documentation can be hosted on a number of websites for free. The primary hosting service is
`ReadTheDocs.org`_ and is fairly straight forward to use. Simply create and account, supply the path to
your repository, then wait for your documentation to be built.

 .. _ReadTheDocs.org: https://readthedocs.org/

 .. note::

    In order to have the documentation automatically update when changes are pushed, to your repository,
    you will need to set up a hook within your repository settings.

Version Control
~~~~~~~~~~~~~~~

Sphinx and reStructuredText is compatible with version control systems, however be sure to omit
``_build/`` since it contains information not needed for versioning.

Themes
~~~~~~

A theme can be changed via the ``conf.py`` file.
The themes available can be found online or within the source directory of sphinx.::

    ~/<path>/lib/python2.7/site-packages/sphinx/themes/

Additional Comments
~~~~~~~~~~~~~~~~~~~

* Every sentence/thought, break lines to improve version control modifications and editability.

