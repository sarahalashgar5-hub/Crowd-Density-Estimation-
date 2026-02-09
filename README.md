Crowd Density Estimation using ResNet18
=====================================

This project focuses on estimating crowd density levels using a deep learning
approach based on ResNet18 and PyTorch. The model predicts a continuous density
value, which is later mapped into three crowd density levels: Low, Medium,
and High.

The project demonstrates an end-to-end computer vision pipeline including
dataset creation, model training, evaluation, robustness testing, and
video-based inference.


Project Overview
----------------
Task: Crowd Density Estimation  
Approach: Regression-based deep learning model  
Backbone: ResNet18 (ImageNet pretrained)  
Framework: PyTorch  


Methodology
-----------
- Images are resized to 224 × 224
- ResNet18 is fine-tuned to output a single continuous density value
- Loss Function: Mean Squared Error (MSE)

Evaluation Metrics:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)

Density values are mapped into three classes:
- Low
- Medium
- High


Dataset
-------
The dataset was created and annotated by the author using Roboflow.

- Total images: 4,617
- Classes: Low, Medium, High crowd density

Preprocessing steps:
- Auto-orientation (EXIF information removed)
- Resize to 224 × 224

Note:
The dataset is **not included in this repository** due to size and data usage
considerations.

Dataset structure:
data/
 ├── train/
 │   ├── Low/
 │   ├── Medium/
 │   └── High/
 ├── valid/
 └── test/


Video Inference
---------------
The trained model supports video-based crowd density estimation with:

- Frame-by-frame density prediction
- Temporal smoothing for stable output
- Density level overlay on video frames


Robustness Evaluation
---------------------
The model was evaluated under multiple visual conditions to assess robustness
and real-world generalization:

- Low lighting
- Blur
- Low resolution


Technologies Used
-----------------
- Python
- PyTorch
- Torchvision
- OpenCV
- NumPy
- Scikit-learn
- Matplotlib


Author
------
Sarah Alashgar  
Artificial Intelligence Student  
Imam Abdulrahman Bin Faisal University
