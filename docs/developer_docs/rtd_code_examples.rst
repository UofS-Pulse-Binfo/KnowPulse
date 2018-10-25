Title of File (using title case)
=================================

Introduction text.

.. note::

  This would show up as a boxed note to the reader. It's good for ensuring important points/hints are seen but should be used sparingly. It's also a good way to note that "This guide is under developement."


Section Title
-------------

We use double backticks to indicate ``inline-code`` including file names, function and method names, paths, etc.

Longer code-blocks should begin with the ``.. code-block:: [type]`` directive and should be indented at least one 
level. There should also be a blank line before and after it as shown below.

.. code-block:: bash

  if ($needs_documentation) {
      use $these_guidelines;
      $contribute_docs = $appreciated;
  }

Section 1.1 Title
^^^^^^^^^^^^^^^^^

The use of appropriate sections makes reading documentation and later specific details easier. Sub sections such 
as this one will be hidden unless the main section is already selected.

The following toctree specifies that there are 3 files with additional content for the current page.
The order is as it will appear in the sidebar and the link titles will be the "Title of File" for each file.
 
.. toctree::
   :maxdepth: 2
   :caption: Contents:

   dir/file1
   dir/file2
   dir/file3


