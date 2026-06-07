# RS-OVSGSeg

Official repository for the paper:

**Enhancing Scene Generalization for Open-Vocabulary Remote Sensing Segmentation via Semantic–Structural Collaboration**

## Overview

Open-vocabulary semantic segmentation (OVSS) aims to segment arbitrary semantic categories described by text prompts. Existing remote sensing OVSS methods mainly focus on semantic alignment while overlooking the severe scene variations caused by differences in geographic regions, imaging conditions, spatial resolutions, and land-cover compositions.

To address this issue, we propose **RS-OVSGSeg**, a semantic–structural collaborative framework for **open-vocabulary scene generalization semantic segmentation (OVSGSS)** in remote sensing images. The proposed framework explicitly models the interaction between semantic priors derived from vision–language models and scene-invariant structural representations learned from large-scale remote sensing data.

The main contributions of this work include:

* **Semantic–structural collaborative OVSGSS framework.** We propose a novel framework named **RS-OVSGSeg**, which explicitly models the collaboration between semantic priors and scene-invariant structural representations, thereby improving robustness under large scene variations and enhancing generalization to unseen classes.

* **USGMS-100K dataset and RSIE pretraining.** We construct a large-scale unsupervised multi-sensor dataset named **USGMS-100K** for learning scene-invariant representations. Based on this dataset, we pretrain a **Remote Sensing Invariant Encoder (RSIE)** using masked self-supervised learning to extract hierarchical, multi-scale, and structure-aware visual representations.

* **Semantic–structural interaction modules.** We design a **Semantic–Structural Cost Map Enhancer (SSCME)** and a **Dual-Prior Guided Decoder (DPGD)** to progressively integrate semantic and structural guidance, improving spatial continuity, boundary integrity, and fine-grained category discrimination.

* **Extensive cross-scene evaluation.** Experimental results on five challenging unseen datasets demonstrate that the proposed method consistently outperforms existing state-of-the-art OVSS approaches.

## Framework

<p align="center">
  <img src="./docs/framework.png" width="95%">
</p>

**Figure:** Overall architecture of the proposed RS-OVSGSeg framework.

---

## USGMS-100K Dataset

USGMS-100K is a large-scale unsupervised multi-sensor remote sensing dataset designed for scene-invariant representation learning.

### Dataset characteristics

* **100,000** image patches;
* Fixed patch size of **384 × 384** pixels;
* Constructed from multiple public datasets:

  * OpenEarthMap,
  * EvLab-SS,
  * CASID,
  * DIOR;
* Covers diverse:

  * geographic regions,
  * imaging conditions,
  * spatial resolutions,
  * land-cover types.

The detailed construction pipeline, patch sampling strategy, geographic distribution, and dataset statistics are described in our paper.

### Download

**Baidu Cloud:**

* Dataset: [Link]
* Extraction code: `[XXXX]`

A **Zenodo mirror with DOI** will be released upon acceptance of the paper.

## Pretrained RSIE Weights

We provide the pretrained weights of the proposed **Remote Sensing Image Encoder (RSIE)**.

### Model

| Model | Backbone | Pretraining Strategy                          |
| ----- | -------- | --------------------------------------------- |
| RSIE  | Swin-B   | Masked self-supervised learning on USGMS-100K |

### Download

**Baidu Cloud:**

* Weights: [Link]
* Extraction code: `[XXXX]`

A **Zenodo mirror with DOI** will be released upon acceptance of the paper.

## Code Availability

The complete training and inference code is currently being organized and documented.

The source code will be **publicly released immediately upon acceptance** of the paper.

The released code will include:

* training scripts,
* inference scripts,
* configuration files,
* evaluation protocols,
* pretrained checkpoints,
* instructions for reproducing the reported results.

## Reproducibility Statement

To ensure reproducibility:

* The **USGMS-100K dataset** has been publicly released;
* The **pretrained RSIE weights** are publicly available;
* The complete **training and inference code** will be released upon acceptance;
* A **Zenodo DOI** will be provided for long-term accessibility.

## Citation

## Acknowledgements

USGMS-100K is constructed based on several publicly available datasets. We sincerely thank the authors of the following datasets for making their data available to the research community:

* OpenEarthMap;
* EvLab-SS;
* CASID;
* DIOR.

Users of USGMS-100K should comply with the licenses and usage policies of the original datasets.


## Contact

If you have any questions regarding this work, please feel free to open an issue in this repository.

For academic inquiries, please contact:

**Bill Huang**

E-mail: `[your email address]`

---

**This repository will be continuously updated throughout the review process and after publication.**
