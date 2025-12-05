# 🌾 SAMConvFormer+LLM: Exploring synergistic fusion of Segment Anything Model with joint convolutional transformer and large language model to advance dense agricultural crop analysis

**Muhammad Owais**, *Israa Fahmy, Lakmal Seneviratne, Irfan Hussain*  
*Khalifa University Center for Autonomous Robotic Systems (KUCARS), United Arab Emirates*

📄 **Published in:** Computers and Electronics in Agriculture (2025)  
🔗 **Paper link:** [ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0168169925012980)  
📂 **Dataset:** [Available on Figshare](https://doi.org/10.6084/m9.figshare.XXXXX)  
*(Uploaded and currently under admin approval; the link will be accessible soon.)*

---

## 📦 About this Repository

This repository provides the **official implementation** of:

> **SAMConvFormer+LLM: Exploring synergistic fusion of Segment Anything Model with joint convolutional transformer and large language model to advance dense agricultural crop analysis**

It includes:

- Code for **dense crop instance segmentation** using SAMConvFormer  
- Integration with an **LLM-based crop management assistant**  
- Scripts for **training, evaluation, and ablation studies**  
- Links and tools for using the **real-field dense crop dataset**

---

## 🧠 Abstract

Accurate detection of **densely fruited crops** is essential for yield estimation, ripeness analysis, and actionable recommendations for optimized crop management using large language models.  
However, real-world agricultural environments present challenges like varying illumination, diverse fruit sizes, and highly complex backgrounds, making robust detection difficult.

Existing AI models—trained on controlled datasets—struggle to generalize to real-field conditions.  
To address this, we introduce a **real-field dataset** that captures the complexities of dense crops and propose a novel **SAMConvFormer** framework that **synergizes the Segment Anything Model (SAM)** with a **Joint Convolutional Transformer**.

This fusion enhances **boundary delineation** for overlapping, blurred, and irregular fruit structures.  
Further integration with a **Large Language Model (LLM)** provides a comprehensive pipeline for **yield estimation, ripeness analysis**, and **adaptive crop management recommendations**.

Our model achieves:

- **79.32% Sensitivity**  
- **62.64% IoU**  
- **77.03% Dice Coefficient**

These represent relative improvements of **31%, 18.79%, and 11.56%** over the baseline model, confirming the robustness and precision of our approach for densely fruited crop detection.

---

## 🌱 Key Contributions

1. **Bridging AI and Field Expertise**  
   Integrates direct input from agricultural field experts to ensure practical and explainable solutions.

2. **Novel SAMConvFormer Framework**  
   Combines the **Segment Anything Model (SAM)** with a **Joint Convolutional Transformer** for effective detection of dense crops under complex conditions.

3. **LLM-Integrated Crop Management Pipeline**  
   Incorporates an **LLM** for **yield estimation**, **ripeness analysis**, and **actionable recommendations**, enabling **adaptive decision support** in precision agriculture.

4. **Comprehensive Ablation Study**  
   Demonstrates how each component—SAM, transformer, and convolutional fusion—contributes to overall performance gains.

5. **Open Research Resource**  
   The full **framework, dataset, and materials** will be publicly released to advance dense crop segmentation and support future agricultural AI innovations.

---

## ⚙️ Workflow of the Proposed Framework

**Figure:** Workflow of the proposed SAMConvFormer + LLM pipeline  

![Workflow of the proposed framework](https://github.com/user-attachments/assets/f7b31d25-66a5-4a36-bcfa-5a424484d205)

**Pipeline Overview (High-Level):**

1. **Input Acquisition**  
   - Real-field RGB (or multi-spectral) crop images with densely clustered fruits.  

2. **SAMConvFormer-based Segmentation**  
   - **SAM** provides robust object proposals and coarse masks.  
   - A **Joint Convolutional Transformer** refines boundaries and structures for overlapping and irregular fruit clusters.  

3. **Post-processing & Feature Extraction**  
   - Extracts per-fruit instance statistics: area, count, shape descriptors, color/texture cues.  

4. **LLM-Driven Reasoning & Recommendations**  
   - Encodes these statistics into a structured prompt.  
   - An **LLM** performs:
     - Yield estimation  
     - Ripeness and quality analysis  
     - Generation of **actionable management recommendations** (e.g., harvesting schedule, thinning, irrigation/fertilization hints).  

---

## 📂 Dataset

We introduce a **real-field dense crop dataset**, capturing challenging scenarios such as:

- Varying illumination and shadows  
- Occlusions and overlapping fruit clusters  
- Diverse fruit sizes, shapes, and maturities  
- Complex backgrounds (leaves, branches, soil, sky, wires, etc.)

📂 **Dataset link:** [Figshare DOI](https://doi.org/10.6084/m9.figshare.XXXXX)  
> The dataset has been uploaded to Figshare and is currently under **admin approval**.  
> Once approved, the link will become fully accessible to the public.

(Please open a GitHub issue if you experience any problems accessing the dataset.)

---

## 🧩 Keywords

- Precision Agriculture  
- Densely Fruited Crop  
- Yield Estimation  
- Joint Convolutional Transformer  
- Large Language Model  

---

## 🛠️ Installation

> **Note:** The exact environment and dependencies will be added once the full codebase is released.  
> Below is a generic setup template you can adapt.

```bash
# Clone the repository
git clone https://github.com/Owais-CodeHub/SAMConvFormer-LLM.git
cd SAMConvFormer-LLM

# (Optional) Create a conda environment
conda create -n samconvformer-llm python=3.10 -y
conda activate samconvformer-llm

# Install dependencies
pip install -r requirements.txt
