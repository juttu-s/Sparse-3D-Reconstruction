# Sparse 3D Reconstruction and Bundle Adjustment

This project implements a full Structure from Motion (SfM) pipeline using OpenCV and GTSAM to generate a sparse 3D reconstruction from 24 images of a wooden Buddha sculpture.

---

## 📌 Features

- CLAHE-enhanced grayscale preprocessing
- SIFT keypoint detection and feature matching
- RANSAC-based outlier filtering
- Essential matrix estimation and relative pose recovery
- Triangulation of 3D points across image pairs
- GTSAM-based bundle adjustment for global pose optimization
- Visualizations using Matplotlib and Plotly

---

## Workflow

1. **Preprocessing**
   - Enhance images using CLAHE for better feature contrast.

2. **Feature Detection**
   - SIFT with custom parameters: `nfeatures=5000`, `contrastThreshold=0.025`.

3. **Pose Estimation**
   - Essential matrix via `cv2.findEssentialMat`
   - Relative camera pose via `cv2.recoverPose`

4. **Triangulation**
   - Use `cv2.triangulatePoints` to obtain 3D landmarks.

5. **Bundle Adjustment**
   - Construct factor graph in GTSAM.
   - Optimize poses and landmarks with `Levenberg-Marquardt`.

6. **Visualization**
   - Before/after bundle adjustment 3D plots using Plotly.

---

## 📂 Directory Structure

```
├── images/                     # Input images
├── output/                     # Output plots
├── HW4.ipynb                   # Jupyter notebook version
├── README.md                   # This file
```

---

## ▶️ How to Run
Run the notebook:
```bash
jupyter notebook HW4.ipynb
```

## 🧰 Libraries Used

- Python 3.10+
- OpenCV 4.5+
- NumPy, Matplotlib, Plotly
- GTSAM (via Python wrapper)

## 📜 License

This project is released under the MIT License.
