# AR-Mercury

# AR Object Recognition and Rendering (Unity + YOLOv8)

An AR application built with Unity that detects specific objects using YOLOv8 and renders corresponding 3D models. The project can be packaged and deployed to Android devices.

## 📦 Project Overview

This project integrates Unity's rendering engine with YOLO-based object detection. It supports:

- Real-time object recognition
- ONNX model inference via Unity Barracuda
- Android deployment with camera input and automatic rotation compensation

## 🔧 Versions

| Component       | Version                                                                 |
|----------------|-------------------------------------------------------------------------|
| YOLO           | YOLOv8 ([GitHub](https://github.com/ultralytics/ultralytics))           |
| Model Format   | ONNX 10                                                                 |
| Unity          | 2022.3.23f1                                                             |
| Barracuda      | 3.0.1 ([Docs](https://docs.unity3d.com/Packages/com.unity.barracuda@3.0/manual/index.html)) |

## 📁 Folder Structure

- `YOLO/`  
  Contains training, inference, and export scripts. See [Ultralytics Documentation](https://docs.ultralytics.com/zh) for setup and dependencies.

- Other folders  
  Unity project files. Import these into Unity to get started.  
  The core logic resides in `ObjectDetection.cs`, with detailed comments for guidance.

## ⚠️ Notes

1. When importing a custom ONNX model, use **version 9 or 10**. Other versions may cause errors with Barracuda.
2. On Android, the camera feed is rotated 90° by default. This has been corrected in the code.  
   For **PC use**, remove or adjust the rotation-related code accordingly.

## 🚀 Deployment Instructions

1. Open the Unity project with Unity version `2022.3.23f1`.
2. Ensure Barracuda package version `3.0.1` is installed via Unity Package Manager.
3. Place your ONNX model in the appropriate folder.
4. Build and deploy the project to an Android device.

---

