

# Libraries
```{r include=FALSE}
# Load libraries we need for the assignment
install.packages("fvsLoad")
library(ggplot2)
install.packages(tidyverse)
install.packages(tidyr)
library(tidyverse)
library(dplyr)
library(tidyr)
library(readxl)

```

# Apiary Data File
```{r}
#Total Modelled Data
fvs_data <- read_excel("C:/Users/shawn/Desktop/Woods Creek/LAST_TIME/R_final/FVS_data.xlsx")
fvs_data_TMT2_3 <- read_excel("C:/Users/shawn/Desktop/Woods Creek/LAST_TIME/R_final/FVS_data_TMT2_3.xlsx")
fvs_data_combined <- read_excel("C:/Users/shawn/Desktop/Woods Creek/LAST_TIME/R_final/FVS_data_combined.xlsx")
fvs_data_combined_TPA <- read_excel("C:/Users/shawn/Desktop/Woods Creek/LAST_TIME/R_final/FVS_data_combined_TPA.xlsx")
fvs_data_combined_TMT1 <- read_excel("C:/Users/shawn/Desktop/Woods Creek/LAST_TIME/R_final/FVS_data_combined_Apiary_DF_only.xlsx")
fvs_data_combined_TMT2 <- read_excel("C:/Users/shawn/Desktop/Woods Creek/LAST_TIME/R_final/FVS_data_combined_Apiary_DF_only.xlsx")
fvs_data_combined_TMT3 <- read_excel("C:/Users/shawn/Desktop/Woods Creek/LAST_TIME/R_final/FVS_data_combined_TMT3_FINAL.xlsx")

```





# Apiary Line Graph

```{r}
library(ggplot2)
library(cowplot)

#install.packages(scales)
#library(scales)
#library(viridis)
AVERAGE_BA <- as.numeric(fvs_data_combined$AVERAGE_BA)
#as.numeric(fvs_data$FULL_Year)
#as.numeric(fvs_data$Full_MgmtID)
#(aes(fill = dose), show.legend = FALSE)
 gg1 <- ggplot(data = fvs_data_combined_TMT2, aes(x = FULL_Year, y = TMT1_BA, , group = GRAPH ), position = position_dodge(0.2)) +  
  geom_point(position = position_dodge(0.2)) +    

   
    #  geom_line(linetype = "dashed") +
  
   geom_line(aes(linetype=GRAPH))+
  scale_y_continuous(labels = paste(seq(0, 90, by = 10)), 
                     breaks = seq(0, 95, by = 10), 
                     limits = c(0, 95) )+ 
      #position = position_dodge(0.3)) + 
    geom_errorbar(data =  fvs_data_combined_TMT1, aes(ymin=TMT1_BA - TMT1_SE,  ymax=TMT1_BA + TMT1_SE), width=.2, position=position_dodge(0.01)) +
theme_classic() +
 scale_color_viridis(discrete=TRUE) + theme_classic()  + labs(x = "Year") +  
ylab(expression(paste(BA~m^2/ha))) +
scale_colour_manual(values=c("black", "black", "black")) 
 # +
   #scale_color_brewer(palette = "Dark2", name = "") 
   
gg1

 output <- plot_grid (gg1 + theme(legend.position = "right"), labels = c('D'),  hjust = -3.5, label_size = 20, ncol = 1) 
print(output) 
 ggsave("Apiary.png")
 
```

