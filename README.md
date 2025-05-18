# fire-smoke-detection-yolov8
# 🔥 Fire & Smoke Detection with YOLOv8

This project trains a YOLOv8 object detection model on a diverse dataset of fire and smoke images using Google Colab. The dataset is sourced and preprocessed using Roboflow, and training is done with Ultralytics' YOLOv8 framework.

---

## 📌 Overview

- **Goal**: Detect and distinguish between fire and smoke
- **Model**: YOLOv8 (pretrained `yolov8s.pt`)
- **Dataset**: Roboflow-sourced, merged classes (`fire`, `smoke`)
- **Training Platform**: Google Colab (GPU)

---

## 🗃 Dataset

- Fetched from Roboflow with API
- Original labels cleaned and merged (`Fire`, `fire` → `fire`, `smoke` retained)
- Split into:
  - `Train`: 4000 images
  - `Validation`: 400
  - `Test`: 200

---

## 🚀 Training Details

- Epochs: 150
- Image size: 640×640
- Batch size: 16 (auto-adjusted if memory runs out)
- Optimizer: Auto
- Augmentation: Mosaic disabled in last 10 epochs
- Tracking: ClearML (optional)
- Early stopping & cosine LR scheduling used

---

## 📊 Results

- mAP@0.5 and mAP@0.5:0.95 reported
- Visualizations:
  - Bounding box predictions
  - Precision, recall, loss curves
  - Confusion matrix
- Models and logs saved to both Google Drive and `.zip` for download



## 📂 Files

- `latest_yolov8.ipynb`: Main notebook
- `runs/`: Training outputs
- `FireSmokeSubset/`: Processed dataset
- `results.csv`: Training metrics
- 
## 👩‍💻 Author

Shamsia — Final year project on AI-based fire/smoke detection systems
