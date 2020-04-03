
KnowPulse Content Types
========================

The following breaks down our content types based on the primary Chado table storing their data.

- chado.organism table (full table)

  - Species (OBI:organism)

- chado.project table (seperated using projectprop)

  - Research Project (semantic science ontology; study; SIO:001066)
  - Genome Project (local:genome)

- chado.publication (full table)

  - Publication (TPUB; Publication)

- chado.feature table (seperated using feature.type_id)

  - Variant (Sequence Ontology; sequence_variant)
  - Genetic Marker  (Sequence Ontology; genetic_marker)
  - QTL (Sequence Ontology; QTL; SO:0000771)

- chado.stock (seperated using stock.type_id)

  - Germplasm Accession (Crop ontology; accession; CO_010:0000044)
  - Breeding Cross (local:F1)
  - Registered Varieties (Sequence Ontology; cultivar; CO_010:0000029)
  - Recombinant Inbred Line (local:Recombinant Inbred Line)
  - Biological Sample	(biological sample; sep:00195)

- chado.cvterm (specific cv_id)

  - Chickpea Trait (CO_338:ROOT)
  - Common Bean Trait (CO_335:ROOT)
  - Lentil Trait (CO_339:ROOT)

- chado.featuremap (full table)

  - Genetic Map (data onotology; Map)

- chado.stock_collection (full table)

  - Stock Collections (don't know what term to use yet)

.. toctree::
   :maxdepth: 1
   :caption: General Types:

   content_types/species
   content_types/project
   content_types/pub

.. toctree::
   :maxdepth: 1
   :caption: Genomic Types:

   content_types/genome
   content_types/variant
   content_types/marker

.. toctree::
   :maxdepth: 1
   :caption: Germplasm Types:

   content_types/accession
   content_types/variety
   content_types/cross
   content_types/ril
   content_types/stock_collection
