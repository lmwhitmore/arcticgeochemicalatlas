
## GEOCHEMICAL ATLAS HISTORY

The Geochemical Atlas was compiled to permit pan-Artcic analysis of changes in biogeochemical properties; it was originally published with Polyakov et al., 2020 as a description in the supplement. The files included as the "original upload" include a .mat data file, a document describing the quality control measures taken during compilation of the data sets, and a .txt file with all data in a tabular format. This work was conducted by Matthew Alkire, Kristina Brown, and Igor Polyakov.  

Polyakov, I.V., Alkire, M.B., Bluhm, B.A., Brown, K.A., Carmack, E.C., Chieric, M. Danielson, S.L., Ellingsen, I., Ershova, E.A., Gårdfeldt, K., Ingvaldsen, R.B., Pnyushkov, A.V. Slagstad, D., Wassmann, P. (2020). Borealization of the Arctic Ocean in Response to Anomalous Advection From Sub-Arctic Seas. *Frontiers in Marine Science*, 7. https://doi.org/10.3389/fmars.2020.00491
Front. Mar. Sci. , 02 July 2020

This original data set stops in 2018. The subsequent versions have been updated by Laura Whitmore. 

## Major Changes to the Geochemical Atlas

#Removal of data: 
Bering and Chukchi sea shelf data that is part of the ECOFOCI monitoring program has been compiled into a compendium and throughly 
QA/QC'd by the ECOFOCI team. For this reason, we removed any duplicates with this dataset.

This dataset can be found: CITATION. 

## Data Sets and their original citations 

## Downloadable data types and how to read them 

The original .mat file can be readily loaded into matlab or read into R using the library R.matlab. 

The .txt file is headerless, but can be read: 


;|||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||
;----------------               read the Arctic Ocean data        ------------------------
;|||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||
;
;       1) Year                                                 2) Month                                        3) Day                                  4) Latitude             
;       5) Longitude                                    6) Pressure                                     7) Temperature                  8) Salinity (primary)           
;       9) Dissolved oxygen (primary)   10) Bottle salt (ignore)        11) Bottle O2 (ignore)  12) Phosphate
;       13) Nitrate+nitrite                             14) Silicate                            15) DIC                                 16) TA         
;       17) d18O                                                18) Cruise ID                           19) Station ID                  20) Station ID_new
;   21) N:P ratio                                       22) pNO3                                        23) NO                                  24) PO
;   25) O2sat                                           26) pO2sat                                      27) fPAC                                28) SIM
;   29) MW                                                      30) PAC                                         31) ATL
;
;

Reading is using this line:


   readf,1,iyr,imo,ida,sla,slo,p,t,s,o2,sd,o2d,po4,ni,si,dic,ta,d18o,idc,ids1,ids2,npr,pno,no,po,o2sat,po2sat,fpw,sim,mw,pac,aw   ; v4.3



This is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that includes both content as well as the output of any embedded R code chunks within the document. You can embed an R code chunk like this:


```{r cars}
summary(cars)
```

## Including Plots

You can also embed plots, for example:

```{r pressure, echo=FALSE}
plot(pressure)
```

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.
