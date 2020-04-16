# Die-off Project

The following study was funded by the Center for Produce Safety (2018CPS04).

#### Abstract

The Food Safety Modernization Act (FSMA) includes a time-to-harvest interval following the application of non-compliant water to pre-harvest produce to allow for microbial die-off. However, additional scientific evidence is needed to support this rule. This study aimed to determine the impact of weather on the die-off rate of _E. coli_ and _Salmonella_ on spinach and lettuce under field conditions. Standardized, replicated field trials were conducted in California, New York, and Spain over two years. Baby spinach and lettuce were grown and inoculated with a ~104 CFU/mL cocktail of _E. coli_ and attenuated _Salmonella_. Leaf samples were collected at 7 timepoints (0-96h) following inoculation; _E. coli_ and _Salmonella_ were enumerated. The associations of die-off with study design factors (location, produce type, and bacteria) and weather were assessed using log-linear and biphasic segmented log-linear regression. A segmented log-linear model best fit die-off on inoculated leaves in most cases, with a greater variation in the segment 1 die-off rate across trials [-0.46 (95% confidence interval (95% CI): -0.52, -0.41) to -6.99 (95% CI: -7.38, -6.59) log10 die-off/day] compared to the segment 2 die-off rate [0.28 (95% CI: -0.20, 0.77) to -1.00 (95% CI: -1.16, -0.85) log10 die-off/day]. A lower relative humidity was associated with a faster segment 1 die-off and an earlier breakpoint (the time when segment 1 die-off rate switches to the segment 2 rate). Relative humidity was also found to be associated with whether die-off would comply with FSMA’s specified die-off rate of -0.5 log10 die-off/day.

#### Importance
The log-linear die-off rate proposed by FSMA is not always appropriate, as the die-off of foodborne bacterial pathogens and specified agricultural water quality indicator organisms appear to commonly follow a biphasic die-off pattern with an initial rapid decline followed by a period of tailing. While we observed substantial variation in the net culturable population levels of _Salmonella_ and _E. coli_ at each time point, die-off rate and FSMA compliance (i.e., at least a 2 log10 die-off over 4 days) appear to be impacted by produce type, bacteria, and weather; die-off on lettuce tended to be faster than that on spinach, die-off of _E. coli_ tended to be faster than that of attenuated _Salmonella_, and die-off tended to become faster as relative humidity decreased. As such, the use of a single die-off rate for estimating time-to-harvest intervals across different weather conditions, produce types, and bacteria should be revised.

## Data sets
The following data sets were used for analysis: 
"AllData.csv" - Microbial count data and sample metadata from the CPS funded die-off project.
"weather_final.csv" - Hourly weather data from the CPS funded die-off project.

A description of the variables included in each of these datasets can be found, below.

"AllData.csv"
|Variable|Description  |
|--|--|
|ID|Unique numerical id for each data point. Values range from 1 to 5252|
|date_time|Date and time of sample collection, in the following format: month/day/year hours:minutes:seconds AM/PM|
|PlotID|Unique id for each plot, in the following format: Location (CA, NY, SP) – cohort/ trial # (C#, where number is trial number within a location) – produce type and plot number (S/L#, where the number is the plot number within a given trial and produce type). For example, NY-C1-S1 for NY trial 1, spinach plot 1|
|SampleID|Unique id for each sample. The format is the same as PlotID, with replicate sample number on the end (R#). For example, NY-C1-S1-R1 for the NY trial 1, spinach plot 1, replicate sample 1|
|Location|Location the data point was collected for. Levels: CA (Davis, California), NY (Freeville, New York), SP (Murcia, Spain)|
|Cohort1|Cohort (trial) number. This cohort number is only unique within a given location (i.e., there are cohorts 1 to 4 for CA, cohorts 1 to 4 for NA, and cohorts 1 to 4 for NY)|
|Time|Time of sample collection in hours. Sample collection occurred at the following seven time points: 0, 4, 8, 24, 48, 72, and 96h for all cohorts|
|Plot|Plot number. The plot number is only unique within a produce type for a single cohort/trial|
|Rep|Replicate sample number. The replicate sample number is only unique within a time point from a given plot|
|Stype|Produce type of the sample. Either spinach or lettuce|
|Svariety1|Produce variety of the sample. Either “old” (Enza Zaden Tamarindo lettuce and Enza Zaden Acadia F1 spinach) or “new” (Harris Seeds Seaside F1 spinach)|
|Bacteria|Bacteria being enumerated in the given sample. Either “EC” (_Escherichia coli_) or “Sal” (_Salmonella_)|
|Weight|Weight of the produce that makes up the given sample (in grams)|
|Wash_Vol|Volume of phosphate buffered saline added to the sample for enumeration (in mL). A 1:5 dilution was performed on samples collected at 0, 4, and 8h following inoculation. A 1:10 dilution was performed on samples collected at 24, 48, 72, and 96h following inoculation|
|V1|Volume plated for the 1st of up to 3 plates for the given sample (in mL)|
|CFU1|Colony forming units (CFU) of _E. coli_ or _Salmonella_ on the 1st of up to 3 plates for the given sample. All CFU’s are indicated as integer values. The following codes indicate plates that were not able to be counted: UAC (unable to count), TMTC (too muddy to count), >1600 (too numerous to count), TNTC (too numerous to count), tierra (unable to count), UAL (unable to count), 0.9 (no colony forming units)|
|V2|Volume plated for the 2nd of up to 3 plates for the given sample (in mL). If the cell is blank, a 2nd volume was not plated|
|CFU2|Colony forming units of _E. coli_ or _Salmonella_ on the 2nd of up to 3 plates for the given sample. If the cell is blank, a 2nd volume was not plated. All CFU’s are indicated as integer values. The following codes indicate plates that were not able to be counted: UAC (unable to count), TMTC (too muddy to count), >1600 (too numerous to count), TNTC (too numerous to count), tierra (unable to count), UAL (unable to count), 0.9 (no colony forming units)|
|V3|Volume plated for the 3rd of up to 3 plates for the given sample (in mL). If the cell is blank, a 3rd volume was not plated|
|CFU3|Colony forming units of _E. coli_ or _Salmonella_ on the 3rd of up to 3 plates for the given sample. If the cell is blank, a 3rd volume was not plated. All CFU’s are indicated as integer values. The following codes indicate plates that were not able to be counted: UAC (unable to count), TMTC (too muddy to count), >1600 (too numerous to count), TNTC (too numerous to count), tierra (unable to count), UAL (unable to count), 0.9 (no colony forming units)|
|Enrich1|Y (yes)/ N (no), indicates if the sample was enriched. Enrichment was performed when no detectable colonies were present on the plates for the given sample|
|Presence1|P (positive)/ N (negative), if the sample was enriched, indicates if the sample was positive for either _E. coli_ or _Salmonella_. If the cell is blank, no enrichment was performed|

"weather_final.csv"
|Variable|Description|
|--|--|
|date_time|Date and time of sample collection, in the following format: month/day/year hours:minutes:seconds AM/PM|
|leaf.wet.min|Leaf wetness (minutes)|
|RH|Relative humidity (%)|
|DP|Dew point (C)|
|precip|Total precipitation (mm)|
|soil.temp|Soil temperature (C)|
|SR|Solar radiation (kilowatts per square meter, kW/m^2)|
|temp|Temperature (C)|
|wind|Wind speed (m/s)|
|location|Location of data point (CA, NY, SP). The geographic coordinates (WGS 84 Web Mercator) of the weather stations were: Lat: 38.53, Lon: -121.79 (elevation: 18.3 m) in California; Lat: 42.52, Lon: -76.33 (elevation: 335.3 m) in New York; and Lat: 38.11, Lon: -1.03 (elevation: 135 m) in Spain|
|date|Date of sample collection, in the following format: month/day/year|
|hour|Hour of the day. “0” indicates 12:00:00 AM|
|Eto|Evapotranspiration (mm)|
|res.wind|Residual wind speed (m/s)|
|v.pressure|Vapor pressure (kPa)|
|leaf.wet.mV|Leaf wetness (mV)|
|id|Unique numerical id for each data point. Values range from 1 to 12319|
|trial|Trial (cohort) number. A unique integer value from 1 to 12 was given to each trial|
|hpi|<![endif]--> Hours past inoculation for a given trial. “NA” denotes no trial was occurring during that hour of weather data collection|

