---
layout: default
title: Projects &amp; Funding
permalink: /projects/
description: Active research projects, grants, datasets and tools developed by Dr. Muhammad Ibrahim.
---

# Projects &amp; Funding

I lead and contribute to a portfolio of computer science projects in remote sensing, robotics, high-performance computing, big data processing, cloud computing, 3D vision, and multimodal data, spanning autonomous systems, smart cities, plant phenomics, and decision-support tools. Below are the most active projects and the funded compute and research grants behind them.

## Active research projects

### Agri-analytics Hub — Food Agility CRC (June 2024 – June 2025)

A multi-institutional digital decision-support platform integrating **satellite, soil, weather and yield datasets** across **~450,000 paddocks** in Western Australia. Partners: **DPIRD, Curtin University CCSDM, NGIS**.

- Co-developed the spatial hybrid yield-prediction model (Transformers / CNNs / Mamba) — published at **IGARSS 2025**.
- Applied PCA and SHAP-based explainability to identify yield drivers and quantify productivity opportunities.
- Designed scenario-analysis workflows and interactive dashboards for stakeholder-facing decision support.

### Australian Plant Phenomics Network (APPN) — DPIRD node

National Research Infrastructure for **high-throughput, FAIR-aligned plant phenotyping**.

- Built an **end-to-end UAV imagery pipeline** (orthomosaic, geo-correction, radiometric calibration, vegetation classification, biomass / NDVI / GLI traits) hosted on Pawsey supercomputing.
- Designed a **drone data organisation desktop application** that converts raw UAV captures into FAIR-ready, metadata-rich datasets — used by APPN partners for publication.
- Working across **LiDAR, hyperspectral, mm-resolution Phase-One RGB, IoT sensors** for weather/soil, and **Sentinel-2** via Google Earth Engine.

### 3D City Mapping &amp; Scene Understanding (UWA Adjunct programme)

Working with **Prof. Ajmal Mian** and international partners (University of Jeddah) on the next generation of city-scale 3D perception.

- Multi-sensor LiDAR + GNSS + IMU fine alignment via Dynamic Time Warping (*JSTARS 2026*).
- City-scale 3D change detection (*Scientific Reports 2026*).
- GPU-parallel cylindrical state-space modelling — CylinMamba3D (ECCV 2026 submission).
- Structured latent flow for 3D city-scale point cloud generation — GridFlow (NeurIPS 2026 submission).

### Root Phenotyping (July 2025 – present)

Foundation-model-based deep learning to predict **volumetric water content** at various depths of soil using Dualm Electromagnetic sensor data, replacing manual sampling and enabling scalable, repeatable field measurement.

### Legacy Data Governance &amp; Analytics — DPIRD (Nov 2025 – present)

- Structuring and classifying **42 years** of historical crop datasets — establishing governance, metadata standards and publishing pathways.
- Developed an executable comparative analytics tool evaluating **CSIRO and DPIRD predictive models** to support evidence-based executive investment decisions.

### Southern Rangelands Revitalisation Program (SRRP)

Processing drone-derived multispectral imagery into orthomosaics and 3D point clouds for **quantitative vegetation assessment**, with cost / feasibility analysis to guide technology adoption.

### Dental School Visualisation Tool — UWA

In collaboration with **Mithran Goonewardene (UWA Dental School)**, developed a Python desktop application for visualisation, clinical examination of teeth quality, and statistical analysis of bone and soft tissue near the midline of the front teeth. The tool is now used by Master's and PhD students in the school.

### Optometry AI Collaboration — UWA

With **Dr. Khyber Alam, Prof. Fred K. Chen** (UWA Optometry / Lions Eye Institute), AI-based classification of inherited retinal diseases from fundus autofluorescence and ultrawide retinal images (*Journal of Ophthalmology* 2026).

## Funded research &amp; compute grants

<ul class="pub-list">
  <li>
    <span class="tag gold">A$80k-equiv.</span>
    <strong>3D Scene Understanding using LiDAR Sensor</strong> — University of Jeddah, Saudi Arabia. Grant <strong>UJ-24-SUTU-1290</strong>. Awarded 2025. <em>200,000 SAR.</em>
  </li>
  <li>
    <span class="tag gold">~A$150k value</span>
    <strong>Pawsey Supercomputing Research Centre — 2× allocations</strong>:
    <em>(1) Remote Visualization and High-Memory Compute for APPN Crop Phenotyping (DPIRD)</em>, Reference A001653, Nebula Remote Visualisation, accepted April 2026; and
    <em>(2) Multimodal UAV Crop Phenotyping Data Storage for APPN (DPIRD node)</em>, Reference A001647, Managed Storage 30 TB, accepted April 2026.
    Combined commercial-cloud-equivalent value <strong>~A$150,000</strong>.
  </li>
  <li>
    <span class="tag">Industry / CRC</span>
    <strong>Food Agility CRC — Agri-analytics Hub</strong> (DPIRD / Curtin / NGIS), June 2024 – June 2025.
  </li>
  <li>
    <span class="tag">Federal (US)</span>
    <strong>DARPA / University of Central Florida joint project</strong> — Data Scientist (part-time, 2020–2022).
  </li>
</ul>

## Open datasets &amp; software

<div class="card-grid">
  <div class="card">
    <h3>SWAN Dataset</h3>
    <p>16 B points, 10,000 frames, 24 classes — Perth CBD, 64-channel Ouster LiDAR. <a href="https://ieee-dataport.org/documents/swan" target="_blank" rel="noopener">IEEE DataPort</a></p>
  </div>
  <div class="card">
    <h3>PC-Urban</h3>
    <p>4.3 B points, 66,000 frames, 25 semantic classes. <a href="https://ieee-dataport.org/documents/pc-urban-outdoor-dataset-3d-point-cloud-semantic-segmentation" target="_blank" rel="noopener">IEEE DataPort</a></p>
  </div>
  <div class="card">
    <h3>Perth-WA Localization</h3>
    <p>30,000 LiDAR frames with 6DoF pose annotations. <a href="https://ieee-dataport.org/documents/perth-wa-localization-dataset-3d-point-cloud-maps" target="_blank" rel="noopener">IEEE DataPort</a></p>
  </div>
  <div class="card">
    <h3>PC-Annotate</h3>
    <p>Open annotation tool for large-scale 3D semantic segmentation, with point-cloud registration and volumetric sample generation.</p>
  </div>
  <div class="card">
    <h3>FoSEM</h3>
    <p>LiDAR-based framework for tree stem extraction and modelling (radiata pine plantations).</p>
  </div>
  <div class="card">
    <h3>WA Drone-LiDAR Phenotyping App</h3>
    <p>Python application that extracts individual field plots from 3D LiDAR maps and computes plant height, biomass and volume — replacing manual measurement.</p>
  </div>
  <div class="card">
    <h3>Mobile App for Video labeling</h3>
    <p>Developed a mobile application, initially tested on a Samsung Galaxy S25 Android phone, to annotate objects in video for object detection and tracking.</p>
  </div>
</div>

## Awards &amp; recognition (selected)

- **Winner of Merit Award, INCITE Awards (Research &amp; Innovation)** — WAITTA, Perth, 2023.
- **Finalist, National iAwards 2023 in Innovation category**, Adelaide, South Australia, 2023
- **Finalist, 31st INCITE Awards (Research &amp; Innovation)** — WAITTA, Perth, 2022.
- **Best Paper Runner-Up — Deep Learning for Earth Observation &amp; Remote Sensing**, DICTA 2021.
- **UWA Convocation Postgraduate Research Travel Award** ($3,000), 2022.
- **Scholarship for International Research Fees (SIRF)** + **PG Top-Up** scholarship (~$10k/yr × 4 yr), UWA, 2019.
- **Two Ad-Hoc Scholarships** (UWA), 2021 &amp; 2023.
- **PSA Fieldwork &amp; Data Collection Awards** (×2), UWA, 2021 &amp; 2022.
- **Best Organiser** — MEGA Challenge national competition, FAST-NUCES, 2015.
- **Bestway Scholarship** for MSc, University of Bradford, UK, 2009.

## Service to the discipline

- Reviewer for *IEEE T-ITS*, *Remote Sensing*, *IEEE Access*, PAMI, ICRA, IROS, IGARSS, DICTA.
- Volunteer, **Women in Data Science (WiDS)** Perth, 2023.
- Active member of the **Australian Plant Phenomics Network** community.
- Adjunct supervisor for HDR students at UWA.
