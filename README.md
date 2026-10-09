# AI-Based Body Posture Recognition System

## Project Overview

This project focuses on automated body posture classification using a hybrid deep learning and machine learning approach. It identifies human posture as **Good Posture, Forward Bending, or Backward Bending** from images using object detection and geometric feature extraction.

## Objectives

- Detect the head, nose, and full body from posture images.
- Extract spatial and geometric features from detected bounding boxes.
- Classify body posture using machine learning algorithms.
- Evaluate and compare classification performance.

## Technologies and Tools Used

- **Programming Language:** Python
- **Deep Learning / Object Detection:** YOLOv11
- **Computer Vision:** OpenCV
- **Data Processing:** NumPy, Pandas
- **Machine Learning:** Scikit-learn, XGBoost
- **Version Control:** Git, GitHub

## Dataset

A dataset containing **1,100 unrotated posture images** was collected across three categories:

1. Good Posture
2. Forward Bending
3. Backward Bending

Initially, 500 images were manually annotated with bounding boxes for the head, nose, and body. These annotated images were used to fine-tune the YOLOv11 object detection model.

The trained model was then used to generate bounding boxes for all 1,100 images.

**Dataset Download:** https://drive.google.com/drive/folders/1dx2NEENLgQtDm9d4Pdx1vQ-TG-xrKGn2

## Methodology

1. **Data Collection:** Collected 1,100 unrotated images representing three posture categories.
2. **Annotation:** Manually annotated 500 images with bounding boxes for the head, nose, and body.
3. **Object Detection:** Fine-tuned YOLOv11 to detect the required body regions.
4. **Feature Extraction:** Extracted a 14-dimensional feature vector containing 12 bounding-box features and two geometric angle features.
5. **Dataset Splitting:** Divided the dataset into training (70%), validation (20%), and testing (10%) sets using stratified sampling.
6. **Model Training:** Trained Decision Tree, Random Forest, and XGBoost classifiers.
7. **Evaluation:** Compared model performance using accuracy metrics and confusion matrices.

## Results

XGBoost achieved the highest reported test accuracy of approximately **97%** among the evaluated classifiers.

Additional experiments compared the performance of angle-only features and bounding-box-only features to understand their contributions to posture classification.

## Project Workflow

Image Input → YOLOv11 Detection → Bounding Box Extraction → Feature Engineering → Machine Learning Classification → Posture Prediction

## Applications

- Posture awareness and monitoring
- Ergonomic assessment
- Educational and workplace posture analysis

## Future Enhancements

- Extend posture classification to additional categories, such as right and left leaning.
- Develop a real-time webcam-based posture monitoring interface.
- Improve generalization using more diverse posture images.

## Author

**Eraianbu D M**

GitHub: https://github.com/eraianbudm

LinkedIn: https://www.linkedin.com/in/eraianbu-dm
