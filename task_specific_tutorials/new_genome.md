# Steps to add a new Genome Build to KnowPulse

## Overview
The following list is a general overview. More details will be added below as needed.
1. Create a blast database and register it with the Tripal Blast UI module.
2. Create a JBrowse instance and register it with the Tripal JBrowse module.
3. Setup bulk download, if desired.

## Blast
1. Prefix the record names in your FASTA file using https://gist.github.com/laceysanderson/12b1de6784413cd69cbb064666063b08. The naming convention is The first letter of the Genus and two letters from the species followed by the version and an underscore. For example, Lens culinaris 1.0 would have "Lcu1.0_" added to the beginning of each record name.
2. Create the BLAST indicies.
> formatdb -p F -t Genus_species_version_genome -i Genus_species_version_genome.fasta -n Genus_species_version_genome -o T
3. Create BLAST database on KnowPulse. Go to Admin Toolbar > Content > Add Content > Blast Database. Convention for naming is "Genus species: Genome version".

**File Location:** Both the prefixed FASTA and the associated indices should be located in the blast_dbs folder with all the other KnowPulse blast databases. If you are uncertain where that is, simply edit an existing blast database to see it's path.

**Restrict Access:** You can restrict the users which can blast against a specific blast database by editing the page created in step #3 above. Near the bottom there is a section for "Access" in the horizontal tabs. Simple select the group you would like to give access (usually "University of Saskatchewan") and all users not in that group will not see that blast database as an option.
 
 **More information on Link-outs to come.**
