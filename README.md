<!-- skills: Linux scheduler, EHR clinical ML, PyTorch, edge computing, cgroups, Intel RAPL, perf_event_open, disaster response AI, sign language recognition, NLP, MLOps, Docker, Kubernetes, real-time systems, graph neural networks, MIMIC-IV, Bayesian inference -->

<div align="center">

# Ankita Maji
### AI/ML Engineer · Systems Researcher · Builder

*I build ML systems where correctness is non-negotiable —*
*from Linux kernel interfaces to clinical EHR pipelines to real-time disaster infrastructure.*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ankitamaji2010)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=firefox&logoColor=white)](https://portfolio-rho-drab-64.vercel.app/)
[![ORCID](https://img.shields.io/badge/ORCID-A6CE39?style=flat-square&logo=orcid&logoColor=white)](https://orcid.org/0009-0003-0303-6375)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=flat-square&logo=leetcode&logoColor=black)](https://leetcode.com/u/Ankita_Maji/)
[![Codeforces](https://img.shields.io/badge/Codeforces-1F8ACB?style=flat-square&logo=codeforces&logoColor=white)](https://codeforces.com/profile/AnkitaMaji)
[![GFG](https://img.shields.io/badge/GeeksforGeeks-2F8D46?style=flat-square&logo=geeksforgeeks&logoColor=white)](https://www.geeksforgeeks.org/profile/ankitama5noe)
[![Email](https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:ankitamaji7033@gmail.com)

</div>

---

## About

Most ML engineers either go deep on systems *or* deep on models. I do both — and I ship.

In the last year I went from building applied ML pipelines to writing a hardware-profiled Linux userspace scheduler targeting USENIX HotEdge, a GNN-based clinical subtyping framework on MIMIC-IV, and a production real-time disaster alerting system. Each project has real metrics, real hardware, or real users — not just notebooks.

> **Actively transitioning from applied ML → ML systems research**, with a focus on efficient inference at the edge and high-stakes AI domains.

---

## Current Focus

- **Systems-aware ML infrastructure** — schedulers, interference modeling, resource-constrained inference
- **Efficient AI for edge environments** — DVFS, energy-aware scheduling, sub-millisecond latency
- **Clinical & high-stakes AI** — EHR trajectory modeling, explainability, survival analysis
- **Distributed inference & orchestration** — Kubernetes, DaemonSet deployments, SSE pipelines

---

## Research

Two papers currently in submission for peer-reviewed publication.

| Paper | Novel Contribution | Venue | Status |
|-------|--------------------|-------|--------|
| **MOSAIC** | First hardware-counter-profiled userspace scheduler evaluated on disaster-scenario edge workloads; online zero-shot workload classifier via nearest-centroid with EW updates | USENIX HotEdge | 🔄 Under Review |
| **T2D Subtyping** | Progression-aware GNN subtyping of Type 2 Diabetes using DTW-attention alignment on longitudinal EHR; validated via Kaplan–Meier survival analysis | TBD | 📝 In Submission |

[![ORCID](https://img.shields.io/badge/ORCID-0009--0003--0303--6375-A6CE39?style=flat-square&logo=orcid&logoColor=white)](https://orcid.org/0009-0003-0303-6375)

---

## Featured Projects

### 🔷 MOSAIC — Linux Userspace Scheduler for Disaster-Response Edge Nodes
[![Repo](https://img.shields.io/badge/GitHub-MOSAIC-181717?style=flat-square&logo=github)](https://github.com/Ankita7033/MOSAIC)
&nbsp;`Python` `C` `Linux cgroups v2` `Intel RAPL` `perf_event_open` `SQLite` `Docker` `Kubernetes`
&nbsp;![Paper](https://img.shields.io/badge/Paper-Under%20Review%20%40%20USENIX%20HotEdge-orange?style=flat-square)

> *First hardware-profiled userspace scheduler designed for disaster-response edge nodes — benchmarked on real hardware, not simulation.*

- **75% reduction in P99 tail latency** (12,738ms → 3,178ms) via a hardware-counter-profiled **6×6 interference matrix** used as an admission control primitive, measured using `perf_event_open()` on real hardware
- **Zero task starvation** (vs 6.3% baseline); **86% energy efficiency gain** (631 → 1,171 tasks/Wh) via Intel RAPL energy feedback wired into cgroups v2 DVFS throttle
- Authored an **online ML workload classifier** (nearest-centroid + EW centroid updates) achieving **perfect benchmark classification accuracy** across 6 evaluated disaster-domain workload classes — zero training data required
- Reproducible benchmark harness: 5 schedulers × 7 metrics × 5 arrival patterns; 63 unit tests, 100% SSE-driven live telemetry dashboard, Docker/Kubernetes DaemonSet deployment
- 6-page workshop paper targeting **USENIX HotEdge**

*Sep 2025 – Feb 2026*

---

### 🔷 Graph-Based Trajectory Modeling for Type 2 Diabetes Subtyping
[![Repo](https://img.shields.io/badge/GitHub-T2D_Subtyping-181717?style=flat-square&logo=github)](https://github.com/Ankita7033/T2D_USING_K-MEANS)
&nbsp;`Python` `PyTorch` `Scikit-learn` `Pandas` `NumPy` `UMAP` `Lifelines` `MIMIC-IV`
&nbsp;![Paper](https://img.shields.io/badge/Paper-In%20Submission-blue?style=flat-square)

> *Moves T2D subtyping beyond static clustering — models how patients evolve over time, then validates that the subtypes actually predict different survival outcomes.*

- Progression-aware subtyping framework using longitudinal MIMIC-IV EHR data, modeling patient trajectories across multiple temporal scales
- **DTW-attention alignment** + **GNN-based phenotype fusion** outperforms static K-Means with a **silhouette score of 0.41**
- Clinically validated subtypes via Kaplan–Meier survival analysis revealing **differential complication risk and treatment response patterns**

*Aug 2025 – Jan 2026*

---

### 🔷 DisasterGuard — AI-Powered Real-Time Disaster Alert System
[![Repo](https://img.shields.io/badge/GitHub-DisasterGuard-181717?style=flat-square&logo=github)](https://github.com/Ankita7033/Disasterguard)
[![Live Demo](https://img.shields.io/badge/Live%20Demo-Vercel-000000?style=flat-square&logo=vercel)](https://disasterguard-nfygj1ppl-ankita4.vercel.app)
&nbsp;`Node.js` `React 18` `Supabase` `PostgreSQL` `HuggingFace` `Leaflet.js` `SSE` `Vercel` `Render` `Tailwind CSS`

> *Monitors 10 Indian cities for disaster risk in real-time — from weather ingestion to shelter assignment in under 500ms.*

- **120 weather events/hour** via OpenWeatherMap API with **sub-500ms alert generation latency**
- Event-driven pipeline: HuggingFace AI risk classification (LOW / MEDIUM / HIGH) + deterministic rule-based fallback + Haversine geodesic algorithm for automatic nearest-shelter assignment across 10 Indian states
- Production system on free-tier infrastructure (Vercel + Render + Supabase): SSE real-time map updates, Supabase Auth, Gmail SMTP alerts, GitHub Actions CI/CD, **100% uptime** via UptimeRobot

*Feb 2026 – Mar 2026*

---

### 🔷 SFG-ISL — Real-Time Indian Sign Language Understanding
[![Repo](https://img.shields.io/badge/GitHub-SFG--ISL-181717?style=flat-square&logo=github)](https://github.com/Ankita7033/Indian-sign-language-)
&nbsp;`Python` `MediaPipe` `OpenCV` `Graph Neural Networks` `Temporal Modeling`

> *Goes beyond hand gestures — interprets the full non-manual signal of ISL including facial expressions, gaze, head pose, and shoulder dynamics.*

- **Semantic graph fusion (SFG)** framework fusing non-manual features — facial expressions, gaze direction, head pose, shoulder dynamics — for holistic ISL interpretation
- Lightweight and explainable: built on **MediaPipe + OpenCV** for real-time inference without GPU dependency
- Temporal stabilization layer reduces jitter in continuous signing sequences, improving practical usability

---

### 🔷 Pulsechain — Early Disease Outbreak Detection
[![Repo](https://img.shields.io/badge/GitHub-Pulsechain-181717?style=flat-square&logo=github)](https://github.com/Ankita7033/pulsechain)
&nbsp;`n8n` `Bayesian Signal Fusion` `Probabilistic Modeling`

> *Detects outbreaks 7–14 days before traditional surveillance systems by fusing probabilistic signals rather than waiting for confirmed case counts.*

- Bayesian probabilistic signal fusion with regional seasonal baselines, explainable alert reasoning, and cross-region spread modeling

---

## Tech Stack

### Core Expertise
`Python` `C` `PyTorch` `Linux cgroups v2` `Intel RAPL` `perf_event_open` `Docker` `Kubernetes` `scikit-learn` `Graph Neural Networks` `FastAPI`

### Also Proficient In
`C++` `Java` `JavaScript` `TensorFlow` `Keras` `Pandas` `NumPy` `SciPy` `MLflow` `Plotly` `React` `Node.js` `Supabase` `PostgreSQL` `MongoDB` `AWS` `Azure` `Vercel` `Flask` `Streamlit` `Socket.io` `Tailwind CSS` `Git` `GitHub Actions`

---

## Competitive Programming

Actively solving DSA & CP problems with automated GitHub sync across platforms.

**Focus areas:** Graphs · Dynamic Programming · Greedy · Trees · Binary Search

[![LeetCode](https://img.shields.io/badge/LeetCode-Ankita__Maji-FFA116?style=flat-square&logo=leetcode&logoColor=black)](https://leetcode.com/u/Ankita_Maji/)
[![Codeforces](https://img.shields.io/badge/Codeforces-AnkitaMaji-1F8ACB?style=flat-square&logo=codeforces&logoColor=white)](https://codeforces.com/profile/AnkitaMaji)
[![GFG](https://img.shields.io/badge/GeeksforGeeks-ankitama5noe-2F8D46?style=flat-square&logo=geeksforgeeks&logoColor=white)](https://www.geeksforgeeks.org/profile/ankitama5noe)

---

## GitHub Stats

<div align="center">

![Streak](https://streak-stats.demolab.com/?user=Ankita7033&theme=tokyonight&hide_border=true)

![Trophies](https://github-trophies.vercel.app/?username=Ankita7033&theme=tokyonight&no-frame=true&margin-w=6&column=7)

![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=Ankita7033&theme=tokyo-night&hide_border=true&area=true)

</div>

---

<div align="center">

*Always building. Always measuring. Always shipping.*

![Profile Views](https://komarev.com/ghpvc/?username=Ankita7033&color=blueviolet&style=flat-square&label=Profile+Views)

</div>
