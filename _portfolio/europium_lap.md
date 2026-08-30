---
title: "Optically Stimulated Luminescence of Europium-Doped LaAlO3"
excerpt: "Optical spectroscopy and time-resolved characterization of europium-doped lanthanum aluminate, including excitation-dependent decay dynamics, temperature-dependent phosphorescence, and a coupled rate-equation model. <br/>"
collection: portfolio
date: 2025-01-01
role: Undergraduate Researcher
institution: Franklin & Marshall College · Ken Krebs Lab
read_time: true
authors:
  - Songhang Li
  - J. Kenneth Krebs
teaser: /images/projects/europium-lap/SamplePicture2.png
---

{% if page.authors %}
<div class="page__meta" style="margin: 0 0 1rem 0;">
  <strong>Authors:</strong> {{ page.authors | join: ", " }}
</div>
{% endif %}

{% include toc %}

# Project Overview

This project investigated the optical response of europium-doped lanthanum aluminate, $\mathrm{LaAlO_3:Eu^{3+}}$ (LAP:Eu). This phosphor system is relevant to lighting and display technologies as well as X-ray and computed-tomography imaging. The work connected three parts of the material response: the Eu$^{3+}$ electronic-level structure, the measured emission spectrum, and the time-dependent fluorescence and phosphorescence following ultraviolet excitation.

The study had three main objectives:

1. Compare calculated Eu$^{3+}$ energy levels with the measured emission spectrum.
2. Measure the decay dynamics of the excited europium population after pulsed UV excitation.
3. Test whether a compact population-transfer model could explain the observed fluorescence and phosphorescence.

# Material System

The sample consisted of Eu$^{3+}$ ions incorporated into a $\mathrm{LaAlO_3}$ host. The host crystal provides the local environment for the optically active europium ions, while charge traps introduce slower population-transfer pathways that can produce persistent emission after excitation.

![Crystal structure of europium-doped lanthanum aluminate]({{ site.baseurl }}/images/projects/europium-lap/Structure1.png)

The mounted sample was inspected under room illumination and UV excitation. The UV-excited image provides a direct qualitative check of the europium emission before time-resolved measurements.

<div class="responsive-row">
  <div class="row-media" style="--image-max-width: 360px;">
    <figure>
      <img src="{{ site.baseurl }}/images/projects/europium-lap/SamplePicture.png" alt="Mounted LAP europium sample under room light">
      <figcaption>Mounted sample under room light.</figcaption>
    </figure>
  </div>
  <div class="row-media" style="--image-max-width: 360px;">
    <figure>
      <img src="{{ site.baseurl }}/images/projects/europium-lap/SamplePicture2.png" alt="Mounted LAP europium sample under ultraviolet excitation">
      <figcaption>Visible luminescence under UV excitation.</figcaption>
    </figure>
  </div>
</div>

# Experimental Setup

Pulsed 337 nm and 266 nm excitation sources were used to populate different portions of the material's excited-state and trap system. The fluorescence near 618 nm was isolated optically and recorded using a monochromator and oscilloscope. A photodiode monitored the excitation pulse to provide a timing reference.

![Optical setup for pulsed excitation and time-resolved emission measurements]({{ site.baseurl }}/images/projects/europium-lap/setup_diagram.png)

This arrangement supported both spectral measurements and time-resolved decay acquisition. Comparing the two excitation wavelengths helped distinguish direct europium excitation from higher-energy processes involving charge traps.

# Emission Spectrum

The emission spectrum under 266 nm excitation contains several narrow features associated with transitions between Eu$^{3+}$ $4f$ levels. The strongest measured features occur near 595 nm and 618 nm, with additional weaker emission at longer wavelengths.

![Measured emission spectrum following 266 nm excitation]({{ site.baseurl }}/images/projects/europium-lap/Emission.png)

The measured transition energies were compared with density-functional-theory calculations of the Eu$^{3+}$ electronic levels. The correspondence between the calculated levels and measured peaks supported the assignment of the observed emission to europium-centered transitions.

![Calculated Eu3+ electronic levels and optical transitions]({{ site.baseurl }}/images/projects/europium-lap/Eu3+ElectronicLevels_.png)

# Population-Transfer Model

A three-population model was used to describe the emission dynamics:

- $S$: population of Eu ions in the emitting $^5D_0$ state;
- $T$: trapped-charge population;
- $H$: population in higher-energy states;
- $f_{ij}$: transfer rate from population $i$ to population $j$;
- $f_{sr}$: radiative decay rate of the emitting state.

The coupled rate equations are

$$
\begin{aligned}
\dot{S} &= Hf_{hs}+Tf_{ts}-Sf_{sr}, \\
\dot{T} &= Hf_{ht}-Tf_{ts}, \\
\dot{H} &= -H\left(f_{ht}+f_{hs}\right).
\end{aligned}
$$

After the initial filling of $S$ and $T$ from $H$ is neglected, the emitting-state population can be written as a sum of two exponential components:

$$
S(t)=C_S e^{-f_{sr}t}
  +\left(\frac{f_{ts}}{f_{sr}-f_{ts}}\right)C_T e^{-f_{ts}t}.
$$

The fast component represents direct fluorescence from the Eu$^{3+}$ emitting state, while the slower component represents delayed population transfer from traps. This produces the biexponential behavior observed in measurements that strongly populate the trap pathway.

![Numerical solution of the emitting-state and trap populations]({{ site.baseurl }}/images/projects/europium-lap/numerical_solution.png)

# Results

## 337 nm excitation

The room-temperature decay following 337 nm excitation was well described by a predominantly single-exponential response. The fitted lifetime was approximately 2.7 ms. A short population rise immediately after the pulse was also resolved, while this excitation wavelength produced no measurable long-lived phosphorescence contribution.

![Room-temperature lifetime measurement under 337 nm excitation]({{ site.baseurl }}/images/projects/europium-lap/RoomTem337nmLifetime.png)

## 266 nm excitation and temperature dependence

Higher-energy 266 nm excitation produced both a fast fluorescence component and a slower phosphorescence component. Measurements across approximately 78-255 K were described well by the biexponential model.

![Low- and high-temperature decay measurements under 266 nm excitation]({{ site.baseurl }}/images/projects/europium-lap/LowHighTem266nmLifetime.png)

The fitted trap-to-emitter transfer rate, $f_{ts}$, increased by approximately 35% across the measured temperature range. Equivalently, the transfer rate decreased as the sample was cooled. This temperature dependence supports the interpretation that the slow component is controlled by thermally assisted release from trapped states.

# Conclusions

- Eu-doped $\mathrm{LaAlO_3}$ samples produced by combustion synthesis exhibited identifiable Eu$^{3+}$ emission features.
- The measured emission spectrum agreed well with calculated $4f$ electronic-level transitions.
- Both fluorescence and phosphorescence decay dynamics were measured after pulsed excitation.
- A compact biexponential population-transfer model described the two decay components.
- The trap-to-europium transfer rate decreased at lower temperature, demonstrating the thermal sensitivity of the persistent-luminescence pathway.

# Research Presentation

This work was presented as a research poster at a Mid-Atlantic Section meeting of the American Physical Society at Temple University in Pennsylvania.

# References

1. P. Głuchowski, W. Stręk, M. Lastusaari, and J. Hölsä, “Optically stimulated persistent luminescence of europium-doped LaAlO3 nanocrystals,” *Physical Chemistry Chemical Physics*, vol. 17, pp. 17246-17252, 2015.
2. C. Furetta and G. Kitis, “Models in thermoluminescence,” *Journal of Materials Science*, vol. 39, pp. 2277-2294, 2004.
