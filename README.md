# DMS-CfC: Ionospheric Anomaly Extraction via a Decoupled Multi-Scale Closed-form Continuous-Time Network

<p align="center">
  Minhao Sun<sup>1,†</sup>, Shanzhi Dong<sup>2,†</sup>, Feng Mu<sup>1</sup>, Jie Zhang<sup>1</sup>, 
  Changfeng Qin<sup>1</sup>, Chengquan Chi<sup>1,*</sup>, and Zining Yu<sup>2,*</sup>, Member, IEEE
</p>

<p align="center">
  <sup>1</sup>School of Artificial Intelligence, Hainan Normal University, Haikou 571158, China<br>
  <sup>2</sup>College of Electronic Engineering, Ocean University of China, Qingdao 266404, China
</p>

<p align="center">
  <sup>†</sup>Minhao Sun and Shanzhi Dong contributed equally to this work.<br>
  <sup>*</sup>Corresponding authors: 
  <a href="mailto:cqcq@hainnu.edu.cn">Chengquan Chi</a> and 
  <a href="mailto:yuzining@ouc.edu.cn">Zining Yu</a>
</p>

### 🎯 Core Innovation
<div align="center">

- **Cross-regional ionospheric anomaly extraction framework.**  
  A data-driven framework is designed for extracting potential pre-earthquake ionospheric magnetic anomalies from Swarm satellite observations.

- **Background-oriented anomaly detection.**  
  The model learns a stable geomagnetic background representation and highlights abnormal residual variations instead of directly fitting all observed fluctuations.

- **Decoupled continuous-time modeling.**  
  A decoupled multi-scale continuous-time network is introduced to improve the separation between background evolution and transient disturbances.

- **Case-based validation.**  
  The framework is evaluated on representative strong-earthquake events to analyze the temporal evolution of possible ionospheric precursor anomalies.
<div>

## 📑 Table of Contents

<details open>
<summary><b>Click to expand/collapse navigation</b></summary>

- **[📌 Highlights](#-highlights)** - Key contributions and novelty
- **[🔬 Abstract](#-abstract)** - Research overview
- **[🎯 Research Motivation](#-research-motivation)** - Problem and challenges
- **[🏗️ Methodology](#%EF%B8%8F-methodology)** - STMN-EQA framework
  - [Transfer Learning Strategy](#transfer-learning-strategy)
  - [SVMD Frequency Decomposition](#1-svmd-frequency-decomposition)
  - [TimesNet Temporal Modeling](#2-timesnet-temporal-modeling)
  - [GNN Spatial Correlation](#3-gnn-spatial-correlation)
  - [Statistical Analysis](#4-statistical-analysis)
- **[📊 Experimental Results](#-experimental-results)** - Two earthquake case studies
  - [2022 Ms 6.8 Luding Earthquake](#2022-ms-68-luding-earthquake)
  - [2019 Ms 6.0 Changning Earthquake](#2019-ms-60-changning-earthquake)
  - [Performance Comparison](#performance-comparison)
  - [Ablation Studies](#ablation-studies)
- **[💻 Code (Coming Soon)](#-code-coming-soon)** - Implementation details
- **[📚 Citation](#-citation)** - BibTeX entry
- **[🙏 Acknowledgments](#-acknowledgments)** - Funding and data support
- **[📧 Contact](#-contact)** - Get in touch

</details>
