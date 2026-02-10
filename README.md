# 🏏 Sports_YOLO

A custom **YOLO-based object detection project** trained to recognize different sports in images and live video streams.

This project focuses on detecting the following sports:

- 🏸 Badminton
- ⚽ Football
- 🏉 Rugby
- 🤾 Takraw

The model is trained using **Ultralytics YOLO** and supports both **offline inference** and **real-time webcam detection**.

---

## 📌 Features

- Custom-trained YOLO model for sports detection
- Google Colab–based training pipeline (no local GPU required)
- Dataset preprocessing, train/validation split, and evaluation
- Real-time inference using laptop or external webcam
- Easy-to-run CLI commands for prediction

---

## 🧠 Model & Training

- Framework: **Ultralytics YOLO**
- Task: Object Detection
- Classes: 4 (Badminton, Football, Rugby, Takraw)
- Training environment: **Google Colab (GPU-enabled)**
- Input size: Configurable (recommended: 640×640 for performance)

---

## 📓 Google Colab Notebook

The complete training and setup process is available in the Colab notebook below:

🔗 **Colab Notebook:**  
https://colab.research.google.com/drive/1WZgHgsaUX3UblBSPTaLqpb406wVQTUeo?usp=sharing

The notebook includes:

- Dataset upload and extraction
- Folder structure setup
- `data.yaml` configuration
- Training and validation
- Model evaluation and export

---

## 📂 Dataset Structure
