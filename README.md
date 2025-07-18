# 🎨 Gradient-Domain Fusion & Poisson Blending  
**CS445: Computational Photography — Project 3**  
📅 **Due Date:** April 2, 2025  
👨‍💻 **Author:** Taha Wasiq  
📓 **Notebook:** `Gradient_Domain_Fusion.ipynb`

---

## 🧠 Overview

This project implements gradient-domain image processing, with a focus on **Poisson blending**, a technique that enables seamless compositing of image regions by solving a least-squares problem on image gradients.

Applications explored in this project:
- Gradient-based image reconstruction
- Seamless object blending across images
- Mixed gradient blending (e.g., text transfer)
- Advanced grayscale conversion (`Color2Gray`)
- Laplacian pyramid blending (optional extension)

---

## 🧪 Implemented Features

### ✅ Toy Problem (20 pts)
- Reconstructs an image from its gradients and one known pixel
- Solved as a sparse linear system using `scipy.sparse.linalg.lsqr`

### ✅ Poisson Blending (50 pts)
- Selects a source region and blends it into a target image
- Preserves source gradients while matching target edges
- Handles each RGB channel independently

### ✅ Mixed Gradients (20 pts)
- Uses the stronger gradient between source and target for blending
- Improves results in text/image overlays and subtle blends

---

## 🌟 Bells & Whistles (Extra Credit)

### 🖤 Color2Gray (20 pts)
- Retains visual contrast of RGB image better than standard grayscale
- Uses gradient-domain optimization to preserve visual cues

### 🏔 Laplacian Pyramid Blending (20 pts)
- Multi-scale approach to combine images using alpha masks
- Smoother low-frequency transitions, sharp high-frequency edges

---

## 📂 Project Structure

```text
/
├── Gradient_Domain_Fusion.ipynb         # ✔️ Main notebook
├── utils.py                             # ✔️ Provided utility functions
├── samples/                             # ✔️ Toy images, blending samples, color2gray test images
├── results/                             # ✔️ Blending and output images
├── report.pdf                           # ✔️ Final write-up
└── README.md                            # ✔️ This file
