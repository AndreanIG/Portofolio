---
layout: page
title: "Face Mapping API — Telkom Indonesia Internship"
subtitle: "Automating face recognition and attendance for Telkom employees"
permalink: /projects/face-mapping/
description: "Internship project at Telkom Indonesia: Developed a face mapping API for employee attendance, overcoming real-world dataset and deployment challenges with DLIB, OpenCV, and data cleaning."
---


<strong>Face Mapping API</strong> was developed as part of my Data Scientist internship at <strong>Telkom Indonesia</strong> (October–November 2022), supervised by Tryan Aditya Putra. The main goal was to automate the recognition of employee faces in attendance photos (flag ceremony) using deep learning, making the attendance process more efficient and reliable.

## Problem

Telkom needed a system to automate the mapping and recognition of employee faces from various attendance photo sources (e.g., Zoom screenshots, in-person photos). The real-world dataset presented several challenges:

- **Varied photo formats:** Images came from both virtual (Zoom) and direct (on-site) attendance, with inconsistent naming and backgrounds.
- **Labeling issues:** Many photos lacked proper filenames (no NIK or full name), making face–identity mapping difficult.
- **Technical constraints:** DLIB-based face recognition hit memory limits, and inaccurate detections led to mismatches.

## My Contribution

### Weeks 1–2: Early Work & Preparation
- Contributed to ongoing AI/Data Science tasks, adapting algorithms (dynamic programming, database research) to meet supervisor specs.

### Weeks 3–4: Face Mapping Implementation

- **Developed Face Mapping pipeline** using Python, DLIB, and OpenCV2 DNN for face detection and recognition.
- **Data cleaning:** Fixed filename issues and ensured each image had both a name and NIK for matching.
- **Overcame DLIB memory issues:** Switched to OpenCV2 DNN for more scalable face detection.
- **Improved data preprocessing:** Designed new workflows for background removal and name mapping, increasing face detection accuracy even in noisy group photos.
- **Fallback logic:** For problematic Zoom images, extracted the first detected face in a red background.

### Results
![Training Example](/assets/img/face-train.png)
{:.figcaption}
*Example of Zoom screenshot used for training (blurred for privacy).*

![Face Mapping Result](/assets/img/face-api.jpg)
{:.figcaption}
*Example of automated face detection and mapping on group attendance photos (blurred for privacy).*

- **Automated Face Mapping API** ready for internal use, enabling more accurate, automated attendance tracking.
- Increased face recognition accuracy on Telkom’s real-world dataset despite messy labels and inconsistent input.
- Built practical skills in troubleshooting, iterative solution design, and data cleaning for computer vision projects.
## Key Learnings

- **Requirement Analysis:** Interpreted project specs directly from supervisor direction and user needs, adapting rapidly as requirements evolved.
- **Technical Adaptation:** Learned to pivot quickly between tools (DLIB, OpenCV2 DNN) to address real-world constraints (memory, file format).
- **Collaboration:** Worked closely with the team, frequently seeking feedback to ensure alignment with the evolving project vision.

## Reflection

Working on Face Mapping at Telkom challenged me to go beyond textbook Machine Learning, I learned that real-world AI projects are less about perfect algorithms and more about adapting to messy data and business needs. Rapid feedback and iterative problem-solving were crucial, and overcoming technical bottlenecks (like memory limits and poor labeling) made this project one of my most hands-on computer vision experiences.

---

*Keywords: face recognition, attendance, DLIB, OpenCV, data cleaning, Python, real-world AI, Telkom Indonesia, internship*
