
Research Project
================

Currently just a regular old project page. Stored in the Chado Project table. Need a way to break out? What about datasets which are currently projects with data? These pages should include all metadata about the project and summarize all the data generated by it.

.. warning::

  Not yet available as a Tripal3 content type. Currently in progress.
  
Overview Pane
--------------

- Project meta-data (stored as project properties)

    - Years
    - Collaborators
    - Funders
    - Locations
    - Measurements/Traits being collected
    - Genotyping being done?
    - Germplasm collection
    
- Abstract
- Methods

Genomic Data
-------------

- Barchart or infographic summarizing the types and amount of genomic data (sequence, genes, etc.) generated as part of this project.
- Assembly information if generated as part of this project?

Genotypic Data
---------------

- Barchart or infographic summarizing the types and amount of genotypic data (markers, variants, germplasm assayed, genotype calls, etc.) for this project.
- Genotypes Search: Redirects to the genotype matrix pre-filtered for the current project. Provides form elements to further restrict the matrix.

Phenotype Data
--------------

- Barchart or infographic summarizing the siteyears, traits and germplasm phenotyped for this project.

Germplasm
----------

- List the germplasm associated with this project with download. It might be a long list so make it searchable. Also, we should support stock collections which would then be listed at the top. For example, AGILE is using the Lentil Diversity Panel so it would be nice to say that at the top so users know it's not a random list ;-).
- We also need a way to add germplasm to a project through the form so keep in mind this one will need a form element.

