---
layout: page
permalink: /
hide_title: true
buttons:
  print: true
  pdf: /Portfolio/assets/files/resume-andrean.pdf
  json: /Portfolio/assets/files/resume.json
---

<section class="ai-home hero" style="text-align:center; padding:4rem 1rem;">

  <h1 class="ai-title">
    Hi, I’m Andrean — 
    <span class="ai-rotator">
      <span class="ai-role role-1">Data Scientist</span>
      <span class="ai-role role-2">AI Engineer</span>
      <span class="ai-role role-3">ML Researcher</span>
    </span>
  </h1>

  <p class="ai-subtitle">
    🤖 Data Scientist • AI Engineer • Machine Learning Researcher
  </p>

  <p class="ai-lead">
    I build and deploy machine learning systems from data processing to production deployment.<br>
    Focused on computer vision, scalable ML pipelines, and applied AI solutions.
  </p>

  <p class="ai-highlight">
    Master’s in Data Science (High Distinction, Deakin University) ·
    Former Data Scientist at Telkom Indonesia ·
    Microsoft Certified (Azure AI Engineer) ·
    Best Research Paper Award (ICCSCI 2021)
  </p>

  <div class="hero-links ai-links">
    <a href="{{ site.baseurl }}/projects/" class="ai-btn">Projects</a>
    <a href="{{ site.baseurl }}/resume/" class="ai-btn">Resume</a>
    <a href="{{ site.baseurl }}/career/" class="ai-btn">Career</a>
  </div>

</section>

---

### 🚀 What I Do

- Build and deploy machine learning and computer vision systems
- Develop end-to-end AI pipelines from data to production
- Deploy models using cloud and container technologies
- Translate research into production-ready applications

---

### 🏆 Highlights

- Master of Data Science, High Distinction, Deakin University
- Data Scientist at Telkom Indonesia, built face recognition system (80% accuracy, 1000+ faces)
- Improved machine learning pipeline performance by 5–6 percent
- Best Research Paper Award, ICCSCI 2021
- Microsoft Certified, Azure AI Engineer (AI-102)
- Experience across Indonesia and Australia industry environments

---

### ⚙️ Technical Toolkit

Languages: Python, SQL, Java, JavaScript  
Machine Learning: PyTorch, TensorFlow, Scikit-learn, OpenCV  
Cloud & DevOps: Azure, Docker, Jenkins  
Data Tools: Power BI, Tableau, Pandas, NumPy  
Tools: Git, Linux, VS Code  

---

### 🌱 Outside Work

I enjoy gaming, designing databases, and following the latest AI research developments.  

---
### 📬 Contact

<a class="btn" href="https://github.com/AndreanIG" target="_blank">
  <i class="icon-github"></i> GitHub
</a>

<a class="btn" href="https://www.linkedin.com/in/andrean-ignasius/" target="_blank">
  <i class="icon-linkedin"></i> LinkedIn
</a>

<a class="btn" href="mailto:andrean.2000@gmail.com">
  <i class="icon-mail"></i> Email
</a>

<style>
.ai-home .ai-title{
  font-size:2.6rem;
  font-weight:800;
  margin-bottom:0.6rem;
}

/* ROTATION ONLY FOR TEXT (UNCHANGED VISUAL FEATURE) */
.ai-rotator{
  display:inline-block;
  position:relative;
  height:1.2em;
  overflow:hidden;
  vertical-align:bottom;
  color:#06B6D4;
}

.ai-rotator span{
  display:block;
  animation: ai-slide 9s infinite;
}

@keyframes ai-slide {
  0%,10%   {transform:translateY(0%);}
  33%,43%  {transform:translateY(-100%);}
  66%,76%  {transform:translateY(-200%);}
  100%     {transform:translateY(0%);}
}

.ai-lead{
  max-width:750px;
  margin:0 auto 1.5rem;
  font-size:1.1rem;
  color:var(--muted, #777);
}

.ai-highlight{
  max-width:800px;
  margin:0 auto 2rem;
  font-size:1rem;
  font-weight:600;
  opacity:0.85;
}

/* SIMPLE BUTTONS (NO ROTATION) */
.ai-links{
  display:flex;
  justify-content:center;
  gap:1rem;
  flex-wrap:wrap;
}

.ai-btn{
  padding:.75rem 1.5rem;
  border-radius:999px;
  text-decoration:none;
  border:1px solid rgba(0,0,0,.15);
  background:transparent;
  color:inherit;
  font-weight:600;
  transition:.2s ease;
}

.ai-btn:hover{
  transform:translateY(-2px);
  background:rgba(0,0,0,.05);
}

@media (prefers-color-scheme: dark){
  .ai-btn{
    border:1px solid rgba(255,255,255,.2);
  }
  .ai-btn:hover{
    background:rgba(255,255,255,.08);
  }
}
</style>