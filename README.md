# MICCAI-2025-ToothFairy3-Task-1

## Environments and Requirements:
### 1. nnUNet Configuration
Install nnUNetv2 as below.  
You should meet the requirements of nnUNetv2, our method does not need any additional requirements.  
For more details, please refer to https://github.com/MIC-DKFZ/nnUNet  

```
git clone https://github.com/MIC-DKFZ/nnUNet.git
cd nnUNet
pip install -e .
```
### 2. Dataset

Load ToothFairy3 Dataset from [https://ditto.ing.unimore.it/toothfairy2/](https://toothfairy3.grand-challenge.org/dataset/)

### 3. Preprocessing

Conduct automatic preprocessing using nnUNet.

```
nnUNetv2_plan_and_preprocess -d 301 --verify_dataset_integrity
```


### 4. Training

Train by nnUNetv2. 

Run script:

```
nnUNetv2_train 301 3d_fullres all -tr nnUNetTrainerNoDA
```


### 4. Inference

Train by nnUNetv2. 

Run script:

```
python test_3D.py
```
