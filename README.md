# 🧠 Fine-Tuning SAM (Segment Anything) for Medical Image Segmentation

This repository contains code for **fine-tuning Meta’s Segment Anything Model (SAM)** on a **custom medical image segmentation dataset**, inspired by **MedSAM**.  
The project was executed and tested in **Google Colab with GPU acceleration**.

---

## 🚀 Project Overview

🩺 Medical images often include complex tissue structures where classical segmentation fails.  
🎯 This work fine-tunes **facebook/sam-vit-base** to better handle domain-specific features.

The workflow includes:

- Loading a medical dataset (image + mask pairs)
- Preprocessing using 🤗 Transformers `SamProcessor`
- Generating bounding-box prompts from ground-truth masks
- Training the model (encoder + mask decoder)
- Monitoring validation performance
- Saving checkpoints to local storage + Google Drive

---

## 📊 Results

This work fine-tunes SAM for **liver boundary detection** from **smartphone RGB images**.

| Metric | Dataset | Result |
|--------|---------|--------|
| **Dice = 0.90** | Unseen validation set | Accurate segmentation of clinical liver contours |
| **Dice = 0.91** | Color-calibrated domain-adapted dataset | Improved robustness & boundary precision |

🟢 Demonstrates the advantage of task-specific adaptation and domain consistency.

---

## 📂 Repository Structure

