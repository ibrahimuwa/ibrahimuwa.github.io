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

<div class="ticker" role="region" aria-label="Latest research news">
  <span class="ticker-label"><span class="dot"></span>Latest</span>
  <div class="ticker-viewport">
    <div class="ticker-track">
      <span class="item"><span class="badge hot">New</span><b>GridFlow accepted at ECCV 2026</b> — structured latent flow for seamless city-scale 3D point cloud generation (top-tier computer vision venue).</span>
      <span class="sep">◆</span>
      <span class="item"><span class="badge">Accepted</span><b>IEEE JSTARS</b> — Geo-Registration of terrestrial LiDAR point clouds with satellite imagery without GNSS.</span>
      <span class="sep">◆</span>
      <span class="item"><span class="badge">Published</span><b>IEEE JSTARS</b> — Dynamic Hypergraph-guided Mamba for TLS point cloud foliage separation.</span>
      <span class="sep">◆</span>
      <span class="item"><span class="badge">Accepted</span><b>IEEE JSTARS</b> — LiDAR, GNSS &amp; IMU fine alignment via Dynamic Time Warping for 3D city maps.</span>
      <span class="sep">◆</span>
      <span class="item"><span class="badge">Under review</span><b>IEEE TGRS</b> — Hierarchical multi-scale Transformer&ndash;Mamba crop-yield model for ~450,000 WA paddocks.</span>
      <span class="sep">◆</span>
      <span class="item"><span class="badge">Grant</span><b>2&times; Pawsey allocations</b> &amp; a 200,000 SAR University of Jeddah research grant.</span>
      <span class="sep">◆</span>
    </div>
  </div>
</div>

## Biography

I am a Research Scientist at **DPIRD (Government of Western Australia)** and an **Adjunct Research Fellow at The University of Western Australia (UWA)**. My research sits at the intersection of **High Performance Computing, Remote Sensing, Robotics, and Multimodal Deep Learning**. I design GPU-accelerated and parallel algorithms that turn very large multimodal datasets, including **LiDAR**, **Hyperspectral**, **multispectral**, **thermal**, **IoT** sensor streams, and **satellite** imagery, into actionable scientific knowledge for **autonomous systems, smart cities, and precision agriculture**.

My PhD (UWA, 2019–2023, supervised by Prof. Ajmal Mian) focused on **3D scene understanding from LiDAR point clouds**, producing benchmark datasets (PC-Urban, SWAN, Perth-WA) and state-of-the-art transformer-based segmentation, localization and detection methods published in *IEEE TITS, ICRA, IROS, IGARSS,* and *Remote Sensing*. Today I extend this work to **city-scale 3D mapping, change detection, and crop phenomics**, while introducing **Mamba state-space models, hypergraph learning, and CUDA/OpenCL parallelism** to point cloud processing.

I am committed to translating my research into impact: I have delivered AI-driven decision-support systems to government and industry, developed open datasets and tools used by the international research community, and supervised HDR students in collaboration with UWA, Curtin University, and the University of Jeddah. I am a strong believer in **research-led teaching** and am keen to bring this expertise to the undergraduate and postgraduate curriculum at UWA.

<div class="callout">
  <strong>Recent highlight</strong> — <em>GridFlow</em>, our work on structured latent flow for seamless city-scale 3D point cloud generation, has been <strong>accepted at ECCV 2026</strong>, one of the top-tier computer vision conferences. This adds to three 2026 papers accepted/published at <em>IEEE JSTARS</em> (IF 5.3) on multimodal LiDAR-GNSS-IMU 3D city mapping, GNSS-free geo-registration, and Mamba-based foliage separation, with further manuscripts under review at <em>IEEE TGRS</em>, <em>IEEE TIP</em> and <em>IEEE TCSVT</em>.
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

- **2026** — 🎉 *GridFlow* **accepted at ECCV 2026** (top-tier computer vision): "Structured Latent Flow for Seamless City-Scale 3D Point Cloud Generation."
- **2026** — Paper accepted at *IEEE JSTARS* (IF 6.3): "Geo-Registration of Terrestrial LiDAR Point Clouds with Satellite Images without GNSS."
- **2026** — Paper accepted at *IEEE JSTARS* (IF 6.3): "LiDAR, GNSS and IMU Sensor Fine Alignment through Dynamic Time Warping to Construct 3D City Maps."
- **2026** — Paper published in *IEEE JSTARS* (IF 6.3): "Dynamic Hypergraph-guided Mamba for TLS Point Cloud Foliage Separation" — [code](https://github.com/ZhangIceNight/foliage_segmentation).
- **2026** — Manuscript submitted to *IEEE TGRS*: "A Hierarchical Multi-Scale Hybrid Transformer–Mamba Model for Crop-Yield Prediction in Western Australia" (~450,000 paddocks).
- **2026** — Manuscript submitted to *IEEE TIP*: "Identity Prototype Diffusion Distillation with Context Modulation for Unsupervised Person Re-Identification."
- **2026** — Manuscript submitted to *IEEE TCSVT*: "Evidence-Grounded Progressive Chain-of-Thought Reasoning for Multi-modal Object Re-Identification."
- **2026** — Manuscript submitted to *Scientific Reports*: "LiDAR-based 3D Change Detection at City Scale."
- **2026** — *CylinMamba3D* — a CUDA / OpenCL GPU-parallel cylindrical state-space model for 3D point clouds — manuscript in preparation.
- **2026** — Paper published in *Remote Sensing*: "BAWSeg: A UAV Multispectral Benchmark for Barley Weed Segmentation."
- **2025** — Two Pawsey Supercomputing Centre allocations granted for APPN crop phenotyping (30 TB Acacia storage + Nebula remote visualisation), saving ~A$150k vs. commercial cloud.
- **2025** — Awarded a **200,000 SAR research grant** from the University of Jeddah (UJ-24-SUTU-1290) for "3D Scene Understanding using LiDAR Sensor."
- **2025** — IGARSS 2025 paper: "A Spatial Hybrid Model for Crop Yield Prediction in Western Australia."
- **2025** — IROS 2025 paper: "Multistream Network for LiDAR and Camera-based 3D Object Detection in Outdoor Scenes."

## Get in touch

I welcome collaborations on **3D vision, LiDAR / Hyperspectral analytics, HPC, and AI for science**. The fastest way to reach me is by [email](mailto:ibrahim80876@gmail.com).
