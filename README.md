<h2 align='center'> Project Description </h2>
<h4 align='center'><img src="https://github.com/alanbui2808/RSNA-MICCAI_Brain_Tumor_Radiogenomic_Classification/assets/47062764/49c990e5-2cb6-4f2e-8866-baa6e1d03117" alt="my banner"> </h4>

Brain cancer, especially glioblastoma, has a grim prognosis, and current treatment with alkylating chemotherapy varies in effectiveness. To assess treatment suitability, invasive surgery is required to test MGMT promoter methylation. Streamlining this process, such as using MRI scans, could save time, benefiting patients and enhancing early treatment outcomes. In this project, we chose to use FLAIR. Among the four scan types, FLAIR exhibited the longest repetition time (TR) and time to echo (TE), resulting in enhanced accentuation of abnormalities, particularly tumors. This led us to choose FLAIR scans as the optimal choice for tumor analysis. We choose to train a 3D CNN due to the special structure of the dataset. Each data point consists of a series of slice over the brain of a particular patient. The dataset goes through pre-processing steps such as padding, augmentation (rotation) and min-max normalization before the training step. 
![img1](https://github.com/alanbui2808/RSNA-MICCAI_Brain_Tumor_Radiogenomic_Classification/assets/47062764/039247dc-a7f0-4313-9550-03f24a099d73)

![img2](https://github.com/alanbui2808/RSNA-MICCAI_Brain_Tumor_Radiogenomic_Classification/assets/47062764/9c836d82-e5f7-42de-ab9d-120fa32ce4bd)

![img3](https://github.com/alanbui2808/RSNA-MICCAI_Brain_Tumor_Radiogenomic_Classification/assets/47062764/e5418ea2-574b-420c-9eed-19777a128561)

The label is either 0 or 1 denoting the presence of MGMT and thus metrics used are accuracy and AUC.







### Table of Contents

1. [Dataset Information](#dataset_info)
2. [Dependencies](#depend)
3. [Files](#files)
4. [How to Run](#run)

### Dataset Information<a name="dataset_info"></a>
We will be using a real-world dataset collected and authorized by the RSNA (Radiological Society of North America) and the MICCAI Society (Medical Image Computing and Computer Assisted Intervention Society) released in 2021. The dataset contains 585 cases (patients) and their mpMRI brain scans divided in 4 categories (subfolders). The 4 types of mpMRI scans include: FLAIR, T1w, T1Gd and T2. Correspondingly, the label of each case is MGMT_value - 0: unmethylated and 1: methylated. The distribution of the MGMT_value is ∼53% for 0 and ∼47% for 1. The size of the dataset is 132GB.

### Dependencies<a name="depend"></a>
1. Pydicom: Reading DICOM Files

    `!pip install pydicom`
  
2. Numpy: Perform several mathematical evaluations in the preprocessing of the datasets
   
    `pip install numpy  `

4. Pandas: Loading/Processing/Storing of the different datasets

    `pip install pandas `
  
5. Matplotlib: Plotting of the training curves.

    `pip install matplotlib`
  
6. Tensor: Model

    `pip install tensorflow={desired version}`
  
### Files<a name="files"></a>
* `saved_models`: Models saved at each checkpoint where they show improvements from previous checkpoints (epochs) during training.
* `figures`: Curves, etc.
* `training_histories`: Loss, accuracy and auc during training.
* `2D_saved_models`: Experimented 2D CNNs.

### How to Run<a name="run"></a>
* The notebook is pretty straightforward, you are recommended to run on Google Colab. However uploading the dataset can be a hassle :)
  
