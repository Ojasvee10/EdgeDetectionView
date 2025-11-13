# EdgeViewerMinimal-Native Sobel Edge Detection (Android + C++ + Web Viewer)
A minimal and dependency-free Android project demonstrating real-time Sobel edge detection on camera frames using Kotlin + JNI + C++ (NDK).
This project intentionally does not use OpenCV — instead, it implements a lightweight native edge-processing library to keep the build clean, compact, and easy to understand.

Perfect for:
Mobile computer-vision beginners
JNI/NDK integration learners
Developers wanting a minimal camera → native processing pipeline
Edge-detection demos without heavy SDKs

**What’s Inside**
Android App (Kotlin):
Camera capture pipeline
JNI bridge for frame processing
Simple preview UI
GPU/GL texture upload stubs
Native C++ Library (edgeproc):
Lightweight Sobel operator
Zero dependencies
Optimized for real-time processing
Built via Android NDK + CMake
Web Viewer (TypeScript):
Mini viewer to preview an exported processed PNG
Useful for showcasing processed outputs

## Tech Stack Overview
Component	Technology
Android App	Kotlin
Native Layer	C++ (NDK)
Build System	CMakeLists.txt
Rendering	OpenGL ES (stubbed)
Web Demo	TypeScript + HTML

## Project Structure
EdgeViewerMinimal/
│── android/
│   ├── app/src/main/java/.../MainActivity.kt
│   ├── app/src/main/cpp/edgeproc.cpp
│   ├── app/CMakeLists.txt
│── web/
│   ├── index.html
│   ├── viewer.ts
│── assets/
│   └── sample_processed_frame.png
└── README.md

## How to run
🛠️ Prerequisites
Android Studio (latest)
Android NDK + CMake support enabled
Physical Android device with a camera

📲 Steps
Open the project:
EdgeViewerMinimal/android/

Allow Gradle to sync.
Build the project.
Run on a real device (camera required).
Grant camera permission when prompted.
You should now see live camera feed processed by the Sobel operator.

## Notes
- The native C++ module implements a simple Sobel filter (fast + dependency-free).
- Designed as a minimal learning template for:
Camera → JNI → native processing → texture upload.
- The `web` folder contains a small viewer that displays a sample processed PNG.

# 📸 Screenshots & Demo

## 🎥 Demo GIF
![Demo](assets/working_gif.gif)

## 📸 Processing Flow

<p align="center">
  <img src="assets/img1.png" width="230" />
  <img src="assets/img2.png" width="230" />
  <img src="assets/img3.png" width="230" />
</p>

<p align="center">
  <img src="assets/img4.png" width="230" />
  <img src="assets/img5.png" width="230" />
  <img src="assets/img6.png" width="230" />
</p>


## Files of interest
Purpose                    	File
Main Android Activity	      android/app/src/main/java/com/example/edgeviewer/MainActivity.kt
Sobel Implementation	      android/app/src/main/cpp/edgeproc.cpp
Native Build Rules	        android/app/CMakeLists.txt
Web Demo	                  web/ folder

## License
MIT License
