[README.txt](https://github.com/user-attachments/files/28849993/README.txt)
Hamilton Harbour Fish Community Analysis and Size-Spectra Visualization Toolkit
==========================================================================

OVERVIEW
--------
This collection of Python scripts was developed to analyze long-term fish
community dynamics in Hamilton Harbour (Lake Ontario) from 1988–2023.
The scripts generate abundance, biomass, size-spectrum, breakpoint,
catchability, survivorship, and trophic guild visualizations used in
ecological modeling and fisheries assessments.

FOLDER STRUCTURE
----------------

Project/
│
├── Data/
│   │
│   ├── HH_YearSpecie.csv
│   │      Input for Relative_Abundance.py
│   │
│   ├── HH_SumYearSpecieWeight.csv
│   │      Input for Relative_Weight.py
│   │
│   ├── HH_Ab_SumYearSpecie.csv
│   │      Input for Species_Abundance.py
│   │
│   ├── ObsWeightPooledData.csv
│   │      Input for ObsWeightPooled_Data.py
│   │
│   ├── PredWeightPooledData.csv
│   │      Input for PredWeightPooled_Data.py
│   │
│   ├── TimeSeries.csv
│   │      Input for Local_Kernel_Regression.py
│   │
│   ├── EstimTimeSeries1.csv
│   │      Input for Estimated_Local_Kernel_Regression.py
│   │
│   ├── AllSpecies.csv
│   │      Input for Plot_All_Species.py
│   │
│   ├── PooledBeta.csv
│   │      Input for Scatter_PooledBeta.py
│   │
│   ├── Time.csv
│   │      Input for Time_Boxplot.py
│   │
│   ├── Site.csv
│   │      Input for Site_Boxplot.py
│   │
│   ├── Catchability_Parameters.csv
│   │      Optional input for Catchability_Analysis.py
│   │
│   └── Survivorship_Parameters.csv
│          Optional input for Survivorship_Analysis.py
│
├── Scripts/
│   ├── Relative_Abundance.py
│   ├── Relative_Weight.py
│   ├── Species_Abundance.py
│   ├── ObsWeightPooled_Data.py
│   ├── PredWeightPooled_Data.py
│   ├── Local_Kernel_Regression.py
│   ├── Estimated_Local_Kernel_Regression.py
│   ├── Plot_All_Species.py
│   ├── Scatter_PooledBeta.py
│   ├── Time_Boxplot.py
│   ├── Site_Boxplot.py
│   ├── Catchability_Analysis.py
│   ├── Survivorship_Analysis.py
│   └── Surv_Catch_Dist_Utility.py
│
└── Output/


SOFTWARE REQUIREMENTS
---------------------
Python 3.11 or higher

Required packages:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

Installation:
pip install pandas numpy matplotlib seaborn scikit-learn

SCRIPT DESCRIPTIONS
-------------------

Relative_Abundance.py
    Relative abundance trends by trophic guild.

Relative_Weight.py
    Relative biomass trends by trophic guild.

Species_Abundance.py
    Species-specific abundance trajectories.

ObsWeightPooled_Data.py
    Breakpoint versus observed size-spectrum coefficients.

PredWeightPooled_Data.py
    Breakpoint versus predicted size-spectrum coefficients.

Local_Kernel_Regression.py
    Kernel-smoothed temporal trends with uncertainty.

Scatter_PooledBeta.py
    Year versus β0, β11, and β12 relationships.

Time_Boxplot.py
    Temporal variability boxplots.

Site_Boxplot.py
    Spatial variability boxplots.

Catchability_Analysis.py
    Catchability curve simulations and visualization.

Survivorship_Analysis.py
    Survivorship model generation and comparison.

INPUT DATA REQUIREMENTS
-----------------------

Example: ObsWeightPooledData.csv

Required columns:
- Breakpoint
- Beta 0
- Beta 1
- Beta 2
- Trophic Guild
- CommonName

Additional scripts may require:
- Year
- Weight
- Abundance
- Common.Name
- Site
- Time
- Trophic

OUTPUT FIGURES
--------------

Generated figures include:
- Relative abundance trends
- Relative biomass trends
- Species-specific abundance trajectories
- Breakpoint–β relationships
- Kernel-smoothed temporal trends
- Bootstrap confidence intervals
- Temporal variability boxplots
- Spatial variability boxplots
- Catchability distributions
- Survivorship analyses

FIGURE FORMATTING STANDARDS
---------------------------

All plots are generated using a standardized publication-quality format:
- Okabe–Ito colour-blind-safe palette
- Publication-quality figure dimensions
- Bold scientific axis labels
- Black marker outlines
- Consistent trophic guild colours
- Draggable species labels (selected plots)
- Bootstrap confidence intervals (kernel regression analyses)
- High-resolution export suitable for journals and presentations

RECOMMENDED WORKFLOW
--------------------

1. Prepare and validate input datasets.
2. Run abundance and biomass summaries.
3. Generate species-level trajectories.
4. Evaluate size-spectrum coefficients and breakpoints.
5. Produce temporal trend analyses using kernel smoothing.
6. Assess catchability and survivorship scenarios.


