---
layout: page
title: "Grape Disease Classification — VGG-16 + XGBoost"
subtitle: "CNN feature extraction with VGG-16, gradient-boosted tree classifier, and a Flask demo"
permalink: /projects/grape-disease/
description: "Built a grape leaf disease classifier using VGG-16 feature extraction and XGBoost classification; compared against pure CNN baselines (VGG-16, ResNet50) and deployed a simple Flask web app."
---

We built a computer-vision pipeline to detect grape leaf diseases (**black rot**, **black measles**, **leaf blight**) from images. The model uses **VGG-16** for deep feature extraction and **XGBoost** as the final classifier, outperforming pure CNN baselines (VGG-16 and ResNet50) on our modified dataset. A lightweight **Flask** app demonstrates end-to-end prediction.

---

### Problem & Dataset
- **Task:** Image → {Healthy, Black Rot, Black Measles, Leaf Blight}.  
- **Source:** Derived from public plant-disease datasets (PlantVillage lineage); filtered to grape classes, with train/val/test split.  
- **Preprocessing:** Resize to 256×256; use framework `preprocess_input` to match backbone expectations (channel order, zero-centering).

---

### Approach
- **Backbones:** VGG-16 and ResNet50 as feature extractors (frozen base, custom head).  
- **Our best model:** VGG-16 (as feature extractor) → **Flatten** → **Dense** layers → **penultimate feature vector** → **XGBoost** (classifier).  
- **Why XGBoost on deep features?** Tree ensembles can separate non-linear boundaries efficiently with strong regularization, often improving small/medium data generalisation compared to a fully-connected softmax head alone.  
- **Serving:** Minimal **Flask** app to upload an image and return the predicted class.

---

### Results

| Model                 | Accuracy | Precision | Recall |
|:----------------------|---------:|----------:|------:|
| **ResNet50 (CNN)**    | 0.9590   | 0.9597    | 0.9570 |
| **VGG-16 (CNN)**      | 0.9199   | 0.9413    | 0.9201 |
| **VGG-16 + XGBoost**  | **0.9870** | **0.9857** | **0.9876** |

All scores computed on the project’s test split.
{:.figcaption}

---
### Implementation Notes
- **Image size:** 256×256 input to backbones.  
- **Heads:** Flatten → Dense (×2) for CNN-only variants; for the hybrid, export features then fit XGBoost.  
- **Regularisation:** L2 regularisation for the XGBoost setup performed best in our tests.  
- **Training tips:** Monitor class balance; consider light augmentation (color/flip) to avoid overfitting.

---

### What I Learned
- **Hybrid models** (deep features + tree ensembles) can beat pure CNN heads on modest datasets.  
- **Backbone choice matters,** but the classifier head/regularisation can shift results significantly.  
- Simple **Flask** deployment is great for communicating results to non-technical audiences.

---

### Tech Stack
- **TensorFlow/Keras** (VGG-16, ResNet50), **XGBoost**, **Flask**, **NumPy/Pandas**, **Matplotlib**.

---