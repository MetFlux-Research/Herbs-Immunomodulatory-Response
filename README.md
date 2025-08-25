# Herbs-Immunomodulatory-Response 

# Overview
This MATLAB code is designed to model and predict rates of change in biomarkers associated with immune processes (adaptive and innate immunity) following interventions with specific ingredients (e.g., herbs, bioactive compounds, or dietary components).  
The pipeline integrates data from multiple published randomized controlled trials (RCTs) for each ingredient/component, computes the median rate of biomarker change, and uses this to estimate post-intervention biomarker values under different scenarios.  
The framework also supports multi-ingredient formulations, varying dosages, and different intervention durations to simulate potential combined or dose-dependent effects.  

# Key Features
- Data-driven modelling: Uses biomarker changes reported in multiple peer-reviewed articles.  
- Robust estimation: Median rate of change across studies is used to minimize bias from outliers.  
- Flexible prediction: Post-intervention biomarker values are estimated using three scenarios:  
  1. Mean + SD  
  2. Mean  
  3. Mean – SD  
  (as described in the methodology of the reference article).  
- Rate calculation: Compute the percentage rate of change for each study  
- Compositional extension: Allows prediction of effects for different ingredient combinations and dosages.  
- Time-dependent modelling: Supports predictions at different intervention durations.  

# Input Data
The required input data comes from randomized controlled trials (RCTs) and should be entered in the provided Excel sheet.  

**Excel Format:** Refer sample `data_code_21AUG.xlsx`  

# Output
- Tables/Excel files with predicted biomarker values for each scenario.  
- Plots (if enabled) showing trajectory of biomarker changes over duration, dosage, or composition.  

# Requirements
- MATLAB R2020a or later  
- Excel input file (template provided)  
- MATLAB Toolboxes:  
  - Statistics and Machine Learning Toolbox  
  - Curve Fitting Toolbox (optional, for dose–response simulations)  

# Usage
1. Open MATLAB.  
2. Place the Excel input file (`sample data_code_21AUG.xlsx`) in the project folder.  
3. Run the main script:  
4. `Search_engine_manuscript_code.m`  
5. Review output tables and figures generated in the `/results/` folder.  

# Notes
- Ensure the biomarkers are standardized to the same units across studies.  
- The additive assumption for multi-ingredient effects can be adjusted in the code if interaction models are preferred.  
- Duration scaling is approximate and based on proportional effects unless otherwise specified in literature.  

# Citation
If you use this code in your research, please cite the corresponding article where the methodology was originally described.  

