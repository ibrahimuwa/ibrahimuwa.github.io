---
layout: default
title: About
description: Dr. Muhammad Ibrahim — Research Scientist and Adjunct Research Fellow at UWA, working on LiDAR, Hyperspectral remote sensing, 3D scene understanding, HPC and multimodal deep learning.
---

<section class="hero">
  <img class="avatar" src="{{ '/assets/img/profile.jpg' | relative_url }}" alt="Dr. Muhammad Ibrahim" onerror="this.style.display='none'">
  <div>
    <h1>Dr. Muhammad Ibrahim</h1>
    <p class="role"><strong>Research Scientist</strong>, Department of Primary Industries and Regional Development (DPIRD), WA</p>
    <p class="role"><strong>Adjunct Research Fellow</strong>, School of Physics, Mathematics &amp; Computing, The University of Western Australia</p>
    <p class="affiliations">PhD in Computer Science (UWA) · MSc in Personal Mobile &amp; Satellite Communication (Bradford, UK) · BSc Computer Systems Engineering (UET, Pakistan)</p>
    <div class="quick-links">
      <a href="mailto:ibrahim80876@gmail.com">Email</a>
      <a href="https://scholar.google.com/citations?user=T_JUvg0AAAAJ&hl=en" target="_blank" rel="noopener">Google Scholar</a>
      <a href="https://github.com/IbrahimUWA" target="_blank" rel="noopener">GitHub</a>
      <a href="https://www.linkedin.com/in/muhammad-ibrahim-83643b1a2/" target="_blank" rel="noopener">LinkedIn</a>
      <a href="{{ '/cv/' | relative_url }}">CV</a>
    </div>
  </div>
</section>

## Biography

I am a Research Scientist at **DPIRD (Government of Western Australia)** and an **Adjunct Research Fellow at The University of Western Australia (UWA)**. My research sits at the intersection of **High Performance Computing, Remote Sensing, Robotics, and Multimodal Deep Learning**. I design GPU-accelerated and parallel algorithms that turn very large multimodal datasets, including **LiDAR**, **Hyperspectral**, **multispectral**, **thermal**, **IoT** sensor streams, and **satellite** imagery, into actionable scientific knowledge for **autonomous systems, smart cities, and precision agriculture**.

My PhD (UWA, 2019–2023, supervised by Prof. Ajmal Mian) focused on **3D scene understanding from LiDAR point clouds**, producing benchmark datasets (PC-Urban, SWAN, Perth-WA) and state-of-the-art transformer-based segmentation, localization and detection methods published in *IEEE TITS, ICRA, IROS, IGARSS,* and *Remote Sensing*. Today I extend this work to **city-scale 3D mapping, change detection, and crop phenomics**, while introducing **Mamba state-space models, hypergraph learning, and CUDA/OpenCL parallelism** to point cloud processing.

I am committed to translating my research into impact: I have delivered AI-driven decision-support systems to government and industry, developed open datasets and tools used by the international research community, and supervised HDR students in collaboration with UWA, Curtin University, and the University of Jeddah. I am a strong believer in **research-led teaching** and am keen to bring this expertise to the undergraduate and postgraduate curriculum at UWA.

<div class="callout">
  <strong>Recent highlight</strong> — Two 2026 first-author/co-author papers accepted at <em>IEEE JSTARS</em> (IF 5.3) on multimodal LiDAR-GNSS-IMU 3D city mapping and Mamba-based foliage separation; submissions under review at <em>ECCV 2026</em> and <em>NeurIPS 2026</em> on geometry-aware cylindrical state-space models and city-scale 3D point cloud generation.
</div>

## Research Interests

<div class="card-grid">
  <div class="card">
    <h3>High Performance Computing</h3>
    <p>Parallel algorithms with OpenMP / MPI / CUDA / OpenCL · GPU-accelerated 3D point cloud processing · MapReduce / Spark / HDFS · supercomputing on Pawsey Setonix and AWS / Azure clouds.</p>
  </div>
  <div class="card">
    <h3>Remote Sensing</h3>
    <p>Multispectral, hyperspectral and thermal UAV imagery · Sentinel-2 satellite analytics via Google Earth Engine · radiometric calibration and orthomosaicking · spatial-temporal modelling of agricultural and urban systems.</p>
  </div>
  <div class="card">
    <h3>LiDAR &amp; 3D Vision</h3>
    <p>Terrestrial, aerial, mobile and TLS LiDAR · 6DoF localization · semantic and instance segmentation · object detection · city-scale HD mapping · change detection.</p>
  </div>
  <div class="card">
    <h3>Multimodal Deep Learning</h3>
    <p>Transformers, Mamba state-space models, hypergraph networks · sensor fusion for LiDAR + camera + radar + GNSS + IMU · diffusion / flow-based 3D generative models.</p>
  </div>
  <div class="card">
    <h3>Big Data &amp; Cloud</h3>
    <p>Petabyte-scale agricultural data pipelines · Dask / Spark · Pawsey Acacia &amp; Nebula · Azure / AWS · FAIR-aligned data governance and metadata.</p>
  </div>
  <div class="card">
    <h3>Robotics &amp; Autonomy</h3>
    <p>Sensor calibration and synchronisation (LiDAR-GNSS-IMU) · mapping and SLAM · perception for autonomous vehicles and UAVs · intelligent agents and decision making.</p>
  </div>
  <div class="card">
    <h3>LLMs &amp; Prompt Engineering</h3>
    <p>Applying large language models for code generation, scientific writing assistance, agentic data pipelines, and educational tooling for HPC, scripting and computational thinking.</p>
  </div>
  <div class="card">
    <h3>Precision Agriculture</h3>
    <p>Crop phenotyping · yield prediction · weed and disease detection · root water-content estimation · explainable AI (SHAP) for agronomic decision support.</p>
  </div>
</div>

## News

- **2026** — Paper accepted at *IEEE JSTARS* (IF 5.3): "LiDAR, GNSS and IMU Sensor Fine Alignment through Dynamic Time Warping to Construct 3D City Maps."
- **2026** — Paper accepted at *IEEE JSTARS* (IF 5.3): "Dynamic Hypergraph-guided Mamba for TLS Point Cloud Foliage Separation."
- **2026** — *CylinMamba3D* submitted to **ECCV 2026**: a CUDA / OpenCL GPU-parallel cylindrical state-space model for 3D point clouds.
- **2026** — *GridFlow* submitted to **NeurIPS 2026** on city-scale structured latent flow for 3D point cloud generation.
- **2026** — Paper accepted at *Scientific Reports*: "LiDAR-based 3D Change Detection at City Scale."
- **2026** — Paper published in *Remote Sensing*: "BAWSeg: A UAV Multispectral Benchmark for Barley Weed Segmentation."
- **2025** — Two Pawsey Supercomputing Centre allocations granted for APPN crop phenotyping (30 TB Acacia storage + Nebula remote visualisation), saving ~A$150k vs. commercial cloud.
- **2025** — Awarded a **200,000 SAR research grant** from the University of Jeddah (UJ-24-SUTU-1290) for "3D Scene Understanding using LiDAR Sensor."
- **2025** — IGARSS 2025 paper: "A Spatial Hybrid Model for Crop Yield Prediction in Western Australia."
- **2025** — IROS 2025 paper: "Multistream Network for LiDAR and Camera-based 3D Object Detection in Outdoor Scenes."

## Get in touch

I welcome collaborations on **3D vision, LiDAR / Hyperspectral analytics, HPC, and AI for science**. The fastest way to reach me is by [email](mailto:ibrahim80876@gmail.com).
