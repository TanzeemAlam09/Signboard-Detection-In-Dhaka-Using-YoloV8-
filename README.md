This repository contains a project aimed at detecting signboards in Dhaka city using the YOLOv8 object detection model.
The system is designed to identify signboards with high accuracy and handle scenarios with overlapping signboards. 
It is built on a robust dataset collected from the city and can be extended for further improvements, including night-time detection.

Features

High Accuracy: Detects signboards in urban environments with strong precision.

Overlap Detection: Identifies and handles overlapping signboards effectively.

Customizable Training: Retrain the model with new data to enhance performance or adapt to specific needs.

Dataset

The dataset used for this project includes:

3,500 images: Collected by BRAC University students.

500 images: Captured personally from various locations in Dhaka.

You can extend the dataset by adding more images to improve model accuracy and diversity. Future plans include working on detection in night-time settings.

**Getting Started**

**Prerequisites**

Python 3.8+

YOLOv8 Installation: Install the Ultralytics YOLOv8 package. You can follow their installation guide.

Dependencies: Install required Python libraries:

pip install -r requirements.txt

Dataset Preparation

Organize the dataset into folders for training, validation, and testing.

dataset/
|-- train/
|-- val/
|-- test/

Annotate images using tools like LabelImg or Roboflow.

Training the Model

Clone this repository:

git clone https://github.com/TanzeemAlam09/signboard-detection-yolov8.git
cd signboard-detection-yolov8

Train the YOLOv8 model:

yolo task=detect mode=train data=data.yaml model=yolov8n.pt epochs=50 imgsz=640

Replace yolov8n.pt with your desired YOLOv8 model variant.

Modify data.yaml to point to your dataset.

Inference

**Use the trained model to detect signboards:**

yolo task=detect mode=predict model=best.pt source=your_image_or_video_path

Results

Detection Accuracy: The model achieves high accuracy in detecting signboards in Dhaka city, even in complex scenarios.

Overlap Handling: Successfully identifies and separates overlapping signboards.

Future Improvements

Night-Time Detection: Extend the dataset and train the model for signboard detection under low-light conditions.

Further Dataset Expansion: Add more diverse images from different times, weather conditions, and locations.

Contributing

Contributions are welcome! To contribute:

Fork this repository.

Create a new branch for your feature or bugfix.

Submit a pull request with a detailed description of your changes.

**Acknowledgments**

BRAC University Students: For their contributions in collecting the majority of the dataset.

Ultralytics: For providing the YOLOv8 model.

**Contact**

For questions or suggestions, feel free to reach out at [tanzeemrahhe511@gmail.com].
