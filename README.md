# 🌾 SAMConvFormer+LLM: Exploring synergistic fusion of Segment Anything Model with joint convolutional transformer and large language model to advance dense agricultural crop analysis

<div align="center">

**Muhammad Owais, Israa Fahmy, Lakmal Seneviratne, Irfan Hussain**  
Khalifa University Center for Autonomous Robotic Systems (KUCARS), United Arab Emirates  

[![Paper](https://img.shields.io/badge/Computers%20and%20Electronics%20in%20Agriculture-2025-informational)](https://www.sciencedirect.com/science/article/pii/S0168169925012980)
[![Dataset](https://img.shields.io/badge/Dataset-Figshare-pending)](https://doi.org/10.6084/m9.figshare.XXXXX)
![Status](https://img.shields.io/badge/Status-Active%20research-brightgreen)

📄 **Published in:** *Computers and Electronics in Agriculture* (2025)  
🔗 **Paper link:** [ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0168169925012980)  
📂 **Dataset:** [Available on Figshare](https://doi.org/10.6084/m9.figshare.XXXXX) *(Uploaded and currently under admin approval; the link will be accessible soon.)*

</div>

---

## 🔍 Overview

This repository contains the official implementation and resources for:

> **SAMConvFormer+LLM: Exploring synergistic fusion of Segment Anything Model with joint convolutional transformer and large language model to advance dense agricultural crop analysis**

Real-world agricultural environments feature dense fruit clusters, illumination variability, and cluttered backgrounds, making robust instance-level fruit detection and segmentation extremely challenging. **SAMConvFormer+LLM** addresses these challenges by:

- Leveraging the **Segment Anything Model (SAM)** for high-quality, promptable segmentation.
- Introducing a **Joint Convolutional Transformer (ConvFormer)** to better model local texture and global context in dense crop scenes.
- Integrating a **Large Language Model (LLM)** to turn perception outputs into **actionable recommendations** for precision agriculture (yield estimation, ripeness assessment, and decision support).

---

## 🧠 Abstract

Accurate detection of densely fruited crops is essential for yield estimation, ripeness analysis, and actionable recommendations for optimized crop management using large language models. However, real-world agricultural environments present challenges like varying illumination, diverse fruit sizes, and highly complex backgrounds, making robust detection difficult.

Existing AI models—trained on controlled datasets—struggle to generalize to real-field conditions. To address this, we introduce a real-field dataset that captures the complexities of dense crops and propose a novel **SAMConvFormer** framework that synergizes the **Segment Anything Model (SAM)** with a **Joint Convolutional Transformer**.

This fusion enhances boundary delineation for overlapping, blurred, and irregular fruit structures. Further integration with a **Large Language Model (LLM)** provides a comprehensive pipeline for yield estimation, ripeness analysis, and adaptive crop management recommendations.

Our model achieves:

- **79.32%** Sensitivity  
- **62.64%** IoU  
- **77.03%** Dice Coefficient  

These represent relative improvements of **31%**, **18.79%**, and **11.56%** over the baseline model, confirming the robustness and precision of our approach for densely fruited crop detection.

---

## 📚 Table of Contents

- [Overview](#-overview)
- [Abstract](#-abstract)
- [Key Contributions](#-key-contributions)
- [Workflow of the Proposed Framework](#️-workflow-of-the-proposed-framework)
- [Dataset](#-dataset)
- [Installation](#-installation)
- [Quick Start](#-quick-start)
  - [Inference / Segmentation](#inference--segmentation)
  - [Yield & Ripeness Analysis](#yield--ripeness-analysis)
  - [LLM-based Recommendation Pipeline](#llm-based-recommendation-pipeline)
- [Results](#-results)
- [Repository Structure](#-repository-structure)
- [Keywords](#-keywords)
- [Citation](#-citation)
- [Acknowledgements](#-acknowledgements)
- [Contact](#-contact)

---

## 🌱 Key Contributions

1. **Bridging AI and Field Expertise**  
   Integrates direct input from agricultural field experts to ensure practically meaningful and explainable solutions for farmers and agronomists.

2. **Novel SAMConvFormer Framework**  
   Combines the **Segment Anything Model (SAM)** with a **Joint Convolutional Transformer** for accurate detection and segmentation of dense crops under highly complex real-field conditions.

3. **LLM-Integrated Crop Management Pipeline**  
   Incorporates a **Large Language Model (LLM)** for yield estimation, ripeness analysis, and actionable recommendations, enabling adaptive decision support in precision agriculture.

4. **Comprehensive Ablation Study**  
   Demonstrates how each component—**SAM**, transformer, and convolutional fusion—contributes to overall performance gains in dense crop detection and segmentation.

5. **Open Research Resource**  
   The full framework, dataset, and materials will be publicly released to advance dense crop segmentation and support future agricultural AI innovations.

---

## ⚙️ Workflow of the Proposed Framework

<div align="center">

**Figure 1 – Workflow of the proposed SAMConvFormer+LLM pipeline**

<!-- Update the image path below to match your repo location -->
<img src="PATH/TO/samconvformer_llm_pipeline.jpg" alt="Workflow of the proposed framework" width="90%"/>

</div>

The pipeline consists of three main stages:

1. **SAMConvFormer Segmentation**
   - Uses SAM with a ConvFormer backbone to segment dense fruits under challenging illumination and occlusion.
   - Enhances boundary delineation for overlapping, blurred, and irregular structures.

2. **Yield Estimation & Ripeness Analysis**
   - Post-processing of masks for:
     - Object extraction and non-overlapping instance isolation  
     - Shape/roundness analysis  
     - Color- and feature-based clustering for ripeness levels  
   - Outputs **total yield** (e.g., estimated weight and count) and **ripeness distribution**.

3. **LLM-based Decision Support**
   - Structured outputs (yield, ripeness, temporal trends, and metadata) are fed into an LLM (e.g., Llama 3).
   - The LLM generates natural-language recommendations for:
     - Harvest scheduling and maturity forecasting  
     - Under/over-ripe management  
     - Loss prevention and labor planning  
     - Pricing and market strategy  
     - Long-term crop lifecycle management  

---

## 📂 Dataset

- **Type:** Real-field images of densely fruited crops  
- **Variations:**  
  - Illumination changes (shadowed, overexposed, diffused light)  
  - Diverse fruit sizes and occlusions  
  - Complex natural backgrounds (leaves, branches, soil, nets, etc.)  

The dataset will be hosted on **Figshare**:

> 📂 **Dataset:** [Available on Figshare](https://doi.org/10.6084/m9.figshare.XXXXX)  
> *(Uploaded and currently under admin approval; the link will be accessible soon.)*

Once the dataset is public, we will provide:

- Download instructions  
- Train/val/test splits  
- Data format and annotation description  

---

## 🛠 Installation

> ⚠️ **Note:** Adjust the Python and CUDA versions below according to your environment and the dependencies used in this repository.

```bash
# 1. Clone the repository
git clone https://github.com/Owais-CodeHub/SAMConvFormer-LLM.git
cd SAMConvFormer-LLM

# 2. (Optional but recommended) create a virtual environment
python -m venv samconv_env
source samconv_env/bin/activate  # On Windows: samconv_env\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt
