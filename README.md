<svg width="100%" height="280" viewBox="0 0 1200 280" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#0a0a14"/>
      <stop offset="50%" stop-color="#0d0d1f"/>
      <stop offset="100%" stop-color="#0a0a14"/>
    </linearGradient>

    <linearGradient id="neonPurple" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#ff00c8"/>
      <stop offset="50%" stop-color="#8b5cf6"/>
      <stop offset="100%" stop-color="#00e5ff"/>
    </linearGradient>

    <filter id="glow" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="4" result="blur1"/>
      <feMerge>
        <feMergeNode in="blur1"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <filter id="strongGlow" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="8" result="blur2"/>
      <feMerge>
        <feMergeNode in="blur2"/>
        <feMergeNode in="blur2"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <pattern id="grid" width="40" height="40" patternUnits="userSpaceOnUse">
      <path d="M 40 0 L 0 0 0 40" fill="none" stroke="#1a1a2e" stroke-width="1"/>
    </pattern>

    <radialGradient id="scanGlow" cx="50%" cy="50%" r="60%">
      <stop offset="0%" stop-color="#8b5cf6" stop-opacity="0.15"/>
      <stop offset="100%" stop-color="#8b5cf6" stop-opacity="0"/>
    </radialGradient>
  </defs>

  <!-- Background -->
  <rect width="1200" height="280" fill="url(#bgGrad)"/>
  <rect width="1200" height="280" fill="url(#grid)" opacity="0.5"/>
  <rect width="1200" height="280" fill="url(#scanGlow)"/>

  <!-- Animated scan line -->
  <rect x="0" y="0" width="1200" height="3" fill="#00e5ff" opacity="0.6">
    <animate attributeName="y" values="0;280;0" dur="4s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0;0.8;0" dur="4s" repeatCount="indefinite"/>
  </rect>

  <!-- Floating particles -->
  <circle cx="100" cy="60" r="2" fill="#ff00c8">
    <animate attributeName="cy" values="60;220;60" dur="6s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.2;1;0.2" dur="3s" repeatCount="indefinite"/>
  </circle>
  <circle cx="1100" cy="40" r="2.5" fill="#00e5ff">
    <animate attributeName="cy" values="40;240;40" dur="7s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.2;1;0.2" dur="4s" repeatCount="indefinite"/>
  </circle>
  <circle cx="950" cy="220" r="2" fill="#8b5cf6">
    <animate attributeName="cy" values="220;50;220" dur="5s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.3;1;0.3" dur="3.5s" repeatCount="indefinite"/>
  </circle>
  <circle cx="180" cy="230" r="1.8" fill="#00e5ff">
    <animate attributeName="cy" values="230;30;230" dur="8s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.2;0.9;0.2" dur="4.5s" repeatCount="indefinite"/>
  </circle>

  <!-- Corner brackets (terminal/HUD style) -->
  <g stroke="#8b5cf6" stroke-width="2" fill="none" opacity="0.7">
    <path d="M 30 30 L 30 60 M 30 30 L 60 30"/>
    <path d="M 1170 30 L 1170 60 M 1170 30 L 1140 30"/>
    <path d="M 30 250 L 30 220 M 30 250 L 60 250"/>
    <path d="M 1170 250 L 1170 220 M 1170 250 L 1140 250"/>
  </g>

  <!-- Glitch layers behind main text (red/cyan offset) -->
  <text x="600" y="118" font-family="'Courier New', monospace" font-size="56" font-weight="700"
        text-anchor="middle" fill="#ff00c8" opacity="0.5">
    GERALDO AUGUSTA
    <animate attributeName="x" values="600;598;603;600" dur="2.5s" repeatCount="indefinite"/>
  </text>
  <text x="600" y="118" font-family="'Courier New', monospace" font-size="56" font-weight="700"
        text-anchor="middle" fill="#00e5ff" opacity="0.5">
    GERALDO AUGUSTA
    <animate attributeName="x" values="600;603;597;600" dur="2.2s" repeatCount="indefinite"/>
  </text>

  <!-- Main title with neon glow -->
  <text x="600" y="118" font-family="'Courier New', monospace" font-size="56" font-weight="700"
        text-anchor="middle" fill="#ffffff" filter="url(#strongGlow)">
    GERALDO AUGUSTA
    <animate attributeName="opacity" values="1;0.85;1;1;0.7;1" dur="3s" repeatCount="indefinite"/>
  </text>
  <text x="600" y="118" font-family="'Courier New', monospace" font-size="56" font-weight="700"
        text-anchor="middle" fill="url(#neonPurple)" opacity="0.9">
    GERALDO AUGUSTA
  </text>

  <!-- Underline accent -->
  <rect x="350" y="145" width="500" height="2" fill="url(#neonPurple)" filter="url(#glow)">
    <animate attributeName="width" values="0;500;500" dur="1.5s" fill="freeze"/>
  </rect>

  <!-- Subtitle with typing cursor feel -->
  <text x="600" y="190" font-family="'Courier New', monospace" font-size="22" font-weight="500"
        text-anchor="middle" fill="#00e5ff" filter="url(#glow)">
    &gt; Data Science Enthusiast | ML Explorer | Informatics Student_
    <animate attributeName="opacity" values="1;1;0;1" dur="2s" repeatCount="indefinite"/>
  </text>

  <!-- Tag chips -->
  <g font-family="'Courier New', monospace" font-size="13" font-weight="600">
    <rect x="430" y="215" width="90" height="28" rx="14" fill="none" stroke="#ff00c8" stroke-width="1.5"/>
    <text x="475" y="234" text-anchor="middle" fill="#ff00c8">PYTHON</text>

    <rect x="535" y="215" width="60" height="28" rx="14" fill="none" stroke="#8b5cf6" stroke-width="1.5"/>
    <text x="565" y="234" text-anchor="middle" fill="#8b5cf6">ML</text>

    <rect x="610" y="215" width="160" height="28" rx="14" fill="none" stroke="#00e5ff" stroke-width="1.5"/>
    <text x="690" y="234" text-anchor="middle" fill="#00e5ff">DATA ANALYSIS</text>
  </g>
</svg>

<br/>

## 👨‍💻 About Me

```python
class GeraldoAugusta:
    def __init__(self):
        self.role = "Informatics Engineering Student"
        self.focus = ["Data Science", "Machine Learning", "Data Analysis"]
        self.location = "Indonesia 🇮🇩"
        self.currently_learning = ["Advanced Data Analysis", "Machine Learning"]
        self.motto = "Turning Data Into Insights and Ideas Into Reality"

    def say_hi(self):
        print("Thanks for visiting my profile! 🚀")

me = GeraldoAugusta()
me.say_hi()
```

- 🎓 Informatics Engineering Student
- 📊 Interested in Data Science, Data Analysis, and Machine Learning
- 🌱 Currently deepening my skills in Advanced Data Analysis & ML
- 🤝 Open to collaborating on Data Science / ML projects
- 📍 Based in Indonesia

<br/>

## 🛠️ Tech Stack

<div align="center">

**Languages & Web**

<img src="https://skillicons.dev/icons?i=python,laravel,html,css,js,php" />

**Data Science & Analytics**

<img src="https://skillicons.dev/icons?i=python,sklearn" />

![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-444876?style=for-the-badge)
![ScikitLearn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)

**Tools & Platforms**

<img src="https://skillicons.dev/icons?i=git,github,vscode,mysql,figma" />

</div>

<br/>

## 📊 GitHub Analytics

<div align="center">
<img width="49%" src="https://github-readme-stats.vercel.app/api?username=GeraldoAugusta&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" />
<img width="49%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=GeraldoAugusta&layout=compact&theme=tokyonight&hide_border=true" />
</div>

<div align="center">
<img width="60%" src="https://github-readme-streak-stats.herokuapp.com/?user=GeraldoAugusta&theme=tokyonight&hide_border=true" />
</div>

<div align="center">
<img width="80%" src="https://github-readme-activity-graph.vercel.app/graph?username=GeraldoAugusta&theme=tokyo-night&hide_border=true" />
</div>

<br/>

## 🚀 Featured Projects

<div align="center">

| Project | Description |
|---|---|
| 📈 **Data Analysis Dashboard** | Interactive dashboard for analyzing business and sales performance |
| 🤖 **Machine Learning Project** | Predictive model development using Python and Scikit-Learn |
| 🎨 **Data Visualization Project** | Transforming raw datasets into meaningful visual insights |
| 🌐 **Web Development Project** | Responsive and user-friendly web application development |

</div>

<br/>

## 📫 Connect With Me

<div align="center">

<a href="https://github.com/GeraldoAugusta">
  <img src="https://skillicons.dev/icons?i=github" />
</a>
<a href="https://linkedin.com/in/geraldoaugusta">
  <img src="https://skillicons.dev/icons?i=linkedin" />
</a>
<a href="mailto:geraldonyoman14@gmail.com">
  <img src="https://skillicons.dev/icons?i=gmail" />
</a>

</div>

<br/>

<div align="center">

### ✨ "Turning Data Into Insights and Ideas Into Reality" ✨

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:8b5cf6,100:6366f1&height=120&section=footer" width="100%"/>

</div>
