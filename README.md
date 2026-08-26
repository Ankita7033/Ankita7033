<div align="center">

# Hi, I'm Ankita Maji 👋

### AI/ML Engineer · Systems Researcher · Builder

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&pause=1000&color=58A6FF&center=true&vCenter=true&width=700&lines=Building+ML+systems+where+correctness+is+non-negotiable;From+Linux+kernel+interfaces+to+clinical+EHR+pipelines;Hardware-profiled+schedulers+%7C+Real-time+disaster+AI;Currently%3A+1+paper+%2B+2+patents+under+review+%2B+open-source+contributor" alt="Typing SVG" />

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ankitamaji2010)
[![Medium](https://img.shields.io/badge/Medium-12100E?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@ankitamaji7033)
[![Dev.to](https://img.shields.io/badge/dev.to-0A0A0A?style=for-the-badge&logo=devdotto&logoColor=white)](https://dev.to/ankitamaji7033](https://dev.to/ankita_maji_edf930db9b4b5))
[![Hashnode](https://img.shields.io/badge/Hashnode-2962FF?style=for-the-badge&logo=hashnode&logoColor=white)]([https://hashnode.com/@ankitamaji7033](https://hashnode.com/@ankitamaji))
[![Reddit](https://img.shields.io/badge/Reddit-FF4500?style=for-the-badge&logo=reddit&logoColor=white)]([https://www.reddit.com/user/ankitamaji7033](https://www.reddit.com/user/ankitamaji_ml/))
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=firefox&logoColor=white)](https://portfolio-rho-drab-64.vercel.app/)
[![ORCID](https://img.shields.io/badge/ORCID-A6CE39?style=for-the-badge&logo=orcid&logoColor=white)](https://orcid.org/0009-0003-0303-6375)
[![Email](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ankitamaji7033@gmail.com)

</div>

<br>

<div align="center">

|  🔬 1 Paper + 2 Patents Under Review  |  ⚡ 75% Tail-Latency Cut (MOSAIC)  |  🌍 120 Events/hr (DisasterGuard)  |  🛠️ 5 End-to-End ML Systems Shipped  |
|:---:|:---:|:---:|:---:|

</div>

---

## 📋 Quick Facts

| | |
|---|---|
| 🎯 **Focus** | Systems-aware ML infrastructure, edge AI, and clinical/high-stakes ML |
| 🎓 **Education** | B.Tech CSE (AI/ML), Lovely Professional University |
| 💼 **Status** | 🟢 Open to ML/AI Engineering & Systems internships, full-time roles |
| 🔬 **Research** | 1 paper in peer-reviewed submission (Springer Nature) · 2 patents under review |

---

## 🌱 Currently

- ✍️ Actively writing technical blogs (Medium, dev.to, Hashnode) — systems and ML architecture deep-dives
- 🔬 Building **CADENCE** — a causal drift attribution system for production ML retraining
- 🧭 Researching **directional damage in continual learning**
- ⚙️ Building an automated **Codeforces → GitHub sync pipeline** (GitHub Actions + scraping-based submission capture)
- 📚 Sharpening DSA fundamentals (Graphs, DP, Greedy, Trees, Binary Search) for technical interviews

---

## About

Most ML engineers go deep on systems *or* deep on models. I do both — and I ship.

In the last year I went from building applied ML pipelines to writing a hardware-profiled Linux userspace scheduler, a GNN-based clinical subtyping framework on MIMIC-IV, and a production real-time disaster alerting system. Every project here has real metrics, real hardware, or real users — not just notebooks.

> **Actively transitioning from applied ML → ML systems research**, with a focus on efficient inference at the edge and high-stakes AI domains.

---

## 🔬 Research

<sup>⚠️ Note: standardize venue acronym below to whichever is correct — your source file had it both ways (ICNCCom / ICCNCom).</sup>

| Paper | Novel Contribution | Venue | Status |
|---|---|---|---|
| **MOSAIC** | First hardware-counter-profiled userspace scheduler evaluated on disaster-scenario edge workloads; online zero-shot workload classifier via nearest-centroid with EW updates | ICCNCom | 🔄 Accepted |
| **T2D Subtyping** | Progression-aware GNN subtyping of Type 2 Diabetes using DTW-attention alignment on longitudinal EHR; validated via Kaplan–Meier survival analysis | Springer Nature | 🔄 Under Review |

[![ORCID](https://img.shields.io/badge/ORCID-0009--0003--0303--6375-A6CE39?style=flat-square&logo=orcid&logoColor=white)](https://orcid.org/0009-0003-0303-6375)

---

## 📜 Patents

| Patent | Core Contribution | Filing Stage |
|---|---|---|
| **CAAG** — Cause-Attributed Adaptation Gating for On-Device ML | Gates on-device model self-updates behind a label-free cause-attribution layer: before letting a deployed model adapt to a distribution shift, it fuses cross-channel coherence, temporal signature, and plausibility-prior evidence to work out whether the shift is a genuine change in the world or just a faulty sensor — then routes to guarded bounded adaptation, channel masking/recalibration, or a wait-and-track mode accordingly | 🔄 Provisional — under review |
| **PBPEC** — Wearable Bioimpedance System for Non-Invasive Circadian Phase Estimation | Infers a person's internal circadian phase continuously from multi-frequency skin bioimpedance, extracting four Cole-Cole electrical parameters and running them through a biologically-constrained Bayesian state-space estimator (period locked to 20–28h, priors from clock-gene ion-channel data); an optional closed-loop module delivers confidence-gated microcurrent stimulation to nudge phase alignment | 🔄 Provisional — under review |

<details>
<summary><b>📂 Patent details</b> — click to expand</summary>

<br>

### 🔷 CAAG — Cause-Attributed Adaptation Gating in On-Device Machine Learning

*Stops an edge/wearable model from silently corrupting itself when a "distribution shift" is actually just a loose electrode.*

- Sits between drift detection and the model-update step: a **Change Trigger** flags a distributional shift, but the **Cause-Attributed Adaptation Gate (CAAG)** must first diagnose *why* before any update runs
- Fuses three label-free evidence channels — **Cross-Channel Coherence Signature**, **Temporal Signature**, **Plausibility Prior Manifold** — into a posterior cause estimate with a confidence score
- Cause-conditioned routing: sensor fault → suppress adaptation + mask/recalibrate the channel; genuine drift (high confidence) → **Guarded Bounded Adaptation** with a rollback-protected trust budget; ambiguous → defer and track relative change
- Emits machine-readable health telemetry (attributed cause, confidence, per-channel reliability) for fleet monitoring or clinical alerting
- Filed as a provisional IDF at LPU; four claim-independent inventive pillars identified for potential patent-family splitting

### 🔷 PBPEC — Wearable Multi-Frequency Bioimpedance Circadian Phase System

*Reads your body clock off your skin's electrical properties instead of drawing blood every hour.*

- Multi-frequency (1/10/50 kHz) bioimpedance sensing at 2–3 skin sites, fitting a Cole-Cole model to extract four time-varying parameters (Cm, Ri, Re, α) every ~20 minutes
- **BCPE** algorithm: a circadian-period-constrained (20–28h) Bayesian state-space estimator with biologically-derived amplitude priors and a heavy-tailed likelihood for artifact robustness
- **MPCV** validator uses the Re parameter as an internal "negative control" to reject environmentally-contaminated readings — a reversal of how conventional bioimpedance devices are designed
- Optional **PREM** module: closed-loop, confidence-gated biphasic microcurrent stimulation for circadian phase realignment, gated only when posterior uncertainty is low enough
- Currently at the feasibility/computational-simulation stage (no physical prototype yet); a four-phase in-vitro → in-vivo validation program is planned before a complete specification is filed

</details>

---

## 🚀 Featured Projects

### 🔷 MOSAIC — Linux Userspace Scheduler for Disaster-Response Edge Nodes

*First hardware-profiled userspace scheduler designed for disaster-response edge nodes — benchmarked on real hardware, not simulation.*

`Python` `C` `Linux cgroups v2` `Intel RAPL` `perf_event_open` `SQLite` `Docker` `Kubernetes`
&nbsp;![Paper Status](https://img.shields.io/badge/Paper-Under%20Accepted%20%40%20ICCNCom-orange?style=flat-square)

- **75% reduction in P99 tail latency** (12,738ms → 3,178ms) via a hardware-counter-profiled **6×6 interference matrix** used as an admission control primitive, measured with `perf_event_open()` on real hardware
- **Zero task starvation** (vs. 6.3% baseline) and **86% energy efficiency gain** (631 → 1,171 tasks/Wh) via Intel RAPL feedback wired into cgroups v2 DVFS throttling
- Authored an **online ML workload classifier** (nearest-centroid + EW centroid updates) achieving **perfect classification accuracy** across 6 disaster-domain workload classes — zero training data required
- Reproducible benchmark harness: 5 schedulers × 7 metrics × 5 arrival patterns, 63 unit tests, 100% SSE-driven live telemetry dashboard, Docker/Kubernetes DaemonSet deployment
- 6-page workshop paper targeting **USENIX HotEdge** · *Sep 2025 – Feb 2026*

**[📦 Repo](https://github.com/Ankita7033/MOSAIC)**

---

### 🔷 Graph-Based Trajectory Modeling for Type 2 Diabetes Subtyping

*Moves T2D subtyping beyond static clustering — models how patients evolve over time, then validates that the subtypes actually predict different survival outcomes.*

`Python` `PyTorch` `Scikit-learn` `Pandas` `NumPy` `UMAP` `Lifelines` `MIMIC-IV`
&nbsp;![Paper](https://img.shields.io/badge/Paper-In%20Submission-blue?style=flat-square)

- Progression-aware subtyping framework on longitudinal MIMIC-IV EHR data, modeling patient trajectories across multiple temporal scales
- **DTW-attention alignment + GNN-based phenotype fusion** outperforms static K-Means with a **silhouette score of 0.41**
- Clinically validated subtypes via **Kaplan–Meier survival analysis**, revealing differential complication risk and treatment response patterns
- *Aug 2025 – Jan 2026*

**[📦 Repo](https://github.com/Ankita7033/T2D_USING_K-MEANS)**

---

### 🔷 DisasterGuard — AI-Powered Real-Time Disaster Alert System

*Monitors 10 Indian cities for disaster risk in real time — from weather ingestion to shelter assignment in under 500ms.*

`Node.js` `React 18` `Supabase` `PostgreSQL` `HuggingFace` `Leaflet.js` `SSE` `Vercel` `Render` `Tailwind CSS`

- **120 weather events/hour** ingested via OpenWeatherMap API with **sub-500ms alert generation latency**
- Event-driven pipeline: HuggingFace AI risk classification (LOW/MEDIUM/HIGH) + deterministic rule-based fallback + Haversine geodesic algorithm for automatic nearest-shelter assignment across 10 Indian states
- Production system on free-tier infrastructure (Vercel + Render + Supabase): SSE real-time map updates, Supabase Auth, Gmail SMTP alerts, GitHub Actions CI/CD, **100% uptime** via UptimeRobot
- *Feb 2026 – Mar 2026*

**[📦 Repo](https://github.com/Ankita7033/Disasterguard)** · **[🔗 Live Demo](https://disasterguard-nfygj1ppl-ankita4.vercel.app)**

<br>

<details>
<summary><b>📂 More Projects</b> — click to expand</summary>

<br>

### 🔷 SFG-ISL — Real-Time Indian Sign Language Understanding

*Goes beyond hand gestures — interprets the full non-manual signal of ISL including facial expressions, gaze, head pose, and shoulder dynamics.*

`Python` `MediaPipe` `OpenCV` `Graph Neural Networks` `Temporal Modeling`

- **Semantic graph fusion (SFG)** framework fusing non-manual features — facial expressions, gaze direction, head pose, shoulder dynamics — for holistic ISL interpretation
- Lightweight and explainable: built on MediaPipe + OpenCV for real-time inference with **no GPU dependency**
- Temporal stabilization layer reduces jitter in continuous signing sequences

**[📦 Repo](https://github.com/Ankita7033/Indian-sign-language-)**

---

### 🔷 PulseChain — Early Disease Outbreak Detection

*Detects outbreaks 7–14 days before traditional surveillance systems by fusing probabilistic signals rather than waiting for confirmed case counts.*

`n8n` `Bayesian Signal Fusion` `Probabilistic Modeling`

- Bayesian probabilistic signal fusion with regional seasonal baselines, explainable alert reasoning, and cross-region spread modeling

**[📦 Repo](https://github.com/Ankita7033/pulsechain)**

</details>

---

## 🛠️ Tech Stack

**Languages**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

**ML / AI & Data**
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white)

**Systems & Infra**
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)

**Backend & Databases**
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)

**Frontend & Tools**
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/TailwindCSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

---

## 📊 GitHub Analytics

<table>
<tr>
<td width="60%">
<img src="https://github-readme-stats.vercel.app/api?username=Ankita7033&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" alt="GitHub Stats" />
</td>
<td width="40%">
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Ankita7033&layout=compact&theme=tokyonight&hide_border=true" alt="Top Languages" />
</td>
</tr>
</table>

<div align="center">

![Streak](https://streak-stats.demolab.com/?user=Ankita7033&theme=tokyonight&hide_border=true)

![Daily Contributions](https://github-readme-activity-graph.vercel.app/graph?username=Ankita7033&theme=tokyo-night&hide_border=true&area=true)

</div>

---

## 💻 Competitive Programming

Actively solving DSA & CP problems, with automated sync across platforms.

**Focus areas:** Graphs · Dynamic Programming · Greedy · Trees · Binary Search

[![LeetCode](https://img.shields.io/badge/LeetCode-Ankita__Maji-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/Ankita_Maji/)
[![Codeforces](https://img.shields.io/badge/Codeforces-AnkitaMaji-1F8ACB?style=for-the-badge&logo=codeforces&logoColor=white)](https://codeforces.com/profile/AnkitaMaji)
[![GFG](https://img.shields.io/badge/GeeksforGeeks-ankitama5noe-2F8D46?style=for-the-badge&logo=geeksforgeeks&logoColor=white)](https://www.geeksforgeeks.org/profile/ankitama5noe)

---

<div align="center">

## 📫 Let's Connect

I'm actively looking for **ML/AI Engineering and Systems internship & full-time roles** where I can build things that matter. If that's what you're hiring for — let's talk.

[![LinkedIn](https://img.shields.io/badge/Message%20me%20on-LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ankitamaji2010)
[![Medium](https://img.shields.io/badge/Read%20my%20writing%20on-Medium-12100E?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@ankitamaji7033)
[![Email](https://img.shields.io/badge/Email%20me-ankitamaji7033%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ankitamaji7033@gmail.com)

*Always building. Always measuring. Always shipping.*

![Profile Views](https://komarev.com/ghpvc/?username=Ankita7033&color=blueviolet&style=flat-square&label=Profile+Views)

</div>
