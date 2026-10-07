# TUT-BM-Dataset

## TUT-BM_version1: Bone Marrow Cytology Image Dataset

**TUT-BM_version1** is a curated image dataset of bone marrow cytology developed for research and educational applications in automated cell image analysis, computer vision, and deep learning.

The dataset was collected from bone marrow smear specimens and contains annotated images representing leukocyte, erythroid/RBC, and platelet-related cell categories. The primary benchmark focuses on **19 leukocyte categories**, while the broader annotated collection includes additional erythroid/RBC and platelet-related categories.

The dataset preserves the naturally occurring distribution of cell types and was not artificially balanced during dataset construction.

---

## Dataset Overview

| Property | Description |
|---|---|
| Dataset name | TUT-BM_version1 |
| Repository | TUT-BM-Dataset |
| Image modality | Bone marrow cytology microscopy |
| Number of patients | 80 |
| Initially acquired microscope images | 6,229 |
| Retained microscope images after quality control | 5,129 |
| Annotated single-cell images | 18,670 |
| Primary leukocyte images | 11,520 |
| Leukocyte benchmark classes | 19 |
| Platelet-related categories | 4 |
| Erythroid/RBC categories | 23 |
| Standardized single-cell image size | 250 × 250 pixels |
| Annotation method | Expert hematologist annotation |
| Dataset characteristics | Naturally imbalanced multi-class dataset |

---

## Dataset Scope

TUT-BM_version1 includes annotated bone marrow cell images covering three major groups.

### 1. Leukocyte Categories

The primary benchmark contains **19 leukocyte categories**:

1. Band
2. Basophil
3. Blast
4. Eosinophil
5. Lymphoblast
6. Lymphocyte
7. Metamyelocyte
8. Mitosis
9. Monoblast
10. Monocyte
11. Myeloblast
12. Myelocyte
13. PMN
14. Plasma Cell
15. Prolymphocyte
16. Promonocyte
17. Promyelocyte
18. Reactive Lymphocyte
19. Smudge Cell

These 19 categories constitute the main classification benchmark reported for TUT-BM_version1.

### 2. Platelet-related Categories

The broader annotated collection also contains four platelet-related categories:

1. Megakaryocyte
2. Platelet
3. PlateletAggregate
4. PlateletGiant

### 3. Erythroid/RBC Categories

The broader collection includes **23 erythroid/RBC categories**:

1. Acantocyte
2. BasophilicNormoblast
3. BurrCell
4. Dacrocyte
5. Elliptocyte
6. HelmetCell
7. HowellJolly
8. IrregularRBC
9. Keratocyte
10. Leptocyte
11. Macrocyte
12. MicroRBC
13. Normoblast
14. nRBC
15. Ovalocyte
16. Polychromasia
17. ProErythroblast
18. RBC
19. RouleauxFormation
20. Schistocyte
21. Somatocyte
22. Spherocyte
23. TargetCell

The broader annotated collection therefore covers **46 cell categories** across leukocyte, erythroid/RBC, and platelet-related groups.

---

## Data Collection

Bone marrow smear specimens were obtained from patients evaluated at hematology centers affiliated with **Tabriz University of Medical Sciences**, including **Shahid Ghazi Hematology Center** and **Behbood Specialty Hospital**.

Microscopic images were acquired using a **Bresser Science ADL 601F microscope** equipped with a **Canon EOS 1300D digital camera**.

The original images were acquired at a resolution of **5184 × 3456 pixels**. Standardized imaging conditions were maintained during image acquisition, including fixed focus, exposure, white balance, shutter speed, and ISO settings.

Bone marrow smears were prepared using **May-Grünwald-Giemsa (MGG) staining**.

---

## Image Processing and Annotation

A total of **6,229 microscopic images** were initially acquired. Following quality control, duplicate removal, and exclusion of unsuitable images or regions, **5,129 images** were retained.

Individual cells were annotated using bounding boxes. The annotated regions were cropped to generate single-cell images and standardized to **250 × 250 pixels**.

The resulting dataset contains **18,670 annotated single-cell images**, including leukocytes, erythroid/RBC cells, and platelet-related categories.

The primary leukocyte subset contains **11,520 images** distributed across 19 leukocyte categories.

The current leukocyte ZIP package contains **11,572 images**, including 11,520 images from the final 19-class benchmark and 52 images belonging to four excluded leukocyte categories.

The dataset was constructed from naturally occurring cell distributions, without artificial class balancing.

---

## Quality Control

Quality control was applied to improve the consistency and usability of the released images.

The quality-control process included removal of:

- blurred or unsuitable images;
- duplicate images;
- incorrect or irrelevant regions;
- images unsuitable for reliable cell annotation.

The annotated cells were reviewed by hematology experts as part of the annotation and quality-control process.

Further details regarding the annotation protocol and quality-control procedure are provided in the associated scientific publication and dataset documentation.

---

## Class Distribution

The leukocyte subset exhibits a **naturally imbalanced class distribution**, reflecting the unequal occurrence of different cell types in bone marrow smears.

The final 19-class benchmark contains **11,520 images**.

| Class | Image Count | Status |
|---|---:|---|
| Band | 275 | Included |
| Basophil | 24 | Included |
| Blast | 97 | Included |
| Eosinophil | 137 | Included |
| Lymphoblast | 1,103 | Included |
| Lymphocyte | 2,337 | Included |
| Metamyelocyte | 405 | Included |
| Mitosis | 37 | Included |
| Monoblast | 405 | Included |
| Monocyte | 718 | Included |
| Myeloblast | 422 | Included |
| Myelocyte | 274 | Included |
| PMN | 2,779 | Included |
| PlasmaCell | 44 | Included |
| Prolymphocyte | 42 | Included |
| Promonocyte | 230 | Included |
| Promyelocyte | 368 | Included |
| ReactiveLymphocyte | 419 | Included |
| SmudgeCell | 1,404 | Included |
| **Total** | **11,520** | **19 classes** |

The dataset preserves this natural class distribution rather than applying artificial oversampling, undersampling, or class balancing during dataset construction.

The complete class counts and inclusion status are provided in:

`metadata/class_counts.csv`

---

## Excluded Leukocyte Classes

The original annotated leukocyte collection contained 23 cell categories. Four categories with very limited representation were excluded from the final 19-class benchmark because of insufficient sample representation.

The excluded categories are:

| Class | Image Count | Status |
|---|---:|---|
| Dysplasia | 11 | Excluded |
| LargeGranularLymphocyte | 14 | Excluded |
| MetamyelocyteEo | 13 | Excluded |
| MyelocyteEo | 14 | Excluded |
| **Total** | **52** | **Excluded** |

The final leukocyte benchmark therefore contains **19 classes and 11,520 images**.

The current leukocyte ZIP package contains **11,572 images in total**, including the 11,520 images from the final 19-class benchmark and the 52 images belonging to the four excluded categories.

The complete class counts and inclusion status are provided in:

`metadata/class_counts.csv`

---

## Dataset Structure
---
## Intended Use

TUT-BM_version1 is intended for research and educational applications, including:

- automated bone marrow cell classification;
- computer vision and deep learning research;
- image-based hematology research;
- evaluation of classification methods under natural class imbalance;
- development of image-analysis pipelines for bone marrow cytology;
- benchmarking of machine-learning methods;
- development of educational resources for hematology and biomedical image analysis.

The dataset does **not** provide a clinical diagnosis for individual patients and should not be used as a standalone diagnostic tool.

---

## Baseline Validation

A baseline experiment using **ResNet-50** was performed to provide an initial technical validation of the 19-class leukocyte benchmark.

The experiment used a stratified training/validation procedure together with an independent test set.

Data augmentation was applied to the training data, including image flipping, rotation, and zoom transformations.

The model was trained using categorical cross-entropy loss and the Nadam optimizer.

No explicit class rebalancing, loss weighting, or oversampling was applied during the baseline experiment.
---

## Reproducibility

The repository is intended to provide sufficient documentation for researchers to understand the dataset organization and reproduce the baseline analysis.

Where applicable, the repository includes:

- dataset metadata;
- class-distribution information;
- preprocessing documentation;
- baseline training and evaluation scripts;
- evaluation metrics;
- figures and tables;
- configuration information.

The complete dataset is distributed separately through the associated Figshare record.

---

## Limitations

Despite the potential value of this dataset for developing and evaluating artificial intelligence-based methods for blood cell classification, several limitations should be acknowledged.

One important limitation is the limited number of samples in some rare cell categories, which is an inherent challenge in many clinical datasets due to the naturally low prevalence of these cells in bone marrow smears.

In addition, the current benchmark focuses primarily on leukocyte classification. The broader annotated collection contains erythroid/RBC and platelet-related categories, but these groups are not yet incorporated into the primary benchmark.

The dataset also does not provide individual-patient diagnostic labels, disease-stage information, treatment-response information, or other clinical outcome variables.

---

## Future Development

This study was conducted with the aim of preparing a bone marrow leukocyte dataset. However, bone marrow evaluation inherently relies on examining the relationships and interactions among all hematopoietic lineages.

Extending this framework to simultaneously assess erythroid, megakaryocytic/platelet, and leukocyte lineages using the collected data will be an important next step in this work.

Future versions may also include expanded annotations, additional cell categories, improved metadata, and further benchmark tasks.

---

## Data Availability

The complete dataset is intended to be publicly available through **Figshare**.

**Dataset DOI:** `10.6084/m9.figshare.34070649

The Figshare record will serve as the primary distribution point for the dataset, while this GitHub repository provides documentation, metadata, analysis resources, and supporting materials.

---

## Associated Publication

A detailed description of the dataset, including data acquisition, annotation, quality control, dataset characteristics, and technical validation, is being prepared for submission to *...

**Publication:** To be added after publication.

---

## Citation

If you use **TUT-BM_version1** in your research, please cite the dataset and the associated publication.

The final recommended citation will be updated after the dataset record and associated publication are finalized.

---

## Ethics and Privacy

The dataset was prepared from anonymized clinical material.

No directly identifying patient information is intended to be included in the publicly released dataset.

Further information regarding ethical approval, anonymization, and data governance is provided in the associated scientific publication and dataset documentation.

---

## License

The license for redistribution and reuse will be specified in the final public dataset release.

---

## Contact

For questions regarding the dataset, annotation, access, or potential research collaboration, please refer to the contact information provided in the associated publication and dataset record.

---

## Acknowledgments

The authors acknowledge the contributions of the participating clinical centers, hematology experts, and research collaborators involved in specimen preparation, image acquisition, annotation, and quality control.

---

## Keywords

`bone marrow cytology` · `bone marrow dataset` · `hematology` · `leukocyte classification` · `cell classification` · `microscopy` · `medical image analysis` · `deep learning` · `computer vision` · `class imbalance` · `TUT-BM`

---

## Version

**TUT-BM_version1**

This repository will be updated as additional documentation, metadata, analysis resources, and future dataset versions become available.
