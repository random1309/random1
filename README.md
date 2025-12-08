
# SAMConvFormer+LLM: Exploring synergistic fusion of Segment Anything Model with joint convolutional transformer and large language model to advance dense agricultural crop analysis

**Muhammad Owais**, *Israa Fahmy, Lakmal Seneviratne, Irfan Hussain*  
*Khalifa University Center for Autonomous Robotic Systems (KUCARS), United Arab Emirates*

<span>
<a href="https://www.sciencedirect.com/science/article/pii/S0168169925012980"><img src="https://img.shields.io/badge/Paper-ScienceDirect-orange.svg" height="22.5"></a>
<a href="https://doi.org/10.1016/j.compag.2025.111192"><img src="https://img.shields.io/badge/Journal-Comp.%20%26%20Elec.%20in%20Agri.-green.svg" height="22.5"></a>
<a href="https://doi.org/10.6084/m9.figshare.XXXXX"><img src="https://img.shields.io/badge/Dataset-Figshare-blue.svg" height="22.5"></a>
<!-- Add/modify when code is public -->
<!-- <a href="https://github.com/your-repo/SAMConvFormer-LLM"><img src="https://img.shields.io/badge/Code-GitHub-black.svg" height="22.5"></a> -->
</span>

Code for the paper:  
[SAMConvFormer+LLM: Exploring synergistic fusion of Segment Anything Model with joint convolutional transformer and large language model to advance dense agricultural crop analysis](https://www.sciencedirect.com/science/article/pii/S0168169925012980).

---

## 📦 About this Repo

This repository will host the **official implementation** of **SAMConvFormer+LLM** for dense agricultural crop analysis, including:

- Training and inference code for SAMConvFormer.
- Scripts for LLM-based yield and ripeness analysis.
- Real-field dense crop dataset and annotations.
- Pretrained checkpoints and example configs.

---

## 🧠 Abstract

> Accurate detection of **densely fruited crops** is essential for yield estimation, ripeness analysis, and actionable recommendations for optimized crop management using large language models. However, real-world agricultural environments present challenges like varying illumination, diverse fruit sizes, and highly complex backgrounds, making robust detection difficult.  
>  
> Existing AI models—trained on controlled datasets—struggle to generalize to real-field conditions. To address this, we introduce a **real-field dataset** that captures the complexities of dense crops and propose a novel **SAMConvFormer** framework that **synergizes the Segment Anything Model (SAM)** with a **Joint Convolutional Transformer**.  
>  
> This fusion enhances **boundary delineation** for overlapping, blurred, and irregular fruit structures. Further integration with a **Large Language Model (LLM)** provides a comprehensive pipeline for **yield estimation, ripeness analysis**, and **adaptive crop management recommendations**.  
>  
> Our model achieves:  
> - **79.32% Sensitivity**  
> - **62.64% IoU**  
> - **77.03% Dice Coefficient**  
>  
> These represent relative improvements of **31%, 18.79%, and 11.56%** over the baseline model, confirming the robustness and precision of our approach for densely fruited crop detection.

---

## 🌱 Key Contributions

1. **Bridging AI and Field Expertise**  
   Integrates direct input from agricultural field experts to ensure practical, explainable, and deployable solutions in real farming conditions.

2. **Novel SAMConvFormer Framework**  
   Combines the **Segment Anything Model (SAM)** with a **Joint Convolutional Transformer** for robust detection and segmentation of dense crops under challenging illumination, occlusion, and background clutter.

3. **LLM-Integrated Crop Management Pipeline**  
   Incorporates a **Large Language Model (LLM)** for **yield estimation**, **ripeness analysis**, and **actionable crop management recommendations**, enabling **adaptive decision support** in precision agriculture.

4. **Comprehensive Ablation Study**  
   Demonstrates how each component—**SAM**, **transformer**, and **convolutional fusion**—contributes to overall performance gains on dense fruit detection and segmentation.

5. **Open Research Resource**  
   The full **framework, dataset, and materials** will be publicly released to advance dense crop segmentation and support future agricultural AI innovations.

---

## 🔥 News / TODO

- [x] Paper accepted in **Computers and Electronics in Agriculture (2025)**.
- [x] Real-field dense crop dataset uploaded to **Figshare** (awaiting admin approval).
- [ ] Release **source code** of SAMConvFormer+LLM.
- [ ] Release **pretrained weights** for SAMConvFormer and LLM pipeline.
- [ ] Add **training & inference scripts** with example configs.
- [ ] Deploy **online demo** for interactive analysis.

---

## ⚙️ Workflow of the Proposed Framework

**Figure:** Workflow of the proposed SAMConvFormer + LLM pipeline  

<p align="center">
  <img src="https://github.com/user-attachments/assets/f7b31d25-66a5-4a36-bcfa-5a424484d205" width="950">
</p>

### 🔩 Pipeline Overview

1. **Real-Field Image Acquisition**  
   - Collect dense crop images in real orchards/fields with natural variation in **illumination**, **viewpoints**, and **background clutter**.

2. **SAM-Based Region Proposal and Boundary Extraction**  
   - Apply **Segment Anything Model (SAM)** to obtain initial masks and boundary-aware regions for densely packed fruits.
   - Handles **overlapping**, **blurred**, and **irregularly shaped** fruits.

3. **Joint Convolutional Transformer (SAMConvFormer)**  
   - Convolutional layers capture **local spatial details** and fine-grained fruit texture.  
   - Transformer layers model **global context** and long-range dependencies (e.g., fruit clusters, foliage).  
   - Fusion improves **boundary delineation** and object separation in highly dense scenes.

4. **Refined Dense Fruit Segmentation**  
   - Produce high-quality segmentation maps for fruits (instance-level or region-level) suitable for counting, sizing, and coverage estimation.

5. **LLM-Driven Crop Intelligence**  
   - Extract summary statistics (fruit counts, sizes, area coverage, spatial patterns).  
   - Feed these into an **LLM** to perform:  
     - **Yield estimation** (per plant/row/field).  
     - **Ripeness assessment** and quality estimation.  
     - **Adaptive crop management recommendations** (e.g., harvest timing, thinning strategies, irrigation and fertilization suggestions).

---

## 📈 Performance

Model performance on densely fruited crop detection (real-field data):

| Metric             | Value     | Relative Improvement over Baseline |
|--------------------|----------:|------------------------------------|
| **Sensitivity**    | **79.32%** | **+31.00%**                        |
| **IoU**            | **62.64%** | **+18.79%**                        |
| **Dice Coefficient** | **77.03%** | **+11.56%**                        |

These results highlight that **SAMConvFormer+LLM** significantly improves:

- **Detection reliability** (higher Sensitivity) in cluttered and occluded regions.  
- **Segmentation quality** (higher IoU and Dice) for overlapping and irregular fruit structures.  
- **Downstream analytic reliability** for LLM-based yield and ripeness reasoning.

---

## 🧩 Keywords

- Precision Agriculture  
- Densely Fruited Crop  
- Yield Estimation  
- Ripeness Analysis  
- Segment Anything Model (SAM)  
- Joint Convolutional Transformer  
- Large Language Model (LLM)  

---

## 📬 Citation

If you use this work, please cite:

```bibtex
@article{Owais2025SAMConvFormerLLM,
  title   = {SAMConvFormer+LLM: Exploring synergistic fusion of Segment Anything Model with joint convolutional transformer and large language model to advance dense agricultural crop analysis},
  author  = {Muhammad Owais and Israa Fahmy and Lakmal Seneviratne and Irfan Hussain},
  journal = {Computers and Electronics in Agriculture},
  year    = {2026},
  issn    = {0168-1699},
  doi     = {10.1016/j.compag.2025.111192},
  url     = {https://www.sciencedirect.com/science/article/pii/S0168169925012980}
}
