---
title: "Characterization of Ferroelectric Material (PLZT Thin Film)"
excerpt: "Electrical and Optical Measurement of Ferroelectric Material (PLZT)  <br/>"
collection: portfolio
date: 2024-12-01
---

Refraction index and dielectric constant of PLZT film based on silicon substrate

# Overview

- Investigated the relation between the refraction index and dielectric constants of PLZT film.
- Built multilayer models by ellipsometry data analysis software CompleteEASE to model measurements of the thickness of thin films.
- Measured the refraction index using J.A. Woollam M-2000 spectrum ellipsometry.
- Made a two-plate capacitor with PLZT as dielectric layer to obtain the dielectric constant from
capacitance measurements.

# PLZT sample information

(PLZT)  is a perovskite material that has piezoelectric effect. The inner electric field after polarized the film will increase the dielectric constant.

- 10052604: $1" \times 1"$ ITO
- Cleaned with lens paper and methional
- Spun on Program A
- 0.200 mL PLZT
- Pushed through Fahrenheit at 650 degrees

<img src="{{ site.baseurl }}/images/PLZTFilm1.jpeg" alt="Description" style="width: 80%; display: block; margin: 0 auto;">

# Ellipsometry measurement process: calibration, alignment, acquiring data

- Turn on the EC-400 power, M-2000V Lamp Power and vaccum
- Calibrate the incident emitter, sample stage and receiver.
- Conduct sample alignment each time before acquiring data. (Center the cursor to match the cross shown on the calibration panel)
- Set the angle parameter to 65 degrees, choose robust measurement mode.
- Click acquiring data button under the measurement panel
- Save the file as the SE. file type and Snapshot
- Conduct Data analysis section
- Build a model for corresponding PLZT film
- Click Generate button under the Analysis panel
- Click Fit button near the Generate button under the analysis panel

<img src="{{ site.baseurl }}/images/PLZTFilm2.jpeg" alt="Description" style="width: 80%; display: block; margin: 0 auto;">

# Acquiring thickness, refraction index

## Fit

* **MSE** = 6.901
* **Roughness** = 25.06 ± 0.179 nm
* **Thickness #1** = 96.73 ± 0.069 nm
* **Cauchy Parameters:**
  * A = 2.094 ± 0.001754
  * B = 0.02620 ± 0.001044
  * C = -0.00080784 ± 0.00013435
* **% Thickness Non-uniformity** = 20.88 ± 0.776
* **n of Cauchy Film** (@ 632.8 nm) = 2.15427

## Model
* Include Surface Roughness = ON 
* Roughness = 25.06 nm (fit)

* **Layer #1 = Cauchy Film**
  * Thickness #1 = **96.73 nm** (fit)
  * A = 2.094 (fit), B = 0.02620 (fit), C = -0.00080784 (fit)
  * k Amplitude = <u>0.0000</u>, Exponent = <u>1.500</u>
  * Band Edge = 400.0 nm
  * Substrate = `SI_JAW`
  * Angle Offset = <u>0.00</u>

* **MODEL Options**
  * Include Substrate Backside Correction = OFF
  * Model Calculation = Include Thickness Non-uniformity
  * % Thickness Non-uniformity = 20.88 (fit)
  * \# of Pts = 9

## Capacitance
* **C<sub>m</sub>** = 7.62 ± 0.3 pF
* **C** = (ε<sub>A</sub>A) / d = (3.8 × 71.33 × 10<sup>-6</sup>) / (0.2 × 10<sup>-3</sup>)
* **ε<sub>m</sub>** = (C<sub>m</sub>d) / A = (7.62 × 10<sup>-12</sup> × 0.2 × 10<sup>-3</sup>) / (11.33 × 10<sup>-6</sup>) = 0.021 × 10<sup>-9</sup> = 2.1 × 10<sup>-11</sup>
* **K** = ε<sub>m</sub> / ε<sub>0</sub> = (2.1 × 10<sup>-11</sup>) / (8.854 × 10<sup>-12</sup>) = 2.3
