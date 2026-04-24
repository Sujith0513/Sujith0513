<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=venom&color=0:0a0a0f,30:0d1b2a,60:1a1a2e,100:0f3460&height=280&section=header&text=R%20Sujith%20Gopi&fontSize=72&fontColor=e2d9f3&fontAlignY=40&desc=ECE%20%C3%97%20Data%20Science%20%7C%20Robots%20that%20Dive%20%7C%20Eyes%20that%20See%20%7C%20Signals%20that%20Speak&descAlignY=62&descSize=15&descColor=9d8ec7&animation=twinkling" />

</div>

<div align="center">

```
╔══════════════════════════════════════════════════════════════════╗
║  IIITDM Kancheepuram  ×  IIT Madras  ║  CGPA 9.4 × 8.67        ║
║  B.Tech ECE  +  BS Data Science & Applications                   ║
║  AUV 🥇 IIT Bombay  ·  AUV 🥈 IIT Madras  ·  Subject Topper    ║
╚══════════════════════════════════════════════════════════════════╝
```

<a href="https://github.com/Sujith0513">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=16&pause=1200&color=9d8ec7&center=true&vCenter=true&width=700&lines=Autonomous+Underwater+Vehicles+%E2%80%94+1st+Place+%40+IIT+Bombay+%F0%9F%8F%86;Deep+Learning+for+Retinal+Vessel+Segmentation+%26+DR+Grading;Document+Binarisation+surpassing+DIBCO+competition+winners;AI+Agents+%7C+LangGraph+%7C+Multi-LLM+Cross-Validation;Embedded+Systems+%7C+ROS2+%7C+ESP32+%7C+PID+Control;Signal+Processing+%7C+FFT+%7C+LMS%2FRLS+%7C+CLAHE" />
</a>

<br/>

[![Email](https://img.shields.io/badge/rsujithgopi%40gmail.com-0d1b2a?style=flat-square&logo=gmail&logoColor=9d8ec7)](mailto:rsujithgopi@gmail.com)
[![LinkedIn](https://img.shields.io/badge/sujith--gopi--r-0d1b2a?style=flat-square&logo=linkedin&logoColor=9d8ec7)](https://linkedin.com/in/sujith-gopi-r)
[![GitHub](https://img.shields.io/badge/Sujith0513-0d1b2a?style=flat-square&logo=github&logoColor=9d8ec7)](https://github.com/Sujith0513)
![](https://komarev.com/ghpvc/?username=Sujith0513&label=visitors&color=9d8ec7&style=flat-square)

</div>

---

## ⚙️ `whoami`

```python
@dataclass
class RSujithGopi:
    # ── Identity ───────────────────────────────────────────────────
    location        : str  = "India 🇮🇳"
    degrees         : list = ["B.Tech ECE @ IIITDM Kancheepuram (9.4 CGPA)",
                              "BS Data Science @ IIT Madras (8.67 CGPA)"]
    
    # ── What I build ───────────────────────────────────────────────
    domains         : list = [
        "🤖  Autonomous Robotics  (ROS / ROS2, AUV navigation)",
        "🧠  Deep Learning        (Medical Imaging, Document AI)",
        "📡  Signal Processing    (FFT, LMS/RLS, Bio-signals)",
        "🔌  Embedded Systems     (STM32, ESP32, Sensor Fusion)",
        "🕵️  AI Agents            (LangGraph, Multi-LLM pipelines)",
        "📊  Data Science         (Time-Series, EDA, Forecasting)",
    ]

    # ── Philosophy ─────────────────────────────────────────────────
    belief          : str  = "Hardware without software is sculpture. \
                              Software without hardware is poetry. I write both."
    
    current_obsession : str = "Brain waves — mapping EEG/fMRI signals to cognition"
    
    fun_fact        : str  = "My neural net learned to read ancient manuscripts \
                              better than DIBCO competition winners. No big deal. 📜"

me = RSujithGopi()
```

---

## 🏆 Notable Wins

| 🎖️ Achievement | 📍 Venue | 📅 Year |
|:---|:---|:---|
| 🥇 **1st Place** — AUV Competition | IIT Bombay | 2025 |
| 🥈 **2nd Place** — AUV Competition | IIT Madras | 2024 |
| 🏅 **Subject Topper Award** | IIT Madras | 2024 |
| 🏸 **Badminton Captain** + Smashers & Elite Tournament Winner | IIITDM KCP | 2024–25 |
| 🎾 Selected for **Inter-IIIT Sports Meet** | National | 2026 |

---

## 🔬 Research & Deep Projects

> *These aren't tutorials. These are original systems built from scratch.*

<details>
<summary><b>👁️ VesselFormer-DR — Retinal Vessel Segmentation & Diabetic Retinopathy Grading</b></summary>
<br>

**Two-stage deep learning pipeline for automated DR severity grading from fundus images.**

- **Stage 1 — HybridVesselNet**: ResNet-34 encoder-decoder + dual CBAM attention, trained on 840 images with composite Dice + BCE + consistency loss and patch-based Gaussian-blended inference
  - `97.40% accuracy` · `80.52% Dice` · `99.11% specificity`
- **Stage 2 — VesselAwareDRNet**: EfficientNet-B0 extended to 4-channel input (RGB + vessel mask) fused with anatomical coordinate MLP for 5-class ordinal DR grading
  - `QWK 0.61` (primary metric) · Grad-CAM confirmed lesion-region attention
- **Ongoing**: Replacing Focal Loss with ordinal CORN/EMD loss + soft-mask fusion

`PyTorch` `ResNet-34` `EfficientNet-B0` `CBAM` `Grad-CAM` `OpenCV` `CLAHE`

</details>

<details>
<summary><b>📜 UNet7 — Document Image Binarisation (Beats DIBCO Competition Winners)</b></summary>
<br>

**Engineered a 7-channel manuscript-aware feature stack and a custom 7-level residual U-Net.**

- Feature engineering: RGB + L-CLAHE + Sauvola adaptive prior + multi-scale Gaussian gradient + local variance
- Architecture: 48M parameter U-Net, bottleneck at H/128, edge-weighted Dice-BCE loss (5× boundary penalty)
- Trained on 96 DIBCO images (2009–2014), evaluated on **fully held-out H-DIBCO 2016**:
  - `FM 0.9869` · `SSIM 0.9118` · `PSNR 17.79 dB` — **surpassing competition winners** (FM 0.92–0.96)

`PyTorch` `Sauvola` `CLAHE` `AdamW` `Mixed-Precision AMP` `DIBCO dataset`

</details>

<details>
<summary><b>🤖 Haptic Feedback Writing Tutor — Robotic Guidance Device</b></summary>
<br>

**Robotic haptic-guidance device to teach children correct handwriting strokes.**

- Mechanical core: back-drivable planar 5-bar parallel linkage + custom cable-driven capstan transmission (5:1 reduction) for low-inertia force feedback
- AS5600 12-bit magnetic encoders track end-effector position
- ESP32 runs high-frequency PID + haptic boundary-enforcement loops
- ROS2 manages kinematic transformations (IK/FK) and module coordination
- Cross-platform Flutter app delivers real-time animated stroke-fill feedback

`ROS2` `ESP32` `Flutter` `PID Control` `Python/C++`

</details>

<details>
<summary><b>🕵️ Hardware Sourcing & Specifications AI Agent</b></summary>
<br>

**Autonomous AI agent for electronic component research via multi-stage pipeline.**

- LangGraph StateGraph pipeline: `plan → search → extract → price → validate`
- Dual-LLM cross-validation (Gemini 2.0 Flash + 1.5 Flash) for high-reliability data extraction
- Streamlit dashboard + FastAPI backend with Server-Sent Events (SSE) for real-time streaming
- Integrated Tavily Search API + YouTube API for targeted document and tutorial retrieval

`LangGraph` `FastAPI` `Streamlit` `Gemini API` `Tavily` `Pydantic v2`

</details>

<details>
<summary><b>🧠 Brain Waves Analysis (In Progress)</b></summary>
<br>

**Analysing structural and functional brain signals to map neural activity to cognitive states.**

- Processing EEG + fMRI using FreeSurfer, FSL, and custom bio-signal pipelines
- Correlating neural patterns with cognitive states and behaviours

`Python` `FreeSurfer` `FSL` `EEG/fMRI Bio-signal Processing`

</details>

---

## 🚀 Other Projects

| Project | Description | Stack |
|:---|:---|:---|
| [⚡ EV Sales India](https://github.com/Sujith0513/Electric-Vehicle-Sales-by-States-in-India) | State-wise EV adoption trends + regression forecasting | Python, Pandas, Matplotlib |
| [📈 Coca-Cola Stock](https://github.com/Sujith0513/Coca-Cola-Stock---Live-and-Updated) | Live stock tracker with Facebook Prophet time-series | Python, Prophet, Plotly |
| [🏅 Olympic Analytics](https://github.com/Sujith0513/Olympic-Data-Analysis) | Medal prediction + deep-dive analysis across decades | Python, Seaborn, Scikit-learn |
| [🌸 Iris Classifier](https://github.com/Sujith0513/Iris-Classification) | ML classification pipeline with hyperparameter tuning | Python, Scikit-learn |
| [🔇 Active Noise Cancellation](https://github.com/Sujith0513) | Real-time adaptive DSP (LMS/RLS) + medical image enhancement | Python, NumPy, OpenCV, DSP |

---

## 🛠️ Full Tech Arsenal

<div align="center">

**Core Languages**

![Python](https://img.shields.io/badge/Python-0d1b2a?style=for-the-badge&logo=python&logoColor=9d8ec7)
![C++](https://img.shields.io/badge/C%2FC%2B%2B-0d1b2a?style=for-the-badge&logo=cplusplus&logoColor=9d8ec7)
![MATLAB](https://img.shields.io/badge/MATLAB-0d1b2a?style=for-the-badge&logo=mathworks&logoColor=9d8ec7)
![SQL](https://img.shields.io/badge/SQL-0d1b2a?style=for-the-badge&logo=postgresql&logoColor=9d8ec7)
![Dart](https://img.shields.io/badge/Dart%2FFlutter-0d1b2a?style=for-the-badge&logo=flutter&logoColor=9d8ec7)

**AI / ML / Deep Learning**

![PyTorch](https://img.shields.io/badge/PyTorch-0d1b2a?style=for-the-badge&logo=pytorch&logoColor=9d8ec7)
![TensorFlow](https://img.shields.io/badge/TensorFlow-0d1b2a?style=for-the-badge&logo=tensorflow&logoColor=9d8ec7)
![Scikit-learn](https://img.shields.io/badge/Scikit--Learn-0d1b2a?style=for-the-badge&logo=scikit-learn&logoColor=9d8ec7)
![LangChain](https://img.shields.io/badge/LangChain%2FGraph-0d1b2a?style=for-the-badge&logo=chainlink&logoColor=9d8ec7)
![OpenCV](https://img.shields.io/badge/OpenCV-0d1b2a?style=for-the-badge&logo=opencv&logoColor=9d8ec7)

**Robotics / Embedded**

![ROS2](https://img.shields.io/badge/ROS%2FROS2-0d1b2a?style=for-the-badge&logo=ros&logoColor=9d8ec7)
![ESP32](https://img.shields.io/badge/ESP32-0d1b2a?style=for-the-badge&logo=espressif&logoColor=9d8ec7)
![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-0d1b2a?style=for-the-badge&logo=raspberrypi&logoColor=9d8ec7)
![STM32](https://img.shields.io/badge/STM32-0d1b2a?style=for-the-badge&logo=stmicroelectronics&logoColor=9d8ec7)

**Data & APIs**

![Pandas](https://img.shields.io/badge/Pandas-0d1b2a?style=for-the-badge&logo=pandas&logoColor=9d8ec7)
![Plotly](https://img.shields.io/badge/Plotly-0d1b2a?style=for-the-badge&logo=plotly&logoColor=9d8ec7)
![FastAPI](https://img.shields.io/badge/FastAPI-0d1b2a?style=for-the-badge&logo=fastapi&logoColor=9d8ec7)
![Streamlit](https://img.shields.io/badge/Streamlit-0d1b2a?style=for-the-badge&logo=streamlit&logoColor=9d8ec7)

</div>

---

## 📊 GitHub Stats

<div align="center">

<img width="49%" src="https://github-readme-stats.vercel.app/api?username=Sujith0513&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=9d8ec7&icon_color=9d8ec7&text_color=8b949e&ring_color=9d8ec7" />
<img width="49%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Sujith0513&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=9d8ec7&text_color=8b949e&langs_count=8" />

<img width="70%" src="https://github-readme-streak-stats.herokuapp.com/?user=Sujith0513&theme=github-dark-blue&hide_border=true&background=0d1117&stroke=9d8ec7&ring=9d8ec7&fire=e2d9f3&currStreakLabel=9d8ec7&sideLabels=8b949e&dates=8b949e" />

</div>

---

## 📈 Contribution Activity

<div align="center">
<img width="95%" src="https://github-readme-activity-graph.vercel.app/graph?username=Sujith0513&theme=github-compact&bg_color=0d1117&color=9d8ec7&line=9d8ec7&point=e2d9f3&area=true&hide_border=true&area_color=1a1a2e" />
</div>

---

<div align="center">

```
┌─────────────────────────────────────────────────────────────────┐
│  I build things that move underwater, see inside the eye,       │
│  read ancient manuscripts, listen to brain waves,               │
│  and source components from the internet autonomously.          │
│                                                                  │
│  If it involves signals, models, or microcontrollers —          │
│  I'm probably already building it.                              │
└─────────────────────────────────────────────────────────────────┘
```

[![Email](https://img.shields.io/badge/rsujithgopi%40gmail.com-0d1b2a?style=for-the-badge&logo=gmail&logoColor=9d8ec7)](mailto:rsujithgopi@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0d1b2a?style=for-the-badge&logo=linkedin&logoColor=9d8ec7)](https://linkedin.com/in/sujith-gopi-r)
[![Phone](https://img.shields.io/badge/%2B91%2075988%2031502-0d1b2a?style=for-the-badge&logo=phone&logoColor=9d8ec7)](tel:+917598831502)

</div>

<img width="100%" src="https://capsule-render.vercel.app/api?type=venom&color=0:0f3460,50:1a1a2e,100:0a0a0f&height=120&section=footer&reversal=true" />
