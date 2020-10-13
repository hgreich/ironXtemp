# ironXtemp

## Welcome to the github page for the paper "Iron availability modulates the response of symbiotic dinoflagellates to heat stress." Reich et al, 2020. Journal of Phycology

But first! Check out the **prequel** "Endosymbiotic dinoflagellates pump iron: Differences in iron and other trace metal needs among the Symbiodiniaceae" here: https://link.springer.com/article/10.1007/s00338-020-01911-z

Read the **sequel** online here: https://onlinelibrary.wiley.com/doi/abs/10.1111/jpy.13078 
DOI: 10.1111/jpy.13078

### Below, please a brief overview of each file and the abstract. Feel free to reach out w/ questions anytime via email: hgreich16 [at] gmail [dot] com

## General remarks 
**Species Abbreviations**: min/bmin/bm/m = Breviolum minutum; psyg/psygmo/bpsyg/bp/b = Breviolum psygmophilum

**Iron concentration abbreviations** The data files use the total desolved iron concentrations throughout. the treatments are referred to by their bioavailable iron concentrations (pM Fe') which makes the study comparable to others. the metadata often lists the total dissolved iron concentration (nM total dissolved Fe). In the paper, we explain how these relate to one another: "With the addition of EDTA 50, 250, and 500 pM Fe' are bioavailable, which corresponded to the total dissolved iron concentrations 10, 50, and 100 nM Fe, respectively). Hereafter, the iron concentrations will be referred to by their inorganic or bioavailable (Fe')."

## File overview

### Data files
**cell_density.xlsx** Excel file with raw cell count data (raw_cellden sheet). Cell densities were calculated with a beckman coulter counter for 2 Breviolum species exposed to 3 iron concentrations and 3 temperatures. Other important sheets include "spgrowth_r" and "spgrowth_calc" - these are the sheets for the specific growth figure (Fig 1) and calculations (respectively). The "pH" sheet includes the pH data for each treatment at various growth stages (used for Fig S1). The "vol" sheet includes the cell density, cell volume, and volume (mL) of aliquot for the various analyses (trace metal, pigment, C, N) for each triplicate replicate.

**fire_results_git.xlsx** Excel file with raw photophysiology data for each triplicate replicate. FIRe data analyses includes PSII (photosystem) cross section absorption (σPSII/sigma), PSII photochemical efficiency (Fv/Fm), and connectivity factory (p aka p_conn), and electron re-oxidation rate of QA (quencher/quinone pool A, Tau, τQA aka TauAv1. Data are blank corrected and results were generated using FirePro software. Info on acquisition of blank, etc are described in the manuscript. This also file includes max+min flourescence (Fo, Fm) etc for transparency. Metadata matches the other spreadsheets so they can be joined with dplyr when normalizing measurements.

**chla_data_git.xlsx** Excel file with raw chla data (ug/L, "raw_data" sheet) and output from calculations (converts to pg/cell, "calc_Routput"). The bolded "pg_chla_cell" column in the "calc_Routput" is the data used for stats & figures

**metal_data_git.xlsx** Excel file with metal (and phosphorus) content data. The "raw_data" sheet has raw data (nM metal, already internal standard and blank corrected). The "metal_calc_Routput" sheet converts from nM to pg/cell. The bolded "pg_metal_cell" columns in the "metal_calc_Routput" sheet contain the data used for stats & figs. 

**pocpon_data_git.xlsx** Excel file with organic carbon & nitrogen data. the units are pg c/cell and pg n/cell

**lipid_quant.xlsx** Excel file with total lipid content for each triplicate replicate

### Code for figures & stats
**Fig_1_specific_growth.Rmd** Rmarkdown file for figure 1 (specific growth for Breviolum spp at various [Fe] & temperatures). Calls upon the "spgrowth_r" sheet in cell_density.xlsx

**Figs_2_S2_fire_stats_figs.Rmd** Rmarkdown file for figures involving photophys - figs 2 (and corresponding stats). Both stats and figures call upon "fire_results_git.xlsx".

**Figs_3_S4-S6_metal_stats_figs.Rmd** Rmarkdown file for figures involving metals (and phosphorus) - figs 3, S4, S5, S6 (and corresponding stats). Both stats and figs call upon "metal_data_git.xlsx". Please note that the units for fig S5 metal:phosphorus ratios are from pg metal/ cell and pg P/ cell data. These are slightly different from the ratios in Reich et al 2020 coral reefs (mmol metal: mol P) but show the same patterns (Bpsyg has higher metal:P than Bmin).

**Fig_S1_pH.Rmd** Rmarkdown file for figure S1 (pH for Breviolum spp at various [Fe] & temperatures). Calls upon the "pH" sheet in "cell_density.xlsx"

**Fig_S2_chla_calc_stats.Rmd** Rmarkdown file for figure S2 (chla at various [Fe] & temps) and corresponding stats. Calls upon "raw_data" sheet from "chla_data_git.xlsx." Converts chla from ug/L (culture media) to pg/cell. Output of calculations is in the "calc_Routput" sheet of the same excel file.

**Fig_S3_total_lipid.Rmd** Rmarkdown file for figure S3 and corresponding statistics (lipid content for Breviolum spp at various [Fe] & temperatures). Calls upon "lipid_quant.xlsx"

**Fig_S6_macronutrient_stats_figs.Rmd** Rmarkdown file for figure S6 and corresponding statistics (C, N, and P for Breviolum spp at various [Fe] & temperatures). Calls upon "pocpon_data_git.xlsx" and "metal_data_git.xlsx"

**Table_1_summarystats.Rmd** Rmarkdown file for table 1. Combines all datasets (specific growth, chla, lipid, photophys - FIRe, C, N, P, metals) and produces average & sd by treatment. NOTE: the final table in the manuscript "only" includes specific growth, C, N, P, and metals (for space reasons). Also the units for the metals were converted to fg metal/ cell so the numbers were friendlier to look at.

## Abstract
Warming and nutrient limitation are stressors known to weaken the health of microalgae. In situations of stress, access to energy reserves can minimize physiological damage. Because of its widespread requirements in biochemical processes, iron is an important trace metal; especially for photosynthetic organisms. Lowered iron availability in oceans experiencing rising temperatures may contribute to the thermal sensitivity of reef-building corals, which rely on mutualisms with dinoflagellates to survive. To test the influence of iron concentration on thermal sensitivity, the physiological responses of cultured symbiotic dinoflagellates (genus Breviolum; family Symbiodiniaceae) were evaluated when exposed to increasing temperatures and a range of iron concentrations. Declines in photosynthetic efficiency at elevated temperatures indicated sensitivity to heat stress. Furthermore, five times the amount of iron was needed to reach exponential growth during heat stress (50 pM Fe' at 26-28 ºC versus 250 pM Fe' at 30 ºC). In treatments where exponential growth was reached, Breviolum psygmophilum grew faster than B. minutum, possibly due to greater cellular content of trace metals. The metal composition of B. psygmophilum shifted only at the highest temperature (30 ºC), whereas changes in B. minutum were observed at lower temperatures (28 ºC). The influence of iron availability in modulating each alga’s response to thermal stress suggests the importance of trace metals to the health of coral-algal mutualisms. Ultimately, a greater ability to acquire scarce metals may improve the tolerance of corals to physiological stressors; and contribute to the differences in performance associated with hosting one symbiont species over another.

### Feel free share this paper/github on twitter (@HannahGReich) if you agree that trace metals are cool :-)
