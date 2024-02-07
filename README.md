# New York State Wastewater Surveillance Data

Table of Contents as of 03/24/23.
This is all a work in progress and subject to change!

~/
  1) genetic-sequencing.csv: freyja generated variants and their concentration within sequenced samples
  2) nys-wws-sars2-concentration.csv: quantification of sars2 (and also crassphage), as well as some other per-sample data. ***Please only use this file for analysis, not for reporting (i.e., memos). It is a work in progress***

~/archived_data/
   1) 20230314_genetic-sequencing.csv: Previous version of sequencing data. Eventually we will likely remove this file from the git, but keeping it here for now
  
~/metadata/
  1) lineage-map.csv: mapping over-detailed lineage names to thier more "summary" names. Also will soon include color...
  2) sewershed-metadata.csv: information about the sewersheds. Sewershed ids will correspond to sample_ids in sequencing or concentration files
  3) variants-of-concern.csv: this tells us which variants to focus on in some of our reports that we generate
  
~/scripts/
  Nothing here as of now

## File overview

### nys-wws-sewersheds.csv

| Variable name | Description |
| --- | --- |
| county | County the sewershed resides in |
| county_names | ID consisting of the state and county FIPS codes |
| region | Region of New York in which the sewershed is located |
| zipcode | ZIP code the sewershed resides in |
| wwtp_name | Name of the facility |
| sw_id | Unique ID used to identify the facility |
| epaid | ID consisting of the state abbreviation and SPDES permit number |
| cdc_id | ID consisting of the state abbreviation, county FIPS code, SPDES permit number, and a reference letter for either the wastewater treatment plant (A) or upstream locations (B, C, D, etc.) |
| site_id | *See "cdc_id"* |
| sample_location | Location within the sewershed where the sample is taken (*i.e.*, wwtp or upstream) |
| sample_location_specify | Specific name of sampling location (*see "sample_location"*) |
| method | Type of location where sample is taken with regard to flow (*e.g.*, influent or upstream) |
| capacity_mgd | Maximum allowed flow in millions of gallons per day (MGD) |
| population_served | Estimated number of persons connected to the sampling point |
| institution_type | Clarification of health, academic, or other institutional specific connection to the sewershed |
| reporting_jurisdiction | Jurisdiction the facility resides in for reporting purposes |
| wwtp_jurisdiction | Jurisdiction the facility resides in |
| wwtp_latitude | Latitude of the facility in degrees |
| wwtp_longitude | Longitude of the facility in degrees |

### sars2-concentration.csv

| Variable name | Description |
| --- | --- |
| sample_collect_date | Date the sample was collected |
| date_received | NA |
| test_result_date | Date the results were quantified |
| date_reported | NA/inconsistent |
| sample_id | ID consisting of the date and site ID.
| sw_id | Unique ID used to identify the facility |
| site_id | ID consisting of the state abbreviation, county FIPS code, SPDES permit number, and a reference letter for either the wastewater treatment plant (A) or upstream locations (B, C, D, etc.) |
| pcr_lab | Name of receiving and processing lab |
| sars_pos | Number of tested sample replicates returning a measurement above the LOD (between 0 and 3) |
| ct | Ct value from RT-qPCR measurement |
| sars2_copies_ml | Ct values converted to concentration of SARS-CoV-2 |
| hum_frac_mic_copies_ml | Measured concentration of endogenous control (crAssphage or PMMoV) |
| rec_eff_percent | Percentage of BCoV vaccine spike recovered following sample processing and measurement |
| sample_temp_f | NA |
| sample_type | Method of wastewater sampling |
| flow_rate | Measurement of wastewater volume passing through the sewer system per day (in millions of gallons per day/MGD). *Note: Refer to “flow_rate_flag” for further information.*
| flow_rate_flag | Quality control flag stating issues with recorded flow, such as flow greater than capacity, flow that is 2 standard deviations above or below the mean, or if the record was manually corrected following input |
| quadrant_sample_id | NA |
| withheld | NA |

### sars2-genetic-sequencing.csv
| Variable name | Description |
| --- | --- |
| sample_id | Unique ID comprised of date and sewershed of collection |
| variant | Variant detected in sample |
| variant_pct | Relative abundance of variant in sample |
