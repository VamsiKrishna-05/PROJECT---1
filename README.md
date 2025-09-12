# 🚗 Embedded AI In-Cabin Passenger Monitoring System

An **embedded AI system** for monitoring passengers inside autonomous vehicles.  
The project focuses on **detecting passengers, recognizing their in-cabin activities, and specifically identifying mobile phone usage** to improve safety and reduce distractions.  

---

## ✨ Features
- **👤 Person Detection** – Detects multiple passengers inside the vehicle cabin using **YOLOv8**.  
- **📱 Mobile Usage Recognition** – Identifies if a passenger is using a mobile phone by detecting persons + phones.  
- **🔎 Activity Classification** – A CNN classifier distinguishes between:
  - **Using Mobile**  
  - **Not Using Mobile**  
- **📂 Dataset Handling** – Processes real-world cabin images, labeled for training/testing.  
- **📊 Performance Metrics** – Reports **Accuracy, F1-score, Precision, and Recall**.  
- **🖼️ Visual Outputs** – Annotated images showing bounding boxes for passengers and mobile usage.  

---

## 📁 Dataset Structure
The dataset `using_mobile/` contains cabin images labeled as mobile usage (1) or not (0).  

```text
using_mobile/
    img001.jpg
    img002.jpg
    ...
labels_dict = {
  'img001.jpg': 1,  # Using Mobile
  'img002.jpg': 0,  # Not Using Mobile
}
```
🛠️ Technologies Used

Python 3

YOLOv8 (Ultralytics) – Passenger & phone detection

TensorFlow / Keras – CNN for activity classification

OpenCV & Matplotlib – Image processing & visualization

🚀 How to Run
1. Clone the repository
```
git clone https://github.com/yourusername/in-cabin-monitoring.git
cd in-cabin-monitoring
```
3. Install dependencies
```

pip install ultralytics tensorflow opencv-python-headless matplotlib scikit-learn
```
5. Run detection
Use YOLOv8 scripts in /detection/ to detect persons and mobile phones inside images.

7. Train CNN model
Run the provided script/notebook to classify Using Mobile vs Not Using Mobile:

```
python train_cnn.py
📂 Project Structure
text
Copy code
/using_mobile/               # Dataset of cabin images
/detection/                  # YOLO scripts for person & phone detection
/train_cnn.py                # CNN training script
/utils.py                    # Data loading & preprocessing utilities
/readme.md                   # Project documentation
```
📊 Results
✅ Reliable passenger detection with YOLOv8

📱 CNN Classifier achieves strong performance on mobile usage detection

🖼️ Visualization with bounding boxes highlighting detected mobile use

🔮 Future Work
Extend to video-based action recognition (LSTM / 3D CNN).

Improve phone detection with fine-tuned in-cabin annotations.

Expand monitoring to other activities (seatbelt usage, distraction detection).

Implement semi-supervised dataset annotation.

📚 References
YOLOv8 - Ultralytics

TensorFlow

MediaPipe Pose & Hands



Scikit-learn – Metrics and evaluation

Google Colab – Development and experimentation
