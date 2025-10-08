# Data Card: Acute Lymphoblastic Leukemia (ALL) Image Dataset — Mehradaria

**Dataset Title:** Acute Lymphoblastic Leukemia (ALL) Image Dataset  
**Source / URL:** [Kaggle – mehradaria / leukemia](https://www.kaggle.com/datasets/mehradaria/leukemia) :contentReference[oaicite:0]{index=0}  
**Creator / Uploader:** Mehradaria :contentReference[oaicite:1]{index=1}  
**Last Updated / Version Info:** 4 years ago 
**License:** *[Database: Open Database, Contents: © Original Authors](http://opendatacommons.org/licenses/odbl/1.0/)*   

---

## Dataset Overview  
This dataset contains peripheral blood smear (PBS) images from patients suspected of having ALL (Acute Lymphoblastic Leukemia). It is intended for classification / diagnostic aid in hematology. :contentReference[oaicite:2]{index=2}  

---

## Data Characteristics  

- **Total images:** 3,256 images :contentReference[oaicite:3]{index=3}  
- **Number of patients / sources:** 89 suspected ALL patients :contentReference[oaicite:4]{index=4}  
- **Classes / Labels:**  
  - Class 0: Benign (non-ALL) — 504 images :contentReference[oaicite:5]{index=5}  
  - Class 1: Early malignant — 985 images :contentReference[oaicite:6]{index=6}  
  - Class 2: Pre malignant — 963 images :contentReference[oaicite:7]{index=7}  
  - Class 3: Pro malignant — 804 images :contentReference[oaicite:8]{index=8}  
- **Image format / modality:** PBS (microscopic) images; format: JPG (from description) :contentReference[oaicite:9]{index=9}  
- **Resolution / channels:** (Not explicitly documented; likely RGB color images)  
- **Preprocessing / augmentation in published work:** Data augmentation (horizontal / vertical flips, 90° rotation) to balance classes to 1,500 images each in some studies :contentReference[oaicite:10]{index=10}  

---

## Tasks / Use Cases  

- Multiclass classification of blood cell images into benign / early / pre / pro ALL stages  
- Training / benchmarking deep networks for leukemia detection  
- Comparative studies / method development in medical image classification  

---

## Strengths & Benefits  

- Relatively large dataset (3,256 images) with multiclass labels  
- Captures more granular stages of ALL (beyond just binary)  
- Widely used in literature for ALL classification tasks :contentReference[oaicite:11]{index=11}  

---

## Limitations & Risks  

- Lack of metadata: imaging device, staining protocol, patient demographics not documented  
- Class imbalance (prior to augmentation)  
- No segmentation masks / location annotations  
- Variability in imaging conditions may reduce generalization  

---

## Ethical / Privacy Considerations  

- Images are anonymized (no patient identifiers)  
- Use for research only; models should not be used for clinical diagnosis without validation  
- If combining with additional clinical data (if exists), ensure anonymization and consent  

---

## Recommendations / Best Practices  

- Use augmentation carefully (but do document it)  
- Use stratified splits to preserve class proportions  
- Report metrics per class (precision, recall, F1)  
- Possibly use cross-validation or hold-out test split  
- Combine with other datasets to improve generalization  

---

## Citation  
> Mehradaria, *Acute Lymphoblastic Leukemia (ALL) image dataset*, Kaggle.  
> Available at: https://www.kaggle.com/datasets/mehradaria/leukemia :contentReference[oaicite:12]{index=12}  

---

