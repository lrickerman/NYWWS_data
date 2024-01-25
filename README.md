# NYWWS_data
New York State Wastewater Surveillance Data

## File overview

### nys-wws-sewersheds.csv

This file contains metadata of all municipal sewersheds within NYS. Information in this dataset includes the location of the sewershed, naming conventions for sewershed identifiers, characteristics of the WWTPs, and estimated population statistics.

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
| site_id | ID consisting of the state abbreviation, county FIPS code, SPDES permit number, and a reference letter for either the wastewater treatment plant (A) or upstream locations (B, C, D, etc.) |
| sample_location | Location within the sewershed that the sample is taken (at the wastewater treatment plant or upstream) |
| sample_location_specify | Alternate shorthand name for the facility |
| method | Location within the sewershed that the sample is taken (influent to the wastewater treatment plant, an upstream pump station close to the treatment plant, or an upstream location outside of the treatment plant’s vicinity) |
| capacity_mgd | Maximum allowed flow in millions of gallons per day (MGD) |
| population_served | Estimated number of persons connected to the sampling point |
| institution_type | Clarification of health, academic, or other institutional specific connection to the sewershed |
| reporting_jurisdiction | Jurisdiction the facility resides in for reporting purposes |
| wwtp_jurisdiction | Jurisdiction the facility resides in |
| wwtp_latitude | Latitude of the facility in degrees |
| wwtp_longitude | Longitude of the facility in degrees |

### sars2-concentration.csv

This file contains the measurements of raw abundance from wastewater samples, as well as sample metadata, including collection method and extraction method. Within the dataset, each row consists of the results from a single sampling event and necessary information to perform spatial and/or temporal analyses.

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

The relative abundance of variants detected by the Freyja algorithm in each sample is uploaded to a data file. Each line contains information about where the sample was collected and the collection date. The sample ID field can be cross referenced to other data files for sewershed and sample metadata.

| Variable name | Description |
| --- | --- |
| sample_id | Unique ID comprised of date and sewershed of collection |
| variant | Variant detected in sample |
| variant_pct | Relative abundance of variant in sample |
