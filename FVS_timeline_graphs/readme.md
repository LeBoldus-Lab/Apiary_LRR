# To make changes to basal area for different plots:
- The only excel file that should need to be edited is the "AP_FVS_data_combined_TMT1_STND2.xlsx" file.


# For example if you want to enter data from a new run and use TMT1 STAND4 you would edit the basal "TMT1_BA" for TMT1 STAND4
- Make the edits then save the file as AP_FVS_data_combined_TMT1_STND4.xlsx

![image](https://user-images.githubusercontent.com/49656044/160902656-43da1f36-2c22-4957-a2cd-dd653175c318.png)


# Withint the R markdown file you then change this line:
![image](https://user-images.githubusercontent.com/49656044/160903218-8c6e29df-211c-42ea-9e51-be07d0e227c3.png)

# Error bars can be added within the "TMT1_SE" columns and then uncommenting this section of the code:
![image](https://user-images.githubusercontent.com/49656044/160903472-387cc8ba-190f-433e-9deb-68a754a88d32.png)
