This is a self-taugh research project on predicting exoplanet habitability and water potential using data from the NASA Exoplanet Archive and the Earth Similarity Index (ESI).

I trained a machine learning model (Random Forest) to predict exoplanet habitability based on 4 essential features according to the ESI index: temperature, radius, orbital and mass, analyzed the importance of the features, checked for missing scenarios, and used Bayesian Uncertainty Estimation to evaluate prediction confidence.

**Dataset & Features:**

The dataset is obtained from the NASA Exoplanet Archive, specifically the Planetary Systems Composite Table.

**Methodology:**

First, I cleaned the data in the downloaded Exoplanet file and ranked the 10 most habitable planets according to the ESI formula, then used scatterplots and heatmaps to visualize.

Based on the ESI score between 0.6 and 0.8, with labels of 1 (has water) and 0 (no water), I got the result that 2 planets showed signs of water. Usually, planets with ESI index from 0.8 to 1 are considered the most similar to Earth, supporting more life. But because Mars with ESI 0.7 also showed signs of water, I expanded the index to 0.6 and 0.7, but did not get different results.

Follow that, I did an experiment: remove each feature, check the missing features and the importance feature, from which there is conclusion that radius and mass are the two most important features to determine if a planet has life, and Random Forest can still make predictions. This shows the flexibility of Random Forest in still predicting despite missing information.

I visualize uncertainty in ESI predictions using a Bayesian approach, and realized that unlike a single-point prediction, Bayesian uncertainty gives a range of plausible ESI values, and helps in ranking exoplanets by confidence level, not just by mean ESI.

**References**:
  - NASA Exoplanet Archive: https://exoplanetarchive.ipac.caltech.edu
  - The Planetary Habitability Laboratory (PHL): https://phl.upr.edu/projects/earth-similarity-index-esi
  - Dirk Schulze-Makuch, Abel Méndez, Alberto G. Fairén, Philip von Paris, Carol Turse, Grayson Boyer, Alfonso F. Davila, Marina Resendes de Sousa António, David Catling, and Louis N. Irwin (2011). A Two-Tiered Approach to Assessing the Habitability of Exoplanets. _Astrobiology_ vol.10 no.11. **DOI: 10.1089/ast.2010.0592**.
