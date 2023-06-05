# Performance and robustness analysis reveals phenotypic trade-offs in yeast!
##### R Toolbox for the quantification of the robusntess of cellular functions starting from a high-throughput setup and multivariate analysis of phenomics dataset

**NOTE**: The main findings of the study are summarized below and in a study which is currently submitted for peer-review. 
We analysed more than 10000 phenotypic data from 24 **Saccharomyces cerevisiae** strains cultivated in 29 growth conditions. The phenotypes analysed were: maximum specific growth rate (1/h), lag phase(h), ethanol and biomass yields (g/g) and cell dry weight (g/L). In addition to the performance we also calculated the robustness of the phenotyes (listead above) with a previous published methodology [Quantification of microbial robustness in yeast](https://pubs.acs.org/doi/10.1021/acssynbio.1c00615) and with the R tools already availble on GitHub [Quantification of Microbial Robusntess](https://github.com/cectri/Quantification-of-microbial-robustness#quantification-of-microbial-robusntess). To expand the perturbation space we included as a perturbation a cell transfer step. The cultures were reinoculated after 48h in the same cultivation setup and the maximum specific growth rate of the second cultivation was assessed. Correlations among performance, robustness and the short-term adaptation (percentage of improvement of the umax in teh second cultivation) were analysed.

Main findings of the study: 
1. High-throughput micro cultivations revealed novel behaviors in yeast phenotypes that could only be identified thanks to the large data set collected. 
2. Robustness quantification adds information beyond performance measurement for multiple phenotypes, not only to identify strain targets for industrial production but also to study physiological mechanisms. 
3. Performance and robustness trade-off, but only for three out of five of the investigated phenotypes. 

&nbsp;  
&nbsp;  
This GitHub page includes:
 1. First cultivation growth data for each strain (growth_data_1 folder). Each .xlsx file is formatted with the first column corresponding to the time in minutes and each column to a well in the 96-well plate. The layout of the plate is in the plate_layout folder. 
 2. Second cultivation growth data for each strain (growth_data_2 folder). .xlsx files are formatted as above and the plate layout is the same as the first cultivation. 
 3. Final sugars and ethanol concentrations measured with enzymatic assays as well as final OD_600 and slope to convert OD in cell dry weight are summarised in the phenotype_raw_data folder, grouped for each strain. 
 4. Raw data were processed using "strain_phenotype_calc.Rmd" in the scripts folder. The processed data were saved in the processed_data folder. 
 5. Performance analysis was performed on all the strains using "preprocessing.Rmd" and "ExploratoryAnalysis.Rmd". 
 6. Robusntess and correlations between robustness adn performance were analysed using "robusntess.Rmd". 
 7. Improvement of the umax and relative correlations with robustness and performance were analysed using "adaptation.Rmd". 

**NOTE** for each of the scripts mentioned above there is a corresponding knitted .html page run on the available data. This is to facilitate the output and results visualization of the data of our study. The scripts above can be adapted to any high-throughput setup and can be used to calculate phenotypic variables as well as checking correlations between performance and robusntess. 

&nbsp;  

Cecilia Trivellin, *cectri@chalmers.se*, Industrial Biotechnology Division, Chalmers University of technology

Created: 23-06-05

The scripts were tested with R Version: Version 2023.03.1+446 (2023.03.1+446) RStudio
Mac OS Ventura 13.4
The following R libraries were used in the scripts and referenced in the manuscript: 
deSolve, growthrates, ggplot2, ggExtra, naniar, ggpubr, statmod, readr, rstatix, ggridges, ggsci, RColorBrewer, stats, gghighlight, ggbeeswarm, uwot, GGally

&nbsp;  

--------

Acknowledgment of support: This material is based upon work supported by the Novo Nordisk Foundation grant DISTINGUISHED INVESTIGATOR 2019 - Research within biotechnology-based synthesis & production (#0055044).
Société Industrielle Lesaffre, Division Leaf, is kindly acknowledged for providing the Ethanol Red strain.

&nbsp;  
