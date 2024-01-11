# BET_BatterySizing_CellChemistry

This repository provides the open-source code to the following Paper:

Spoilt for Choice: User-Centric Choice of Battery Size and Chemistry for Battery-Electric Long-Haul Trucks

DOI: https://doi.org/10.1016/j.etran.2023.100253

Following contributions of the mentioned paper, are provided by this repo:

- Comprehensive analysis of the feasibility of varying battery capacities for different use cases
This paper presents the first comprehensive analysis, which battery size is feasible for a long-haul BET considering charging power, payload, cell-individual vehicle restrictions as well as degradation effects.

- Novel investigation on the cost-effectiveness of oversizing the battery
We analyze the trade-off between rising investment costs and less need to replace the battery during lifetime, caused by the degradation of the cell. We model the aging effects based on cell chemistry as well as available charging power and transported payload.
	
- Detailed analysis of the cost-optimal and use case individual choice of cell chemistry
In-depth comparison of the two mentioned cell chemistries, regarding cost-effectiveness. We significantly enhance the state of the art, considering detailed aging modeling and the dependency on available charging infrastructure. We additionally conduct a sensitivity analysis in order to make the influence of our assumptions as transparent as possible.

## Prerequisites
To run the code, you'll need the following python packages:

numpy
scipy
matplotlib
tqdm
multiprocessing
time
pandas

  
## Running the Model/Code
The results and all figures are generated by executing the file main.py. 

The script is divided in 5 parts:
  1. Parameter Initialization
     
     	In this part all relevant parameters are initialized for the following modules
     
  2. Energy Consumtion Calculation
     
     	Here the energy consumption dependend on the gross vehicle weight is calculated. In order to save execution time there is the option to use previous calculated 	results, which can be controlled via the variable "Energy_Calculation_Recalculate".
     
  3. Scenario Calculation (inkl. Thermo-Electric + Aging Coefficient Calculation)
     
     	In this module the thermo-electric and aging results are generated for every defined use case. An option is implemented to use multiprocessing to reduce the 		calculation time for a high number of use cases. This can be controled via the variable "multiprocessing". Here the option to use precalculated results can be 		controlled via the variable "Variation_Recalculate".
     
  4. TCO Calculation
     
     	In this module the TCO for each use case is calculated. Like in the previous modules, also a option exists to use previously calculated results instead of running 	the whole code in every execution. This can be controlled via the variable "TCO_Recalculate". A sensitivity analysis is also included in this module.

5. Plots
   	In this module the results, presented in the paper are created and saved in the corresponding folders.


  
## Contributing and Support
  
If you would like to contribute to this work or have any feedback, please do not hesitate to contact me at jakob.js.schneider@tum.de
  

## Authors
Jakob Schneider, Olaf Teichert, Maximilian Zähringer, Korbinian Götz, Markus Lienkamp
  
## License
