# TUT-BM-Dataset

## TUT-BM_version1: Bone Marrow Cytology Image Dataset for Leukocyte Classification

**TUT-BM_version1** is a curated image dataset of bone marrow cytology developed for research on automated leukocyte image analysis and classification using computer vision and deep learning methods.

The dataset was collected from bone marrow smear specimens and contains images representing 19 leukocyte cell types. It was developed as a research resource for automated analysis of bone marrow cytology images, including studies addressing naturally occurring class imbalance.

---

## Dataset Overview

| Property | Description |
|---|---|
| Dataset name | TUT-BM_version1 |
| Repository | TUT-BM-Dataset |
| Image modality | Bone marrow cytology microscopy |
| Number of patients | 80 |
| Number of retained microscope images | 5,129 |
| Number of annotated single-cell images | 18,681 |
| Primary leukocyte images | 11,531 |
| Number of leukocyte classes | 19 |
| Image format | Cropped single-cell images |
| Input image size | 250 × 250 pixels |
| Annotation method | Expert hematologist annotation |
| Dataset characteristics | Naturally imbalanced multi-class dataset |

---

## Data Collection

Bone marrow smear specimens were obtained from patients evaluated at hematology centers affiliated with **Tabriz University of Medical Sciences**.

Microscopic images were acquired using a **Bresser Science ADL 601F microscope** equipped with a **Canon EOS 1300D digital camera**.

The original images were acquired at a resolution of **5184 × 3456 pixels**. Standardized imaging conditions were maintained during image acquisition, including fixed focus, exposure, white balance, shutter speed, and ISO settings.

The bone marrow smears were prepared using **May-Grünwald-Giemsa staining**.

---

## Image Processing and Annotation

A total of **6,229 microscopic images** were initially acquired. Following quality control, duplicate removal, and exclusion of unsuitable regions, **5,129 images** were retained.

Individual cells were annotated using bounding boxes, and the annotated regions were cropped to generate single-cell images.

The resulting dataset contains **18,681 annotated single-cell images**, including leukocytes, erythrocytes, and platelets. The primary leukocyte subset contains **11,531 images** distributed across 19 leukocyte categories.

The leukocyte images were standardized to **250 × 250 pixels** for machine-learning applications.

---

## Leukocyte Classes

The final version of TUT-BM_version1 contains **19 leukocyte categories**.

Three classes with very limited representation in the original dataset were excluded from the final version.

The dataset preserves the naturally occurring class distribution and does not apply artificial class balancing during dataset construction.

---

## Dataset Structure

The public dataset will be distributed through **Figshare**.

The final directory and file organization will be documented in the Figshare record and accompanying metadata.

---

## Intended Use

TUT-BM_version1 is intended for research and educational applications, including:

- automated bone marrow cell classification;
- computer vision and deep learning research;
- evaluation of classification methods under class imbalance;
- development of image-analysis pipelines for hematology;
- benchmarking of machine-learning methods for bone marrow cytology.

The dataset does **not** provide a clinical diagnosis for individual patients and should not be used as a standalone diagnostic tool.

---

## Baseline Validation

A baseline experiment using **ResNet-50** was performed to provide an initial technical validation of the dataset.

The baseline classification experiment used the 19 leukocyte categories and evaluated classification performance using multiple metrics, including accuracy, macro-averaged precision, recall, F1-score, weighted F1-score, and Matthews correlation coefficient (MCC).

Detailed experimental procedures and results will be reported in the associated scientific publication.

---

## Data Availability

The complete dataset will be made publicly available through **Figshare**.

**Dataset DOI:** To be added after Figshare publication.

**Figshare record:** To be added.

---

## Associated Publication

A detailed description of the dataset, data acquisition procedure, annotation process, quality control, and technical validation is being prepared for submission to **Scientific Data**.

**Publication:** To be added.

---

## Citation

If you use TUT-BM_version1 in your research, please cite the associated dataset and publication.

The recommended citation will be provided after the Figshare record and DOI are finalized.

---

## Ethics and Privacy

The dataset was prepared from anonymized clinical material. No directly identifying patient information is intended to be included in the publicly released dataset.

Further information regarding ethical approval, anonymization, and data governance is provided in the associated scientific publication and dataset documentation.

---

## License

The license for redistribution and reuse will be specified in the final public Figshare release.

---

## Contact

For questions regarding the dataset, annotation, access, or potential research collaboration, please refer to the contact information provided in the associated publication and Figshare record.
