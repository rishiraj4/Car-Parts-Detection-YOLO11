# Car Parts Detection using YOLO11

This project implements an automated object detection system to identify 19 different car components. The model is designed to support automated damage assessment and parts inventory in automotive applications.

## 📊 Performance Metrics
The model was trained for 50 epochs using the YOLO11n (nano) architecture.

| Metric | Value |
| :--- | :--- |
| **mAP@50** | **0.6521** |
| **mAP@50-95** | **0.5098** |
| **Training Time** | ~7 Minutes (Tesla T4 GPU) |

### Class-Specific Analysis
* **Top Performing Classes:** `front_bumper` (0.989 mAP50), `hood` (0.966 mAP50), and `front_glass` (0.95 mAP50).
* **Most Challenging Class:** `left_mirror` (0.235 mAP@50-95).
* **Technical Insight:** Smaller components like mirrors and lights showed lower localization accuracy. Increasing the input resolution from 640 to 1024 is recommended for future iterations to improve pixel-level feature extraction for small objects.

## 📦 Repository Structure
- `CV_Course_Project_Rishi_Raj.ipynb`: Full training pipeline with visual detection results.
- `data.yaml`: Configuration file defining the 19 classes and dataset paths.
- `.gitignore`: Configured to exclude heavy image datasets and local checkpoints.

## 🚀 How to Run
1.  **Clone the Repo:**
    ```bash
    git clone [https://github.com/rishiraj4/Car-Parts-Detection-YOLO11.git](https://github.com/rishiraj4/Car-Parts-Detection-YOLO11.git)
    ```
2.  **Dataset:** This project uses the [Car-Parts-Segmentation](https://github.com/dsmlr/Car-Parts-Segmentation.git) dataset.
3.  **Inference:** Open the notebook in Google Colab and run the "Visualize Predictions" section to see the model in action.

## 🛠️ Tech Stack
- **Framework:** Ultralytics YOLO11
- **Language:** Python
- **Environment:** Google Colab (GPU Accelerated)
- **Libraries:** OpenCV, Matplotlib, PyYAML
