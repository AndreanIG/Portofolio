---
layout: page
permalink: /
hide_title: true
buttons:
  print: true
  pdf: /Portofolio/assets/files/resume-andrean.pdf
  json: /Portofolio/assets/files/resume.json
---

<section class="ai-home hero" style="text-align:center; padding:5rem 1rem; position:relative; overflow:hidden;">
  <div class="ai-bg"></div>

  <h1 class="ai-title">
    Hi, I’m Andrean — 
    <span class="ai-rotator">
      <span class="ai-role role-1">Data Scientist</span>
      <span class="ai-role role-2">AI Engineer</span>
      <span class="ai-role role-3">ML Researcher</span>
    </span>
  </h1>

  <p class="ai-lead">
    I build reliable <strong>AI and computer vision systems</strong> — from dataset to deployment.<br>
    Projects include <em>Computer Vision Models</em>, <em>Dashboards</em>, and <em>vLLMs</em>.
  </p>

  <div class="hero-links ai-links">
    <a href="{{ site.baseurl }}/projects/" class="ai-btn ai-rotate delay-1">Explore Projects</a>
    <a href="{{ site.baseurl }}/resume/"   class="ai-btn ai-rotate delay-2">View Resume</a>
    <a href="{{ site.baseurl }}/career/"   class="ai-btn ai-rotate delay-3">Career Journey</a>
  </div>
</section>
---

### 🎯 What I Do
- Build and deploy **AI/ML models**.  
- Develop **full-stack web applications** using the **VILT stack** (Vue, Inertia, Laravel, Tailwind).  
- Research **multimodal and vision-language models (VLMs)** for smarter, context-aware AI systems.  
- Translate research ideas into **practical, user-centered solutions** through UX-driven design.


---

### ⚙️ Technical Toolkit
**Languages:** Python, C#, PHP, JavaScript, Java, SQL  
**Frameworks:** PyTorch, TensorFlow, FastAPI, Laravel, Vue, Tailwind  
**Cloud & DevOps:** Azure, Docker, Jenkins  
**Data Tools:** Power BI, Tableau, TensorBoard  

---

### 🌱 Outside of Work
I’m into **gaming**, **design**, and checking out the latest in **AI and tech**, especially new generative tools and **vision-language models**.  
When I’m not behind a screen, you’ll probably find me **pet-sitting** or staying active,  it keeps a nice balance between tech, creativity, and a bit of real-world.

---

## 🧾 A Printable Resume
You can get my Resume right here or visit my [Resume Page]({{ site.baseurl }}/resume/):

{% include resume-button.html %}

---

[![GitHub](https://img.shields.io/badge/GitHub-AndreanIG-black?logo=github)](https://github.com/AndreanIG)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-AndreanIgnasius-blue?logo=linkedin)](https://www.linkedin.com/in/andrean-ignasius/)
[![Email](https://img.shields.io/badge/Email-andrean.2000@gmail.com-red?logo=gmail)](mailto:andrean.2000@gmail.com)

---


“This Portofolio is built with the help of **[Hydejack](https://hydejack.com)** v9.2.1”

<style>
/* ---------- THEME BASE ---------- */
.ai-home {
  --ai1:#4F46E5;
  --ai2:#06B6D4;
  --ai-muted: var(--muted, #9ca3af);
}

/* Background animation */
.ai-home .ai-bg{
  position:absolute; inset:0;
  background:
    radial-gradient(60% 40% at 20% 25%, rgba(79,70,229,.14), transparent 70%),
    radial-gradient(50% 35% at 80% 75%, rgba(6,182,212,.16), transparent 70%);
  animation: ai-float 12s ease-in-out infinite alternate;
  z-index:-1;
}
@keyframes ai-float { from{transform:translateY(-8px)} to{transform:translateY(8px)} }

/* ---------- TITLE + ROTATOR ---------- */
.ai-home .ai-title{
  font-size:clamp(2rem,4vw,3rem);
  font-weight:800;
  line-height:1.2;
  margin-bottom:1rem;
  background:linear-gradient(90deg,var(--ai1),var(--ai2));
  -webkit-background-clip:text;
  background-clip:text;
  color:transparent;
  display:inline-block;
  position:relative;
  white-space:nowrap;
}
.ai-home .ai-rotator{
  display:inline-block;
  position:relative;
  height:1.2em;
  overflow:hidden;
  vertical-align:bottom;
  color:var(--ai2);
}
.ai-home .ai-rotator span{
  display:block;
  height:1.2em;
  animation: ai-slide 9s infinite;
}
@keyframes ai-slide {
  0%,10%   {transform:translateY(0%);}
  33%,43%  {transform:translateY(-100%);}
  66%,76%  {transform:translateY(-200%);}
  100%     {transform:translateY(0%);}
}
.ai-home .role-2, .ai-home .role-3 { transform: translateY(-10px); }

/* ---------- BODY TEXT ---------- */
.ai-home .ai-lead{
  max-width:700px; margin:0 auto 2rem;
  font-size:1.15rem; color:var(--ai-muted);
}

/* ---------- BUTTONS ---------- */
.ai-home .ai-links{
  display:flex; justify-content:center; flex-wrap:wrap; gap:.8rem;
}
.ai-home .ai-btn{
  position:relative; display:inline-block;
  padding:.9rem 1.7rem; border-radius:999px;
  font-weight:700; text-decoration:none;
  overflow:hidden;
  border:1px solid rgba(0,0,0,.1);
  background:rgba(255,255,255,.72);
  color:#111;
  transition:transform .25s ease, box-shadow .25s ease;
}
.ai-home .ai-btn:hover{ transform:translateY(-2px); }

/* ---------- SMOOTH FADE-IN/FADE-OUT SEQUENCE ---------- */
.ai-home .ai-rotate{
  animation: ai-btn-cycle 9s ease-in-out infinite;
}
.ai-home .delay-1{ animation-delay: 0s; }
.ai-home .delay-2{ animation-delay: 3s; }
.ai-home .delay-3{ animation-delay: 6s; }

@keyframes ai-btn-cycle {
  0% {
    background:rgba(255,255,255,.72);
    color:#111;
    box-shadow:none;
    opacity:0.7;
    border:1px solid rgba(0,0,0,.1);
  }
  15% {
    background:linear-gradient(90deg,var(--ai1),var(--ai2));
    color:#fff;
    opacity:1;
    box-shadow:0 10px 24px rgba(79,70,229,.25);
    border-color:transparent;
  }
  35% {
    background:linear-gradient(90deg,var(--ai1),var(--ai2));
    color:#fff;
    opacity:1;
  }
  50% {
    background:rgba(255,255,255,.72);
    color:#111;
    box-shadow:none;
    opacity:0.7;
    border:1px solid rgba(0,0,0,.1);
  }
  100% {
    background:rgba(255,255,255,.72);
    color:#111;
    opacity:0.7;
  }
}

/* ---------- DARK MODE ---------- */
@media (prefers-color-scheme: dark){
  .ai-home .ai-btn{
    background:rgba(255,255,255,.08);
    color:#fff;
    border:1px solid rgba(255,255,255,.25);
  }
  @keyframes ai-btn-cycle {
    0% {
      background:rgba(255,255,255,.08);
      color:#fff;
      opacity:0.6;
    }
    15% {
      background:linear-gradient(90deg,var(--ai1),var(--ai2));
      color:#fff;
      opacity:1;
      box-shadow:0 10px 24px rgba(79,70,229,.35);
      border-color:transparent;
    }
    35% {
      background:linear-gradient(90deg,var(--ai1),var(--ai2));
      opacity:1;
    }
    50%,100% {
      background:rgba(255,255,255,.08);
      color:#fff;
      opacity:0.6;
      box-shadow:none;
      border:1px solid rgba(255,255,255,.25);
    }
  }
}
</style>
