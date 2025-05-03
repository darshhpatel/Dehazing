# 🚗 Dehazing and YOLOv8 Object Detection

A lightweight, real-time system for enhancing foggy dashcam footage and detecting road objects using YOLOv8.

Now with support for the **D2-City dataset** for large-scale urban scene analysis.

---

## 🎯 Objective

Improve the reliability of autonomous vehicles and traffic surveillance under poor visibility by:
- Enhancing contrast in foggy frames using CLAHE-based dehazing [@clahe]
- Detecting objects like cars, buses, trucks, and potholes using YOLOv8 [@yolov8]
- Comparing detection performance between raw and dehazed frames

---

## 🔧 Pipeline Overview

1. **Video Input** — Load dashcam footage (supports custom videos + D2-City)
2. **CLAHE Dehazing** — Boost contrast for better visibility [@clahe_original]
3. **YOLOv8 Detection** — Real-time object detection [@yolov8]
4. **Side-by-Side Visualization** — Compare detections on raw vs dehazed frames
5. **Detection Analysis** — Count and evaluate object detections frame-by-frame

---

## 📦 Dependencies

- `OpenCV` [@opencv]
- `NumPy`
- `Ultralytics` (YOLOv8) [@ultralytics]
- `Matplotlib`
- `Pandas`

Install with:

```bash
pip install -r requirements.txt
