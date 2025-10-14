---
layout: page
title: "Smart Recycling — Waste Classification"
subtitle: "Deep learning pipeline to reduce recycling contamination using RealWaste images"
permalink: /projects/waste-classifier/
description: "Built a bin-type image classifier (Red/Green/Yellow) with PyTorch, augmentation, profiling, and domain generalisation experiments. Includes reproducible notebook output and report PDFs."
accent_color: rgb(104,176,74)
date: 2024-04-01
---

I implemented a computer-vision system that classifies household waste photos into Australia’s three-bin scheme:  
**Red (general)**, **Green (organics)**, and **Yellow (recyclables)** — using the **RealWaste** dataset.

---

### 🧩 Problem & Dataset
- **Task:** Image → {Red, Green, Yellow} bin label to help reduce recycling contamination.  
- **Dataset:** [RealWaste (Kaggle)](https://www.kaggle.com/datasets/joebeachcapital/realwaste) (materials like Cardboard, Glass, Metal, Plastic, Food Organics, etc.), remapped to 3 bins.  
- **Split:** ~80/10/10 train/val/test after regrouping images into bin folders.  

![Training dataset distribution and samples](/assets/img/project-waste-train.png){: .img-fluid .rounded .shadow }  
<small>*Sample images and distribution from the training dataset.*</small>

---

### ⚙️ Approach
- **Baseline model:** Small CNN (“WasteNet”), CrossEntropy, Adam, 50 epochs; track Accuracy, F1, Recall, Precision.  
- **Data augmentation:** resize + random flip/rotation + color jitter; normalisation with ImageNet stats; applied to train only.  
- **Profiling:** Compared plain vs augmented input pipelines; identified loader/CPU transforms as bottleneck; sped up with `num_workers=4`.  
- **Equal-time study:** Trained “plain” vs “augmented” under the same one-hour budget to compare generalisation.  
- **Generalisation (D-task):** Collected a new test set from different sources (phone/web) and built an improved CNN with BN/Dropout/Pooling.  

![Training result of plain baseline model](/assets/img/project-waste-plain.png){: .img-fluid .rounded .shadow }  
<small>*Result on baseline (plain) model — accuracy and F1 on validation set.*</small>

---

### 📊 Results (highlights)

| Setup                                | Test Acc |   F1  | Notes                      |
|:-------------------------------------|---------:|------:|:---------------------------|
| Baseline (no augmentation)           |   69.5%  | 0.44  | —                          |
| With augmentation (equal time)       |   70.6%  | 0.47  | Better recall/F1           |
| Improved (BN/Dropout/Pooling)        |   82.98% | 0.71  | On original test set       |
| New domain test — old model          |   ~55%   |  —    | Phone/web images           |
| New domain test — improved model     |   ~70%   |  —    | Higher F1/recall, robust   |

Approximate values marked with “~”.
{:.figcaption}

![Comparison of improved model results on new domain data](/assets/img/project-waste-improved.png){: .img-fluid .rounded .shadow }  
<small>*Improved model showing higher F1 and better domain robustness.*</small>

---

### 🧠 What I Learned
- Balanced **recall/F1** matters more than raw accuracy for waste sorting (missing positives is costly).  
- **Augmentation** helps generalisation but must be profiled/tuned; parallel data loading reduced pipeline time ~5×–6×.  
- Architectural tweaks (**BN, Dropout, Pooling**) significantly improved robustness across domains.  

---

### 🧰 Tech Stack
- **PyTorch**, **TorchVision**, **TensorBoard**, **PyTorch Profiler**, **scikit-learn** metrics.  
- Trained on GPU where available.

---

<p><small><em>Andrean Ignasius</em></small></p>