# 🚗 Dehazing and YOLOv8 Object Detection

A lightweight, real-time system that enhances foggy dashcam footage and detects road objects using YOLOv8.

## 🎯 Objective

This project aims to improve safety in autonomous and surveillance systems under poor visibility conditions by:
- Enhancing foggy dashcam footage using CLAHE-based dehazing
- Detecting objects like cars, buses, trucks, and potholes using YOLOv8
- Comparing detection accuracy between original and dehazed frames

## 🔧 Pipeline Overview

1. **Video Input** — Load real-world foggy dashcam footage
2. **Dehazing with CLAHE** — Enhance image contrast to improve visibility
3. **Object Detection** — Use YOLOv8 for detecting target classes
4. **Side-by-Side Comparison** — Show detections on both original & dehazed frames
5. **Detection Count Analysis** — Count & compare detections frame-by-frame

## 📦 Dependencies

- OpenCV
- NumPy
- Ultralytics (YOLOv8)
- Matplotlib
- Pandas

## 🛠️ Techniques Used

- **CLAHE (Contrast Limited Adaptive Histogram Equalization)** for dehazing
- **YOLOv8** pre-trained model (via Ultralytics) for object detection
- **OpenCV + Matplotlib** for video frame handling and visualization

## 📊 Performance Metrics

Based on evaluation results:
- Average Raw Detections/Frame: 564.64
- Average Dehazed Detections/Frame: 578.09
- Detection Gain: 2.38%

### Detailed Metrics:
- Precision: 0.9965
- Recall: 0.9533
- F1 Score: 0.9744

## 🚀 Usage

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Run the main pipeline:
```python
from main import process_all_videos

# Process videos in a folder
video_folder_path = "dataset1"
results = process_all_videos(video_folder_path, max_frames=20, save_visuals=True)
```

## 📝 Features

- Multiple dehazing methods available:
  - CLAHE (default)
  - Gamma Correction
  - Brightness/Contrast Adjustment
  - Histogram Equalization
  - Dark Channel Prior

- Target object classes:
  - Cars
  - Buses
  - Trucks
  - Potholes

## 📈 Results

The system shows improved detection rates in dehazed frames compared to original foggy footage, with:
- Increased detection accuracy
- Better visibility of road objects
- Real-time processing capabilities

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details. 