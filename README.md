# drought-risk-analysis-scotland 

Method detailed in Kirkpatrick Baird, F., Spray, D., Hall, J., and Stubbs Partridge, J. 2023. Projected increases in extreme drought frequency and duration by 2040 affect specialist habitats and species in Scotland. Ecological Solutions and Evidence, and in Kirkpatrick Baird, F., Stubbs Partridge, J. & Spray, D. 2021. Anticipating and mitigating projected climate-driven increases in extreme drought in Scotland, 2021-2040. NatureScot Research Report No. 1228. 

Datasets included in this repository are .csv and GIS outputs from the analysis. GIS data can also be found at NatureScot's Open Data Hub: https://opendata.nature.scot/. All data are available under an Open Government License: https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/. GIS data can also be requested from data_supply@nature.scot.

The GIS data consist of a set of 24 .tif files showing past or future extreme drought risk in Scotland. These were produced as part of a NatureScot study on 
changing drought risk in Scotland by 2040. The .tifs are derived from observed or modelled climate data, with drought risk calculated using the Standardised
Precipitation Evapotransipiration Index (SPEI), as described in detail in the methodology. 

## Description of the GIS data and file structure

Note that .tifs do not retain symbology, so the colours assigned to cells when the data are opened are random and meaningless. 

Naming convention: naturescot_drought_[events/months]_[modelagreement/observations/projected]_[change/actual]_[seasonal/total]

- events/months: the metric being measured, whether extreme drought events or extreme drought months.
    - extreme drought months = any month with an SPEI value ≤ -2
    - extreme drought events = one or more months with a continuous SPEI of ≤ -2
- modelagreement/observations/projected: type of data
    - model agreement = a measure of error when combining the 12 members of the climate model (climate models come in multiple runs, known as members, which have to be combined together). The model agreement datasets show how many of the 12 members agree with the sign of the median, ie, agree with an increase or decrease in extreme drought.
    - observations = datasets based on observed data, derived from the HADUK-Grid Observational dataset
    - projected = datasets based on modelled data, derived from the UKCP18 climate model
- change/actual: is the dataset calculated change from baseline, or actual values
    - change = only for projected datasets - change calculated from the baseline (1981-2001) to the future (2021-2040)
    - actual = observed, model agreement, and some projected datasets - actual values, not change from baseline
- seasonal/total: calculated by season, or annually
    - seasonal = separated by spring (March/April/May), summer (June/July/August), autumn (September/October/November), winter (December/January/February). Only extreme drought months, not events, as events can span multiple seasons
    - total = calculated annually

## Description of the .csv data

Naming convention:
- Drought change from baseline: change[events/months]_[season]_comb
- Modelled future drought occurence: mod[events/months]_[season]_comb

Terminology:
- Events = number of drought events over a 20 year period 
- Months = number of drought months over a 20 year period
- Comb = all model members combined
- Present_early = 2001-2010
- Present_late = 2011-2020

Full definitions are available in the paper and report.

DOI:10.5281/zenodo.7791179
