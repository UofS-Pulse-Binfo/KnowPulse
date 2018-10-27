
Species (Organism)
==================

The organism content type will include each of our crops and wild relatives. Stored in the Chado Organism table. Design-wise we are thinking of these as launch pads which both summarize the data per crop and link to pre-filtered searches.

Genome Pane
-----------

- Current Assembly: This field should provide information on the most recent genome assembly or assemblies for this species.
- Genome Browser: This field should summarize the data in the current JBrowse and have an image linking to the JBrowse instance for the current assembly
- Whole-Genome Diagram: This field should show an embedded CViTjs diagram summarizing the current assembly’s annotation and markers.
- Past Assemblies: This field should list the past assemblies with links to archived information.

Genetic Markers Pane
--------------------

- Types: This field summarizes the types of markers available for this organism.
- Quick Search: This field provides a simple keyword search with limited advanced search collapsed. When the user clicks search, they are redirected to the marker search page with their results pre-filtered.

Genetic Maps & QTL Pane
-----------------------

- Tiled display of available maps with each tile containing map metadata such as population, date generated, number of markers, QTL list
- QTL Quick Search: simple keyword search for QTLs.

Germplasm Pane
---------------

- Types: This field summarizes the types of germplasm available for this organism. Should this be subject to permissions?
- Quick Search: This field provides a simple keyword search. No need for advanced search or breakdown by type.
- Recent UofS Varieties: a list of the most recent varieties.
- Variety Spotlight: Highlight a single variety
- RIL Populations: This could be a cool search that lets them select things like interspecific, species, phenotype of interest. Essentially allow people to search for a RIL without knowing it’s number 
- Germplasm Diversity: Show a map with each of our germplasm indicated.
- Wild Relatives: summarize the gene pools and/or phylogeny

Phenotypes
-----------

- Quick Search: This field provides a simple keyword search. No need for advanced search? It would be helpful this field searched both names and linked cvterms.
- Phenotype Projects: Highlight our biggest and/or most recent phenotyping projects. Should show metadata for each such as population phenotyped, purpose, siteyears w/ data, funders logos if applicable. Links to project pages.
