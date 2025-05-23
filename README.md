# Human-Emotion-recognition-using-YOLO-v8-and-roboflow

This project provides a comprehensive solution for performing human action detection using YOLOv8, a powerful object detection model, integrated with the Roboflow platform for efficient dataset management. Human action detection is a vital task in computer vision, with applications ranging from video surveillance to human-computer interaction.

## Introduction

Human action detection involves detecting and classifying human actions or activities in videos or image sequences. This project utilizes YOLOv8, an efficient and accurate object detection model, to detect humans in images and classify their actions. By leveraging Roboflow, a platform for managing computer vision datasets, the project streamlines the dataset preparation process, making it easier to train and deploy robust action detection models.

## Features

- **Efficient Human Detection**: Utilizes YOLOv8 for real-time and accurate human detection.
- **Action Classification**: Classifies human actions or activities detected in images or videos.
- **Roboflow Integration**: Seamless dataset management and preprocessing with Roboflow.
- **Scalability**: Can be scaled for large datasets and real-time applications.

## Tech Stack

- **Python**: Core language for the project.
- **Ultralytics YOLO**: Object detection library for implementing YOLOv8.
- **Roboflow**: Dataset management platform for preprocessing and versioning.
- **matplotlib**: Data visualization library for creating plots and graphs.

## Dataset Information

- **Images**: Training - 1470, Validation - 140, Test - 70.
- **Preprocessing**:
  - **Auto-Orient**: Applied
  - **Resize**: Stretch to 640x640
- **Augmentations Outputs per training example**:
  - **Flip**: Horizontal
  - **Grayscale**: Apply to 15% of images
  - **Blur**: Up to 1px
  - **Noise**: Up to 5.01% of pixels
### Backend (Training)

1. **Installation**: Install required libraries using pip. Open your terminal or command prompt, navigate to your project directory, and run the following command:
   
   ```bash
   pip install -r requirements.txt
   ```

2. **Dataset Retrieval**: Retrieve the dataset from Roboflow Universe by following these steps:
   
   - Visit [Roboflow Universe](https://universe.roboflow.com/).
   - Search for the desired dataset using keywords or browse through the categories.
   - Once you find the dataset, click on it to view details.
   - Follow the instructions to download the dataset in YOLOv8 format.

3. **Training**: Train the YOLOv8 model using the downloaded dataset. 

## Instructions on Running the App

1. **Backend (Training)**:
    - Setup Roboflow account and download dataset in YOLOv8 format.
    - Train the YOLOv8 model using the provided code snippets:

    ```python
    from roboflow import Roboflow
    from ultralytics import YOLO

    # Replace 'YOUR_API_KEY' with your actual Roboflow API key
    api_key = "YOUR_API_KEY"
    rf = Roboflow(api_key)

    # Replace 'YOUR_WORKSPACE' and 'YOUR_PROJECT' with your Roboflow workspace and project names
    workspace_name = "YOUR_WORKSPACE"
    project_name = "YOUR_PROJECT"
    project = rf.workspace(workspace_name).project(project_name)

    # Download the dataset associated with version 1 of the project using YOLOv8 format
    version = 1
    form = "yolov8"
    dataset = project.version(version).download(form)


## requirements.txt

```
ultralytics
roboflow
glob2
matplotlib
```

