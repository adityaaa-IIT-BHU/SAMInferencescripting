# 🧠 AI-Driven Liver Segmentation for Biomedical Imaging

**Supervisor:** Prof. Gemma Piella Fenoy  
**Institute:** Universitat Pompeu Fabra (UPF), Barcelona, Spain  
**Duration:** Oct 2025 – Present

This repository contains the complete workflow for developing a **mobile-deployable liver boundary segmentation system** for point-of-care imaging using **RGB smartphone cameras**.

The pipeline includes:
- SAM fine-tuning for precise liver segmentation
- Lightweight liver localization using TFLite
- Domain adaptation using color-calibrated data
- Ongoing YOLO-based detection with anatomical priors for robust localization

---

## 🧬 Project Motivation

Early liver disease diagnosis often relies on **resource-intensive imaging** (CT, MRI).  
This work enables **low-cost, accessible liver boundary detection** using ** consumer-grade cameras**, improving:
- Remote screening
- Telehealth workflows
- Biomedical imaging accessibility in low-resource regions

---

## 📊 Results Summary

| Component | Method | Dataset | Performance | Status |
|----------|--------|---------|-------------|-------|
| Segmentation | Fine-tuned **SAM-Vit-Base** | Unseen validation | **0.90 Dice** | Completed |
| Segmentation — Domain Adapted | SAM + Color-calibrated dataset | Adapted validation | **0.91 Dice** | Completed |
| Liver Localization | Lightweight **TFLite CNN** | Smartphone RGB | **0.70 Dice** (bbox) | Completed |
| Detection + Spatial Priors | **YOLO-based** anatomical guidance | WIP | — | In Progress |

⚡ Domain adaptation significantly improved edge precision on dark-skin and low-illumination samples.

---

## 🖥️ System Architecture

