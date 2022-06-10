# Composite multiple linear regression (MLR) model
 This folder contains the MLR model of carboante parameters (DIC, pH, and Omega) based on GOMECC2 cruise data in the MAB and the SAB region.
 This is the model results published in [DOI] (link to be updated)
 
 # User instrucition
 1.To load this MATLAB built-in function, please use function 'loadLearnerForCoder'.
 
 2. Load your own data to the Workspace
 
 3. Centralize your own Temp, Sal and Oxy data by substracting the mean hydrographic data (Tm, Sm and Om);
 
 4. Use built-in function 'predict' to apply the centralized data into the MLR model

# Example code
```Matlab
%Eample
%Load your own data (Temperature, Salinity and Oxygen concentration)
%Data limitation： below mixed layer(20m) and above 1000m
Rawdata = load('ExampleTSO.mat');
%Centralized data
load('mean_MAB.mat');
Tc = ExampleTSO.T - mean_MAB.Tm;
Sc = ExampleTSO.S - mean_MAB.Sm;
Oc = ExampleTSO.O - mean_MAB.Om;
X = [Tc, Sc, Oc]
%Load MLR model for predictions
%MAB DIC as an example
mdl_DIC_MAB = loadLearnerForCoder('DIC_MAB.mat');
%Predict DIC
Est_DIC_MAB = predict(mdl_DIC_MAB,X);
```
