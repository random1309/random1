<p align="center">
  <!-- Replace with your own logo path -->
  <img src="./docs/logo.png" height=150>
</p>

# 🌾 SAMConvFormer+LLM: Exploring synergistic fusion of Segment Anything Model with joint convolutional transformer and large language model to advance dense agricultural crop analysis

<span>
<a href="https://www.sciencedirect.com/science/article/pii/S0168169925012980"><img src="https://img.shields.io/badge/Paper-ScienceDirect-orange.svg" height=22.5></a>
<a href="https://doi.org/10.1016/j.compag.2025.111192"><img src="https://img.shields.io/badge/Journal-Comp.%20%26%20Elec.%20in%20Agri.-green.svg" height=22.5></a>
<a href="https://doi.org/10.6084/m9.figshare.XXXXX"><img src="https://img.shields.io/badge/Dataset-Figshare-blue.svg" height=22.5></a>
<!-- Uncomment / edit when ready
<a href="https://your-project-page-url"><img src="https://img.shields.io/badge/project-SAMConvFormer%2BLLM-purple.svg" height=22.5></a>
<a href="https://your-demo-url"><img src="https://img.shields.io/badge/🌐%20Demo-Coming%20Soon-lightgrey" height=22.5></a>
-->
</span>

Code for the paper  
[SAMConvFormer+LLM: Exploring synergistic fusion of Segment Anything Model with joint convolutional transformer and large language model to advance dense agricultural crop analysis](https://www.sciencedirect.com/science/article/pii/S0168169925012980).

### About this repo

This repository contains the **official implementation** of **SAMConvFormer+LLM** for dense agricultural crop analysis.

---

## 🧠 Introduction 

> Accurate detection of **densely fruited crops** is essential for yield estimation, ripeness analysis, and actionable recommendations for optimized crop management using large language models. However, real-world agricultural environments present challenges like varying illumination, diverse fruit sizes, and highly complex backgrounds, making robust detection difficult.  
>  
> Existing AI models—trained on controlled datasets—struggle to generalize to real-field conditions. To address this, we introduce a **real-field dataset** that captures the complexities of dense crops and propose a novel **SAMConvFormer** framework that **synergizes the Segment Anything Model (SAM)** with a **Joint Convolutional Transformer**.  
>  
> This fusion enhances **boundary delineation** for overlapping, blurred, and irregular fruit structures. Further integration with a **Large Language Model (LLM)** provides a comprehensive pipeline for **yield estimation, ripeness analysis**, and **adaptive crop management recommendations**.  
>  
> Our model achieves:  
> • **79.32% Sensitivity**  
> • **62.64% IoU**  
> • **77.03% Dice Coefficient**  
>  
> These represent relative improvements of **31%, 18.79%, and 11.56%** over the baseline model, confirming the robustness and precision of our approach for densely fruited crop detection.
<br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/f7b31d25-66a5-4a36-bcfa-5a424484d205" width="950"/>
</p>

---

## 🔥 News / TODO

- [x] Paper accepted in **Computers and Electronics in Agriculture (2025)**.
- [x] Dataset uploaded to **Figshare** (under admin approval).
- [ ] Release cleaned and documented **source code**.
- [ ] Release pretrained **SAMConvFormer+LLM weights**.
- [ ] Provide **inference scripts** and **demo notebooks**.
- [ ] Release **web demo** for interactive crop analysis.

---

## 🌾 Framework 

> **Overview of the SAMConvFormer+LLM Pipeline.**  
> A real-field agricultural image is first processed by **SAM** to produce high-quality region proposals and boundary-aware features for dense clusters of fruits. These features are fused with a **Joint Convolutional Transformer**, which combines local texture information and global contextual cues to generate refined segmentation masks for densely packed fruits. The resulting instance- or semantic-level representations are then passed to an **LLM-based reasoning module**, which performs **yield estimation**, **ripeness analysis**, and generates **adaptive crop management recommendations** for growers and agronomists.

**High-level stages:**

1. **Real-Field Data Acquisition**  
   - Images captured directly in orchards/fields under **natural conditions** (lighting, occlusions, cluttered foliage).

2. **SAM-Based Proposal and Boundary Extraction**  
   - **Segment Anything Model (SAM)** produces initial masks and boundary cues for fruit regions.
   - Handles **overlapping**, **partially occluded**, and **irregularly shaped** fruits.

3. **SAMConvFormer (Joint Convolutional Transformer)**  
   - Convolutional blocks capture **fine-grained local patterns** (fruit texture, edges).  
   - Transformer blocks model **global context** (fruit clusters, branches, background).  
   - Feature fusion improves segmentation quality in dense, noisy scenes.

4. **Refined Crop Segmentation**  
   - Outputs high-quality masks for **individual fruits** or **dense fruit regions**, suitable for counting and area estimation.

5. **LLM-Integrated Decision Support**  
   - Aggregates predictions (fruit count, size, coverage, spatial distribution).  
   - An **LLM** interprets these statistics to provide:  
     - **Yield estimation** (per plant/row/field).  
     - **Ripeness and quality analysis** based on visual cues and metadata.  
     - **Adaptive management recommendations** (harvest timing, thinning, irrigation, nutrient adjustments).

---

## 💾 Dataset & Resources

- 📂 **Real-field dense crop dataset:**  
  - **Figshare:** [https://doi.org/10.6084/m9.figshare.XXXXX](https://doi.org/10.6084/m9.figshare.XXXXX)  
  - Includes **real-field images**, **dense fruit annotations**, and **metadata** (lighting, crop variety, etc.).  
  - Link becomes accessible upon Figshare admin approval.

- 💻 **Code & Models:**  
  - SAMConvFormer+LLM source code: _to be released_  
  - Pretrained checkpoints: _to be released_  

(Once you have URLs for code/checkpoints, replace the placeholders above.)

---

## 🚜 Quick Start (planned)

> **Note:** This section assumes the code is released. Update the commands to match your final repo structure.

### 1️⃣ Environment Setup

```bash
# create new conda env
conda create -n samconvformer python=3.10
conda activate samconvformer

# install required packages
pip install -r requirements.txt
