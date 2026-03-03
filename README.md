🌾 Reverse Weed Detection in Paddy Plants
Capstone Project – B.Tech CSE | PES University (Aug–Dec 2025)

A deep learning–based precision agriculture system that detects paddy plants first and then identifies weeds as remaining vegetation using a novel reverse detection approach.

📌 Project Overview

Weed control is one of the biggest challenges in rice farming. Traditional methods:

❌ Manual weeding – Labor intensive

❌ Herbicides – Environmentally harmful

❌ Direct weed detection – Requires multi-class weed datasets

This project introduces a Reverse Weed Detection Strategy:

🌱 Detect Paddy Plants → Mask Paddy Regions → Extract Remaining Green Regions as Weeds

This reduces dataset complexity and improves recall in real-field conditions.

🚀 Key Highlights

✅ Faster R-CNN (ResNet-50 + FPN) for paddy detection

✅ Multi-scale detection for better recall

✅ HSV + Vegetation Index (ExG, Green Ratio) based weed segmentation

✅ Reverse detection pipeline (Crop-first approach)

✅ Region-based and Pixel-based evaluation metrics

✅ Threshold tuning analysis

🏗️ System Architecture
Input Image
     ↓
Preprocessing (Resize, Normalize, Augment)
     ↓
Faster R-CNN (Detect Paddy Plants)
     ↓
Generate Paddy Mask
     ↓
Vegetation Mask (ExG + HSV Threshold)
     ↓
Subtract Paddy Mask
     ↓
Final Weed Segmentation Output
🧠 Model Details
Paddy Detection

Model: Faster R-CNN

Backbone: ResNet-50 FPN

Classes:

0 → Background

1 → Paddy Plant

Multi-scale detection: 1.0, 1.25, 1.5, 2.0

NMS for duplicate removal

Weed Segmentation

ExG (Excess Green Index)

HSV Thresholding

Morphological Refinement

Paddy mask subtraction

📊 Dataset Details

Field images collected in real agricultural environments

Categories:

Only Paddy

Only Weeds

Mixed Images

Annotation tool: Roboflow

Format: COCO

Train/Val/Test Split:

70% Training

20% Validation

10% Testing

📈 Performance Results
Metric	Score

Recall	0.8500

Accuracy	0.8976
🔎 Interpretation

High Recall → Most weeds detected (important in agriculture)



⚙️ Tech Stack
💻 Programming Language

Python 3.8+

🔬 Libraries & Frameworks

PyTorch

Torchvision

OpenCV

Pycocotools

Pandas

Matplotlib

tqdm

Roboflow (dataset preparation)

🖥️ Hardware Requirements
Minimum

GPU: GTX 1650 / RTX 2060 (6–8GB)

RAM: 8–16GB

CPU: Intel i5 / Ryzen 5

OS: Windows 10

Recommended

GPU: RTX 3060 / 4070+

RAM: 32GB

CUDA-enabled system

🧪 Evaluation Metrics
Detection Metrics

Precision

Recall

F1-Score

mAP

Segmentation Metrics

IoU (Intersection over Union)

Dice Coefficient

Pixel-level Accuracy

📂 Project Structure (Suggested)
Reverse-Weed-Detection/
│
├── dataset/
├── models/
├── training/
├── testing/
├── utils/
├── results/
├── checkpoints/
└── README.md
🎯 Why Reverse Detection?

Instead of detecting multiple weed species:

✔ Requires only Paddy annotation
✔ Works under natural field lighting
✔ Reduces annotation complexity
✔ Scalable to large farms
✔ Suitable for precision agriculture

🔮 Future Work

Instance Segmentation (Mask R-CNN)

Hybrid deep learning + color index models

Drone-based deployment

Testing across growth stages

Real-time embedded deployment

👨‍💻 Team Members

Saiganesh

Shashank Kote

Shilpa M Talawar

Spandana M Poojary



📜 License

This project is developed for academic and research purposes (Capstone Project – PES University).
