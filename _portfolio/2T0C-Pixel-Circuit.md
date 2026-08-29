---
title: "2T0C microLED Pixel Circuit Design"
excerpt: "From single-pixel layout to HD-panel RC delay, refresh rate, and power analysis. <br/>"
collection: portfolio
date: 2026-04-01
role: Circuit and Layout Designer
institution: Columbia University · ELEN 4193 Modern Display Science & Technology
teaser: /images/projects/2t0c-pixel-circuit/pixel_array.png
---
{% if page.authors %}
<div class="page__meta" style="margin: 0 0 1rem 0;">
  <strong>Authors:</strong> {{ page.authors | join: ", " }}
</div>
{% endif %}

{% include toc %}


# Project Overview

This project develops a **two-transistor, zero-capacitor (2T0C) active-matrix pixel** for a microLED display. The work connects device selection, physical layout, parasitic extraction, LTspice verification, and panel-level performance estimates in one design flow.

The pixel uses an **IGZO switching TFT** for low leakage and an **LTPS driving TFT** for high mobility and LED drive capability. Because the 2T0C architecture has no explicit storage capacitor, the driving transistor's gate capacitance and the low leakage of the switching device preserve the programmed state during emission.

## Design Targets and Technology Choices

| Category | Selection | Design rationale |
|---|---|---|
| Switching TFT, $T_S$ | IGZO | Low leakage supports a longer data-hold interval |
| Driving TFT, $T_D$ | LTPS | High mobility provides the current needed by the microLED |
| Emitter | microLED | High luminance and efficiency |
| Interconnect | Aluminum | Low sheet resistance with moderate process cost |
| Oxide thickness | 100 nm | Used for device and parasitic-capacitance estimates |

The pixel measures **440 × 440 µm**, corresponding to approximately **57.7 PPI**. Both TFTs use a channel width of **100 µm** and a channel length of **10 µm**; the microLED emission area is **120 × 120 µm**.

# Pixel Schematic

The SCAN signal enables $T_S$, allowing the DATA line to program the gate of $T_D$. After SCAN returns low, the stored gate voltage keeps $T_D$ conducting and sustains microLED emission until the next write or reset operation.

![LTspice schematic of the 2T0C pixel]({{ site.baseurl }}/images/projects/2t0c-pixel-circuit/spice_schematic.png)

The extracted line resistances and overlap capacitances were included in the simulation model rather than treating the interconnect as ideal.

# Physical Layout

![Physical layout of one 2T0C pixel]({{ site.baseurl }}/images/projects/2t0c-pixel-circuit/pixel_layout.png)

The single-pixel layout integrates the two TFTs, microLED region, and shared SCAN, DATA, and $V_{DD}$ routing inside a repeatable 440 µm pitch.

![Tiled array of 2T0C pixels]({{ site.baseurl }}/images/projects/2t0c-pixel-circuit/pixel_array.png)

Tiling the cell verifies that the horizontal and vertical interconnects remain continuous across an array and provides the geometry used for panel-level RC estimates.

## Extracted Parasitics

For 20 µm-wide, 440 µm-long aluminum lines with a sheet resistance of $0.26\ \Omega/\square$, the SCAN and DATA resistances are each:

$$R = \frac{440}{20}(0.26) = 5.72\ \Omega$$

The 20 × 20 µm overlap regions, separated by 100 nm of oxide, produce approximately 0.138 pF per crossing.

| Parameter | Symbol | Value |
|---|---:|---:|
| SCAN-line resistance | $R_{SCAN}$ | 5.72 Ω |
| DATA-line resistance | $R_{DATA}$ | 5.72 Ω |
| SCAN-to-DATA capacitance | $C_{SCAN-DATA}$ | 0.138 pF |
| SCAN-to-$V_{DD}$ capacitance | $C_{SCAN-VDD}$ | 0.138 pF |
| DATA-to-$V_{DD}$ capacitance | $C_{DATA-VDD}$ | 0.138 pF |
| $T_S$ gate capacitance | $C_{g-T_S}$ | 0.345 pF |
| Total SCAN capacitance | $C_{SCAN}$ | **0.621 pF** |
| Total DATA capacitance | $C_{DATA}$ | **0.276 pF** |

At the pixel level, the resulting time constants are only **3.55 ps** for SCAN and **1.58 ps** for DATA. The more important limitation appears when these parasitics accumulate along a full display row or column.

# LTspice Verification

![Set, hold, and reset simulation waveforms]({{ site.baseurl }}/images/projects/2t0c-pixel-circuit/spice_simulation.png)

The transient simulation demonstrates the three operating states:

1. **Set:** SCAN and DATA overlap, programming the internal gate node and turning on the microLED.
2. **Hold / emission:** SCAN goes low while the internal node retains its voltage, maintaining approximately **4.1 µA** of LED current.
3. **Reset:** SCAN is asserted while DATA is low, discharging the internal node and turning the pixel off.

![Simulated microLED power during the emission interval]({{ site.baseurl }}/images/projects/2t0c-pixel-circuit/spice_simulation_power.png)

The simulated microLED consumes approximately **12 µW** during emission. Assuming a Lambertian emitter and 683 lm/W luminous efficacy, this corresponds to an estimated peak luminance of approximately **6,738 cd/m²** over the pixel area.

# Panel-Level Analysis

Scaling the extracted RC network to a **1920 × 1080** array gives estimated distributed interconnect delays of:

- SCAN line: **6.54 µs**
- DATA line: **0.92 µs**

Using a $3\tau$ row-settling interval gives a maximum estimated refresh rate of **47.2 Hz**. The design is therefore functional, but the SCAN network would need lower resistance, lower capacitance, or segmentation to reach a conventional 60 Hz target with the same settling margin.

## Power Budget

At a 60 Hz operating point and 50% average pixel activity, the estimated HD-panel power is:

| Contribution | Power |
|---|---:|
| SCAN switching | 0.966 mW |
| DATA switching | 0.464 W |
| microLED emission | 12.44 W |
| **Total** | **12.9 W** |

Approximately **96% of the panel power is spent on light emission**, so emitter efficiency and brightness control dominate the power budget more than the SCAN and DATA backplane switching.

# Results

The design achieves:

- **6,738 cd/m²** estimated peak luminance
- **57.7 PPI** pixel density
- **47.2 Hz** estimated maximum refresh rate
- **12.9 W** estimated HD-panel power at 50% activity
- **83,678 cd·Hz·PPI/(m²·W·cost-unit)** figure of merit

The project shows how a compact pixel that performs well in a single-cell simulation can become limited by interconnect delay when scaled to a full panel. The next design iteration would focus on improving the SCAN-line RC constant while preserving the low-leakage hold behavior of the IGZO/LTPS 2T0C architecture.
