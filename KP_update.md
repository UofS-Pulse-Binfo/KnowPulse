# Standard Protocol for Updating KnowPulse
The following documentation outlines the steps and testing that should be done when updating KnowPulse, whether it be simply updating a custom module or updating Drupal itself. Updating between major versions (e.g. Drupal 7 => 8 or Tripal 2 => 3) is beyond the scope of this document.

The following are the basic steps to be taken. There is more information below if needed.
1. Create a fresh clone (Dev Fresh) of the production site
2. Upgrade the clone.
     - In the directory for the site, execute `drush up`. This will tell you what modules need to be updated and prompt you to do so. Remember, if you don't have permission on the directory you will need to use sudo.
3. Test the upgrade by checking the pages listed under "To be Checked" below.
4. If there are no errors (check the current page, the recent log messages and the apache error log) then upgrade the production site using the same steps.
     - Recent Log Messages: http://knowpulse.usask.ca/portal/admin/reports/dblog
     - Apache Error Log: /var/log/apache2/error.log (requires sudo).
5. Check the pages listed under "To be Checked" on the production site as well.

## To Be Checked
This list should be ever expanding. Feel free to document the specifics under each page.
- Home Page: http://knowpulse.usask.ca/
- BLAST: http://knowpulse.usask.ca/portal/blast/nucleotide/nucleotide
   - You should actually execute an example blast to ensure that the functionality works.
- JBrowse: http://knowpulse.usask.ca/portal/jbrowse/Lentil
   - Ensure you have your cache killer turned on!
   - Make sure to turn on/off tracks, navigate side to side and search.
- Views Search: http://knowpulse.usask.ca/portal/search/variants
   - Check multiple combinations of filters (e.g. genus:Lens, type:SNP, name:p390).
   - If you get no results, you likely need to re-apply the Tripal Views patch.
   - To apply views patch, navigate to views module directory and execute `git apply ../tripal/tripal_views/views-sql-compliant-three-tier-naming-1971160-30.patch`
- Feature Page: http://knowpulse.usask.ca/portal/feature/lens-culinaris/SNP/LcC00002p390
   - Check the genotypes & sequence panes especially.
- Raw Phenotypes 
   - Chart: http://knowpulse.usask.ca/portal/phenotypes/raw
   - Backup: http://knowpulse.usask.ca/portal/phenotypes/raw/backup
- Germplasm: http://knowpulse.usask.ca/portal/stock/Lens/culinaris/Variety/KP%3AGERM58
   - Check that you can collapse nodes & follow links on the pedigree
- Research Category: http://knowpulse.usask.ca/portal/node/21
   - Check that there are projects listed & pager works.

## How to create a fresh clone of the productions site
**Note: Replace *** with the name of the database user in all the commands below.**
1. Backup the production site to your home directory
     - `pg_dump kp_live --user *** --host thunder > ~/kp_live.2017Aug18.sql`
2. Remove the existing Clone. This should be safe since no one is supposed to develop on the clone. That said, it wouldn't hurt to tell your collegues that you're about to delete everything on the clone ;-)
     - Specifically, remove the dev/fresh directory entirely and drop kp_clone on thunder.
3. Re-create the clone database and restore the production site backup to it.
     - `psql kp3_live --user *** --host thunder --command "CREATE DATABASE kp_clone WITH OWNER ***"`
     - `psql kp_clone --user *** --host thunder < ~/kp_live.2017Aug18.sql`
4. Copy the production site files to dev/fresh.
5. **Change the database in the dev/fresh/sites/default/settings.php from kp_live to kp_clone**. 
     - You need to use sudo to change this file.
