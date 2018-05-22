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

