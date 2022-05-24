# Data description
This data management plan will focus on data collected last summer in Coal Creek, a sub-alpine headwater stream to the Upper Colorado River. Samples were collected along a longitudinal gradient along Coal Creek approximately weekly between June-September 2021. These samples were then analyzed, by five separate labs, for radon, anions, cations, stable isotopes, and trace metals. At the time of collection, basic water quality data, including pH, specific conductivity, ORP (oxidation reduction potential), DO (dissolved oxygen), and water temperature were measured using a YSI Professional Plus multiparameter sonde. 

Radon samples were collected in 2L plastic bottles without headspace using a Grainger surface water pump (Model IL200P, RULE, Rye Brook, NY) powered by a 12V battery. A 3.65 m (12 ft) silicone tube (inner diameter of ½ inch) was connected to the pump outlet. The surface water pump was placed in the thalweg of the stream and the end of the tubing was placed in the bottom of the 2L bottle. The bottle was rinsed once with surface water from the collection site then placed in a 5-gallon bucket with the tubing inside. The bottle was filled until water overflowed out of the bottle and until the water level in the bucket was above the top of the 2L bottle. The pump was disconnected from the battery and the tube was removed from the bottle. The bottle was capped underwater without headspace to minimize degassing of radon and the cap was sealed with Parafilm™. Samples were shipped in coolers overnight to Laurance Berkeley National Lab for analysis using a Rad-7 radon detector.

Grab samples for anions, cations, water isotopes, and trace metals were taken from the stream in acid washed 120 mL HDPE Nalgene bottles, transferred to a plastic syringe, and filtered through 0.45-micron Nylon filters into respective acid washed bottles. Anion and water isotope samples were collected in the same vial in the field and then later parsed out for analysis. Anion and water isotope samples were collected without headspace in 2.0 mL glass vials with Septa caps and were refrigerated until analysis. Cation samples were collected in acid washed 60 mL HDPE Nalgene bottles. Samples were acidified with nitric acid for preservation. Anions and water isotopes were analyzed in Crested Butte by LBNL using an ion chromatograph and mass spectrometer, respectively. Cations were analyzed at the Keck lab at OSU using an ICP-MS, then shipped to LBNL for trace metal analysis on an ICP-MS. These stream chemistry data are stored in csv files and each sample is identified by site name and date collected. This data will be < 1 GB.

Springs were also located and sampled around the watershed. Samples from the springs were collected and analyzed as described above for anions, water isotopes, cations, and trace metals, but most springs (7/10) were not sampled for radon. Springs were also not sampled using the YSI and thus data for pH, specific conductivity, DO, ORP, and water temperature do not exist for springs. These data are stored in separate csv files. This data will be < 1 GB.
Metadata forms for locations of spring and stream samples also exist, as well as metadata documenting units for chemical constituents and lab where they were run. This is one file, < 1 GB.

# Roles and responsibilities
The data management plan will be implemented by myself, Pamela Sullivan (PI), and Eric Parrish (NSF Data Manager, Critical Zone Network). Eric Parrish facilitates the actual sharing of data to NSF and the public, but I will be doing the organizing, metadata creation, and QA/QC on the data. Pamela Sullivan, the PI of our lab and co-PI on the grant funded by NSF, facilitates sharing between myself and Eric Parrish, but does not do any of the physical data handling.

DMP Roles:
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

# Storage and security
During the project my data is stored within Box and backed up to an external hard drive. The Box folder is a shared folder with Pam (PI) and backed up to the cloud. I back up my computer to my external hard drive at least weekly, but usually multiple times each week. All physical samples are stored in a fridge at LBNL in Berkeley, California. These can be rerun if need be. The data are not confidential.

# Access and data sharing
The Box drive is shared with PI so when I graduate it will continue to be available and will not be lost.  The data is currently being organized to be uploaded to Hydroshare, an open source online data, code, and models data base for hydrologic data. This data will be shared with the NSF, our funder. These data will be stored there as soon as I finish organizing but will not be made publicly available until the paper I am working on that uses the data is published. In total there will be 3 copies at the end of the project (Box, Hydroshare, External hard drive) plus the ability to run samples again if need be.

# Archiving and preservation

The following answers are applicable to both the raw data collected and the modeled data output.

There are no factors that limit the availability of the data; it does not contain any sensitive information.

My data will be made publicly available after publication of the paper I am working on – probably no later than summer 2023. It will be published on HydroShare, a data repository for hydrology-related data. Data and metadata will be published as csvs, and code will be published as R files. Code will also be on my GitHub page. This data will be published under Creative Commons license, with the expectation that people will cite me if they are using the data (a common and expected practice in academia).

My data will be archived and preserved both on HydroShare and on our lab Box Drive. I am unsure how long it will be on either of those; our lab is relatively new and we don’t have standards for how long data is preserved. I am unsure about how long data stays on HydroShare, but it is my understanding that it is up there for as long as HydroShare is active. Data and code can be accessed simply by downloading from HydroShare. If an individual is in our lab, they will have access to the Box drive and will be able to access it also by downloading it. All data and metadata will be preserved as csvs and all code will be in R files.
