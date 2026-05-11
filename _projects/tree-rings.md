---
layout: page
title: Karst Hydrogeology & Bald Cypress Tree Rings
description: Investigating how karst spring hydrology modulates bald cypress climate sensitivity in the Texas Hill Country
img: assets/img/tree_rings/drought_conceptual_model_cartoonV3.jpg
importance: 2
category: work
related_publications: true
---

Central Texas sits at the boundary between the arid west and the humid east, making it
acutely vulnerable to both intense droughts and flooding. As the region's population grows and
climate change increases drought frequency, understanding the full range of past hydroclimate
variability becomes essential for water resource planning. The current planning benchmark —
the 1950s drought of record — may not represent a worst-case scenario. Extending the climate
record beyond the ~150-year instrumental period requires paleoclimate proxies, and bald cypress
(*Taxodium distichum*) trees growing along the spring-fed streams of the Edwards Plateau offer
a promising archive — if their hydrogeologic setting is properly accounted for.

---

## Study Site & Motivation

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid
       loading="eager"
       path="assets/img/tree_rings/MapandCrosssectionV2.jpg"
       title="Geologic map and hydrogeologic cross section of the Pedernales River study area"
       class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Geologic map (left) and cross section (right) of the Pedernales River basin study area,
  approximately 25 miles west of Austin, TX. Red circles mark ephemeral spring-fed trees
  (above the water table); blue circles mark perennial spring-fed trees (below). The cross
  section illustrates how karst aquifer flow paths — diffuse matrix flow vs. conduit flow —
  differ between the two hydrogeologic settings.
</div>

The study area is underlain by flat-lying lower Cretaceous carbonates of the Edwards Plateau.
Perennial springs emerge at the contact between the Cow Creek Limestone and the underlying
Hammett Shale, defining a regional water table. Bald cypress trees growing in creek reaches
*below* this water table receive perennial spring flow; those *above* it are fed by ephemeral
springs that cease flow during drought. This natural experiment makes the Pedernales basin
ideal for isolating the effect of hydrogeologic regime on tree-ring climate sensitivity.

---

## Methods

Increment cores were collected from 31 mature bald cypress trees across five sites: the UT
Hill Country Field Station (Elder and Roy Creeks), Westcave Outdoor Discovery Center, Reimers
Ranch County Park, and the Pedernales River mainstem. Each tree was classified as perennial or
ephemeral based on its elevation relative to the regional water table, verified by two years of
field monitoring.

Ring widths were measured to 0.01 mm precision, visually and statistically crossdated using
CooRecorder, CDendro, and COFECHA, then standardized in R using the dplR package with
negative exponential detrending and a robust biweight mean. Three chronologies were developed:
a full Pedernales River basin chronology (n = 18 cores), and separate perennial (n = 16) and
ephemeral (n = 8) chronologies. Climate sensitivity was evaluated by comparing ring width
indices (RWI) to a 0.5° gridded self-calibrating Palmer Drought Severity Index (scPDSI) over
the 1901–2024 instrumental period using Seascorr, LOWESS regression, and threshold
correlation analysis.

---

## The Pedernales Chronology

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid
       loading="eager"
       path="assets/img/tree_rings/PedernalesChronologyFig.jpg"
       title="Pedernales River Basin ring-width chronology and scPDSI correlation"
       class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Full Pedernales River Basin ring-width chronology (top), with robust signal (SSS > 0.85)
  from 1887–2024. The chronology correlates strongly with central Texas June scPDSI,
  with significant correlation extending from northern Mexico to Oklahoma (bottom left),
  and seasonal correlation peaking in summer months (bottom right).
</div>

The full chronology spans 1448–2024, with robust subsample signal strength (SSS > 0.85) from
1887 onward. The truncation of older records is attributed to late 19th-century logging activity
in the Pedernales region following German settlement in the 1860s. The chronology correlates
most strongly with June scPDSI (r = 0.45, p < 0.001), consistent with previous Texas bald
cypress studies, and shows spatially coherent correlation extending across much of central and
south Texas.

---

## Asymmetric Climate Sensitivity

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid
       loading="eager"
       path="assets/img/tree_rings/TimeseriesFig.jpg"
       title="Time series comparison of perennial and ephemeral chronologies with scPDSI"
       class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Ring width index (RWI) vs. scPDSI for the full Pedernales (A), perennial (B), and ephemeral
  (C) chronologies, 1900–2024. The 1950s drought of record and the 2011 drought are
  highlighted. Note the perennial chronology's muted response to both drought events,
  while the ephemeral chronology preserves their intensity.
</div>

Despite nearly identical overall correlations with scPDSI (r = 0.45, p < 0.001 for both), the
perennial and ephemeral chronologies diverge markedly in how they respond to drought vs.
wet periods:

- **During droughts** (scPDSI < 0): the ephemeral chronology shows a strong, significant
  correlation (r = 0.42, p < 0.001), while the perennial chronology's response is weak and
  insignificant (r = 0.16, p = 0.22). During the extreme 1950s drought of record, perennial tree
  growth shows little reduction — as if the drought were mild.
- **During wet periods** (scPDSI > 0): the pattern reverses. The perennial chronology responds
  robustly (r = 0.33, p < 0.01), while the ephemeral chronology becomes unresponsive
  (r = 0.06, p = 0.67).

<div class="row">
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid
       loading="eager"
       path="assets/img/tree_rings/LOWESSFig.jpg"
       title="LOWESS regression of RWI vs. scPDSI for ephemeral and perennial chronologies"
       class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid
       loading="eager"
       path="assets/img/tree_rings/ThresholdCorrelationFig.jpg"
       title="Threshold correlation analysis across drought and wet period intensities"
       class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Left: LOWESS regression (with bootstrapped 95% confidence intervals) of RWI vs. scPDSI
  for ephemeral (red) and perennial (blue) chronologies. The ephemeral chronology responds
  linearly to dry periods but plateaus during wet periods; the perennial chronology shows the
  opposite pattern. Right: Threshold correlation analysis isolating dry (scPDSI ≤ 0, –1, –1.5,
  –2) and wet (scPDSI ≥ 0, 1, 1.5, 2) periods. The divergence between groups is statistically
  significant for moderate drought and wet conditions.
</div>

---

## A Karst Hydrogeologic Mechanism

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid
       loading="eager"
       path="assets/img/tree_rings/drought_conceptual_model_cartoonV3.jpg"
       title="Conceptual model of karst hydrogeologic control on tree-ring climate sensitivity"
       class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Conceptual model illustrating how characteristic karst flow paths produce asymmetric
  climate sensitivity. During drought (top), diffuse matrix flow sustains perennial springs
  while ephemeral springs cease — buffering perennial trees from moisture stress while
  ephemeral trees record the full drought signal. During wet periods (bottom), rapid conduit
  recharge drives variable perennial spring discharge, while ephemeral springs flow
  semi-perennially regardless of precipitation intensity.
</div>

The asymmetric sensitivity is explained by the dual-porosity nature of karst aquifers. During
**drought**, slow diffuse flow from matrix storage continues to supply perennial springs,
buffering perennial trees from moisture stress even during severe multi-year events like the
1950s drought of record. Ephemeral springs above the water table go dry, leaving ephemeral
trees directly exposed to soil moisture variability and heat stress. During **wet periods**, rapid
conduit flow causes perennial spring discharge to vary with precipitation, producing a strong
growth response in perennial trees. Ephemeral springs flow semi-perennially but the trees they
supply show a suppressed response, possibly due to nutrient limitation, multi-year growth
suppression, or variable water use strategies.

This model is consistent with concurrent geochemical research on spring flow paths in the
area, and with broader literature on climate-modulated karst hydrology.

---

## Implications for Paleoclimate Reconstruction

These findings have direct consequences for how existing Edwards Plateau drought
reconstructions should be interpreted:

- **Drought underestimation**: chronologies built from perennial spring-fed trees — including
  the widely used Krause Springs record — may systematically underestimate the occurrence,
  duration, and intensity of past droughts. This matters most for short, intense events like
  the 2011 drought, which killed an estimated 300 million trees in Texas but may not have
  sufficiently reduced perennial spring discharge to register in perennial tree rings.
- **Standard methods are insufficient**: traditional spatiotemporal correlation, interseries
  correlation, and SSS evaluation do not detect this asymmetric signal loss. The ephemeral
  chronology achieves a robust SSS with only 8 cores, compared to 16 for the perennial
  chronology — reflecting more coherent shared signal, not smaller sample size.
- **Chronology building needs revision**: the standard robust biweight mean implicitly
  assumes symmetric climate signal preservation across trees. Given that perennial trees
  systematically down-weight drought years, mixed chronologies are biased toward
  underestimating past droughts.

---

## Conclusions

Karst hydrogeology fundamentally modulates the climate signal recorded by bald cypress
tree rings in central Texas. Perennial spring-fed trees underestimate droughts; ephemeral
spring-fed trees underestimate wet periods. Previous Edwards Plateau scPDSI reconstructions
likely underestimate the occurrence and intensity of past droughts as a consequence.

Two promising directions emerge from this work: (1) perennial spring-fed trees may serve
as proxies for past spring flow and karst groundwater response to climate, opening a new
paleoclimate archive; and (2) hydrogeology-aware chronology building methods — weighting
individual cores by their hydrogeologic regime — could substantially improve the fidelity of
future drought reconstructions in karst terrain.

---

## Data & Code

Ring-width measurements and chronologies are available upon request pending ITRDB
submission. Analysis code (R/Python) is available on
[GitHub](https://github.com/yourusername/yourrepo).

---

## Associated Thesis

Eagle, W. H. (2026). *Karst Hydrogeology Modulates Bald Cypress Tree-ring Climate
Sensitivity*. Bachelor of Science in General Geology with Honors, The University of Texas
at Austin. Supervised by Jay Banner.