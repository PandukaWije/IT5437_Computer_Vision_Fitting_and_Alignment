# IT5437 Assignment 2 — Fitting and Alignment

**Name:** W.M.P.S. Wijesundara  
**Index:** 258846K  
**Course:** IT5437 Computer Vision  

---

## Overview

This repository contains the complete solution for Assignment 2 on **Fitting and Alignment**, covering:

| Question | Topic | Key Method |
|----------|-------|-----------|
| Q1(a) | Line fitting — Line 1 only | Total Least Squares via SVD |
| Q1(b) | Line fitting — all 300 points | Sequential RANSAC (×3) |
| Q2 | Earring size estimation | Pinhole camera model |
| Q3(a/b) | Homography — manual | 6 hand-picked correspondences |
| Q3(c) | Feature matching | SIFT + Lowe ratio test |
| Q3(d) | Homography — automatic | SIFT + RANSAC |

---

## Files

| File | Description |
|------|-------------|
| `IT5437_A2_Fitting_and_Alignment.ipynb` | Jupyter notebook with all code, results, and discussion |
| `258846K_a02.pdf` | Final 3-page PDF report |
| `lines.csv` | Dataset for Q1 (3 line scatter, 100 pts each) |
| `earrings.jpg` | Input image for Q2 |
| `c1.jpg`, `c2.jpg` | Circuit board images for Q3 |
| `q1a_plot.png` | TLS fit figure |
| `q1b_plot.png` | RANSAC 3-line figure |
| `q2_plot.png` | Earring detection figure |
| `q3ab_manual.png` | Manual homography warp & diff |
| `q3c_matches.png` | SIFT feature matches |
| `q3d_auto.png` | Auto homography warp & diff |

---

## Key Results

- **Q1(a) TLS:** `y = 1.2207x − 5.9872`
- **Q1(b) RANSAC:** Three lines with 84, 66, 66 inliers respectively
- **Q2 Earrings:** ≈ 72 mm wide × 78 mm tall per earring
- **Q3 Manual H:** Mean |diff| = 18.3/255 (≈15° rotation)
- **Q3 Auto H:** Mean |diff| = 17.1/255 (861/901 SIFT inliers, RANSAC)

---

## Running the Notebook

```bash
pip install numpy matplotlib opencv-python-headless
jupyter notebook IT5437_A2_Fitting_and_Alignment.ipynb
```

> Place `lines.csv`, `earrings.jpg`, `c1.jpg`, `c2.jpg` in the same directory as the notebook.
