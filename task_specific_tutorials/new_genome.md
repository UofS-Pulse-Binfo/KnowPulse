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
3. Create BLAST database on KnowPulse. Go to Admin Toolbar > Content > Add Content > Blast Database. Convention for naming is "Genus species: Genome version". You can restrict access to blast by changing the Access on this page. The blast database should be located in the same place as all others on KnowPulse.
 
 
