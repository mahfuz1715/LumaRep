# LumaRep

### Interpretable Lumbar Spinal MRI Classification with Self-Supervised Learning

LumaRep is a deep-learning research project for three-class lumbar spinal MRI classification with a focus on representation learning, interpretability, and practical clinical decision support.

The study compares supervised CNN baselines with self-supervised and semi-supervised learning strategies, including BYOL, DINO, and STAC. The strongest configuration, **BYOL-VGG16**, achieved the best overall classification performance.

> **Status:** Accepted for oral presentation as a regular paper at the **2027 IEEE 16th International Conference on Communication Systems and Network Technologies (CSNT 2027)**, with minor revisions.

---

## Research Focus

This work explores whether self-supervised representation learning can improve lumbar spinal MRI classification while keeping model predictions interpretable.

The study focuses on:

- supervised baseline comparison,
- self-supervised representation learning,
- semi-supervised learning,
- explainability using Grad-CAM,
- occlusion sensitivity analysis,
- and a lightweight Streamlit-based prototype.

---

## Dataset

After duplicate removal, the final dataset contains **13,036 lumbar spinal MRI images** across three classes:

| Class | Images |
|---|---:|
| Herniated Disc | 4,215 |
| No Stenosis | 4,400 |
| Thecal Sac | 4,421 |
| **Total** | **13,036** |

A total of **650 duplicate images** were removed from the original collection of 13,686 images.

---

## Models Explored

### Supervised Learning
- VGG16
- ResNet50
- ConvNeXt Small
- DenseNet201
- EfficientNet-B3 exploratory experiments

### Self-Supervised Learning
- BYOL
- DINO

### Semi-Supervised Learning
- STAC

---

## Best Result

The strongest model was **BYOL-VGG16**.

| Metric | Score |
|---|---:|
| Accuracy | **95.63%** |
| Precision | **95.64%** |
| Recall | **95.61%** |
| F1-score | **95.62%** |

These results indicate that self-supervised pretraining can provide strong representations for lumbar spinal MRI classification.

---

## Explainability

LumaRep incorporates two complementary explainability approaches:

### Grad-CAM
Grad-CAM is used to visualize image regions that contribute most strongly to a prediction.

### Occlusion Sensitivity
Occlusion-based analysis is used to examine how predictions change when specific image regions are masked.

Together, these methods help make model behavior more transparent and easier to inspect.

---

## Repository Structure

```text
LumaRep/
├── README.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   ├── 01_supervised_baseline_screening.ipynb
│   ├── 02_convnext_small_baseline.ipynb
│   ├── 03_efficientnetb3_exploratory.ipynb
│   ├── 04_byol_self_supervised.ipynb
│   ├── 05_dino_self_supervised.ipynb
│   └── 06_stac_semi_supervised.ipynb
├── app/
│   ├── app.py
│   ├── .streamlit/
│   │   └── config.toml
│   └── models/
│       └── PUT_MODEL_HERE.txt
└── paper/
    └── README.md
```

Model weights and the dataset are not redistributed through this repository.

---

## Application Prototype

A Streamlit prototype is included for demonstrating the classification workflow.

To run the application:

```bash
streamlit run app/app.py
```

The trained model file should be placed in:

```text
app/models/
```

---

## Paper

**Title:**  
*LumaRep: An Interpretable Lumbar Spinal MRI Classification via Self-Supervised Learning*

### Authors

- Shawna Akter
- **Mahfuz Uddin Ahmed**
- Moin Uddin Ahmed
- Mustari Zaman
- Md Mahfuzur Rahman
- Rafid Bin Taher

### Conference

**2027 IEEE 16th International Conference on Communication Systems and Network Technologies (CSNT 2027)**

### Status

**Accepted for Oral Presentation as a Regular Paper, with Minor Revisions**

The publisher-formatted manuscript is not redistributed in this repository. The official publication link and DOI will be added once the final bibliographic record becomes available.

---

## Research Scope

LumaRep contributes to research at the intersection of:

- Deep Learning
- Medical Image Analysis
- Computer Vision
- Self-Supervised Learning
- Explainable AI
- Representation Learning

---

## Citation

Official citation information will be added after publication.

```bibtex
@misc{lumarep2027,
  title = {LumaRep: An Interpretable Lumbar Spinal MRI Classification via Self-Supervised Learning},
  note  = {Accepted for oral presentation as a regular paper at IEEE CSNT 2027},
  year  = {2027}
}
```
