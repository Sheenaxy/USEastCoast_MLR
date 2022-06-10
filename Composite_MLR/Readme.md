# Composite mutiple linear regression (MLR) model
 This folder contains the MLR model of carboante parameters (DIC, pH, and Omega) based on GOMECC2 cruise data in the MAB and the SAB region.
 This is the model results published in [DOI] (link to be updated)
 
 # User instruciton
 1.To load this MATLAB mld, please use function 'loadLearnerForCoder'.
 
 2. Load your own data to the Workspace
 
 3. Centrailize your own Temp, Sal and Oxy data by substracting the mean hydrographic data (Tm, Sm and Om);
 
 4. Use function 'predict' to apply the centrailized data into the MLR model
