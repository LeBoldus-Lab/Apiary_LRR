## Parameters for 1990 WRD Run:
- Excel file used was "FVS_TMT1_1990_WRD.xlsx"
- Excel file was converted to database file here: https://forest.moscowfsl.wsu.edu/FVSDataConvert/
- Phellinus (Coniferiporia) root disease was used for the root disease type. The keyword and number for this was RRTYPE = 4. 
- Total stand size projections was estimated from the use of unpublished maps received from Hansen, shape files received from the forest service (insert name in acknoldegments) as well as ArcGIS Pro (insert version and reference here). 
- Total roots disease area in acres was calculated by multiplying the percentage of plots within the stands where Coniferporia was found by the total stand size in acres. For e.g.:TMT 1 Stand 1 was 16.63 acres in size and LRR was found at 80% of the plots therefore 16.63 x .8 = 13.304 acres of total root disease within this stand or (insert hectares here). The keyword RRINT was used for this projection. (insert citation here). 
- Number of root diesease centers were not readily detected on the ground during the final survey, therefore the stand was modeled as a one for the disease centere value.
- Parameters for the RRInit keyword, proportion of roots infected 0.4 was estimated overall and used as the standard. This is taking into considerationg that 0.1 (10%) is considered light infection and that tree mortality will occur well before 100% of roots become infected depending on the disease type. Therefore proportion of root system infected was exstimated at 0.4 but was not based upon any type of measurements or data (insert citation for advice from Lance)
- Default parameters were used in regards to bark beetles due to observations and trapping mechanisms that were implemented within the study area. Also consider adding in Hansen et. al paper about bark beetles if it refers to Marys Peak at all. 

- ~~ ~~ (STRIKETHROUGH) 01 = Tree is within 30 feet of a root disease infected tree
- ~~ ~~02 = Symptoms of root disease detected on the tree
- ~~ ~~03 = Symptoms of root disease and crown deterioration detected
 - ~~ ~~Dam code of 62 for all trees that had signs/symptoms (severity code 02) or mortality (severity code 03).
 - ~~ ~~If the plot center tree was infected then every tree within that plot was coded with a 00,01 for that year.
- ~~ ~~If tree was coded with a 02 or 03, an estimation of proximity was done and the previous two trees and the next two trees within the plot were assigned with a 00.
- ~~ ~~If last tree in the plot was coded a 02 or 03 then trees #1 and #2 were coded with a 01 and vice versa if the last two trees within the plot were coded as 02 or 03.





(The above list was revised from the following publication. The parameters that they used and justification for these options can be seen below: https://www.fs.fed.us/rm/pubs/rmrs_p054/rmrs_p054_055_067.pdf)

• Armillaria root disease was identified as the root disease type (keyword
RRTYPE = 3)
• The root disease in the stand or plot was assumed to occur as one center since the
edges of the centers in the study area were not readily discernible on the ground
(typical of root disease centers in mixed-conifer forests in central Oregon).
• For individual variable-radius plot projections, the total size of the area to be modeled was approximated as 1 acre (keyword SAREA).
• For stand projections, the total size of the area to be modeled was approximated as
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
 
 
