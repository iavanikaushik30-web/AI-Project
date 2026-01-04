# AI-Project
Stuent Name Avani Kaushik
Student number s1147275

Project Title
Fabric Classification Using YOLOv11

Overview
You build a fabric image classification system using YOLOv11.
You use pretrained YOLOv11 weights.
You fine tune the model for fabric categories.
You prepare the dataset in YOLO format.

Environment Setup and Requirements

You run the project in Google Colab.
You use Python 3.

Required libraries.
• ultralytics
• numpy
• pandas
• matplotlib
• opencv python
• pillow
• scikit learn

Install command.
pip install ultralytics

Optional.
Google Drive mounted for dataset access.

Instructions to Reproduce Results

Step 1. Download the dataset from Kaggle.
Link. https://www.kaggle.com/datasets/orchit/the-fabrics-dataset-by-ibug

Step 2. Upload the dataset to Google Drive.

Step 3. Mount Google Drive in Colab.

Step 4. Set dataset path.
Update data_root to point to the dataset folder.

Step 5. Run the data preparation script.
This script filters categories.
It counts samples per class.
It creates train, validation, and test folders.

Step 6. Verify class distribution plot.

Step 7. Start training using YOLOv11 pretrained weights.

Steps to Train Your Own Model

Load YOLOv11 pretrained model.

yolo = YOLO("yolov11.pt")

Train the model.

yolo.train(
data="dataset.yaml",
imgsz=640,
epochs=100,
batch=16
)

Adjust epochs, batch size, and image size based on resources.

Results Summary

The model learns discriminative fabric patterns.
Training converges within limited epochs.
Balanced classes improve classification accuracy.
Pretrained weights reduce training time.

Evaluation performed on validation set.

