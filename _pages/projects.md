---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
redirect_from:
  - /projects
---

{% include base_path %}

---

<style>
/* ---- Project cards ---- */
.projects-list {
  display: grid;
  gap: 14px;
}

/* Use <details> for built-in toggle without JS */
.project-card {
  border: 1px solid #e5e7eb;
  border-radius: 12px;
  background: #fff;
  overflow: hidden;
  transition: box-shadow .2s ease, border-color .2s ease;
}
.project-card[open] {
  box-shadow: 0 8px 24px rgba(0,0,0,.06);
  border-color: #d1d5db;
}

/* Summary row: image left, title + button right */
.project-card > summary {
  list-style: none; /* hide default marker */
  display: grid;
  grid-template-columns: 120px 1fr;
  align-items: center;
  gap: 16px;
  padding: 14px;
  cursor: pointer;
}
.project-card > summary::-webkit-details-marker { display: none; }

/* Left image box */
.project-thumb {
  width: 120px;
  height: 90px;
  border-radius: 10px;
  background: #f3f4f6;
  overflow: hidden;
  display: flex; align-items: center; justify-content: center;
  border: 1px solid #eee;
}
.project-thumb img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* Right side: title + "Abstract" button aligned right */
.project-head {
  display: flex;
  align-items: center;
  gap: 12px;
}
.project-title {
  font-weight: 700;
  font-size: 1.05rem;
  flex: 1;
  line-height: 1.2;
}

/* Faux button inside <summary> (clicking anywhere toggles) */
.abstract-btn {
  border: 1px solid #d1d5db;
  padding: 6px 10px;
  border-radius: 8px;
  font-size: .9rem;
  white-space: nowrap;
  background: #f9fafb;
  transition: background .15s ease, border-color .15s ease;
}
.project-card:hover .abstract-btn { background: #f3f4f6; }
.project-card[open] .abstract-btn { background: #eef2ff; border-color: #c7d2fe; }

/* Expanded body */
.project-body {
  padding: 0 14px 14px 14px;
  color: #374151;
  font-size: .96rem;
}

/* Optional meta row (links, tags) */
.project-meta {
  margin-top: 8px;
  display: flex; flex-wrap: wrap; gap: 10px;
  font-size: .9rem;
}
.project-meta a {
  color: #2563eb; text-decoration: none; border-bottom: 1px dashed #93c5fd;
}
.project-meta a:hover { border-bottom-style: solid; }

/* Responsive tweaks */
@media (max-width: 560px) {
  .project-card > summary {
    grid-template-columns: 90px 1fr;
    gap: 12px; padding: 12px;
  }
  .project-thumb { width: 90px; height: 70px; }
}
</style>

<div class="projects-list">

  <!-- PROJECT 1 -->
  <details class="project-card">
    <summary>
      <div class="project-thumb">
        <img src="/images/projects/FTTIs.png" alt="Fluid flow saturation 3D">
      </div>
      <div class="project-head">
        <div class="project-title">Simulation of Fluid Flow in Porous Media for The Development of Flexible Time Temperature Indicators (FTTIs)</div>
      </div>
    </summary>
    <div class="project-body">
      This project models imbibition in porous media and validates Washburn’s equation against simulation and experiment. The first phase focused on matching capillary rise dynamics; subsequent phases explored sensitivity to pore-size distribution, contact angle, and viscosity. Furthermore, imbibtion was explored with different geometric parameters and mixtures.
      <div class="project-meta">
        <a href="/images/projects/final_year_Poster.pdf">View Poster (PDF)</a>
      </div>
    </div>
  </details>

  <!-- PROJECT 2 -->
  <details class="project-card">
    <summary>
      <div class="project-thumb">
        <img src="/images/projects/datacenters.png" alt="Data center CFD">
      </div>
      <div class="project-head">
        <div class="project-title">Hybrid CFD-Deep Learning Approach for Predicting of Thermal flows for Hotspot Mitigation in Datacenter Racks</div>
      </div>
    </summary>
    <div class="project-body">
      We integrate neural surrogates with CFD to accelerate thermal simulations and optimize CRAH setpoints and rack layout under variable loads, reducing time-to-solution and improving cooling efficiency.
    </div>
  </details>

  <!-- PROJECT 3 -->
  <details class="project-card">
    <summary>
      <div class="project-thumb">
        <img src="/images/projects/Ansys4.PNG" alt="2D mesh">
      </div>
      <div class="project-head">
        <div class="project-title">Finite Element Analysis Code Validation with Commercial Solver (ANSYS)</div>
      </div>
    </summary>
    <div class="project-body">
      A custom FEA solver for plane stress/strain with isoparametric elements, Gauss quadrature, and sparse solvers. Validated against Ansys for displacement/stress fields on benchmark geometries.
    </div>
  </details>

  <!-- PROJECT 4 -->
  <details class="project-card">
    <summary>
      <div class="project-thumb">
        <img src="/images/projects/Streamlines.jpg" alt="Streamlines from vortex panel method">
      </div>
      <div class="project-head">
        <div class="project-title">Second Order Vortex Panel Method</div>
      </div>
    </summary>
    <div class="project-body">
      Implemented a second-order panel method to compute lift and Cp distribution on airfoils; validated against thin-airfoil theory and XFOIL for moderate angles of attack. The study was part of Computational Techniques in Aeronautics.
    </div>
  </details>

</div>

