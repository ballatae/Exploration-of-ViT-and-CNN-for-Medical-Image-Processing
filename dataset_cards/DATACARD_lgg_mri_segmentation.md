# Data Card: LGG MRI Segmentation (Brain MRI Tumor / FLAIR Abnormality Segmentation)

**Dataset Title:** LGG MRI Segmentation  
**Source / URL:** [Kaggle – mateuszbuda / LGG MRI Segmentation](https://www.kaggle.com/datasets/mateuszbuda/lgg-mri-segmentation) :contentReference[oaicite:0]{index=0}  
**Creator / Contributors:** Mateusz Buda (and collaborators) :contentReference[oaicite:1]{index=1}  
**Associated Publication / Use:**  
“Association of genomic subtypes of lower-grade gliomas with shape features automatically extracted by a deep learning algorithm” (Buda, Saha, Mazurowski) :contentReference[oaicite:2]{index=2}  
**Last Updated / Version Info:** 6 years ago
**License:** *[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)*  

---

## Overview  
This dataset contains MRI scans (FLAIR modality) of lower-grade gliomas (LGG) along with **manual segmentation masks** of FLAIR abnormal regions (tumor / lesion). :contentReference[oaicite:3]{index=3}  
It is intended for medical image segmentation tasks (pixel-level segmentation).  

---

## Data Characteristics  

- **Modalities / Imaging Type:** Magnetic Resonance Imaging (MRI), FLAIR sequence (fluid-attenuated inversion recovery) :contentReference[oaicite:4]{index=4}  
- **Data Source / Patients:** Derived from The Cancer Imaging Archive (TCIA) / TCGA’s LGG collection; includes ~110 patients :contentReference[oaicite:5]{index=5}  
- **Number of images & masks:** ~7,858 image–mask pairs are used after pruning :contentReference[oaicite:6]{index=6}  
- **Image format, size, channels:** RGB (3 channels), 256×256 pixels for MRI images; masks are single-channel, same resolution :contentReference[oaicite:7]{index=7}  
- **Mask / Annotation:** Manual segmentation masks delineating abnormal FLAIR region (tumor / lesion) :contentReference[oaicite:8]{index=8}  
- **Preprocessing / Pruning:** Some MRI images with little information (e.g. blank images) were manually removed / pruned from original dataset to improve quality :contentReference[oaicite:9]{index=9}  

---

## Tasks / Use Cases  

- Semantic segmentation (pixel-level) of tumor / abnormal FLAIR regions  
- Training / benchmarking U-Net / CNN / deep models for medical segmentation  
- Radiogenomic studies: combining segmented shapes with genomic / clinical data (shape extraction) :contentReference[oaicite:10]{index=10}  
- Feature extraction of tumor morphology for further downstream tasks (e.g. subtype prediction)  

---

## Strengths & Benefits  

- Has pixel-level ground truth (segmentation masks)  
- Based on real clinical MRI data of LGG cases  
- Allows linking imaging phenotype and tumor morphology to genomic / clinical features (in published works) :contentReference[oaicite:11]{index=11}  
- Established baseline / code available (U-Net architectures, etc.) :contentReference[oaicite:12]{index=12}  

---

## Limitations & Risks  

- Lack of detailed metadata on imaging acquisition (scanner type, magnetic field strength, protocol)  
- The pruning / removal of some images may introduce selection bias 
- Class imbalance: region vs background dominance (very large non-tumor regions)  
- Generalization risk: models may not generalize to other MRI protocols / institutions  

---

## Ethical / Privacy Considerations  

- No personally identifiable patient data is included (only MRI scans and anonymized IDs)  
- Use for research only; not for direct clinical diagnosis  
- When combining with clinical / genomic metadata (if available), ensure consent / anonymization  

---

## Recommendations / Best Practices  

- Use data augmentation (flips, rotations, elastic deformation) to expand effective data  
- Use cross-validation across patients (not just slices) to avoid leakage  
- Normalize intensities / standardize preprocessing (skull-stripping, bias correction)  
- Report metrics like Dice coefficient, Intersection-over-Union (IoU), and boundary metrics  
- Consider fine-tuning / transfer learning from other MRI segmentation domains  

---

## Citation  
> Buda, Mateusz, Ashirbani Saha, Maciej A. Mazurowski, *“Association of genomic subtypes of lower-grade gliomas with shape features automatically extracted by a deep learning algorithm”*.  
> Dataset: LGG MRI Segmentation (Kaggle). Available at: https://www.kaggle.com/datasets/mateuszbuda/lgg-mri-segmentation :contentReference[oaicite:13]{index=13}  
> Also see: [GitHub – brain-segmentation-pytorch] (U-Net implementation) :contentReference[oaicite:14]{index=14}  
