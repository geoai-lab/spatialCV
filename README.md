# Spatial cross-validation for GeoAI

### Overall description
Cross-validation (CV) has been widely used in GeoAI research to evaluate the performance of machine learning models. Often, a labeled data set is randomly split into training and validation data, and a machine learning model is trained on the training data and then evaluated on the validation data in an iterative manner. Such a random CV approach could lead to an overestimate of model performance on geographic data, due to the existence of spatial autocorrelation. Random CV can generate many training and validation data instances that are spatially close, and a model trained on such training data can be considered as having already “peeked” into the nearby validation data, given their spatial closeness and likely attribute similarity. Spatial CV can help address this issue by splitting the data spatially rather than randomly, thereby increasing the independence between the training and validation data. While a number of spatial CV methods have been developed, they are scattered in the literature across multiple disciplines, including ecology, remote sensing, GIScience, and computer science. This chapter discusses four main spatial CV methods identified from the multidisciplinary literature, and uses two examples based on real-world data to demonstrate these methods in comparison with random CV.

This repository contains the code and data for implementing random CV approach and four spatial CV approaches (i.e., clustering-based spatial CV, grid-based spatial CV, geo-attribute-based spatial CV, and spatial leave-one-out CV).


<br />
<br />

<p align="center">
<img align="center" src="fig/interpolation&extrapolation.png" width="600" />
<br />
Figure 1. An illustration of two common situations under which machine learning models are applied to geographic data: (a) within-area prediction or interpolation; (b) between-area prediction or extrapolation.
</p>

<br />
<br />
<p align="center">
<img align="center" src="fig/Chicago_splitting.png" width="600" />
<br />
Figure 2. Data splitting results for CBGs in Chicago: (a) random CV; (b) clustering-based spatial CV; (c) grid-based spatial CV; (d) geo-attribute-based spatial CV; (e) spatial leave-one-out CV.
</p>
<br />

<br />
<br />
<p align="center">
<img align="center" src="fig/NYC_splitting.png" width="600" />
<br />
Figure 3. Data splitting results for census tracts in NYC: (a) random CV; (b) clustering-based spatial CV; (c) grid-based spatial CV; (d) geo-attribute-based spatial CV; (e) spatial leave-one-out CV.
</p>
<br />



### Repository organization

* The folder "Code" contains the code used for implementing the two examples to demonstrate the random CV approach and four spatial CV approaches.
* The folder "Data" contains the experimental data for the two examples including domestic violence data, obesity rate data, and shapefile data used for spatial components.
