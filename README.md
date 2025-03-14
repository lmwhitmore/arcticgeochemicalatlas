
## GEOCHEMICAL ATLAS HISTORY

The Geochemical Atlas was compiled to permit pan-Artcic analysis of changes in biogeochemical properties; it was originally published with Polyakov et al., 2020 as a description in the supplement. The files included as the "original upload" include a .mat data file, a document describing the quality control measures taken during compilation of the data sets, and a .txt file with all data in a tabular format. This work was conducted by Matthew Alkire, Kristina Brown, and Igor Polyakov.  

Polyakov, I.V., Alkire, M.B., Bluhm, B.A., Brown, K.A., Carmack, E.C., Chieric, M. Danielson, S.L., Ellingsen, I., Ershova, E.A., Gårdfeldt, K., Ingvaldsen, R.B., Pnyushkov, A.V. Slagstad, D., Wassmann, P. (2020). Borealization of the Arctic Ocean in Response to Anomalous Advection From Sub-Arctic Seas. *Frontiers in Marine Science*, 7. https://doi.org/10.3389/fmars.2020.00491
Front. Mar. Sci. , 02 July 2020

This original data set stops in 2018. The subsequent versions have been updated by Laura Whitmore. 

## Data Quality Control 

The data in this compilation were curated from several sources and analytical approaches. Data went through the following steps of QA/QC to be included in the data file (see pdf for more detail): 
(1) Apply quality flags based on "reasonable ranges" for parameters.
(2) Visually inspect data: vertical profiles -- this is the most subjective step of QC. Any data point with a "large" separation from the cloud of data at a depth bin is flagged and considered for removal from the combined data set. 
(3) Define "acceptable" concentrations for each region of th Arctic; data outside +/- 3 SD of the mean for parameter are flagged and removed from the combined data set. 

For all data sets, any removed or flagged data are articulated in the QA/QC pdf. 

Blank cells/no-data are indicated in the txt with -9999.

The quality flag schema used is as follows: 
Quality flags 0, 1 and 2 usually indicate good data; quality flag of 6 typically denotes an average value.  All other flags indicate missing (= 9), bad (= 4) or questionable (= 3) data.  

However, the final data set does not include flags as all data is presumed "good." 

## Locations of Data 

how many entries, stations, flags. 

## Downloadable data types and how to read them 

The original .mat file can be readily loaded into matlab or read into R using the library R.matlab. 

The .txt file is headerless, but can be read: 

Into Matlab:

```matlab
readf,1,iyr,imo,ida,sla,slo,p,t,s,o2,sd,o2d,po4,ni,si,dic,ta,d18o,idc,ids1,ids2,npr,pno,no,po,o2sat,po2sat,fpw,sim,mw,pac,aw   ; v4.3
```

Headers for columns of the txt are as follows: 
(1) Year (2) Month (3) Day (4) Latitude (5) Longitude (6) Pressure (7) Temperature (8) Salinity (primary) (9) Dissolved oxygen (primary) (10) Bottle salt (ignore) (11) Bottle O2 (ignore) (12) Phosphate (13) Nitrate+nitrite (14) Silicate (15) DIC (16) TA (17) d18O (18) Cruise ID (19) Station ID (20) Station ID_new (21) N:P ratio (22) pNO3 (23) NO (24) PO (25) O2sat (26) pO2sat (27) fPAC (28) SIM
(29) MW (30) PAC (31) ATL

Into R: download txt and identify the filepath on your computer.

```R

atlas = read.csv(file = '/insertfilepath/Pan_Arctic_geochem_v4.txt', sep = ' ', header = F)

colnames(atlas) = c('Year', 'Month', 'Day', 'Latitude', 'Longitude',
                   'Pressure', 'CTD.Temperature', 'CTD.Salinity', 'CTD.Oxygen', 
                   'Bottle.Salinity', 'Bottle.Oxygen', 
                   'Phosphate', 'Nitrate.Nitrite', 'Silicate', 
                   'DIC', 'Total.Alkalinity','d18O.H2O', 
                   'Cruise.ID', 'Station.ID', 'Station.ID.New', 
                   'NP.Ratio', 'pNO3','NO', 'PO', 'O2sat', 'pO2sat',
                   'fPAC', 'SIM', 'MW', 'PAC', 'ATL' 
                   )

```


## Data Sets and their original citations 

Codispoti
	
Cooper_d18O_Nuts_1987_99
	
GEOTRACES 2015

Hydrochemical Atlas (do NOT include in definition of ‘accepted conc. ranges’)

IOS_TADIC

LSSL 2003 (compares well with AOS 2005, use as reference for other LSSL cruises & Mirai data)

LSSL 2004

LSSL 2005
	

LSSL 2007
	

LSSL 2009

LSSL 2010

LSSL 2011

LSSL 2012

LSSL 2013

LSSL 2014

LSSL 2016
	
LSSL 2017

Mirai 1998

Mirai 1999

Mirai 2000

Mirai 2002
	
Mirai 2004

Mirai 2006

Mirai 2008

Mirai 2009

Mirai 2010
	
Mirai 2012

Mirai 2013

NABOS 2005-2009

NABOS 2015

d18O Database
	
SWL d18O

Switchyard

NOTE:  Outliers removed from CCHDO data sets without recording notes here!
