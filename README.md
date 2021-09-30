# Estimating Ocean Surface Currents With Machine Learning

### Citing this Code

[![DOI](https://zenodo.org/badge/233659202.svg)](https://zenodo.org/badge/latestdoi/233659202)

Please cite this code as

> Sinha, Anirban, & Abernathey, Ryan. (2021). _Code for Estimating Ocean Surface Currents With Machine Learning (1.0.0)_. Zenodo. https://doi.org/10.5281/zenodo.5541507


### The Paper

This code accompanies the following paper:

> Sinha, Anirban & Abernathey, Ryan. (2021): _Estimating Ocean Surface Currents With Machine Learning_.
Frontiers in Marine Science vol. 8, p. 612.

**URL**: <https://www.frontiersin.org/article/10.3389/fmars.2021.672477>
	
**DOI**: `10.3389/fmars.2021.672477`

### License

This code is distributed under the [MIT License](LICENSE).

### Abstract

Global surface currents are usually inferred from directly observed quantities like sea-surface height, wind stress by applying diagnostic balance relations (like geostrophy and Ekman flow), which provide a good approximation of the dynamics of slow, large-scale currents at large scales and low Rossby numbers. However, newer generation satellite altimeters (like the upcoming SWOT mission) will capture more of the high wavenumber variability associated with the unbalanced components, but the low temporal sampling can potentially lead to aliasing. Applying these balances directly may lead to an incorrect un-physical estimate of the surface flow. In this study we explore Machine Learning (ML) algorithms as an alternate route to infer surface currents from satellite observable quantities. We train our ML models with SSH, SST, and wind stress from available primitive equation ocean GCM simulation outputs as the inputs and make predictions of surface currents (u,v), which are then compared against the true GCM output. As a baseline example, we demonstrate that a linear regression model is ineffective at predicting velocities accurately beyond localized regions. In comparison, a relatively simple neural network (NN) can predict surface currents accurately over most of the global ocean, with lower mean squared errors than geostrophy + Ekman. Using a local stencil of neighboring grid points as additional input features, we can train the deep learning models to effectively “learn” spatial gradients and the physics of surface currents. By passing the stenciled variables through convolutional filters we can help the model learn spatial gradients much faster. Various training strategies are explored using systematic feature hold out and multiple combinations of point and stenciled input data fed through convolutional filters (2D/3D), to understand the effect of each input feature on the NN's ability to accurately represent surface flow. A model sensitivity analysis reveals that besides SSH, geographic information in some form is an essential ingredient required for making accurate predictions of surface currents with deep learning models.
