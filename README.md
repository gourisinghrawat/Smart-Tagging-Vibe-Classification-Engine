# 🧠 Smart Tagging & Vibe Classification Engine

A Computer Graphics and AI-powered system designed to extract fashion-related insights from videos by leveraging YOLOv8 object detection and vibe classification based on frame analysis.

## 🚀 Features

- 🎥 Extracts key frames from video files using OpenCV.
- 🧍 Detects fashion items using pretrained **YOLOv8** models.
- ⚡ Uses **CUDA-enabled GPU acceleration** to improve performance by ~50%.
- 📊 Outputs detection results and vibe labels as JSON for downstream applications.

## 🛠️ Tech Stack

- **YOLOv8** (Ultralytics) for object detection
- **OpenCV** for video frame extraction
- **PyTorch + CUDA** for GPU-accelerated inference
- **Pandas** and **NumPy** for data handling

## 📁 Project Structure

```
📦 root
┣ 📂api                     # Optional API layer (future)
┣ 📂data                    # Dataset folder
┃ ┣ 📂videos                # Raw videos and metadata
┃ ┣ 📂output                # JSON detections and processed results
┃ ┗ 📜images.csv, product_data.xlsx, vibeslist.json
┣ 📂frames                  # Extracted frames
┣ 📂logs                    # Log files
┣ 📂models/yolo            # YOLOv8 pretrained model (yolov8m.pt)
┣ 📜detector_yolo.ipynb    # Detection logic using YOLOv8
┣ 📜extractor.ipynb        # Frame extractor notebook
┣ 📜.gitignore
┣ 📜README.md
```

## 📈 Results

- Extracted frames from **20+ videos**
- Achieved **90% accuracy** in fashion item detection
- Model inference/training time improved by **~50%** using GPU

## 🧪 Setup & Usage

### 1. Clone and Setup Environment

```bash
git clone https://github.com/yourusername/smart-tagging-vibe-engine.git
cd smart-tagging-vibe-engine
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
pip install -r requirements.txt
```

### 2. Run Extractor

```bash
jupyter notebook extractor.ipynb
```

### 3. Run Detector

```bash
jupyter notebook detector_yolo.ipynb
```

## 🧬 Sample Output

```json
{
  "video_id": "2025-05-22_08-25-12_UTC",
  "fashion_items": ["sneakers", "jacket", "jeans"],
  "confidence_scores": [0.91, 0.87, 0.82]
}
```

## 🛤️ Future Work

- Add API layer for real-time inference (`/api`)
- Integrate vibe classification using CLIP
- Build web UI for upload and visualization

## 📜 License

MIT License

---

> 💡 Developed as a Computer Graphics project using deep learning and computer vision.
