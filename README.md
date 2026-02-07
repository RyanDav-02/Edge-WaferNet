# Edge-WaferNet V2+: High-Efficiency Wafer Defect Classifier
**Phase 1 Submission for IESA DeepTech Hackathon & NXP Vision Design Challenge**

Edge-WaferNet V2+ is an integrated AI system designed for real-time semiconductor wafer defect classification. Optimized specifically for **NXP i.MX hardware**, the system utilizes Depthwise Separable Convolutions to achieve high-precision classification (90%+) with a footprint minimal enough for edge deployment.



## 🚀 Key Features
- **NXP eIQ Ready:** Architecture designed for seamless quantization and deployment using NXP's eIQ™ Inference specialized kernels.
- **Hardware-Efficient CNN:** Utilizes Depthwise Separable Convolutions to reduce FLOPs while maintaining high feature extraction capability.
- **Confidence-Aware Gating:** Integrated logic to reject low-confidence predictions (>0.90 threshold), ensuring high reliability in industrial manufacturing.
- **Nanoscale Preprocessing:** Custom median filtering pipeline to remove industrial sensor noise without blurring critical defect boundaries.

## 📊 Performance Metrics (Phase 1)
| Metric | Result |
| :--- | :--- |
| **Weighted Precision** | **97.52%** (Confidence-Gated) |
| **Weighted Recall** | **97.86%** |
| **Coverage Retained** | **69.59%** |
| **Model Format** | **ONNX (Open Neural Network Exchange)** |
| **Edge Footprint** | **~2.4 MB** |



## 📁 Repository Contents
- `edge_wafernet_v2_plus.py`: Finalized integrated script for training, data cleaning, and ONNX export.
- `edge_wafernet_v2_plus.onnx`: The hardware-ready model artifact (Serialized for NXP deployment).
- `LSWMD.pkl`: Dataset reference (ensure path consistency for the script).



# Edge-WaferNet V2+: Semiconductor Defect Classification

![Python](https://img.shields.io/badge/Python-3.12-blue.svg)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.16+-orange.svg)
![ONNX](https://img.shields.io/badge/ONNX-Standard-blueviolet.svg)

Edge-WaferNet V2+ is an end-to-end deep learning pipeline designed to identify and classify spatial defect patterns in semiconductor wafer maps. It features a high-efficiency CNN architecture optimized for edge deployment using the ONNX format.


## 📊 Dataset: WM-811K (LSWMD)
The model is trained on the **WM-811K** dataset, which consists of 811,457 wafer maps collected from real-world fabrication tools.
* **Source:** [Kaggle WM-811K Dataset](https://www.kaggle.com/datasets/qingyi/wm811k-wafer-map)
* **Defect Classes:** Center, Donut, Edge-Loc, Edge-Ring, Loc, Random, Scratch, and Near-full.



## 🛠️ Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/Edge-WaferNet-V2.git](https://github.com/YOUR_USERNAME/Edge-WaferNet-V2.git)
   cd Edge-WaferNet-V2

## 🏷️ Technical Tags
`Edge-AI` `NXP-iMX` `Semiconductor-Manufacturing` `Computer-Vision` `ONNX` `TinyML`

## 🛠️ Implementation Strategy
The model is exported in **ONNX format (Opset 13)** to ensure maximum compatibility with the NXP eIQ toolkit. By converting to ONNX, the model is prepared for subsequent quantization (INT8/FP16) to leverage the hardware accelerators on i.MX series processors.
