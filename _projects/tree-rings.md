---
layout: page
title: Tree Ring Research
description: Brief one-liner that appears on the projects card
img: assets/img/projects/tree-rings/drought_conceptual_model_cartoonV3.jpg
importance: 2
category: research
related_publications: true
---

<!-- ============================================================
     ALFOLIO PROJECT PAGE — ARTICLE STYLE TEMPLATE
     Drop into _projects/ and rename the file (e.g. tree-rings.md)
     
     Images go in:  assets/img/projects/tree-rings/
     Bibliography:  add entries to _bibliography/papers.bib and
                    reference them with  {% cite yourkey %}
     ============================================================ -->

## Overview

Write a 1–3 paragraph introduction here. Describe the motivation, study system, and
key questions driving this work. This is the "lede" — readers should understand what
you did and why it matters without scrolling further.

---

## Study Sites & Chronology Development

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid
       loading="eager"
       path="assets/img/projects/tree-rings/MapandCrosssectionV2.jpg"
       title="Study site map"
       class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid
       loading="eager"
       path="assets/img/projects/tree-rings/core.jpg"
       title="Field coring"
       class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Left: Map of sampling locations across the study region. Right: Increment core extraction
  from a mature ponderosa pine at [Site Name, elevation]. Scale bar = 10 cm.
</div>

Describe the field and lab methods: species sampled, site selection criteria, cross-dating
procedure, detrending approach (e.g. negative exponential, signal-free standardization),
and any software used (COFECHA, dplR, etc.).

---

## Climate Signal

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid
       loading="eager"
       path="assets/img/projects/tree-rings/chronology.jpg"
       title="Master chronology"
       class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Master ring-width chronology (black) with sample depth (gray fill), AD [start]–[end].
  Shading indicates periods with fewer than [N] series.
</div>

Discuss the climate signal embedded in the chronology: response function results,
dominant climate drivers (PDSI, winter precipitation, temperature), and how the signal
compares to regional reconstructions or instrumental records.

---

## Reconstruction & Results

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid
       loading="eager"
       path="assets/img/projects/tree-rings/reconstruction.jpg"
       title="Climate reconstruction"
       class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  [Variable] reconstruction (blue) vs. instrumental record (orange), [date range].
  Dashed lines mark the 25th and 75th percentile thresholds. Calibration period
  highlighted in gray; R² = [X], RE = [X].
</div>

Present the key reconstruction statistics and highlight notable features — prolonged
droughts, pluvials, anomalous decades — and situate them in historical or
paleoclimatic context.

---

## Comparison with Other Proxies

<div class="row">
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid
       loading="eager"
       path="assets/img/projects/tree-rings/comparison.jpg"
       title="Multi-proxy comparison"
       class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid
       loading="eager"
       path="assets/img/projects/tree-rings/wavelet.jpg"
       title="Wavelet coherence"
       class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Left: Correlation between this reconstruction and regional PDSI atlas grid points.
  Right: Wavelet coherence between reconstruction and [comparison record], showing
  significant periodicity at [X]-year cycles (5% significance cone shown).
</div>

Discuss how this reconstruction aligns with or diverges from nearby tree-ring
chronologies, lake sediment records, or historical documents.

---

## Key Findings

- **Finding one** — e.g. the 16th-century megadrought appears as the most severe
  sustained dry period in the past 500 years.
- **Finding two** — e.g. the reconstruction explains 58% of variance in July PDSI
  over the 1901–2000 instrumental period.
- **Finding three** — e.g. spectral analysis reveals significant quasi-decadal
  periodicity consistent with PDO forcing.

---

## Data Availability

Raw ring-width measurements and the final chronology are archived at the
[ITRDB](https://www.ncei.noaa.gov/products/paleoclimatology/tree-ring) under
accession number **[XXXXX]**. R scripts for detrending and reconstruction are
available on [GitHub](https://github.com/yourusername/yourrepo).

---

## Publications

{% cite YourLastName2024 %}
