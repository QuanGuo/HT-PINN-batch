# HT-PINN-batch-training: Hydraulic Tomography Physics-Informed Neural Network with batch training
Author: Quan G

## About this notebook

This notebook applies PINN to hydraulic tomography inverse modeling to estimate spatially distributed hydraulic conductivity (inverse problem) as well as approximating relative hydraulic heads in pumping tests (forward problem).

Please note this work:
* Assumes the reader is comfortable with Python, especially, python notebook and pytorch.
* Google Cloud is recommended as the computing platform.

## Data

**heads/heads_pump\<id\>.txt**: Hydraulic heads under each pumping test (solved with FEM)
   
**logK_field.txt**: natural log hydraulic transmissivity field (lnT)
   
**alpha_vector.txt**: hidden random variables used to generated logT field with PCA realization generation method
   
**K_measure_id_61.txt**: idx of direct measurement on hydraulic conductivity on domain mesh
   
**pump_well_id_25.txt**: idx of pumping wells on domain mesh
   
 
## Model Training (model_coeff)
   
Recommended hyper-parameters are saved in **hyper_parameters.txt**
   
A well-trained HT-PINN is saved as:
   
   * inverse model (TNN): **inverse.pth**
   
   * forward models at different pumping wells: **forward_\<id\>pth** 


## How to use

1) Clone.

2) Open the notebook: **HT_PINN_batch_training_example.ipynb**.
  
3) Tune hyper-parameters.

4) Train model and save results.

## Citation Format
