..  include:: /Includes.rst.txt

.. _literalinclude:

==============================
Code includes (Literalinclude)
==============================

A drawback of code blocks is that most editors cannot properly highlight or
indent code within code blocks. The directive :rst:`literalinclude` enables you
to store longer code blocks in an external file with the proper file extension.

You can use automatic tools to check the syntax or coding guidelines of the
code snippets then.

By convention files to be included should be prefixed with :file:`_` so
you can quickly see that this file should be included. A file to be included
should be stored close to where it is needed so.

The :rst:`literalinclude` directive imports the file and displays its content as
code block.

..  tabs::

    ..  group-tab:: Source (rst)

        ..  code-block:: rst
            :caption: _MyIncludes/_SomeExample.php

            ..  literalinclude:: _MyIncludes/_SomeExample.php
                :language: php
                :emphasize-lines: 5,10-13
                :linenos:

    ..  group-tab:: Output

        ..  literalinclude:: _MyIncludes/_SomeExample.php
            :language: php
            :emphasize-lines: 5,10-13
            :linenos:

Literal includes can even be used to render the difference between files,
without having to create a diff file first:

..  tabs::

    ..  group-tab:: Source (rst)

        ..  code-block:: rst
            :caption: Documentation/SiteConfiguration/Index.rst

            ..  literalinclude:: _MyIncludes/_example.yaml
                :diff: _MyIncludes/_example_de.yaml

    ..  group-tab:: Output

        ..  literalinclude:: _MyIncludes/_example.yaml
            :diff: _MyIncludes/_example_de.yaml

See also `literalinclude directive
<http://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html#directive-literalinclude>`__.
