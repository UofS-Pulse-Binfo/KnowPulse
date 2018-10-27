
Recombinant Imbred Line
=======================

Stored in the Chado Stock table broken out by type_id.

Overview
--------

- Basic information such as name, accession, what-not. This will remain a default Tripal pane  
- RIL Specific information

     - the original cross
     - parents, 
     - latest generation, 
     - status
     - number of individuals.
     
- It would be great to finally have the breeder short-hand for the pedigree! This could be a separate field from the pedigree diagram so I can put it in the overview.
- 
RIL Development Pane
--------------------

- Reiterate the type of cross (Interspecific, intraspecific) 
- Indicates the parents of the RIL including their species.
- Development timeline including which years & how many individuals
- If the RIL is complete, indicate that and the final number of individuals.

Parental Pedigree
------------------

- Shows the parentage pedigree diagram with all but the first 3 levels collapsed.
- All diagrams should now include a figure legend.

Genotypes Pane
---------------

- Types: This field summarizes the number of markers per type with calls for the current germplasm.
- Genotype Look-up field: a mini-genotype matrix filtered to parents of this RIL. User enters a marker or region to display.
- Genotype Matrix Link: Redirects to the genotype matrix pre-filtered for the parents of this RIL.
- Links to the VCF Filter form for the current RIL to facillitate downloading of the data.

Breeding Markers
----------------

- List the calls for a set of CORE breeding markers. Make the set configurable at the field level.

Phenotypes Pane
----------------

- List the value for a set of CORE phenotypes (e.g. seed coat, cotyledon color). Make the set configurable at the field level. Should it be entereable on the form? How do we handle multiple experiments, siteyears for a single trait/variety combo.
- Phenotype pane should highlight phenotypes specifically of interest for this RIL.

Relationships
--------------

- list any non-parental/progeny relationships.
