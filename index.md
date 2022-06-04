# Data description
This data management plan will focus on data collected last summer in Coal Creek, a sub-alpine headwater tributary to the Upper Colorado River. Samples were collected along a longitudinal gradient within Coal Creek approximately weekly between June-September 2021. These samples were then analyzed, by five separate labs, for radon, anions, cations, stable isotopes, and trace metals. At the time of collection, basic water quality data, including pH, specific conductivity, ORP (oxidation reduction potential), DO (dissolved oxygen), and water temperature were measured using a YSI Professional Plus multiparameter sonde.
Radon samples were collected in 2L plastic bottles without headspace and the cap was sealed with Parafilm™. Samples were shipped in coolers overnight to Laurance Berkeley National Lab for analysis using a Rad-7 radon detector.
Grab samples for anions, cations, water isotopes, and trace metals were taken from the stream in acid washed 120 mL HDPE Nalgene bottles, transferred to a plastic syringe, and filtered through 0.45-micron Nylon filters into respective acid washed bottles. Anion and water isotope samples were collected in the same vial in the field and then later parsed out for analysis. Anion and water isotope samples were collected without headspace in 2.0 mL glass vials with Septa caps and were refrigerated until analysis. Cation samples were collected in acid washed 60 mL HDPE Nalgene bottles. Samples were acidified with nitric acid for preservation. Anions and water isotopes were analyzed in Crested Butte by LBNL using an ion chromatograph and mass spectrometer, respectively. Cations were analyzed at the Keck lab at OSU using an ICP-MS, then shipped to LBNL for trace metal analysis on an ICP-MS. These stream chemistry data are stored in csv files and each sample is identified by site name and date collected. This data will be < 1 GB. Physical cation samples will be stored at LBNL for five years after analysis.
Springs were also located and sampled around the watershed. Samples from the springs were collected and analyzed as described above for anions, water isotopes, cations, and trace metals, but most springs (7/10) were not sampled for radon. Springs were also not sampled using the YSI and thus data for pH, specific conductivity, DO, ORP, and water temperature do not exist for springs. These data are stored in separate csv files from the stream samples. This data will be < 1 GB. Metadata forms for locations of spring and stream samples also exist, as well as metadata documenting units for chemical constituents and lab where they were run. This is one file, < 1 GB.
A python model called StreamTran will be used to estimate groundwater contribution to the stream transect throughout the summer. The documentation for these scripts can be found at https://github.com/boatmorrow/stream_transport_py3. Modified scripts for this project will be stored on GitHub. Each file will be < 1 GB in size. There will be seven python scripts in total, one for estimation of model parameters using Monte Carlo simulation, and six files associated with individual sampling dates. Monte Carlo simluations will vary the groundwater radon concentration and gas exchange velocity, the two parameters least restrained and with the largest influence on the model output. There will be one csv file associated with the Monte Carlo simluation and four csvs associated with each of the sampling date transect model runs, for a total of 25 csv files, all < 1 GB.

### Data Summary
#### Field Data, < 1 GB
-	Metadata form – includes latitude/longitude of springs and stream samples, chemistry units, lab name where samples were analyzed
-	Stream sampling – separate csvs (total = 6)
    - Anions
    - Cations
    - Water Isotopes
    - Trace metals
    - Radon
    - YSI water chemistry
-	Spring sampling – separate csvs (total = 5)
    - Anions
    - Cations
    - Water Isotopes
    - Trace metals
    - Radon
#### Modeling Data, < 1 GB
-	Monte Carlo Simulation – 1 csv containing groundwater radon concentration, gas exchange velocity, and model AIC for 10,000 runs
-	Model Runs – separate csvs (total = 24)
    - Model fit parameters (x6)
    - Estimated stream radon concentration (x6)
    - Estimated stream discharge (x6)
    - Estimated lateral groundwater discharge (x6)

# Roles and responsibilities
The data management plan will be implemented by myself, Pamela Sullivan (PI), and Eric Parrish (NSF Data Manager, Critical Zone Network). Eric Parrish facilitates the actual sharing of data to NSF and the public, but I will be doing the organizing, metadata creation, and QA/QC on the data. Pamela Sullivan, the PI of our lab and co-PI on the grant funded by NSF, facilitates sharing between myself and Eric Parrish, but does not do any of the physical data handling. Once I have graduated, she will be in main contact for this data set. There is no additional data added to this data set; once it is published on Hydroshare additional maintenance will not be necessary. 

#### DMP Roles:
- Archiving and preservation: Eric Parrish
- Data manager: Eric Parrish
- Access control: Eric Parrish
- Software creation and maintenance: CUAHSI (https://www.cuahsi.org/)
- Instrumentation maintenance: Lab managers at Keck Lab (OSU: cations), LBNL Field Lab (located in Crested Butte: anions and isotopes), LBNL (UC Berkeley: trace metals and radon)
- Data analysis: Lab techs from the labs described in instrumentation maintenance above
- Quality control: Keira Johnson/lab techs described in instrumentation maintenance above
- Data collection/data generation: Keira Johnson
- Data organization: Keira Johnson
- Metadata generation: Keira Johnson

# Data standards and metadata
I will be using metadata standards required by NSF for publication of data on HydroShare. HydroShare is an open source NSF-funded data repository that uses metadata standard DCMI. The following methods describe how each data type described above will be documented.

### Field Sample Collection Metadata Format
Each file will be associated with a metadata file to provide information on contents, units, how these data were collected, location of collection, etc. Furthermore, naming conventions are standardized (e.g., DWCZ-CC-SW-RadonArray-KJohnson, DWCZ-CC-IS-RadonArray-KJohnson for spring water and instream sampling, respectively). These naming conventions are consistent across HydroShare. Data files are stored on my personal computer and on Box, not in version control software, since I am not creating new versions of this data. I have one version of the data which is the one I was sent by the labs that analzed the samples. This data was then “cleaned” to get consistent naming conventions and check QAQC. QAQC was verified by checking the difference between field duplicates and between lab duplicates. A difference between duplicates of < 10% was considered acceptable. The "clean" files will be uploaded to HydroShare. Overall site (watershed scale) attributes (nearest city, elevation, watershed size, vegetation, bedrock, etc), constituents analyzed and the associated units, frequency of sampling, location of individual sampling sites, funding agency, and contact information are included in the metadata form. Since sampling was not spatially nor temporally consistent, a sampling schedule was included so that readers know exactly when what sites were sampled. Methods and analysis techniques, as well as the lab they were analyzed at are also included in metadata forms. There are separate metadata forms for instream samples, spring samples, and discharge measurements that are in excel files separate from the data files.

### Monte Carlo and Model Runs Metadata Format
Monte Carlo runs and model analysis files are not stored in the same way as field data, however, metadata files follow the same format as the field samples. The Monte Carlo runs will have one csv file containing groundwater radon concentration, gas exchange velocity, and AIC value for the model with the given set of radon and gas values. One metadata file will be associated with the MC run file, where the column names and units of columns are identified. The MC code will be version controlled using Git and published on GitHub, as well as final parameters used from the MC analysis. The model analysis files will be stored separately than the MC run files but all will be tied to one metadata file. This metadata file will describe each synoptic sampling event associated with the model run and direct users to the raw data in the other metadata and data files. The metadata file will also include information including units and how the model works. There will be one version of each type of file.

# Storage and security
During the project, data is stored within Box and backed up weekly to an external hard drive. The Box folder is a shared folder with all lab members and backed up continuously to the cloud. R code files are version controlled using Git and backed up to GitHub. Cleaned data files and R codes are also stored on Hydroshare, although not publicly available until after publication. Data stored on HydroShare is held in a data center at the Renaissance Computing Institute at UNC Chapel Hill. In addition to the active storage there is failover redundant storage in an offsite location for data recovery. All physical samples are stored in a fridge at LBNL in Berkeley, California and can be rerun for additional analyses. They are preserved with nitric acid to preserve concentrations and prevent sorption. In total there are 3 copies of data (Box, Hydroshare, External hard drive), plus the ability to run samples again if need be. The data are not confidential. See data organization in metadata section.

# Access and data sharing
Data is stored on the lab Box drive and shared NSF, our funder, via HydroShare. HydroShare is an open source NSF-funded data repository striving to share hydrology-related research with collaborators and maintain the FAIR data principles. While the data will be stored on Hydroshare, they will not be made publicly available until publication (summer 2023). Once published, the public will be able to download it directly from HydroShare. Data and metadata will be published as csvs, and code will be published as R files. Code will also be on my GitHub page. This data will be published under Creative Commons -BY license such that it is free to use, share, and add to, with the expectation that people will cite me if they are using the data (a common and expected practice in academia). Articles relating to the data will be published in journals and data sets will be linked via DOI from the journal.

# Archiving and preservation
There are no factors that limit the availability of the data; it does not contain any sensitive information. Physical samples are stored, preserved with nitric acid, at LBNL for five years. These samples can be rerun if questions arise during or after publication. My data will be made publicly available on Hydroshare after publication. Hydroshare archiving is managed by Eric Parrish, the data manager for NSF. HydroShare is committed to maintaining availability of published data indefinitely although subject to 5-year funding cycles. There is an implied commitment for funding to be ongoing to maintain the data. Data will also continue to be shared with the lab via Box. Articles relating to the data will be published in journals and data sets will be linked via DOI from the journal.
