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

- **Decoupled Multi-Scale Closed-form Continuous-Time Network.**  
  A decoupled multi-scale continuous-time network is introduced to improve the separation between background evolution and transient disturbances.

- **Case-based validation.**  
  The framework is evaluated on representative strong-earthquake events to analyze the temporal evolution of possible ionospheric precursor anomalies.
<div>


## 📑 Table of Contents

<details open>
<summary><b>Click to expand/collapse navigation</b></summary>

- **[📌 Highlights](#-highlights)** - Main features and research contributions
- **[🔬 Abstract](#-abstract)** - Research overview
- **[🎯 Research Motivation](#-research-motivation)** - Background and challenges
- **[🏗️ Methodology](#%EF%B8%8F-methodology)** - DMS-CfC framework
  - [Satellite Magnetic Data Processing](#satellite-magnetic-data-processing)
  - [Background-Oriented Modeling](#background-oriented-modeling)
  - [DMS-CfC Temporal Network](#dms-cfc-temporal-network)
  - [Residual-Based Anomaly Extraction](#residual-based-anomaly-extraction)
- **[📊 Experimental Analysis](#-experimental-analysis)** - Case-based validation
  - [Prediction Performance](#prediction-performance)
  - [Anomaly Extraction Results](#anomaly-extraction-results)
  - [Space-Weather Screening](#space-weather-screening)
  - [Multi-Geosphere Comparison](#multi-geosphere-comparison)
- **[💻 Code](#-code)** - Coming Soon
- **[🙏 Acknowledgment](#-acknowledgment)** - Data and funding support
- **[📧 Contact](#-contact)** - Contact information

</details>

---

## 💻 Code (Coming Soon)

### 🚧 Repository Under Construction

**Planned Structure**:
```
DMS-CfC/
├── README.md                              # Project overview and usage guide
├── requirements.txt                       # Python dependencies
├── LICENSE                                # License file
├── .gitignore                             # Ignore data, checkpoints, logs, local configs
│
├── configs/
│   ├── preprocess.yaml            # Example config for Swarm data preprocessing
│   ├── train.yaml                 # Example config for background-model training
│   ├── inference.yaml             # Example config for track-level prediction
│   ├── anomaly.yaml               # Example config for residual anomaly extraction
│   └── control_region.yaml        # Example config for low-seismic-activity control analysis
│
├── data_preprocessing/
│   ├── __init__.py
│   ├── orbit_split.py                 # Time correction, local time calculation, orbit segmentation
│   ├── geomagnetic_coordinates.py     # Mlat / MLT calculation and geomagnetic latitude filtering
│   ├── gap_filling.py                 # Missing/zero-value filling for magnetic-field sequences
│   ├── chaos_residual.py              # CHAOS-based core/lithospheric field removal
│   ├── vmd_decomposition.py           # VMD decomposition and target-band reconstruction
│   ├── region_filter.py               # Spatial filtering for study/control regions
│   └── dataset.py                     # Time-series dataset construction for model training
│── data/
│   ├── raw/.gitkeep                       # Raw data placeholder, ignored by Git
│   ├── processed/.gitkeep                 # Processed data placeholder, ignored by Git
│
├── models/
│   ├── __init__.py
│   └── DMS-CfC.py                   # Optional baseline models
│
├── utils/
│    ├── __init__.py
│    ├── io.py                          # File loading/saving utilities
│    ├── metrics.py                     # RE, CR, AUC and other evaluation metrics
│    ├── plotting.py                    # Visualization utilities
│    └── seed.py                        # Reproducibility settings
│
├── checkpoints/
│   └── best.pth                         # the best Model checkpoint
│
├── results/
│   ├── true.npy                   # true 
│   └── pred.py                    # predication 

├── analysis/
│   ├── __init__.py
│   ├── residual_detection.py          # Residual-based anomaly identification
│   ├── cumulative_analysis.py         # Cumulative anomaly trajectory analysis
│   ├── space_weather.py               # Geomagnetic/solar activity screening
│   └── control_region.py              # Low-seismic-activity control experiments

```

---

### 🙏 Acknowledgment

### Funding Support

This work was supported by:
- **Education Department of Hainan Province** (Project No. Hnky2026ZD-4)

### Data Support

We acknowledge the borehole strain data support from:
- **China Earthquake Networks Center**
- **National Earthquake Data Center**
- **National Institute of Natural Hazards, MEMC**

### Technical Acknowledgments

We thank the authors of the following works for open-sourcing their implementations:
- [TimesNet](https://github.com/thuml/Time-Series-Library) - Multi-periodic temporal modeling
- [PyTorch Geometric](https://github.com/pyg-team/pytorch_geometric) - Graph neural networks
- [VMD-Python](https://github.com/vrcarva/vmdpy) - Variational mode decomposition

---
