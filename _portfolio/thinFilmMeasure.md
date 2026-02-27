---
title: "Characterization of Ferroelectric Material (PLZT Thin Film)"
excerpt: "Electrical and Optical Measurement of Ferroelectric Material (PLZT)  <br/>"
collection: portfolio
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


# Acquiring thickness, refraction index

## Fit
$\mathrm{MSE} = 6.901$

Roughness $= 25.06 \pm 0.179 \,\mathrm{nm}$  

Thickness #1 $= 96.73 \pm 0.069 \,\mathrm{nm}$  

$$
\begin{aligned}
A &= 2.094 \pm 0.001754 \\
B &= 0.02620 \pm 0.001044 \\
C &= -0.00080784 \pm 0.00013435
\end{aligned}
$$

% Thickness Non-uniformity $= 20.88 \pm 0.776$

$n$ of Cauchy Film @ $632.8 \,\mathrm{nm} = 2.15427$

## Model

10052401_PLZT_on_Silicon

Include Surface Roughness = ON  
Roughness = $\underline{\mathbf{25.06 \,\mathrm{nm}}}$ (fit)

- Layer #1 = Cauchy Film  
$k$ Amplitude = $\underline{0.0000}$  
Exponent = $\underline{1.500}$
Band Edge = $400.0 \,\mathrm{nm}$  
Substrate = SI_JAW  
Angle Offset = $\underline{0.00}$  

### MODEL Options

Include Substrate Backside Correction = OFF  

Model Calculation = Include Thickness Non-uniformity  
  &emsp; % Thickness Non-uniformity = $20.88$ (fit)  
  &emsp; # of Pts = 9

## Capacitance

$$
\begin{aligned}
C_m &= 7.62 \pm 0.3 \,\text{gF}

C &= \frac{\varepsilon_A A}{d}
   = \frac{3.8 \times 71.33 \times 10^{-6}}{0.2 \times 10^{-3}}

\varepsilon_m &= \frac{C_m d}{A}
= \frac{7.62 \times 10^{-12} \times 0.2 \times 10^{-3}}{11.33 \times 10^{-6}}
= 0.021 \times 10^{-9}
= 2.1 \times 10^{-11}

K &= \frac{\varepsilon_m}{\varepsilon_0}
= \frac{2.1 \times 10^{-11}}{8.854 \times 10^{-12}}
= 2.3
\end{aligned}
$$
