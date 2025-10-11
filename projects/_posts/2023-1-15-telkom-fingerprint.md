---
layout: page
title: "Fingerprint Detection — Telkom AI Platform"
subtitle: "Automated fingerprint classification and segmentation using Vision Transformers"
permalink: /projects/fingerprint-detection/
description: "Developed multi-stage fingerprint classification and segmentation models as part of an AI platform for Telkom Indonesia, uisng SWIN and Vision Transformers for parent/subclass detection and ridge counting."
---

![Sample Fingerprint Image](/assets/projects/fingerprint/sample.jpg)

<section class="lead" style="text-align: justify;">
<strong>Fingerprint Detection</strong> was a complex AI project at <strong>Telkom Indonesia</strong> focused on automating the identification and classification of fingerprint patterns, a crucial part of their AI platform for workforce management and security.
</section>

## Problem

Manual fingerprint validation was inefficient and error-prone, especially at Telkom’s scale. The project aimed to:

- **Classify fingerprint images** into parent/subclass categories (e.g., pattern type).
- **Detect swirl direction** (left/right) for more granular detail classification.
- **Segment key features** (delta & core) and count fingerprint ridges using automated instance segmentation.

## My Contribution

- **Requirement Analysis:** Proactively clarified objectives and evolving criteria with the supervisor and previous project contributors, ensuring solution relevance.
- **Model Development:**  
  - Built multi-stage pipelines:  
    - **Parent & Subclass Classification:** SWIN Transformer with multi-class outputs.  
    - **Detail Class (Swirl Direction):** SWIN with binary classification.
    - **Instance Segmentation:** Integrated Detectron2 for precise localization of fingerprint features (delta & core).
    - **Ridge Counting:** Assisted in developing algorithms to compute ridge count from segmented images.
  - Addressed key challenges such as imbalanced datasets and noisy labels using advanced data sampling and regular feedback cycles.
- **Technical Research & Upskilling:**  
  - Deepened knowledge of Vision Transformers (ViT, SWIN) and modern computer vision libraries (PyTorch, Detectron2).
  - Iteratively refined hyperparameters and model structures to tackle overfitting and validation accuracy issues.

## Results

- Delivered a working prototype for fingerprint detection and classification, meeting supervisor’s requirements for minimum accuracy and segmentation quality.
- Automated multi-stage processing pipeline, enabling future scalability for workforce management and security systems.
- Developed troubleshooting skills for complex, real-world AI problems, including imbalanced datasets and model instability (e.g., NaN losses).

## Key Learnings

- **Cutting-Edge Model Application:** Acquired practical experience with state-of-the-art vision architectures (SWIN, ViT) and their deployment in production-like environments.
- **Iterative Problem Solving:** Learned to persist through technical setbacks, repeatedly revising model designs and seeking alternative solutions.
- **Stakeholder Communication:** Recognized the importance of constant engagement with supervisors and users to align on objectives and expectations.

## Reflection

The Fingerprint Detection project exemplified the challenges and rewards of real-world computer vision work. Facing noisy, imbalanced data and evolving requirements, I learned the value of adaptability, deep technical research, and teamwork. This experience significantly strengthened my skills in AI model development and gave me the confidence to approach future applied ML projects in both industry and research.

---

*Keywords: fingerprint classification, instance segmentation, SWIN Transformer, Detectron2, PyTorch, ridge counting, computer vision, Telkom Indonesia, internship*
