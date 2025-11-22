# 🔫 Weapon Detection Using AI and Deep Learning

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green.svg)
![YOLOv3](https://img.shields.io/badge/YOLOv3-Deep%20Learning-red.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

An Industrial Oriented Mini Project designed to automatically detect harmful weapons (guns, knives) in real-time CCTV footage and video streams using state-of-the-art Deep Learning algorithms.

---

## 📋 Project Overview

Security and safety are crucial in today's world. Traditional CCTV monitoring relies heavily on human supervision, which can be prone to error due to fatigue. This project automates the surveillance process by leveraging **Deep Learning (specifically YOLOv3)** to detect weapons with high precision and recall in real-time.

### ✨ Key Features

- ✅ Detection of weapons (Guns/Knives) in video files
- ✅ Real-time detection via Webcam
- ✅ Bounding box visualization with confidence scores
- ✅ Built using YOLOv3 architecture
- ✅ Easy-to-use command-line interface

---

## 🛠️ System Requirements

### Hardware
- **Processor:** Intel i3 and above
- **RAM:** 4GB or Higher
- **Hard Disk:** 500GB Minimum

### Software
- **OS:** Windows 8/10/11 (or Linux/macOS)
- **Language:** Python 3.x
- **Libraries:** OpenCV, NumPy

---

## ⚙️ Installation

### Step 1: Clone the Repository
```bash
git clone https://github.com/yourusername/weapon-detection-ai.git
cd weapon-detection-ai
```

### Step 2: Install Python
Ensure Python 3.x is installed and added to your system PATH.

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

**Contents of `requirements.txt`:**
```
opencv-python
numpy
```

---

## 📥 Setup: Model Weights (Critical Step)

⚠️ **Important:** The Deep Learning model requires pre-trained weights to function. The weights file (`yolov3_training_2000.weights`) is too large to include directly in the repository.

### Download the Weights

👉 **[Download yolov3_training_2000.weights](YOUR_DOWNLOAD_LINK_HERE)**

### Place the File
Move the downloaded `yolov3_training_2000.weights` file into the **root directory** of this project (same folder as `weapon_detection.py`).
```
weapon-detection-ai/
├── weapon_detection.py
├── yolov3_testing.cfg
├── yolov3_training_2000.weights  ← Place here
├── requirements.txt
└── ...
```

---

## 🚀 Usage

### Run the Detection Script

1. Open your **Command Prompt (CMD)** or **Terminal**
2. Navigate to the project folder
3. Run:
```bash
python weapon_detection.py
```

### Input Options

The script will prompt:
```
Enter file name or press enter to start webcam:
```

- **For Video File:** Type the name of the video file (e.g., `ak47.mp4` or `gun1234.mp4`) and press Enter
- **For Webcam:** Simply press Enter to start the live camera feed

### Stop Detection
Press the **`Esc`** key to exit the detection window.

---

## 📂 Project Structure
```
weapon-detection-ai/
├── core_mini_project_documentation.docx  # Project Report
├── core_mini_project.pptx                # Project Presentation
├── requirements.txt                      # Python dependencies
├── weapon_detection.py                   # Main detection script
├── yolov3_testing.cfg                    # YOLOv3 network configuration
├── yolov3_training_2000.weights          # Pre-trained weights (Download)
└── README.md                             # This file
```

---

## 📊 Methodology

The system utilizes the **YOLOv3 (You Only Look Once)** algorithm for real-time object detection.

### Pipeline:
1. **Input:** Video frame or Image
2. **Processing:** Frame is passed through the Deep Neural Network (DNN) loaded via OpenCV (`cv2.dnn.readNet`)
3. **Detection:** Network identifies objects and filters them based on the "Weapon" class
4. **Output:** Non-Maximum Suppression (NMS) removes overlapping boxes, and final bounding boxes are drawn on the frame

### Why YOLOv3?
- Fast and accurate real-time detection
- Single-pass detection (processes entire image at once)
- Well-suited for embedded and real-time systems

---

## 📸 Demo

### Sample Detection Output
*Add screenshots or GIFs of your weapon detection results here*

---

## 🔧 Troubleshooting

### Common Issues:

**1. ModuleNotFoundError: No module named 'cv2'**
```bash
pip install opencv-python
```

**2. Weights file not found error**
- Ensure `yolov3_training_2000.weights` is in the project root directory
- Verify the filename matches exactly

**3. Webcam not opening**
- Check if another application is using the camera
- Try changing camera index in the code (from 0 to 1)

---

## 📜 References

- [COCO Dataset](http://cocodataset.org/)
- [YOLO: Real-Time Object Detection](https://pjreddie.com/darknet/yolo/)
- [OpenCV Documentation](https://docs.opencv.org/)

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**B. Nikhil**  
Computer Science & Engineering  
Mahaveer Institute of Science & Technology

- GitHub: [B-Nikhil](https://github.com/B-Nikhil)
- LinkedIn: [Nikhil Kumar Bogam](https://www.linkedin.com/in/nikhilbogam/)
- Email: bogamnikhil112@gmail.com

---

**Note:** This project is for educational purposes. Always comply with local laws and regulations regarding surveillance and AI deployment.
