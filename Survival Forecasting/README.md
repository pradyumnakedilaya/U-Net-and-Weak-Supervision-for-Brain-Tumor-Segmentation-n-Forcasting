In this project, we will investigate weakly supervised methods for analyzing pathology images to predict two-year survival of patients diagnosed with brain tumors.


This project addressed the prediction of patient clinical outcomes from whole-slide pathology images (WSIs). Predicting patient-level labels like diagnosis or clinical outcome is difficult as WSIs are very large, with each image typically containing several billion pixels. Weakly-supervised and multi-instance learning are popular approaches to addressing this problem. These methods treat a WSI as a collection of tiles or instances and use various mechanisms to identify the most salient instances and aggregate their contributions for patient-level prediction.
The aim of this project is to predict the two-year survival of diffuse glioma brain tumors using whole-slide images from the Lower Grade Glioma (LGG) and Glioblastoma (GBM) projects of The Cancer Genome Atlas (TCGA). Diffuse gliomas are a hetergeneous disease encompassing tumors with widely varying molecular characteristics, histologic patterns, and clinical outcomes. Multiple studies have examined the relationship between histology and clinical outcomes using machine learning approaches. In this project, we will perform binary classification of those subjects who survive beyond two years, and those who expire prior to two years. Patients who are right-censored at less than 2 years are not present in the dataset.

### Data:
The data archive contains train, validation, and test folders containing images from 417, 53, and 53 patients respectively. Each patient is represented by a single TensorFlow record (.tfr) file that contains extracted features, clinical outcome labels, and other patient and image metadata. Features were extracted by tiling slides using 224×224 pixel non-overlapping tiles at 100X magnification. An EfficientNetV2S model was used to extract 1280-dimensional features from each tile. A label value of 1 indicates survival beyond two years.

The data can be downloaded here: [tcga glioma.zip](https://drive.google.com/file/d/19hx9ryFiWOkdg_n3hKEm10F_uwibD5ct/view).