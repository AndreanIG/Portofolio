---
layout: page
title: "3D Reconstruction with KinectFusion"
subtitle: "Implementing a real-time dense mapping system using RGB-D data from the TUM dataset."
permalink: /projects/kinectfusion-3d-reconstruction/
description: "Experimented with KinectFusion using RGB-D data from the TUM dataset to perform 3D reconstruction, analyze performance metrics, and evaluate limitations in complex scenes."
---

<section class="lead" style="text-align: justify;">
This project was completed for <strong>SIT789: Robotics, Computer Vision, and Speech Processing</strong> at Deakin University.  
The objective was to experiment with the <strong>KinectFusion</strong> algorithm for real-time 3D reconstruction using RGB-D data from the <strong>TUM dataset</strong>.  
The task focused on executing a published implementation, measuring reconstruction accuracy, and analyzing limitations under different environmental complexities.
</section>

---

### 🎯 Objective

The goal was to:
1. Implement and execute the KinectFusion algorithm on local hardware.  
2. Reconstruct 3D scenes from multiple TUM RGB-D sequences.  
3. Record performance metrics — processing time, FPS, and RMSE.  
4. Analyze how scene complexity affects reconstruction accuracy.

---

### ⚙️ Implementation

The Python-based KinectFusion repository was used from  
<https://github.com/JingwenWang95/KinectFusion>  

All dependencies were installed in an isolated environment to prevent package conflicts.

{% highlight bash %}
pip install imageio
pip install scikit-image
pip install trimesh
pip install open3d
pip install utils
pip install yaml
{% endhighlight %}

Configuration files were manually updated for each TUM dataset sequence under the `configs/` directory.  
Example command for reconstruction:

{% highlight bash %}
python kindu.py --config configs/fr1_desk.yaml --save_dir reconstruct/fr1_desk
{% endhighlight %}

Resulting `.ply` meshes were visualized using the [Open3D viewer](https://www.open3d.org/) or via  
[ImageToSTL 3D viewer](https://imagetostl.com/view-ply-online).

---

### 🧩 Hardware Setup

- **CPU:** Intel® Core™ i7-10750H (2.60 GHz)  
- **GPU:** NVIDIA® GeForce GTX 1660 Ti  
- **Memory:** 32 GB RAM  

This configuration was capable of handling dense depth fusion but did not reach real-time frame rates.  
Each sequence required several minutes of processing depending on scene complexity and voxel resolution.

---

### 📈 Experimental Results

#### Dataset: FR1_RPY
- **Average processing time:** 0.132 s / frame  
- **Frame rate:** 7.55 FPS  
- **RMSE:** 0.064 m  
- **Observation:** Reconstruction accuracy was high; only minor missing polygons in localized regions.

#### Dataset: FR1_Room
- **Average processing time:** 0.158 s / frame  
- **Frame rate:** 6.35 FPS  
- **RMSE:** 0.267 m  
- **Observation:** Reconstruction degraded in complex indoor environments; polygon loss and surface noise were visible.

---

### 🧠 Analysis

Scene complexity had a measurable impact on performance.  
Simpler geometries (FR1_RPY) produced stable meshes with low RMSE, whereas cluttered indoor scenes (FR1_Room) reduced both accuracy and speed.  
Even with discrete GPU acceleration, real-time operation was not achieved.  
The bottleneck occurred during **voxel integration** and **surface fusion**, confirming the trade-off between reconstruction precision and computational speed in volumetric mapping.

---

### 🧭 Reflection

This task provided hands-on understanding of dense SLAM and the computational limits of real-time 3D vision.  
Reconstructing multiple datasets reinforced concepts in:
- RGB-D frame alignment and TSDF fusion  
- Hardware–software performance trade-offs  
- Evaluation metrics (FPS / RMSE)  
- Visual inspection of mesh completeness  

While the results achieved high fidelity for smaller environments, scaling to larger or dynamic scenes remains an open research challenge without dedicated GPU hardware or algorithmic optimization.

---

<p><small><em>Completed May 2024 · SIT789: Robotics, Computer Vision & Speech Processing · Deakin University</em></small></p>