**This is a self-learning research project on predicting exoplanet habitability and water potential using data from NASA's Exoplanet Archive and the Earth Similarity Index (ESI).**

*Main goals and methods of the project:*

- Find and visualize the 10 exoplanets with the highest ESI (>0.8), which means they are most likely to support life and most similar to Earth. However, the 2 scatterplot and heatmap tables visualize the entire dataset, not just the 10 planets with the highest index, to determine the overall trend of the planets, so the dataset is not biased and convenient for training the model.

- I trained Random Forest to determine the water potential of planets based on ESI and 4 features: temperature, radius, mass and orbital period, and analyzed the importance of the factors. The main goal was to find the most important factor that strongly correlates with ESI, which would help improve the method of assessing exoplanet habitability. Based on ESI scores ranging from 0.6 to 0.8, labeled 1 (has water) and 0 (no water), I got 2 planets that showed signs of water. Typically, planets with ESI scores between 0.8 and 1 are considered the most Earth-like, supporting more life. But since Mars with ESI 0.7 also showed signs of water, I extended the index to 0.6 and 0.7, but did not get different results. Then, I conducted an experiment to remove each feature individually and assess its impact on ESI prediction, with the goal is to identify which features have the most significant influence on determining ESI and whether the model can still make accurate predictions when certain features are missing. RF still predicts water even when features are missing, which shows the flexibility of RF in analysis and prediction.

- In addition, the Bayesian Uncertainty Estimation is also used to check the uncertainty in ESI prediction, helping to evaluate planets based not only on the average ESI value but also on its possible range of variation.

*In general, there are a few reasons why I use Machine Learning to predict water probability:*

- This experiment is not to recalculate ESI, but to gain a deeper understanding of which factors are most important.

- The ESI formula cannot explain the importance of each factor by itself, and differential calculus is not enough to analyze a non-linear system like this.

- Random Forest helps to measure the influence of each feature in reality, instead of just relying on the formula.
  
- Bayesian Estimation helps assess the level of uncertainty in ESI prediction, which traditional formulas cannot do.

**References**:
  - NASA Exoplanet Archive: https://exoplanetarchive.ipac.caltech.edu
  - The Planetary Habitability Laboratory (PHL): https://phl.upr.edu/projects/earth-similarity-index-esi
  - Dirk Schulze-Makuch, Abel Méndez, Alberto G. Fairén, Philip von Paris, Carol Turse, Grayson Boyer, Alfonso F. Davila, Marina Resendes de Sousa António, David Catling, and Louis N. Irwin (2011). A Two-Tiered Approach to Assessing the Habitability of Exoplanets. _Astrobiology_ vol.10 no.11. **DOI: 10.1089/ast.2010.0592**.
