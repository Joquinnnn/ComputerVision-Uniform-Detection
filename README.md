# Deteksi Atribut Seragam Sekolah (School Uniform Attribute Detection)

This project is a computer vision application that detects school uniform attributes (Dasi/Tie, Logo Sekolah/School Badge, Topi/Hat, and Ikat Pinggang/Belt) in real-time using a webcam feed. It utilizes Histogram of Oriented Gradients (HOG) features and a Support Vector Machine (SVM) classifier to identify the objects through a sliding window approach.

## Features
- Detects the following attributes:
  - Dasi (Tie)
  - Logo Sekolah (School Badge)
  - Topi (Hat)
  - Ikat Pinggang (Belt)
- Real-time webcam integration.
- Facial region exclusion to reduce false positives (using OpenCV Haar Cascades).
- Custom Non-Maximum Suppression (NMS) for refining overlapping bounding boxes.

## Dataset
This project uses the **Deteksi Seragam** dataset from Roboflow. The dataset contains images of students with bounding box annotations for the uniform attributes.

**Dataset Link:** [Deteksi Seragam Dataset on Roboflow](https://universe.roboflow.com/skripsi-gztjx/deteksi-seragam/dataset/1)

### How to Download the Dataset in Pascal VOC XML Format
To run the training script successfully, you need the dataset annotated in **Pascal VOC XML** format. Follow these steps:

1. Click on the Dataset Link above. Create a free account or log in to Roboflow if you haven't already.
2. Navigate to the **Dataset** tab of the project.
3. Click on the **Download Dataset** button located in the top right area of the page.
4. In the "Format" dropdown menu, select **Pascal VOC**.
5. Select the **Download zip to computer** option (or obtain the download code if you prefer to download it directly via CLI/script).
6. Once the zip file is downloaded, extract it.
7. You should see `train`, `valid`, and `test` folders containing both the `.jpg` images and the `.xml` annotations.
8. Move these `train`, `valid`, and `test` folders directly into the root directory of this project.

# To Run the application just run it in visual studio code and the model will automatically trained (the training should be around 5-10 minutes) but make sure you guys allowed the camera on