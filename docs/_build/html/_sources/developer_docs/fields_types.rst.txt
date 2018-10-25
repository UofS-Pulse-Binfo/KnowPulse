
KnowPulse Field Types
======================

The following sections described common field types.
 
Quick Search (Should be in Core?)
---------------------------------
- This field type allows a user to search for additional content quickly and easily.
- It consists of a single keyword search box and optional, configurable advanced search form.
- Configuration:
  - Search URL this field redirects to
  - what key to use in the query string for entered keywords
  - Drupal Form API definition of advanced search elements where the keys of the elements are used in the query string
  - Description and/or help text to display to the user
  - Quick Search Title

Summary Field (Should be in Core?)
----------------------------------

- This field displays a graphical summary based on a materialized view.
- Configuration:
  - Select the Materialized View to get the summary from
  - Select which mview column maps to the legend (e.g. type name)
  - Optional filter by field: select field and mview column mapping
  - Select chart type: Pie, bar, etc.
  - Figure Title
  - Figure Description
  - Chart type specific configuration

Embedded JBrowse by organism
-----------------------------

- Embeds a JBrowse instance 
- Provided by the JBrowse integration module
- Contains linkout to full JBrowse page for more intensive browsing
- Configuration:
  - Select Organism Field for the current content type
  - Show/Hide Menubar, search, track selector
  - For each organism: select jbrowse, tracks, and location to show

Whole-Genome View by organism
------------------------------

- Embeds a CViTjs diagram 
- Provided by the CViTjs integration module
- Contains linkout to full diagram
- Configuration:
  - Select Organism Field for the current content type
  - Show/Hide Controls, track selector
  - For each organism: select diagram and tracks to show

