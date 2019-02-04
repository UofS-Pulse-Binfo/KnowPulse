
Add new Genome Build to KP
============================================

Overview
---------

The following list is a general overview. More details will be added below as needed.

1. Create a blast database and register it with the Tripal Blast UI module.
2. Create a JBrowse instance and register it with the Tripal JBrowse module.
3. Setup bulk download, if desired.

Blast
-----

1. Prefix the record names in your FASTA file using `this GIST <https://gist.github.com/laceysanderson/12b1de6784413cd69cbb064666063b08>`_. The naming convention is The first letter of the Genus and two letters from the species followed by the version and an underscore. For example, Lens culinaris 1.0 would have ``Lcu1.0_`` added to the beginning of each record name.

.. code-block:: bash

  > perl prefix_fasta.pl [original fasta] [new fasta] [prefix]

2. Create the BLAST indicies.

.. code-block:: bash

  > formatdb -p F -t Genus_species_version_genome -i Genus_species_version_genome.fasta -n Genus_species_version_genome -o T
 
.. code-block:: bash

  > makeblastdb -dbtype 'nucl' -input_type 'fasta' -title Genus_species_version_genome -in Genus_species_version_genome.fasta -parse_seqids -hash_index

3. Create BLAST database on KnowPulse. Go to Admin Toolbar > Content > Add Content > Blast Database. Convention for naming is ``Genus species: Genome version``.

.. note::

  **File Location:** Both the prefixed FASTA and the associated indices should be located in the blast_dbs folder with all the other KnowPulse blast databases. If you are uncertain where that is, simply check the page for an existing blast database to see it's path.

.. note:: 

  **Restrict Access:** You can restrict the users which can blast against a specific blast database by editing the page created in step #3 above. Near the bottom there is a section for ``Access`` in the horizontal tabs. Simple select the group you would like to give access (usually ``University of Saskatchewan``) and all users not in that group will not see that blast database as an option.
 
.. warning::

  **More information on Link-outs to come.**

JBrowse
-------

1. Setup a new JBrowse following the instructions here: https://jbrowse.org/install/. The folder containing the JBrowse files should be named ``[random 5 letters]-[genome prefix]``.

   - Use the prefixed fasta file created for the BLAST as the backbone.
   - Make sure to update any annotation so the backbone/chromosome feature names match.

2. Add KnowPulse themeing to the new JBrowse by copying the CSS files from an existing JBrowse. **This needs to be improved. Ideally all KnowPulse specific changes would be in a single CSS file added to the index.**
3. Edit ``jbrowse.conf`` to change the ``Share`` link to point to the KnowPulse path by adding the following to the ``[General]`` section.

.. code-block:: bash

  ## Set the share link to respect being within an iFrame.
  shareURL=function(browser){ return 'http://knowpulse.usask.ca/portal/[Instance Path]/?loc='+browser.view.visibleRegionLocString()+'&tracks='+(browser.view.visibleTrackNames().join(','));}

.. note::
  Notice the ``[Instance Path]`` in the URL above; this should be changed to the path selected in step 4. Use existing ``jbrowse.conf`` as an example for other configuration changes.

4. Register the JBrowse with KnowPulse by creating a ``JBrowse Instance``. Go to Admin Toolbar > Content > Add Content > JBrowse Instance and fill in the requested information. Also, change the ``URL path settings`` to provide an alias for the JBrowse page. Conventions are as follows:

   - Cultivated crops, current version: ``[Common Name]``
   - Cultivated crops, archived version: ``[Common Name]/[version]``
   - Wild Species, current version: ``[Genus species]``
   - Wild Species, archived version: ``[Genus species]/[version]``

