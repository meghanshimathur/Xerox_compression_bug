# 📉 When Compression Breaks a Downstream Task  
### Rule-Based Character Recognition Under Image Compression

## 📌 Overview

This project demonstrates how **image compression can negatively affect downstream computer vision tasks**.  
A **simple rule-based character recognition and grouping system** is used to show how compression artifacts distort visual structure and lead to recognition failures.

The goal is **not high accuracy**, but to **analyze and visualize failure caused by compression**.

---

## 🎯 Objective

- Study the impact of **lossy image compression** on character recognition  
- Show the fragility of **rule-based computer vision systems**  
- Connect **image quality degradation** with recognition and grouping errors  

---

## 🧠 Core Idea

> Image compression alters pixel structure and edges.  
> Rule-based vision systems rely on these features, so distortion leads to failure.

---

## 🛠️ What This Project Does

1. Loads character/digit images (PNG or JPEG)
2. Applies **JPEG compression** at different quality levels
3. Converts images to binary (black & white)
4. Extracts individual characters
5. Performs **rule-based recognition** (no ML / DL)
6. Measures similarity using:
   - Intersection over Union (IoU)
   - Structural Similarity Index (SSIM)
7. Groups visually similar characters
8. Visualizes grouping results for qualitative analysis

---

## 🧪 Techniques Used

### 🔹 Rule-Based Features
- Aspect ratio  
- Pixel density  
- Geometric shape properties  

### 🔹 Similarity Metrics
| Metric | Purpose |
|------|--------|
| IoU | Measures pixel-level shape overlap |
| SSIM | Measures structural and visual similarity |

### 🔹 Grouping Strategy
- Greedy clustering
- Representative-based comparison
- Threshold-based matching

---

## 📊 Key Observations

- Recognition accuracy decreases as compression increases
- SSIM values drop with heavy compression
- Same characters may be misclassified or split into different groups
- Visual results clearly show shape distortion caused by compression

---

## ✅ Conclusion

This experiment shows that **simple rule-based character recognition systems are highly sensitive to image compression**.  
Compression alters visual structure enough to break geometric rules, leading to recognition and grouping errors.

This explains why modern vision systems rely on **learned features** instead of handcrafted rules.

---

## 🚀 How to Run

1. Clone this repository
2. Open the notebook:
   ```bash
   jupyter notebook Xerox_JBIG2_Compression_Bug.ipynb
