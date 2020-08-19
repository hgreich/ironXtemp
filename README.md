# ironXtemp

## Welcome to the github page for the paper "Iron availability modulates the response of symbiotic dinoflagellates to heat stress." Reich et al, in revision at Journal of Phycology

But first! Check out the prequel "Endosymbiotic dinoflagellates pump iron: Differences in iron and other trace metal needs among the Symbiodiniaceae" here: https://link.springer.com/article/10.1007/s00338-020-01911-z

### Below, please a brief overview of each file and the abstract. Feel free to reach out w/ questions anytime via email: hgreich16 [at] gmail [dot] com

## General remarks 
**Species Abbreviations**: min/bmin/m = Breviolum minutum; psyg/psygmo/bpsyg/b = Breviolum psygmophilum

**Iron concentration abbreviations** The data files use the total desolved iron concentrations throughout. the treatments are referred to by their bioavailable iron concentrations (pM Fe') which makes the study comparable to others.  "With the addition of EDTA 50, 250, and 500 pM Fe' are bioavailable, which corresponded to the total dissolved iron concentrations 10, 50, and 100 nM Fe, respectively (Rodriguez et al., 2016). Hereafter, the iron concentrations will be referred to by their inorganic or bioavailable (Fe') concentrations so that they correspond to other Symbiodiniaceae culture experiments in literature (Rodriguez et al., 2016, Rodriguez & Ho, 2017, Rodriguez & Ho, 2018, Reich et al., 2020)."

## File overview

### Data files
**cell_density.xlsx** Excel file with raw cell count data (raw_cellden sheet). Cell densities were calculated with a beckman coulter counter for 2 Breviolum species exposed to 3 iron concentrations and 3 temperatures. Other important sheets include "spgrowth_r" and "spgrowth_calc" - these are the sheets for the specific growth figure (Fig 1) and calculations (respectively). The "pH" sheet includes the pH data for each treatment at various growth stages (used for Fig S1). The "vol" sheet includes the cell density, cell volume, and volume (mL) of aliquot for the various analyses (trace metal, pigment, POC & PON) for each triplicate replicate.

**hplc_fire_results_git.xlsx** Excel file with raw photophysiology data for each triplicate replicate. FIRe data analyses includes PSII (photosystem) cross section absorption (σPSII/sigma), PSII photochemical efficiency (Fv/Fm), and connectivity factory (p aka p_conn), and electron re-oxidation rate of QA (quencher/quinone pool A, Tau, τQA aka TauAv1. Data are blank corrected and results were generated using FirePro software. Info on acquisition of blank, etc are described in the manuscript. This also file includes max+min flourescence (Fo, Fm) etc for transparency. Metadata matches the other spreadsheets so they can be joined with dplyr when normalizing measurements (i.e., normalizing chla in this sheet to cell vol used for harvest in the cell_density "vol" sheet).

### Code for figures & stats
**Fig1_specific_growth.Rmd** Rmarkdown file for figure 1 (specific growth for Breviolum spp at various [Fe] & temperatures). Calls upon the "spgrowth_r" sheet in cell_density.xlsx

**Figs_2_S2_fire_chla_stats_figs.Rmd** Rmarkdown file for figures 2 and S2 (and corresponding stats). Both stats and figures call upon "hplc_fire_results_git.xlsx". The information of volume & number of cells used for Fig S2 calls upon the "vol" sheet in "cell_density.xlsx". Fig 2 depicts photophysiological changes (Fv/Fm, sigma, Tau) of the two species when grown at the different iron concentrations and temperatures). Fig S2 depicts changes in chla content.

## Abstract
Warming and nutrient limitation are stressors known to weaken the health of microalgae. In situations of stress, access to energy reserves can minimize physiological damage. Because of its widespread requirements in biochemical processes, iron is an important trace metal; especially for photosynthetic organisms. Lowered iron availability in oceans experiencing rising temperatures may contribute to the thermal sensitivity of reef-building corals, which rely on mutualisms with dinoflagellates to survive. To test the influence of iron concentration on thermal sensitivity, the physiological responses of cultured symbiotic dinoflagellates (genus Breviolum; family Symbiodiniaceae) were evaluated when exposed to increasing temperatures and a range of iron concentrations. Declines in photosynthetic efficiency at elevated temperatures indicated sensitivity to heat stress. Furthermore, five times the amount of iron was needed to reach exponential growth during heat stress (50 pM Fe' at 26-28 ºC versus 250 pM Fe' at 30 ºC). In treatments where exponential growth was reached, Breviolum psygmophilum grew faster than B. minutum, possibly due to greater changes in the cellular content of trace metals. The metal composition of B. psygmophilum shifted only at the highest temperature (30 ºC), whereas changes in B. minutum were observed at lower temperatures (28 ºC). The influence of iron availability in modulating each alga’s response to thermal stress suggests the importance of trace metals to the health of coral-algal mutualisms. Ultimately, a greater ability to acquire scarce metals may improve the tolerance of corals to physiological stressors; and contribute to the differences in performance associated with hosting one symbiont species over another.

### Feel free share this paper/github on twitter (@HannahGReich) if you agree that trace metals are cool :-)
