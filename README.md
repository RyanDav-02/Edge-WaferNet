# Edge-WaferNet V2+: High-Efficiency Wafer Defect Classifier

**Phase 1 Submission for IESA & NXP Vision Design Challenge**

Edge-WaferNet V2+ is an integrated AI system designed for real-time semiconductor defect classification. Optimized for **NXP i.MX hardware**, it utilizes Depthwise Separable Convolutions to achieve high accuracy with a low computational footprint.

## 🚀 Key Features
- **Integrated Architecture:** Consolidated hybrid model for 8 defect classes.
- **Hardware Optimized:** Exported to **ONNX format** for seamless NXP eIQ deployment.
- **Precision Engineering:** Includes Nanoscale Median Filtering for high-fidelity denoising.

## 📊 Performance Metrics
| Metric | Result |
| :--- | :--- |
| **Weighted Accuracy** | **89.2%** |
| **Weighted Precision** | **89.1%** |
| **Weighted Recall** | **89.0%** |
| **Model Size** | **~2.4 MB** |

## 📂 Repository Contents
- `edge_wafernet_v2_plus.py`: Complete training, evaluation, and ONNX export script.
- `edge_wafernet_v2_plus.onnx`: The final trained model file.
- `requirements.txt`: Environment dependencies.

## 🛠️ Deployment
The model is compatible with the NXP eIQ toolkit. To run inference:
1. Install dependencies: `pip install -r requirements.txt`
2. Execute the script to train or verify the ONNX export.
