---
layout: default
title: Projects &amp; Funding
permalink: /projects/
description: Active research projects, grants, datasets and tools developed by Dr. Muhammad Ibrahim.
---

# Projects &amp; Funding

I lead and contribute to a portfolio of computer science projects in remote sensing, robotics, high-performance computing, big data processing, cloud computing, 3D vision, and multimodal data, spanning autonomous systems, smart cities, plant phenomics, and decision-support tools. Below are featured systems with their architectures, followed by the most active projects and the funded compute and research grants behind them.

## Featured AI &amp; research systems

<div class="proj">
  <h3>GridFlow — City-Scale 3D Point Cloud Generation</h3>
  <div class="proj-meta">
    <span class="pill flagship">ECCV 2026 · Accepted</span>
    <span class="pill">Generative 3D</span>
    <span class="pill">Flow matching + Diffusion</span>
  </div>
  <p>A multi-stage generative framework that synthesises dense, coloured city-scale 3D point clouds (100k points per 150&nbsp;m tile) conditioned on satellite imagery, semantic maps and digital surface models. A <strong>Grid-Aligned VAE</strong> compresses each tile into a topology-preserving latent grid so adjacent tiles join seamlessly; a conditional <strong>rectified-flow</strong> model generates geometry and an orientation-aware <strong>diffusion</strong> model colourises it. Released with the <em>City3D-MultiGen</em> benchmark (163k tiles, Melbourne &amp; London). Best Chamfer Distance (−29% vs. PVD) and ~4× lower JSD than prior art.</p>
  <figure class="proj-fig">
    <img src="{{ '/assets/figures/gridflow.png' | relative_url }}" alt="GridFlow conditioning and generation pipeline" loading="lazy">
    <figcaption><b>Pipeline (from the paper):</b> satellite imagery, semantic maps and DSM are converted into a grid-aligned condition; a Grid-Aligned VAE, conditional rectified flow and orientation-aware diffusion then generate the coloured city-scale point cloud.</figcaption>
  </figure>
</div>

<div class="proj">
  <h3>Hierarchical Multi-Scale Transformer–Mamba — Crop-Yield Prediction</h3>
  <div class="proj-meta">
    <span class="pill review">IEEE TGRS · Under review</span>
    <span class="pill">First author</span>
    <span class="pill">~450,000 paddocks</span>
  </div>
  <p>A hierarchical, multi-scale yield model for Western Australia built on a <strong>parallel Transformer–Mamba</strong> encoder with a <strong>slot-attention</strong> fusion bottleneck. A per-crop base model trained at paddock scale is specialised to the administrative shire scale and the within-field sub-paddock scale. Introduces the <em>WA Paddock Dataset</em> (soil + weather + Sentinel-2 for ~450k paddocks, 2020–2023) and reaches paddock-level R² up to 0.95 across wheat, canola and barley, with SHAP-based interpretability.</p>
  <figure class="proj-fig">
    <img src="{{ '/assets/figures/cropyield.png' | relative_url }}" alt="Hierarchical multi-scale Transformer-Mamba crop-yield architecture (Fig. 4)" loading="lazy">
    <figcaption><b>Architecture (Fig. 4 from the paper):</b> (a) the paddock base model fuses WA Paddock features after SHAP preprocessing, feeds parallel Transformer and Mamba streams, and combines them through a slot-attention bottleneck; (b) the trained model is fine-tuned to shire and sub-paddock scales.</figcaption>
  </figure>
  <p class="proj-links"><a href="https://github.com/IbrahimUWA/Hierarchical-MultiScale-Crop-Yield-WA" target="_blank" rel="noopener">GitHub repository ↗</a></p>
</div>

<div class="proj">
  <h3>Geo-Registration of LiDAR Point Clouds without GNSS</h3>
  <div class="proj-meta">
    <span class="pill accepted">IEEE JSTARS · Accepted</span>
    <span class="pill">Second author</span>
    <span class="pill">Cross-modal alignment</span>
  </div>
  <p>A fully automatic method that geo-registers terrestrial LiDAR point clouds to satellite imagery in <strong>GNSS-denied</strong> urban environments. Road points are segmented with a Point Transformer, road skeletons and intersections are matched across the LiDAR and satellite views, then a global rigid alignment is refined by a non-rigid thin-plate-spline warp and corrected against SRTM terrain. On KITTI it reduces mean planimetric error from 2.60&nbsp;m to 0.69&nbsp;m — better than the raw GNSS annotations — and is validated on a new Perth CBD dataset.</p>
  <figure class="proj-fig">
    <img src="{{ '/assets/figures/georeg.png' | relative_url }}" alt="GNSS-free geo-registration pipeline (from the paper)" loading="lazy">
    <figcaption><b>Pipeline (from the paper):</b> parallel point-cloud and map branches segment roads, skeletonise and extract intersections, then perform global rigid alignment, non-rigid thin-plate-spline refinement and SRTM-based elevation correction.</figcaption>
  </figure>
</div>

<div class="proj">
  <h3>DHMamba — Hypergraph-Guided Mamba for Foliage Separation</h3>
  <div class="proj-meta">
    <span class="pill published">IEEE JSTARS · Published</span>
    <span class="pill">Code released</span>
    <span class="pill">Forestry / TLS</span>
  </div>
  <p>Leaf–wood separation of terrestrial laser-scanning forest point clouds using a linear-complexity <strong>Mamba</strong> backbone paired with a <strong>dynamic hypergraph</strong> serialization that captures higher-order topological dependencies. Density and geometric priors (planarity, linearity) sharpen multi-scale discrimination of fine branches and leaves. Beats Transformer baselines in mIoU across seven datasets while processing ~5× larger patches under equal memory.</p>
  <figure class="proj-fig">
    <img src="{{ '/assets/figures/foliage.png' | relative_url }}" alt="DHMamba foliage separation pipeline (from the paper)" loading="lazy">
    <figcaption><b>Pipeline (from the paper):</b> FPS / KNN density-aware patches and global density / scale priors feed token embedding, dynamic hypergraph convolution (high / low-density tokens) and a stack of Mamba blocks for point-wise leaf / wood separation.</figcaption>
  </figure>
  <p class="proj-links"><a href="https://doi.org/10.1109/JSTARS.2026.3696349" target="_blank" rel="noopener">DOI ↗</a> · <a href="https://github.com/ZhangIceNight/foliage_segmentation" target="_blank" rel="noopener">Code ↗</a></p>
</div>

<div class="proj">
  <h3>CylinMamba3D — Geometry-Aware Cylindrical State-Space Modelling</h3>
  <div class="proj-meta">
    <span class="pill">Manuscript in preparation</span>
    <span class="pill">CUDA / OpenCL</span>
    <span class="pill">3D deep learning</span>
  </div>
  <p>A geometry-aware <strong>Mamba</strong> framework for 3D point clouds that resolves the mismatch between the unordered nature of points and the sequential order required by state-space models. Token centres are projected to cylindrical (r, θ, z) coordinates and serialized to give a geometry-consistent traversal; a Cylindrical State-Space Module handles long-range propagation while a local module refines geometry. Achieves 94.0% accuracy on ModelNet40 with linear-time efficiency and a GPU-parallel CUDA / OpenCL implementation.</p>
  <figure class="proj-fig">
    <img src="{{ '/assets/figures/cylinmamba.png' | relative_url }}" alt="CylinMamba3D architecture: cylindrical 3D Mamba encoder with C-SSM and LNP" loading="lazy">
    <figcaption><b>Architecture (from the manuscript):</b> after FPS / KNN tokenization and cylindrical coordinate transformation, a stack of Cylindrical 3D Mamba blocks (each pairing a C-SSM global module with local neighbourhood processing) feeds a classification / segmentation head.</figcaption>
  </figure>
</div>

## Applications &amp; tools I have built

<div class="proj">
  <h3>UoJ LiDAR Scene-Understanding Platform</h3>
  <div class="proj-meta">
    <span class="pill app">Web application</span>
    <span class="pill">Three.js · FastAPI · React</span>
    <span class="pill">Bilingual EN / AR</span>
  </div>
  <p>An interactive web platform and 3D annotation prototype for outdoor LiDAR scene understanding, built for the University of Jeddah research programme. A browser-based Three.js / WebGL viewer renders large point clouds for interactive semantic annotation, with a FastAPI backend managing datasets and labels and a React front end providing a bilingual (English / Arabic) interface — feeding curated labels into segmentation-model training.</p>
  <div class="fig-row">
    <figure class="proj-fig">
      <img src="{{ '/assets/figures/uoj_annotate.png' | relative_url }}" alt="UoJ LiDAR platform annotation workspace" loading="lazy">
      <figcaption>Annotation workspace with in-browser point-cloud viewer, runtime and method configuration (Cylinder3D / voxel-based segmentation).</figcaption>
    </figure>
    <figure class="proj-fig">
      <img src="{{ '/assets/figures/uoj_bilingual.png' | relative_url }}" alt="UoJ LiDAR platform bilingual English/Arabic interface" loading="lazy">
      <figcaption>Bilingual English / Arabic class labels with a live per-class score summary.</figcaption>
    </figure>
  </div>
</div>

<div class="proj">
  <h3>WA Drone-LiDAR Phenotyping Application</h3>
  <div class="proj-meta">
    <span class="pill app">Desktop application</span>
    <span class="pill">Python</span>
    <span class="pill">Plant phenomics</span>
  </div>
  <p>A Python application that turns raw UAV LiDAR maps into per-plot phenotypic traits. It filters ground returns, automatically segments individual field plots from a 3D map, and computes plant height, biomass and canopy volume — replacing slow, manual field measurement for the Australian Plant Phenomics Network.</p>
  <div class="flow">
    <div class="flow-step alt"><b>UAV LiDAR map</b>Raw 3D point cloud</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>Ground filter</b>Terrain / canopy separation</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>Plot extraction</b>Segment individual plots</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>Trait compute</b>Height · biomass · volume</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step accent"><b>Report</b>Per-plot CSV / traits</div>
  </div>
</div>

<div class="proj">
  <h3>APPN Drone Data Organisation Tool</h3>
  <div class="proj-meta">
    <span class="pill app">Desktop application</span>
    <span class="pill">FAIR data</span>
    <span class="pill">UAV pipeline</span>
  </div>
  <p>A desktop tool that converts raw UAV captures into FAIR-ready, metadata-rich datasets for the Australian Plant Phenomics Network. It standardises folder structure and metadata, drives orthomosaic and radiometric calibration steps, derives vegetation indices, and prepares publication-ready datasets hosted on Pawsey supercomputing.</p>
  <div class="flow">
    <div class="flow-step alt"><b>Raw captures</b>UAV imagery / sensors</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>Metadata</b>Extract + standardise</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>Calibrate</b>Orthomosaic · radiometric</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>Indices</b>NDVI / GLI / biomass traits</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step accent"><b>FAIR dataset</b>Publish to Pawsey</div>
  </div>
</div>

<div class="proj">
  <h3>Pawsey Uploader — Drone Data Transfer to Supercomputing</h3>
  <div class="proj-meta">
    <span class="pill app">Desktop application</span>
    <span class="pill">rclone · S3</span>
    <span class="pill">HPC</span>
  </div>
  <p>A graphical rclone wrapper that moves terabyte-scale drone datasets from local storage to the <strong>Pawsey Supercomputing Centre</strong>, writing to Acacia <strong>S3</strong> object storage while preserving empty-folder structure via directory markers. Once on Pawsey, data is processed on the <strong>Setonix</strong> HPC system and explored interactively on <strong>Nebula</strong> remote visualisation — saving ~A$150k versus commercial cloud.</p>
  <div class="flow">
    <div class="flow-step alt"><b>Drone data</b>Local terabyte-scale captures</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>rclone GUI</b>Transfer + folder markers</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>Acacia S3</b>Pawsey object storage</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>Setonix HPC</b>Parallel processing</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step accent"><b>Nebula</b>Remote 3D visualisation</div>
  </div>
  <p class="proj-links"><a href="https://github.com/appndpird/pawsey-uploader" target="_blank" rel="noopener">GitHub repository ↗</a></p>
</div>

<div class="proj">
  <h3>DotTrack — Mobile Video Labelling for Detection &amp; Tracking</h3>
  <div class="proj-meta">
    <span class="pill app">Android application</span>
    <span class="pill">Annotation</span>
    <span class="pill">Detection / tracking</span>
  </div>
  <p>An Android application (tested on Samsung Galaxy S25) for annotating objects in video to build object-detection and tracking datasets. Users import or capture video, draw and adjust bounding boxes frame by frame with touch-replay and timeline drag-select gestures, propagate boxes across frames, and export annotations in standard formats.</p>
  <div class="flow">
    <div class="flow-step alt"><b>Video</b>Capture / import</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>Frame view</b>Frame-by-frame scrub</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>Annotate</b>Draw &amp; adjust boxes</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>Track</b>Propagate across frames</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step accent"><b>Export</b>Detection / tracking labels</div>
  </div>
  <p class="proj-links"><a href="https://github.com/IbrahimUWA/AI-based-Annotation-tool" target="_blank" rel="noopener">Related annotation tool ↗</a></p>
</div>

<div class="proj">
  <h3>FlowerPower — Flowering-Date Prediction (AWS)</h3>
  <div class="proj-meta">
    <span class="pill app">Web application</span>
    <span class="pill">AWS</span>
    <span class="pill">Agronomy</span>
  </div>
  <p>A decision-support web application that predicts crop flowering dates from weather-station data using generalised additive and machine-learning models, presented through an interactive dashboard. I am responsible for maintaining, updating and deploying the system on <strong>AWS</strong> for ongoing seasonal use by agronomists.</p>
  <div class="flow">
    <div class="flow-step alt"><b>Weather data</b>Station time series</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>Models</b>GAM / ML predictors</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>Prediction</b>Flowering date by variety</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>Dashboard</b>Interactive web UI</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step accent"><b>Deploy</b>AWS hosting</div>
  </div>
</div>

<div class="proj">
  <h3>Dental School Visualisation Tool (UWA)</h3>
  <div class="proj-meta">
    <span class="pill app">Desktop application</span>
    <span class="pill">Python</span>
    <span class="pill">Clinical analysis</span>
  </div>
  <p>A Python desktop application developed with the UWA Dental School for visualisation and clinical examination of tooth quality and statistical analysis of bone and soft tissue near the midline of the front teeth. It is now used by Master's and PhD students in the school.</p>
  <div class="flow">
    <div class="flow-step alt"><b>Scan data</b>Dental imaging / measurements</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>Midline</b>Reference detection</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>Measure</b>Bone &amp; soft-tissue metrics</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><b>Statistics</b>Comparative analysis</div>
    <div class="flow-arrow">→</div>
    <div class="flow-step accent"><b>Report</b>Clinical visualisation</div>
  </div>
</div>

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

- Multi-sensor LiDAR + GNSS + IMU fine alignment via Dynamic Time Warping (*JSTARS 2026*, accepted).
- GNSS-free geo-registration of LiDAR to satellite imagery (*JSTARS 2026*, accepted).
- City-scale 3D change detection (*Scientific Reports*, submitted).
- Structured latent flow for 3D city-scale point cloud generation — GridFlow (*ECCV 2026*, accepted).
- GPU-parallel cylindrical state-space modelling — CylinMamba3D (manuscript in preparation).

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
