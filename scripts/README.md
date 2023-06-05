Different scripts were created to analyse phenomics data of the 24 _Saccharomyces cerevisiae_ strains in 29 growth conditions (perturbations). 
1. strain_phenotype_calc.Rmd: script to calculate umax and lag phase from growth data. The script was used to calculate biomass and ethanol yields on sugars and the cell dry weight at the end of cultivation. 
2. Preprocessing.Rmd: phenomics data from all strains were merged on a single dataframe. Distributions and normality were analysed. Data were trimmed out for unreasonable values and outliers were identified. 
3. ExploratoryAnalysis.Rmd: performance was analysed and plotted, emphasizing growth conditions and strains. PCA and UMAPS were run as well as corerlations among different phenotypes.
4. robustness.Rmd: calculation of robustness for each phenotype and strain. correlation between robustness and performance were checked. 
5. adaptation.Rmd: calculation of percentage of improvement (%P) of the maximum specific growth rate. correlations between %P, robustness and perfomance were analysed. 

For each of the script a .html page is available to check scripts run on the uploaded data. 
> Results available after peer review. 
