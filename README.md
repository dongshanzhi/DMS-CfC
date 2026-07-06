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

## 📌 Highlights

### Key Innovations

```
Coming Soon
```

### Performance Highlights

```
Coming Soon
```

---

## 🔬 Abstract


```
Coming Soon
```

---

## 🎯 Research Motivation

```
Coming Soon
```

---

## 🏗️ Methodology

```
Coming Soon
```
---

## 📊 Experimental Results
```
Coming Soon
```
---
## 💻 Code (Coming Soon)

### 🚧 Repository Under Construction

**Planned Structure**:
```
DMS-CfC/
├── README.md                              # Project overview and usage guide
├── requirements.txt                       # Python dependencies
├── LICENSE                                # License file
├── .gitignore                             # Ignore data, checkpoints, logs, and local configs
│
├── configs/
│   ├── preprocess.example.yaml            # Example config for Swarm data preprocessing
│   ├── train.example.yaml                 # Example config for background-model training
│   ├── inference.example.yaml             # Example config for track-level prediction
│   ├── anomaly.example.yaml               # Example config for residual anomaly extraction
│   └── control_region.example.yaml        # Example config for control-region validation
│
├── data_preprocessing/
│   ├── __init__.py
│   ├── orbit_split.py                     # Time correction, local time calculation, and orbit segmentation
│   ├── geomagnetic_coordinates.py         # Mlat/MLT calculation and geomagnetic-latitude filtering
│   ├── gap_filling.py                     # Missing-value and zero-value filling
│   ├── chaos_residual.py                  # CHAOS-based background-field removal
│   ├── vmd_decomposition.py               # VMD decomposition and target-band reconstruction
│   ├── region_filter.py                   # Spatial filtering for study/Low_seismic_activity regions
│   └── dataset.py                         # Time-series dataset construction
│
├── models/
│   ├── __init__.py
│   └── dms_cfc.py                       # DMS-CfC model
│
├── analysis/
│   ├── __init__.py
│   ├── residual_detection.py              # Residual-based anomaly identification
│   ├── cumulative_analysis.py             # Cumulative anomaly trajectory analysis
│   ├── space_weather.py                   # Geomagnetic and solar activity screening
│   └── Low_seismic_activity_region.py     # Low-seismic-activity control experiments
│
├── utils/
│   ├── __init__.py
│   ├── io.py                              # File loading and saving utilities
│   ├── metrics.py                         # RE, CR, AUC, and other evaluation metrics
│   ├── plotting.py                        # Visualization utilities
│   └── seed.py                            # Reproducibility settings
│
├── scripts/
│   ├── preprocess_swarm.py                # Run Swarm preprocessing pipeline
│   ├── inference.py                       # Predict satellite-track background signals
│   ├── detect_anomalies.py                # Extract anomalous tracks from residuals
│   ├── run_control_region.py              # Run control-region validation
│   └── compare_baselines.py               # Optional baseline comparison
│
├── data/
│   ├── README.md                          # Data preparation instructions
│   ├── raw/
│   │   └── .gitkeep                       # Raw data placeholder, ignored by Git
│   ├── processed/
│   │   └── .gitkeep                       # Processed data placeholder, ignored by Git
│   └── external/
│       └── .gitkeep                       # External indices/catalogs placeholder
│
├── checkpoints/
│   └── .gitkeep                           # Model checkpoints placeholder, ignored by Git
│
└── results/
│   └── predictions/
│   │   └── .gitkeep                       # Prediction outputs placeholder
│
├── train.py                           # Train DMS-CfC model
│
└── pred.py                           # pred DMS-CfC model

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

---
