This project uses exoplanet data from NASA's Exoplanet Archive to calculate the Earth Similarity Index (ESI), which ranks exoplanets based on how similar they are to Earth in size, temperature, and orbital properties.

By visualizing exoplanet characteristics with scatter plots and heat maps, the project aims to uncover patterns in the habitability index. Based on ESI scores greater than 8.0 and labeled 1 (with water) and 0 (without water), the project uses machine learning models (Random Forests) to predict whether an exoplanet has conditions that could support water - one of the key factors in determining habitability. Only two exoplanets were predicted to have signs of water.

**Data Set**: NASA Exoplanet Archive (CSV data containing exoplanet parameters)

**Tools**: 
  - Python: pandas, numpy, matplotlib, seaborn, scikit-learn
  - Google Colab for analysis and visualization

**Features**:
  - Compute Earth Similarity Index (ESI) to rank exoplanets
  - Visualize exoplanet properties using scatter plots & heatmaps
  - Apply Machine Learning (Random Forest) to predict potential water presence

**References**:
  - NASA Exoplanet Archive: https://exoplanetarchive.ipac.caltech.edu
  - The Planetary Habitability Laboratory (PHL): https://phl.upr.edu/projects/earth-similarity-index-esi
  - Dirk Schulze-Makuch, Abel Méndez, Alberto G. Fairén, Philip von Paris, Carol Turse, Grayson Boyer, Alfonso F. Davila, Marina Resendes de Sousa António, David Catling, and Louis N. Irwin (2011). A Two-Tiered Approach to Assessing the Habitability of Exoplanets. _Astrobiology_ vol.10 no.11. **DOI: 10.1089/ast.2010.0592**.
