# Learned 1D advection solver

## Introduction
This repository is a supplementary to the manuscript "**Learned 1-D advection solver to accelerate air quality modeling** (https://arxiv.org/abs/2211.03906)." Basically this repository contains Julia codes in Jupyter Notebook to emulate L94 advection scheme in 1-D.

The aims of this project include:

* Develop a surrogate scheme of passive scalar advection with spatial and temporal coarse-graining
* Evaluate the performance of surrogate schemes in accuracy and computational speed
* Test the generalization ability of the learned scheme in the regime out of training dataset

## Scripts
1. Van_Leer_Type_Scheme_(L94).ipynb - This notebook has function to integrate the passive scalar advection with given initial condition and wind velocity field.

2. Learning_advection.ipynb - This notebook has codes to build (or load) CNN model and train the model.

3. Statistical_indices_calculation.ipynb - This notebook has codes to bring in the model output and calculate statistical indices including MAE, RMSE, r<sup>2</sup>.

4. Generalization_test_29N_Latitude.ipynb - This notebook has codes to test the generalization ability of learned models in 29N latitude.

5. Generalization_test_45N_Latitude.ipynb - This notebook has codes to test the generalization ability of learned models in 45N latitude.

6. Generalization_test_3_times_longer_integration.ipynb - This notebook has codes to test the stability of the learned schemes during 30 days.

7. Generalization_test_Dirac-delta_initial_condition.ipynb - This notebook has codes to test the generalization ability of the learned scheme with Dirac-delta type initial condition.

8. Generalization_test_Gaussian_shape_initial_condition.ipynb - This notebook has codes to test the generalization ability of the learned scheme with Gaussian distribution shape initial condition.

## Data
1. models_and_outputs - This directory has the learned models and outputs. Those models and outputs are labelled with the training epochs and the spatio-temporal coarsening factor.

2. Velocity - This directory containes the wind velocity field used in this study.

## Acknowledgment
This work is financially supported by the Early Career Faculty grant of National Aeronautics and Space Administration (grant no. 80NSSC21K1813). MP is supported by the Carver Fellowship and Illinois Distinguished Fellowship.
