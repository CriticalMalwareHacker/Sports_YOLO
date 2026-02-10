# 🐍 Running Sports_YOLO with Anaconda (Windows)

This guide explains how to set up **Anaconda**, create a Python environment, install dependencies, and run the trained YOLO model locally.

## 1️⃣ Install Anaconda

1. Download Anaconda (Python 3.10+ recommended):  
   https://www.anaconda.com/products/distribution

2. Run the installer:
   - Select **“Just Me”**
   - Check **“Add Anaconda to PATH”** (optional but recommended)
   - Complete installation

3. Open **Anaconda Prompt** (not CMD or PowerShell)

Verify installation:

```bash
conda --version
```

````

---

## 2️⃣ Navigate to the Model Directory

```bash
cd path\to\Sports_YOLO
```

Example:

```bash
cd C:\Users\tanay\Downloads\my_model
```

---

## 3️⃣ Create and Activate Conda Environment

```bash
conda create -n yolo-env1 python=3.10 -y
conda activate yolo-env1
```

Verify Python:

```bash
python --version
```

---

## 4️⃣ Install Required Packages

### Install Ultralytics YOLO

```bash
pip install ultralytics
```

---

### (Optional) NVIDIA GPU Support

⚠️ **Only do this if you have an NVIDIA GPU**

```bash
pip install torch torchvision --index-url https://download.pytorch.org/whl/cu121
```

Verify CUDA:

```bash
python - <<EOF
import torch
print(torch.cuda.is_available())
print(torch.cuda.get_device_name(0) if torch.cuda.is_available() else "CPU only")
EOF
```

---

## 5️⃣ Run the YOLO Detection Script

### Using Laptop Webcam

```bash
python yolo_detect.py --model my_model.pt --source usb0 --resolution 640x480
```

### Using External USB Webcam

```bash
python yolo_detect.py --model my_model.pt --source usb1 --resolution 640x480
```

⚠️ On Windows, if `usb1` fails, try:

```bash
--source 0
--source 1
```

---

## 6️⃣ Performance Tips

- Use **640×480** instead of 1280×720 for higher FPS
- Close Zoom, Teams, OBS, or browser tabs using the camera
- Use smaller YOLO models for real-time performance

---

## 7️⃣ Common Issues

### Camera not detected

- Ensure webcam drivers are installed
- Restart Anaconda Prompt
- Try different `--source` values

### Low FPS

- Lower resolution
- Use GPU (`torch.cuda.is_available() == True`)
- Reduce visual overlays if supported

---

## ✅ Setup Complete

You are now ready to run **Sports_YOLO** using Anaconda 🎉
````
