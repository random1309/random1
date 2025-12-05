# 🌾 SAMConvFormer+LLM: Exploring synergistic fusion of Segment Anything Model with joint convolutional transformer and large language model to advance dense agricultural crop analysis

<p align="center">
  <img src="https://github.com/user-attachments/assets/f7b31d25-66a5-4a36-bcfa-5a424484d205" alt="Workflow of the proposed SAMConvFormer+LLM framework" width="80%">
</p>

Code for the paper:

> **SAMConvFormer+LLM: Exploring synergistic fusion of Segment Anything Model with joint convolutional transformer and large language model to advance dense agricultural crop analysis**  
> *Computers and Electronics in Agriculture*, 2025  
> DOI: 10.1016/j.compag.2025.111192

📄 **Journal:** Computers and Electronics in Agriculture (2025)  
🔗 **Paper:** [ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0168169925012980)  
📂 **Dataset:** [Figshare (DOI placeholder)](https://doi.org/10.6084/m9.figshare.XXXXX) *(uploaded; under admin approval)*  

---

### 💡 About this repo

This repository contains the **official implementation** of **SAMConvFormer+LLM**, a framework that:

- Performs **dense crop instance segmentation** in complex, real-field environments using **SAM + ConvFormer**  
- Integrates a **Large Language Model (LLM)** for **yield estimation, ripeness analysis, and crop management recommendations**  
- Provides a **real-field dense crop dataset** for benchmarking robust agricultural AI systems  

---

## 🧠 Introduction

> Accurate detection of **densely fruited crops** is essential for yield estimation, ripeness analysis, and actionable recommendations for optimized crop management using large language models. However, real-world agricultural environments present challenges such as varying illumination, diverse fruit sizes, and highly complex backgrounds, making robust detection difficult.

Existing AI models—often trained on controlled datasets—struggle to generalize to these **real-field conditions**.

To address this, we:

- Introduce a **real-field dense crop dataset** that captures practical deployment scenarios
- Propose **SAMConvFormer**, which **synergizes the Segment Anything Model (SAM)** with a **Joint Convolutional Transformer** for precise segmentation
- Integrate a **Large Language Model (LLM)** to build an **end-to-end pipeline** for:
  - Yield estimation  
  - Ripeness and quality assessment  
  - Adaptive crop management recommendations  

Our model achieves:

- **79.32% Sensitivity**  
- **62.64% IoU**  
- **77.03% Dice Coefficient**

These correspond to relative improvements of **31%**, **18.79%**, and **11.56%** over a strong baseline, demonstrating **robustness and precision** for densely fruited crop detection in the wild.

---

## 🔥 News / TODO

- ✅ Paper accepted in **Computers and Electronics in Agriculture (2025)**  
- ✅ Dataset uploaded to **Figshare** (awaiting admin approval)  
- ⏳ Release cleaned training & evaluation code  
- ⏳ Release pretrained checkpoints of SAMConvFormer on the dense crop dataset  
- ⏳ Release example scripts for LLM-based crop management recommendations  
- ⏳ Add full documentation and config files for reproduction  

---

## 🌱 Key Contributions

1. **Bridging AI and Field Expertise**  
   Developed in collaboration with **agricultural field experts** to ensure practical, interpretable, and deployable solutions.

2. **SAMConvFormer: Joint Conv–Transformer Segmentation**  
   A novel framework that **combines SAM** with a **Joint Convolutional Transformer**, improving:
   - Boundary delineation of overlapping fruits  
   - Robustness to illumination, occlusion, and clutter  

3. **LLM-Integrated Crop Management Pipeline**  
   An LLM consumes structured outputs from the segmentation module to provide:
   - Yield estimation  
   - Ripeness & quality analysis  
   - **Adaptive, text-based management recommendations** for precision agriculture  

4. **Comprehensive Ablation Study**  
   Detailed analysis of:
   - SAM vs. non-SAM baselines  
   - Transformer vs. pure convolution backbones  
   - Fusion strategies for SAM + ConvFormer  

5. **Open Research Resource**  
   Planned release of:
   - Real-field dense crop dataset  
   - SAMConvFormer implementation  
   - LLM pipeline scripts & prompts  

---

## 🩺 Framework

> **Overview of the SAMConvFormer+LLM pipeline.** SAM first provides robust object proposals and coarse masks. A Joint Convolutional Transformer refines these masks, enhancing boundary sharpness and instance separation in dense clusters. The resulting instance-level features are aggregated and passed to an LLM, which performs yield estimation, ripeness analysis, and generates actionable crop management recommendations.

<p align="center">
  <img src="https://github.com/user-attachments/assets/f7b31d25-66a5-4a36-bcfa-5a424484d205" alt="Workflow of the proposed SAMConvFormer+LLM framework" width="80%">
</p>

**Pipeline steps (high level):**

1. **Input Acquisition**  
   Real-field RGB (or multispectral) images of dense crop clusters.

2. **SAMConvFormer Segmentation**  
   - **SAM**: generates initial region proposals and coarse masks  
   - **ConvFormer**: refines boundaries, handles occlusion & density, improves shape consistency  

3. **Feature Extraction & Aggregation**  
   - Per-instance features: area, shape, texture, color, spatial distribution  
   - Field-level statistics: fruit counts, density maps, maturity distributions  

4. **LLM-Based Reasoning**  
   - Encodes features into a structured prompt  
   - LLM outputs:
     - Yield estimates  
     - Ripeness distribution  
     - Actionable recommendations (harvesting windows, thinning hints, irrigation/fertilizer suggestions, etc.)  

---

## 📂 Dataset

We introduce a **real-field dense crop dataset** designed to stress-test segmentation and reasoning models under realistic agricultural conditions.

**Characteristics:**

- Diverse **illumination conditions**: shadows, glare, overcast, harsh sunlight  
- **Dense occlusions**: overlapping fruits, leaves, branches  
- Variations in **fruit size, color, and maturity**  
- Complex **backgrounds**: soil, sky, nets, wires, support structures  

📁 **Dataset DOI (Figshare):**  
> `https://doi.org/10.6084/m9.figshare.XXXXX` *(placeholder – replace with final DOI once approved)*  

> The dataset is **uploaded and under Figshare admin approval**. Once the DOI is active, this repository will be updated accordingly.  

---

## 🧩 Keywords

- Precision Agriculture  
- Densely Fruited Crop  
- Instance Segmentation  
- Yield Estimation  
- Joint Convolutional Transformer  
- Large Language Model  

---

## 💾 Checkpoints

> **Coming soon.**

Planned releases:

- ✅ SAMConvFormer trained on the proposed dense crop dataset  
- ⏳ Checkpoints for:
  - Segmentation-only SAMConvFormer  
  - Full SAMConvFormer+LLM pipeline (with reference prompts/configs)  

Once available, checkpoint URLs and performance tables will be added here.

---

## 🚀 Quick Start

> The following is a template. Please adjust script names and paths to match your implementation.

### 1. Environment setup

```bash
# Create conda environment
conda create -n samconvformer-llm python=3.10 -y
conda activate samconvformer-llm

# Install dependencies
pip install -r requirements.txt
