# 3D Stereo Reconstruction & Depth Estimation for Robot Navigation

[![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)](https://www.python.org/)  
Stereo vision pipeline for real-time 3D obstacle detection and autonomous robot navigation using disparity estimation and depth reconstruction.

---
## 📌 Project Info
- 🎓 Course: Image Processing and Computer Vision
- 🏫 University of Bologna
- 📅 Year: 2025
---

## 🧠 About the Project

This project focuses on **stereo vision-based depth estimation** for obstacle-aware robot navigation, using both **Semi-Global Block Matching (SGBM)** and **sparse matching** via chessboard corners.

Developed for the final project in **Image Processing and Computer Vision** (2025), the system allows:

- Real-time 3D reconstruction using stereo cameras
- Safety alerts for obstacle proximity
- Accurate depth mapping and dimensioning
- Interactive calibration and validation with Python & OpenCV

---

## 🗂 Project Structure

```
📦 3d-stereo-depth-ipcv/
├── 📁 project_images/                        # Plots and visualizations
│   ├── 📸 depth_estimation_sgbm.png          # Dense disparity using SGBM
│   ├── 📸 sparse_chessboard_depth.png        # Sparse depth from chessboard
│   ├── 📸 keypoints_overlay.png              # Keypoints and detection
│   └── 📸 robot_3d_view.png                  # 3D obstacle positioning
├── 📁 robot-navigation-video/               # Output video samples
│   ├── 🎥 output_video_final_Keypoints.avi
│   └── 🎥 output_video_final_SGBM.avi
├── 💻 IPCV_Project_Andrea_Perna.ipynb       # Full interactive notebook
├── 💻 IPCV_Project_Andrea_Perna.pdf         # Notebook output PDF
├── 💻 IPCV_Project_Andrea_Perna.html        # HTML export of notebook
├── 💻 Robot_Navigation_Project.pdf          # Project documentation
├── 💻 Project_Outcomes/                     # Evaluation & test results
├── 💻 robot_nav_pointcloud.ply              # Point cloud output
└── 📄 README.md                              # You are here!
```

---

## ⚙️ How to Run

1. Open the main notebook:

```bash
$ jupyter notebook IPCV_Project_Andrea_Perna.ipynb
```

2. Run each section in order to visualize:
   - Stereo calibration (intrinsics/extrinsics)
   - Disparity map generation (SGBM or sparse)
   - Depth reconstruction and 3D visualization
   - Obstacle warnings based on thresholding

3. Use the point cloud `.ply` file in [MeshLab](https://www.meshlab.net/) or similar tools to inspect 3D scenes.

---

## 📷 Visual Outputs

<p float="left">
  <img src="./images/depth_estimation_sgbm.png" width="250"/>
  <img src="./images/sparse_chessboard_depth.png" width="250"/>
  <img src="./images/keypoints_overlay.png" width="250"/>
</p>

<p float="left">
  <img src="./images/robot_3d_view.png" width="300"/>
</p>

🎥 Output Videos (in `/robot-navigation-video/`):
- `output_video_final_Keypoints.avi`
- `output_video_final_SGBM.avi`

---

## 🔍 Technical Highlights

- **Calibration**: Stereo camera parameters estimated via chessboard detection (OpenCV)
- **Depth from Disparity**: 
  - Dense method using OpenCV SGBM
  - Sparse method using triangulated corner points
- **Safety Mechanism**: Alerts if nearest object < 0.8m
- **Real-Time Capable**: Optimized frame-by-frame processing for live integration

---

## 📊 Evaluation & Output

- Disparity error analysis  
- Point cloud visualization  
- Keypoint matching validation  
- Comparison of dense vs sparse results

---

## 📅 Year

2025

---

## 👨‍🎓 Author

- Andrea Perna  
📧 andrea.perna3@studio.unibo.it

---

## 👩‍🏫 Supervisor

- Prof. Luigi Di Stefano

---

## 📎 Resources

- [📘 Project Report (PDF)](./Robot_Navigation_Project.pdf)
- [📄 Notebook Output (PDF)](./IPCV_Project_Andrea_Perna.pdf)
- [📦 Point Cloud](./robot_nav_pointcloud.ply)
- 🎞️ Videos available in `robot-navigation-video/`

---

## 📜 License

All rights reserved. For academic and educational use only.
