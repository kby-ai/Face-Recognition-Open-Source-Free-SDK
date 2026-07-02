# Face-Recognition-Open-Source-Free-SDK
The most powerful face recognition SDK open source for Windows and Linux (Face detection, Face landmark extraction, Face feature extraction, Face template matching)
<p align="center">
  <a href="https://play.google.com/store/apps/dev?id=7086930298279250852" target="_blank">
    <img alt="" src="https://github-production-user-asset-6210df.s3.amazonaws.com/125717930/246971879-8ce757c3-90dc-438d-807f-3f3d29ddc064.png" width=500/>
  </a>  
</p>

### Our facial recognition algorithm is globally top-ranked by NIST in the FRVT 1:1 leaderboards. <span><img src="https://github.com/kby-ai/.github/assets/125717930/bcf351c5-8b7a-496e-a8f9-c236eb8ad59e" alt="badge" width="36" height="20"></span>  
[Latest NIST FRVT evaluation report 2024-12-20](https://pages.nist.gov/frvt/html/frvt11.html)  

![FRVT Sheet](https://github.com/user-attachments/assets/16b4cee2-3a91-453f-94e0-9e81262393d7)

#### 🆔 ID Document Liveness Detection - Linux - [Here](https://web.kby-ai.com)  <span><img src="https://github.com/kby-ai/.github/assets/125717930/bcf351c5-8b7a-496e-a8f9-c236eb8ad59e" alt="badge" width="36" height="20"></span>
#### 🤗 Hugging Face - [Here](https://huggingface.co/kby-ai)
#### 📚 Product & Resources - [Here](https://github.com/kby-ai/Product)
#### 🛟 Help Center - [Here](https://docs.kby-ai.com)
#### 💼 KYC Verification Demo - [Here](https://github.com/kby-ai/KYC-Verification-Demo-Android)
#### 🙋‍♀️ Docker Hub - [Here](https://hub.docker.com/r/kbyai/face-recognition)

## Overview
This repository by [KBY-AI](https://github.com/kby-ai) enables developers to integrate accurate, AI-powered face recognition into their applications with ease. Built on advanced deep learning models, it provides high-precision face detection and recognition while ensuring complete data privacy through on-premises processing. This `SDK` is free to use, open source, and designed for fast, seamless integration into any project.<br/>

> We can customize and improve the SDK to align with customer's specific requirements.

### ◾FaceSDK(Server) Product List
  | No.      | Repository | SDK Details |
  |------------------|------------------|------------------|
  | 1        | [Face Liveness Detection - Linux](https://github.com/kby-ai/FaceLivenessDetection-Docker)    | Face Livness Detection |
  | 2        | [Face Liveness Detection - Windows](https://github.com/kby-ai/FaceLivenessDetection-Windows)    | Face Livness Detection |
  | 3        | [Face Liveness Detection - C#](https://github.com/kby-ai/FaceLivenessDetection-CSharp-.Net)    | Face Livness Detection |
  | 4        | [Face Recognition - Linux](https://github.com/kby-ai/FaceRecognition-Docker)    | Face Recognition |
  | 5        | [Face Recognition - Windows](https://github.com/kby-ai/FaceRecognition-Windows)    | Face Recognition |
  | 6        | [Face Recognition - C#](https://github.com/kby-ai/FaceRecognition-CSharp-.NET)    | Face Recognition |

### ◾Key Features
🔒 `100% On-Premises Processing`: All face detection and recognition are performed locally, ensuring that no data ever leaves your device.</br>
🔧 `Easy Integration`: Developer-friendly `API`s enable seamless integration into existing applications.</br>
🎯 `High Accuracy`: Powered by state-of-the-art deep learning models for reliable face detection and recognition.</br>
🌐 `Cross-Platform Support`: Fully compatible with both `Windows` and `Linux` environments.</br>
⚡ `Real-Time Performance`: Delivers fast, low-latency face detection and recognition for real-time applications.</br>
📱 `GPU Optional`: Optimized to run efficiently on `CPU`-only systems, with optional `GPU` acceleration for enhanced performance.</br>
🆓 `Free and Open Source`: Available at no cost under an open-source license, with no licensing fees or usage restrictions.</br>

### ◾Capabilities
👤 Face detection and bounding box extraction</br>
📍 Facial landmark detection</br>
🧠 Face feature embedding generation</br>
🔍 Face similarity comparison</br>
🖼️ Support for multiple image formats (`JPG`, `PNG`, `BMP`, and more)</br>

## How to Install SDK
1. Install `anaconda` environment if not already installed.</br>
Download [here](https://www.anaconda.com/products/distribution)
2. Create and activate `conda` environment.</br>
```bash
conda create -n kbyai python=3.9
conda activate kbyai
```
3. Install dependencies.</br>
```bash
pip install -r requirements.txt
```
4. Validate installation</br>
```bash
python run.py
```
## Quick Start
1. Basic Usage
```python
from face_recognition_sdk import FaceRecognition

# Initialize the SDK
face_sdk = FaceRecognition()

# Process an image
image_path = "path/to/your/image.jpg"
face_info = face_sdk.GetImageInfo(image_path, faceMaxCount=10)

# Compare two faces
similarity = face_sdk.get_similarity(feature1, feature2)
```
2. Sample Code Lines for Face Comparison
```python
# Compare two images
image1 = "test/1.jpg"
image2 = "test/2.png"

# Get face information from both images
faces1 = face_sdk.GetImageInfo(image1, faceMaxCount=1)
faces2 = face_sdk.GetImageInfo(image2, faceMaxCount=1)

if faces1 and faces2:
    # Compare the first face from each image
    similarity = face_sdk.get_similarity(faces1[0]['embedding'], faces2[0]['embedding'])
    print(f"Similarity: {similarity}%")
    
    # Check if it's the same person (threshold = 75)
    is_same_person = similarity >= 75
    print(f"Same person: {is_same_person}")
```
## API Reference
### Main Fuctions
1. `GetImageInfo(image_path, faceMaxCount)`: Extracts face information from a static image.</br>
    #### Arguments:
    - `image_path` (str): Path to the input image
    - `faceMaxCount` (int): Maximum number of faces to detect
    #### Return Values:
    - `bbox`: Face bounding box coordinates
    - `landmarks`: Facial landmark points
    - `embedding`: Feature embedding vector 
2. `get_similarity(feature1, feature2)`: Compares two face feature vectors.
    #### Arguments:
    - `feature1` (array): First face feature vector
    - `feature2` (array): Second face feature vector
    #### Return Values:
    - `similarity score` (`0`-`100`): The higher values indicate greater similarity
### Configurations
    - `Default Threshold`: `75` (for determining if two faces belong to the same person)
    - `Supported Formats`: `JPG`, `PNG`, `BMP`, TIFF`
    - `Face Detection`: Automatic detection of multiple faces per image.
#### Please contact us to get more accurate solution:</br>
🧙`Email:` contact@kby-ai.com</br>
🧙`Telegram:` [@kbyaisupport](https://t.me/kbyaisupport)</br>
🧙`WhatsApp:` [+13348402323](https://wa.me/+13348402323)</br>
🧙`Discord:` [KBY-AI](https://discord.gg/6wm383re2s)</br>
🧙`Teams:` [KBY-AI](https://teams.live.com/l/invite/FBAYGB1-IlXkuQM3AY)</br>
