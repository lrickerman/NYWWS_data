# New York State Wastewater Surveillance Data
> [!NOTE]
> All sewersheds serving a population of less than 3,000 people have been omitted for privacy. If this information is desired for official use, please submit a [request](https://nywastewatcher.io/contact-us) to be reviewed.

## File overview

### nys-wws-sewersheds.csv

| Variable name | Description |
| --- | --- |
| county | County in which the facility resides |
| county_names | ID consisting of state and county FIPS codes |
| region | Region of New York in which the facility resides |
| zipcode | ZIP code in which the facility resides |
| wwtp_name | Name of the permitted facility |
| sw_id | Facility ID consisting of state and county FIPS codes, SPDES permit number, and a collection of numbers and/or letters unique to each site |
| epaid | SPDES permit number for facility |
| cdc_id | Unique ID consisting of the SPDES permit number and a reference letter for sampling location, either wastewater treatment plant (A) or upstream (B, C, D, etc.) |
| site_id | *See "cdc_id"* |
| sample_location | Location within the sewershed where the sample is taken (*i.e.*, wwtp or upstream) |
| sample_location_specify | Specific name of sampling location (*see "sample_location"*) |
| method | Type of location where sample is taken with regard to flow (*e.g.*, influent or upstream) |
| capacity_mgd | Average hydraulic flow the facility is designed to treat, in millions of gallons per day (mgd) |
| population_served | Estimated number of persons connected to the sampling point |
| institution_type | Clarification of health, academic, or other institutional-specific connections to the facility |
| reporting_jurisdiction | Jurisdiction in which the facility resides |
| wwtp_jurisdiction | *See "reporting_jurisdiction"* |
| wwtp_latitude | Latitude (decimal degrees) |
| wwtp_longitude | Longitude (decimal degrees) |

### sars2-concentration.csv

| Variable name | Description |
| --- | --- |
| sample_collect_date | Date when sample was collected |
| date_received | Date when sample was received, if available |
| test_result_date | Date when results were quantified |
| date_reported | Date when results were reported |
| sample_id | ID consisting of sample collection date and sampling site ID |
| sw_id | Facility ID consisting of state and county FIPS codes, SPDES permit number, and a collection of numbers and/or letters unique to each site |
| site_id | Unique ID consisting of the SPDES permit number and a reference letter for sampling location, either wastewater treatment plant (A) or upstream (B, C, D, etc.) |
| pcr_lab | Name of receiving and processing lab |
| sars_pos | Number of tested sample replicates returning a measurement above the LOD (0-3) |
| ct | Ct value from RT-qPCR measurement |
| sars2_copies_ml | Ct values converted to concentration of SARS-CoV-2 |
| hum_frac_mic_copies_ml | Measured concentration of endogenous control (crAssphage or PMMoV) |
| rec_eff_percent | Percentage of bovine coronavirus control recovered following sample processing and measurement |
| sample_temp_f | Temperature (Fahrenheit) of sample upon receipt, if available |
| sample_type | Method of wastewater sampling |
| flow_rate | Average hydraulic flow the facility is designed to treat, in millions of gallons per day (mgd) |
| flow_rate_flag | Quality control flag regarding recorded flow rate (*see "flow_rate"*) |
| quadrant_sample_id | Sample ID used in processing lab |
| withheld | Indication of whether the results were reported or withheld |

### sars2-genetic-sequencing.csv
| Variable name | Description |
| --- | --- |
| sample_id | ID consisting of sample collection date and sampling site ID |
| variant | SARS-CoV-2 variant detected in sample |
| variant_pct | Relative abundance of variant detected in sample |
