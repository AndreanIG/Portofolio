---
layout: page
title: "Endless Runner: Temple Runner Game"
subtitle: "Building a 3D lane-switcher with shaders, baked lighting, particles, and UI in Unity."
permalink: /projects/temple-runner/
description: "A 3D endless runner for PC featuring randomly generated terrain, collectible coins, power-ups, baked lighting, particle effects, and a responsive UI. Built as part of KTU’s Development of Computer Games and Interactive Applications."
accent_color: rgb(255, 153, 51)
date: 2022-03-01
---

<section class="lead" style="text-align: justify;">
This project was developed for <strong>T120B166 — Development of Computer Games and Interactive Applications</strong> at <strong>Kaunas University of Technology</strong>.  
Our team created a <strong>3D endless runner</strong> with lane switching, coin collection, obstacles, and polish features such as <strong>custom shaders, X-ray effect, baked lighting, particles, animations,</strong> and a <strong>main menu</strong>.
</section>

---

### 🎯 Objective

- Build a playable 3D endless runner on PC with smooth lane-switching and jumping.  
- Implement core gameplay loops: coin collection, obstacle avoidance, scoring, and game over logic.  
- Add production polish: shaders/X-ray, baked lighting with probes, particles, animations, and a clean menu UI.

---

### 🕹️ Game Overview

- **Perspective & Type:** 3D, lane-based endless runner  
- **Platform:** PC  
- **Core loop:** Run as far as possible; collect coins; avoid obstacles (e.g., cones); difficulty increases over time  
- **Progression:** Coins can unlock power-ups (e.g., speed boost, score multipliers) and stronger characters  
- **Enemies:** Basic AI that can damage the player (HP loss) and end the run  
- **Controls:**  
  - **Left / Right Arrow:** switch among three lanes  
  - **Up Arrow:** jump (supports double jump)  
- **Rules:** Hitting an obstacle = game over; collecting coins = score gain

---

### ⚙️ Implementation Highlights

![Development process in Unity Editor showing obstacle setup](/assets/img/game-dev.png){: .img-fluid .rounded .shadow }

#### 1) Shaders & X-ray
- Custom shader work to add a **blinking light** on cones (red/orange hue) for readability and feedback.  
- **X-ray effect** used for stylistic visibility cues through occluding geometry.

#### 2) Baked Lighting
- **Lightmapping** performed per lecture workflow; **Light Probes** placed along playable paths to approximate GI on dynamic objects.  
- Improves stability and frame time on mid-range GPUs while preserving visual quality.

#### 3) Main Menu & UI
- Built with **Unity Canvas** + Text/Buttons.  
- Interaction handled via a menu controller script attached to an empty GameObject under the UI hierarchy.  
- Buttons: **Start** (loads gameplay) and **Exit** (quits application).

![Main menu of the Temple Runner game showing Start and Exit buttons](/assets/img/game-menu.png){: .img-fluid .rounded .shadow }

#### 4) Coin Prefab & Animation
- Created an **80×16** sprite strip split into **16×16** frames.  
- Assembled into an **Animator** clip at **12 FPS** for a smooth spinning coin.  
- Prefab includes collider + pickup logic and score increment.

#### 5) Particles & Feedback
- **Emission-based explosion** VFX spawns when the player collides with an obstacle.  
- Collision handler: instantiate explosion → destroy player → set **Time.timeScale = 0** → show **Game Over** UI.

#### 6) Character Animation System
- Animation clips (e.g., **Jump**) authored in the Animation window.  
- **Animator Controller** manages state transitions (Idle/Run/Jump/Land) with parameterized conditions.  
- Scripts update Animator parameters (e.g., speed, isGrounded, jumpTrigger) for responsive motion.

---

### 🧩 Architecture & Systems

- **Procedural Track/Obstacle Spawning:** Segments and hazards generated ahead of the player; difficulty escalates over distance.  

![Procedural infinite terrain generation in Temple Runner gameplay](/assets/img/game-terrain.png){: .img-fluid .rounded .shadow }

- **Scoring:** Distance-based score with coin multipliers; UI updates in real time.  
- **Game State:** Start → Running → Game Over; menu and HUD toggle based on state.  
- **Performance:** Baked lighting + lightweight shaders keep frame times stable; particle systems pooled to avoid spikes.

---

### 📦 How to Play (PC)

1. Launch the build and press **Start** on the main menu.  
2. Use **← / →** to switch lanes; **↑** to jump (supports double jump).  
3. Collect coins, avoid cones and enemy hits.  
4. On collision with obstacles, the game pauses and shows **Game Over**.

---

### 🧭 Reflection

This project focused on shipping a complete game with immediate feedback.  
Future improvements include: richer enemy behaviors, power-up variety, mobile build with touch controls, and analytics for tuning difficulty curves.

---

<p><small><em>Completed March 2022 · KTU · T120B166 Development of Computer Games and Interactive Applications</em></small></p>
