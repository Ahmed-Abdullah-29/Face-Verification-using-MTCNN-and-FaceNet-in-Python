# Face-Verification-using-MTCNN-and-FaceNet-in-Python
A face verification project that detects faces with MTCNN, extracts embeddings using FaceNet, and compares two uploaded images with Euclidean distance to determine whether they belong to the same person. Built in Python for Google Colab with image preprocessing and similarity scoring.
## Project Overview

Face verification is different from general image classification.  
Instead of predicting one class from many categories, this project compares **two face images** and checks whether they represent the same identity.

This notebook is designed for **Google Colab** and follows a practical workflow:

1. Upload two face images
2. Detect the face region using **MTCNN**
3. Crop and resize each face
4. Generate embeddings using **FaceNet**
5. Normalize the embeddings
6. Compute Euclidean distance
7. Decide whether both faces match based on a threshold

---

## Features

- Upload and compare **two face images**
- Automatic **face detection**
- Face cropping and resizing
- Deep feature extraction using **FaceNet**
- Euclidean distance-based similarity comparison
- Simple **same person / different person** decision
- Similarity score output

---

## Technologies Used

- **Python**
- **Google Colab**
- **NumPy**
- **Matplotlib**
- **OpenCV**
- **Pillow**
- **MTCNN**
- **keras-facenet**

---

## Workflow

### 1. Image Upload
The notebook asks the user to upload exactly **two images** in JPG or PNG format.

### 2. Face Detection
The **MTCNN** model detects faces in both images and selects the largest detected face.

### 3. Face Preprocessing
Each detected face is cropped and resized to **160 × 160 pixels**, which is the required input size for FaceNet.

### 4. Embedding Extraction
The cropped faces are passed through **FaceNet**, which converts each face into a numerical vector called an **embedding**.

### 5. Similarity Comparison
The embeddings are normalized and compared using **Euclidean distance**.

### 6. Verification Decision
A threshold is applied to determine whether both images belong to the **same person** or **different people**.

---

## Example Output

- **Embedding distance:** numeric similarity value  
- **Verification result:** SAME PERSON or DIFFERENT PERSON  
- **Similarity score:** value between 0 and 1  

---

## Project Structure

```bash
