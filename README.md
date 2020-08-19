# ironXtemp

## Welcome to the github page for the paper "Iron availability modulates the response of symbiotic dinoflagellates to heat stress." Reich et al, in revision at Journal of Phycology

But first! Check out the prequel "Endosymbiotic dinoflagellates pump iron: Differences in iron and other trace metal needs among the Symbiodiniaceae" here: https://link.springer.com/article/10.1007/s00338-020-01911-z

### Below, please a brief overview of each file and the abstract. Feel free to reach out w/ questions anytime via email: hgreich16 [at] gmail [dot] com

## General remarks 
**Species Abbreviations**: min/bmin/m = Breviolum minutum; psyg/psygmo/bpsyg/b = Breviolum psygmophilum

**Iron concentration abbreviations** The data files use the total desolved iron concentrations throughout. the treatments are referred to by their bioavailable iron concentrations (pM Fe') which makes the study comparable to others.  "With the addition of EDTA 50, 250, and 500 pM Fe' are bioavailable, which corresponded to the total dissolved iron concentrations 10, 50, and 100 nM Fe, respectively (Rodriguez et al., 2016). Hereafter, the iron concentrations will be referred to by their inorganic or bioavailable (Fe') concentrations so that they correspond to other Symbiodiniaceae culture experiments in literature (Rodriguez et al., 2016, Rodriguez & Ho, 2017, Rodriguez & Ho, 2018, Reich et al., 2020)."

## File overview
**raw_cell_count_tracker** Excel file with raw cell count data (batch sheet). Cell densities were calculated with a beckman coulter counter for 5 Symbiodiniaceae species exposed to 4 iron concentrations. The innoculation density sheet includes cell density info for stock cultures

**fig_2_stats.xlsx** Excel file of cell density and stdev of cultures exposed to four iron concentrations (averages and stdev are from raw cell count tracker file).

**fig_2_cell_density_.Rmd** Rmarkdown file of cell density figure (fig 2) and corresponding statistics. Calls upon the fig_2_stats excel file. 

**fig_3_specific_growth.xlsx** Excel file with sheets including average specific growth (used for R), and the (raw) calculation for each species. 

**fig_3_specific_growth.Rmd** corresponding Rmarkdown file for specific growth figure (Fig 3)

**metal_data.xlsx** Results from HR-ICPMS elemental analysis of Symbiobiodiniaceae species exposed to different iron concentrations.

**fig_4-5_S1_S2_metal_figs_REVISED_112019.Rmd** Metal content, uptake, & efficiency figures (4, 5, S1, S2) and bivariate statsitics. Calls upon metal_data excel file. 

**fig_6_pca.Rmd** Multivariate analysis of Symbiodiniaceae trace metal content (Fig 6). Calls upon metal_data excel file. This PCA uses features from the FactoMineR and ggplot2 packages (so shape can demark one factor and color another factor, see lines 115-130).

**fig_s3_allalgae_growthcomparison_DATA.xlsx** Excel file for Fig S3. Compares specific growth rate of Symbiodiniaceae at different bioavailable iron concentrations to other phytoplankton. These studies are comparable because they calculate/present bioavailable iron concentrations (in addition to total dissolved iron concentrations). Data are incorporated from Sunda & Huntsman 1995; Rodriguez et al 2016; Rodriguez & Ho 2018. Links here: https://www.sciencedirect.com/science/article/pii/030442039500035P; https://www.frontiersin.org/articles/10.3389/fmicb.2016.00082/full; https://www.frontiersin.org/articles/10.3389/fmicb.2018.00142/full

**fig_s3_allalgae_growthcomparison.Rmd** Rmarkdown file for figure S3. Visualizes microalgae specific growth by bioavialable iron concentration for different lineages. Calls upon the growth comparison excel file.
 
**all_posthoc_stats_output.csv** Bivariate kruskal-wallis output for metal content, uptake & efficiency. Pairwise comparisons between each treatment. Please see description of abbreviations in the general remarks (above) for proper interpretation of abbreviations in "comparisons" column.

## Abstract
Warming and nutrient limitation are stressors known to weaken the health of microalgae. In situations of stress, access to energy reserves can minimize physiological damage. Because of its widespread requirements in biochemical processes, iron is an important trace metal; especially for photosynthetic organisms. Lowered iron availability in oceans experiencing rising temperatures may contribute to the thermal sensitivity of reef-building corals, which rely on mutualisms with dinoflagellates to survive. To test the influence of iron concentration on thermal sensitivity, the physiological responses of cultured symbiotic dinoflagellates (genus Breviolum; family Symbiodiniaceae) were evaluated when exposed to increasing temperatures and a range of iron concentrations. Declines in photosynthetic efficiency at elevated temperatures indicated sensitivity to heat stress. Furthermore, five times the amount of iron was needed to reach exponential growth during heat stress (50 pM Fe' at 26-28 ºC versus 250 pM Fe' at 30 ºC). In treatments where exponential growth was reached, Breviolum psygmophilum grew faster than B. minutum, possibly due to greater changes in the cellular content of trace metals. The metal composition of B. psygmophilum shifted only at the highest temperature (30 ºC), whereas changes in B. minutum were observed at lower temperatures (28 ºC). The influence of iron availability in modulating each alga’s response to thermal stress suggests the importance of trace metals to the health of coral-algal mutualisms. Ultimately, a greater ability to acquire scarce metals may improve the tolerance of corals to physiological stressors; and contribute to the differences in performance associated with hosting one symbiont species over another.

### Feel free share this paper/github on twitter (@HannahGReich) if you agree that trace metals are cool :-)
