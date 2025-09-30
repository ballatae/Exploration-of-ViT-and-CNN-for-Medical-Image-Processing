# Data Card: Blood Cell Images for Cancer Detection

**Dataset Title:** Blood Cell images for Cancer detection  
**Source:** [Kaggle – Sumith Singh](https://www.kaggle.com/datasets/sumithsingh/blood-cell-images-for-cancer-detection)  
**Author / Uploader:** Sumith Singh Kothwal  
**Last Updated:** ~8 months ago 
**Dataset Size:** ~127 MB  
**Files:** ~5000 images (microscopic blood cell images)  
**License:** *[Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)*  

---

## Dataset Overview
This dataset contains microscopic images of blood smear samples for cancer detection tasks. It is designed for **computer vision** and **medical image analysis**, particularly classification of blood cells relevant to leukemia and other cancers.

---

## Data Characteristics
- **Type:** Microscopic images of blood cells  
- **Format:** Standard image files (e.g., JPEG / PNG)  
- **Channels:** RGB (color images)  
- **Classes / Labels:** Includes several blood cell types such as:  
  - Myeloblasts (indicative of acute leukemia)  
  - Erythroblasts  
  - Monocytes  
  - *(Additional classes may be present; verify in dataset folders)*  
- **Intended Task:** Classification (blood cell type / cancer detection)  
- **Splits:** No predefined train/validation/test splits provided – users must define their own.  

---

## Uses
- Training machine learning models for cancer cell detection  
- Research in **hematology image analysis**  
- Educational use for computer vision in medical datasets  

---

## Strengths
- Provides real microscopic images of blood smear slides  
- Multiple cell types relevant to **leukemia detection**  
- Useful for building and benchmarking CNN / ViT-based models  

---

## Limitations & Risks
- **Limited metadata**: No information on imaging equipment, staining, or patient demographics  
- **Potential class imbalance**: Distribution across cell types may not be uniform  
- **Generalization risk**: Models trained solely on this dataset may not transfer well to other labs or conditions  
- **No segmentation masks**: Dataset is classification-only  

---

## Ethical Considerations
- Images appear anonymized with no patient-level identifiers.  
- Must not be used for direct clinical diagnosis without validation and regulatory approval.  
- Researchers should ensure proper handling and disclosure of dataset limitations when reporting results.  

---

## Recommendations for Use
- Apply **data augmentation** (rotation, brightness, contrast) to mitigate small dataset size  
- Perform **cross-validation** or hold-out test sets  
- Consider combining with other blood cell image datasets for robustness  
- Document class distribution before training  

---

## Citation

> Sumith Singh, *Blood Cell images for Cancer detection*, Kaggle dataset.  
> Available at: [https://www.kaggle.com/datasets/sumithsingh/blood-cell-images-for-cancer-detection](https://www.kaggle.com/datasets/sumithsingh/blood-cell-images-for-cancer-detection)  

---
