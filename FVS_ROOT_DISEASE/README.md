## Parameters for Apiary Data Western Root Disease Model Runs:
- Excel file used was "TMT1_STAND2_INPUT.xlsx"
- Phellinus (Coniferiporia) root disease was used for the root disease type. The keyword and number for this was RRTYPE = 4. 
- Total stand size projections being used is .25 acres. This takes into account the 5 plots which are each .05 acres in size. 
- Total roots disease area in acres was calculated by using the data sheets provided from Weyco and the Forest Service. For TMT1_STAND2 this was 0.4. 
- Number of root diesease centers were not readily detected on the ground during the final survey, therefore the stand was modeled as a one for the disease centere value.
- Parameters for the RRInit keyword, proportion of roots infected 0.4 was estimated overall and used as the standard. This is taking into considerationg that 0.1 (10%) is considered light infection and that tree mortality will occur well before 100% of roots become infected depending on the disease type. Therefore proportion of root system infected was estimated at 0.4 but was not based upon any type of measurements or data (this conclusion is based upon the advice I received from Lance David).
- Default parameters were used regarding bark beetles considering that the Douglas-fir beetle (Dendroctonus pseudotsugae Hopkins) occurs throughout the extensive range of Douglas-fir (Furniss and Kegley, 2014). Also consider adding in Hansen et. al paper about bark beetles if it refers to the Apiary site at all. 




(The above list was revised from the following publication. The parameters that they used and justification for these options can be seen below: https://www.fs.fed.us/rm/pubs/rmrs_p054/rmrs_p054_055_067.pdf)

- • Armillaria root disease was identified as the root disease type (keyword
- RRTYPE = 3)
- • The root disease in the stand or plot was assumed to occur as one center since the
edges of the centers in the study area were not readily discernible on the ground
(typical of root disease centers in mixed-conifer forests in central Oregon).
- • For individual variable-radius plot projections, the total size of the area to be modeled was approximated as 1 acre (keyword SAREA).
- • For stand projections, the total size of the area to be modeled was approximated as
a constant 15 acres (keyword SAREA = 15) to more adequately describe the study
units compared to the default of 100 acres.
• For projections, the acres in root disease (keyword RRINT) were assumed to be
the stand size (15 acres) multiplied by the proportion of variable-radius plots in
the stand where Armillaria root disease occurred (RDSR >1). Thus, if half of the
plots had a RDSR >1, the area in root disease was set at 7.5 acres compared to the
WRDM default of 25%. Thus, the stand acres in root disease were, on average, 7.5
acres in size with a range from 2–15 acres. Since projections are sensitive to the
acres in root disease in a stand and there was variation in the incidence of root
disease between stands, this adjustment to the default was preferable to setting
it to a constant for all stands (e.g., 15 acres).
• For plot level projections, variable-radius plot were assumed to be a single root
disease center (keyword RRINT) except when there was no measured root disease
on the plot (RDSR = 0 or 1). On plots with RDSR = 0 or 1, some root disease was
assumed to occur within the modeled area because root disease was widespread
throughout the rest of the stand. Since there was no electronically accessible information (the usual situation for vegetation management projects) with respect
to the relative location of infected plots to uninfected plots, the default value of
25% was used.
• The density of infected trees was estimated from the damage codes on individual
measured trees (keyword RRTREIN).
• The model was run with default values for bark beetles since preferential bark
beetle activity was observed inside the root disease centers

## WRD Model Run
- Excel files used was Decktop/LAST_TIME/TMT1/1990/$FILE.xlsx
- Database file used was Decktop/LAST_TIME/TMT1/1990/WRD/FVS_TMT1_1990_WRD.db
- Main output file used was Decktop/LAST_TIME/TMT1/1990/WRD/FVS_TMT1_1990_WRD.txt
- Keyword: StdInfo 
- National Forest: Siuslaw
- Plant Association: CHF211 TSCH/ACTR-OLY
- Root disease parameters were determined using the corresponding excel spreadsheet Desktop/Stand Size Per Acre - Woods Creek Study Area.xlsx

--------------------  Extensions -------------------- 

WRD (Laminated Root Rot)
Keywords: RRInit

RRInit: Specify the number, size, and distribution of disease centers.
Component title   
RRInit: Specify the number, size, and distribution of disease centers.
Disease center configuration  
Disease centers randomly distributed
Number of root disease centers to be located in the stand  
1
Number of infected trees/arcre in the root disease centers  
 3
Number of uninfected trees/arcre in the root disease centers  
 7
Average proportion of root infection  
0.4
Total root disease area (acres)  
 13.30

--------------------  Extensions (continued) -------------------- 


Base FVS system
Keywords: StndInfo

StdInfo: Describes the site characteristics where the stand is located.
Component title   
StdInfo: Describes the site characteristics where the stand is located.
National Forest where stand is located.  
Siuslaw
Plant Association  
CHF211 TSHE/ACTR-OLY
Stand age  
 
 


 
