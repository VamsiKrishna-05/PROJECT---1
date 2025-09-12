Embedded AI In-Cabin Passenger Monitoring System
Project Overview
This project implements an embedded AI system for monitoring passengers inside autonomous vehicles. The main objective is to detect passengers, recognize their activities—specifically focusing on whether passengers are using mobile phones—and improve vehicle safety by analyzing in-cabin behavior using computer vision techniques.

Features
Person Detection: Detect multiple passengers inside vehicle cabins using YOLOv8 object detection.

Mobile Usage Recognition: Detect whether a passenger is using a mobile phone by identifying person and phone bounding boxes.

Activity Classification (Mobile Usage): A CNN-based image classifier to distinguish "Using Mobile" vs. "Not Using Mobile" from cabin images.

Dataset Handling: Processes real-world image datasets captured inside vehicle cabins.

Model Training: Includes training and evaluation pipelines for mobile usage classification.

Performance Metrics: Provides accuracy, F1-score, and classification reports for activity recognition.

Dataset Structure
The dataset folder using_mobile contains images captured inside vehicle cabins showing passengers using or not using mobile phones. Images are manually labeled via a dictionary (or CSV in future).

Example labeling setup:

text
using_mobile/
    img001.jpg
    img002.jpg
    ...
labels_dict = {
  'img001.jpg': 1,  # Using Mobile
  'img002.jpg': 0,  # Not Using Mobile
}
Technologies Used
Python 3

Ultralytics YOLOv8 for person and phone detection

TensorFlow/Keras for CNN model training

OpenCV and Matplotlib for image processing and visualization

Google Colab for development and experimentation

How to Run
Clone the repository:

bash
git clone https://github.com/yourusername/in-cabin-monitoring.git
cd in-cabin-monitoring
Mount Google Drive in Colab and set the dataset path.

Install dependencies:

bash
pip install ultralytics tensorflow opencv-python-headless matplotlib scikit-learn
Run detection scripts to detect persons and mobile phones in images.

Use the provided CNN training notebook/script to train activity recognition on your labeled images.

Project Structure
text
/using_mobile/               # Dataset of images (passengers using or not using mobile)
/detection/                 # YOLO person and mobile detection scripts
/train_cnn.py               # CNN training script for mobile usage classification
/utils.py                   # Utility functions for data loading and preprocessing
/readme.md                  # Project documentation
Results
Achieved reliable person detection in cabin images using YOLOv8.

Preliminary CNN model accurately classifies mobile phone usage with metrics such as Accuracy and F1-score.

Visual demonstrations with annotated bounding boxes highlighting mobile use.

Future Work
Incorporate temporal models (LSTM/3D CNN) for video-based action recognition.

Fine-tune detection models with in-cabin specific annotations for better phone detection accuracy.

Extend activity recognition to other behaviors (e.g., seatbelt usage, distracted driving).

Automate dataset annotation with semi-supervised learning.

References
YOLOv8 - Ultralytics: https://github.com/ultralytics/ultralytics

TensorFlow - https://www.tensorflow.org/

MediaPipe Pose & Hands - https://mediapipe.dev/

Contact
Your Name
Email: your.email@example.com
GitHub: yourusername
