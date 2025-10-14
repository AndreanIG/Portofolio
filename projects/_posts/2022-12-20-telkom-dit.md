---
layout: page
title: "DIT — IndiHome Installation Image Classification"
subtitle: "AI-powered image validation for Telkom’s IndiHome installations"
permalink: /projects/dit-image-classification/
description: "Developed and iteratively improved a computer vision model to classify and validate IndiHome installation photos according to Telkom’s business procedures. Integrated SWIN Transformers and advanced data cleaning for multi-label, multi-class classification."
---

![Sample IndiHome Installation Image](/assets/img/clamp.jpeg)
{:.figcaption}
*Example of IndiHome clamp installation photo used in the dataset (client personal information omitted for privacy).*

<section class="lead" style="text-align: justify;">
<strong>DIT (IndiHome Installation Tracker)</strong> was an AI project assigned during my Data Scientist internship at <strong>Telkom Indonesia</strong>. The project aimed to automate validation of IndiHome installation photos—ensuring all technical requirements were met—using a deep learning approach tailored to Telkom’s strict quality criteria.
</section>

## Problem

With large volumes of IndiHome installation images, manual validation was time-consuming and error-prone. The goal was to build a classification model that could:

- **Detect key installation features** (e.g., neat ODP cable setups) based on Telkom’s procedural standards.
- **Classify and validate** images for business process compliance.
- **Adapt to new validation rules** as they evolved.

## My Contribution

- **Requirement Analysis:** Actively participated in discussions to clarify the evolving goals and business rules for image validation, ensuring the project aligned with real-world needs.
- **Model Development:**  
  - Researched and implemented SWIN Transformer models in Python for multi-label and multi-class classification of installation images.
  - Developed data pipelines for efficient image preprocessing and annotation.
  - Adapted to new validation criteria as updated by Telkom, re-training models as requirements changed.
- **Data Cleaning & Preprocessing:**  
  - Standardized image formats and addressed noisy labels in collaboration with the team.
  - Collaborated with colleagues who previously handled the project to onboard domain-specific insights.
- **Iterative Solution Design:**  
  - Tested different configurations of SWIN and PyTorch, carefully tuning hyperparameters to improve model generalization and performance.
  - Troubleshot issues such as imbalanced datasets and label noise using weighted sampling and frequent feedback cycles.

## Results

- **Functional image validation pipeline** for internal use, reducing manual effort for IndiHome installation checks.
- Achieved working prototype accuracy in both multi-label and multi-class settings, meeting supervisor’s practical requirements.
- Improved collaboration and technical troubleshooting skills, particularly in adapting models for evolving business needs.

## Key Learnings

- **Real-World AI Application:** Gained firsthand experience translating business rules into practical ML workflows and adapting to rapidly changing requirements.
- **Advanced Model Implementation:** Deepened expertise in state-of-the-art architectures (SWIN Transformers), PyTorch, and data engineering.
- **Iterative Teamwork:** Understood the importance of frequent user feedback and clear communication to deliver usable solutions in a business context.

## Reflection

The DIT project taught me that AI success is not just about model accuracy, but also about delivering real business value by working closely with stakeholders and iteratively refining solutions. I became more proactive in clarifying requirements, asking questions, and exploring new model architectures—even when initial results were unsatisfactory. Adapting to constant changes and technical roadblocks gave me a realistic, hands-on understanding of the demands of deploying AI in production.

---

*Keywords: computer vision, image classification, SWIN Transformer, PyTorch, business process automation, data cleaning, Telkom Indonesia, internship*
