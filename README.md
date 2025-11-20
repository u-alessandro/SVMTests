# RobustnessSVM

Cross-validation and noise sensitivity analysis applied to Support Vector Machine (SVM) models used to classify between ASE and lasing phenomena in optical microcavities.

A Radial Basis Function SVM was trained using a dataset of 41 cylindrical polymeric microcavities, characterized through both geometrical and performance parameters (FWHM, Th, λ, Intensity, S1, S2, S1/S2, D, H, D/H, Eccentricity). The data were scaled and projected onto two principal components using PCA. Two feature subsets were selected:

- Subset A: The best-performing configuration including FWHM as a key parameter (S1/S2, λ, H, D/H, FWHM).
- Subset B: The best-performing configuration excluding FWHM (S1, S2, S1/S2, D, D/H, Th).

To test the robustness of the models, cross-validation and noise sensitivity analyses were performed. The changes in decision boundaries under different configurations are presented in this repository:

1. Cross-Validation: 5-fold and 10-fold configurations were used for both subsets. The resulting decision boundaries are shown in animated GIFs, where the actual training vectors for each fold are highlighted with an external black circle. File names follow the format:  
   "Cross-Validation *A/B* *5/10* Folds.gif"

2. Noise Sensitivity:  
   - For Subset A, increasing levels of Gaussian noise (5% to 75%) were applied to the FWHM feature only.  
   - For Subset B, the same noise levels were applied simultaneously to all features.  

   The resulting changes in decision boundaries and performance metrics are shown in GIFs titled:  
   "Noise in *FWHM/all features* Subset *A/B*.gif"
