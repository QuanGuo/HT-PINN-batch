# HT-PINN-batch-training: Hydraulic Tomography Physics-Informed Neural Network with batch training
Author: Quan G

## About this notebook

This notebook applies PINN to hydraulic tomography inverse modeling to estimate spatially distributed hydraulic conductivity (inverse problem) as well as approximating relative hydraulic heads in pumping tests (forward problem).

Please note this work:
* Assumes the reader is comfortable with Python, especially, python notebook and pytorch.
* Google Cloud is recommended as the computing platform.

## Data

**heads/heads_pump<id>**: Hydraulic heads under each pumping test (solved with FEM)
   
**logK_field**: natural log hydraulic conductivity field (lnK)
   
**alpha_vector**: hidden random variables used to generated logK field with PCA realization generation method
   
**K_measure_id_61**: idx of direct measurement on hydraulic conductivity on domain mesh
   
**pump_well_id_25**: idx of pumping wells on domain mesh
   
 
## Model Training (model_coeff)
   
recommended hyper-parameters are saved in **hyper_parameters.txt**
   
A well trained HT-PINN are saved as:
    inverse model: **inverse.pth**
    forward models:
        $NN^{1}$ at pump well 1: **forward_0.pth**
        $NN^{5}$ at pump well 5: **forward_4.pth**
        $NN^{13}$ at pump well 13: **forward_12.pth**
        $NN^{21}$ at pump well 21: **forward_20.pth**
        $NN^{25}$ at pump well 25: **forward_24.pth**
   
   
## How to use

1) Clone.

2) Open the notebook: **HT_PINN_batch_training_example.ipynb**.
  
3) Tune hyper-parameters.

4) Train model and save results.

## Citation Format
