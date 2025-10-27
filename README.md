# Secure_Ultrasound_public

**Anatomical Plane Classification for Fetal Head Ultrasound - Addressing Class Imbalance with Deep Learning**

This repository contains the datasets, results and model predictions associated with our work:  
**“Anatomical Plane Classification for Fetal Head Ultrasound: Addressing Class Imbalance with Deep Learning”**,  
accepted for presentation at the **International Biomedical Instrumentation and Technology Conference (IBITeC 2025)**.

 [Conference Website](https://ibitec.uii.ac.id/#about)

---

## Project Overview

This project focuses on the automated classification of fetal head anatomical planes in ultrasound images using deep learning.  
The study evaluates multiple convolutional neural network architectures trained with transfer learning and a weighted loss function to address severe class imbalance in clinical data.

### Key Objectives
- Classify ultrasound images as **Head vs. Not Head**.  
- Further classify head images into **four anatomical categories**:  
  - **Transventricular (TV)**  
  - **Transthalamic (TT)**  
  - **Transcerebellar (TC)**  
  - **Other (Head)**

### Models Used
- VGG16  
- MobileNet  
- MobileNetV2  
- EfficientNetB0  
- EfficientNetB5  

All models were trained with a learning rate of `0.0001`, `0.001`, `0.01`.

---

##  Folders Description

### 1. `Image Dataset for results/Phantom`
Contains the **test dataset** used for evaluation.

### 2. `Head vs Not Head Prediction`
Includes Excel (`.xlsx`) files with **Head / Not Head** predictions for all five models  
using a learning rate of `0.0001`.

### 3. `Brain Class Prediction`
Includes Excel (`.xlsx`) files with **multi-class predictions** among  
`Transcerebellar`, `Transthalamic`, `Transventricular` and `Other (Head)`  
for all five models using a learning rate of `0.0001`.

### 4. `Loss and Acc`
Includes all the confusion matrix, loss and accuracy graphs for all the 5 models with 3 different learning rates = [0.0001, 0.001, 0.01].

### 5. `Scan2.mp4`
Real time implementation video on the best model (Model 1). 


---

##  Citation

If you use this results in your research, please cite (will be updated once published):

> S. Pravallika and M. Arora,  
> “Anatomical Plane Classification for Fetal Head Ultrasound: Addressing Class Imbalance with Deep Learning,”  
> *Proceedings of the International Biomedical Instrumentation and Technology Conference (IBITeC 2025)*.

---

##  Contact

For questions or collaborations, please contact:  
**Pravallika Saladi**  
UTSAAH Lab, Department of Design and Manufacturing,  
Indian Institute of Science (IISc), Bangalore, India.
