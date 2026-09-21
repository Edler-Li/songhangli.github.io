---
title: "The MOSbius Project - Chip Design and Tape Out"
excerpt: "From schematic to tapeout. Design and optimization of a five-transistor OTA, with emphasis on gain, bandwidth, offset, and gm/ID-based transistor sizing. <br/> Article accepted by _MIT URTC_.  _IEEE Xplore_ submission in prep. <br/>"
collection: portfolio
date: 2026-08-01
role: Analog IC Designer - 5T OTA
institution: IEEE SSCS Chipathon 2026 · GF180MCU
read_time: true
authors:
  - Eli Johnson
  - Maxwell Drucker
  - Songhang Li
  - Manuel Garcia
teaser: /images/projects/chipathon2026/teaser.png
---

{% if page.authors %}
<div class="page__meta" style="margin: 0 0 1rem 0;">
  <strong>Authors:</strong> {{ page.authors | join: ", " }}
</div>
{% endif %}

{% include toc %}

# Project Overview

**Four-Topology MOSbius** is an open-source, programmable analog educational chip developed for the **IEEE SSCS Chipathon 2026**. It has four common amplifier topologies: a folded-cascode OTA, five-transistor (5T) OTA, telescopic-cascode OTA, and common-source stage, so students can measure and compare.

The chip is designed for hands-on exploration of DC gain, gain-bandwidth product, phase margin, slew rate, output swing.

All design work used an open-source flow: **Xschem** for schematic, **Ngspice** for simulation, **KLayout** for physical design and verification, and the **GlobalFoundries GF180MCU** open-source PDK.


# Chip Information
![Top-level interface of the Four-Topology MOSbius chip]({{ site.baseurl }}/images/projects/chipathon2026/top.png)
*DUT by Eli*


**Pins**: 17 -- Power 1, Analog 12 (8 Inputs, 4 Outputs), Digital 4 (3 Inputs, 1 Output) -- We have a 'VSS' Pin in top-level, but this is just ground, which is taken care of in the pad ring. So, it is not listed here.

**Area**: 500um x 400um

## Programmable Transistor

Each amplifier is built from programmable transistor cells. A base device remains active while binary-controlled parallel branches change the effective width, producing selectable sizing from the base configuration through 4×. Transmission gates route the complementary scan-chain control signals to the device branches.

![Programmable PFET cell with selectable parallel device branches]({{ site.baseurl }}/images/projects/chipathon2026/programmable_pfet.png)
*Programmable Transistor by Max*

# Schematics 

![Programmable five-transistor OTA schematic]({{ site.baseurl }}/images/projects/chipathon2026/programmable_5tOTA2.png)

# Layout

![Layout of the programmable five-transistor OTA]({{ site.baseurl }}/images/projects/chipathon2026/5t_layout.png)

## DRC and LVS

- The layout is **DRC clean**.
- Schematic and extracted layout is **LVS clean**.

## PEX

**Parasitic Extraction**
Post-layout netlists were used in 5T OTA inverting-amplifier and step-response testbenches across multiple sizing configurations. This stage checks whether interconnect resistance and capacitance preserve the intended gain and transient behavior after integration.

## ESD
The analog pins include secondary I/O protection at the chip level, while the pad ring provides the primary interface to power, ground, analog signals, and digital programming controls. Pin mapping and protection connectivity were included in the top-level verification flow.

# Tape Out in Progress

The project is in **tapeout preparation** through the IEEE SSCS Chipathon 2026 MOSbius track. The design will the **GlobalFoundries GF180MCU 180 nm process**. 
<!-- Silicon characterization will follow manufacturing, with measurements focused on gain, bandwidth, stability, slew rate, power, output range, and variation across programmable sizing modes. -->

![Top-level interface of the Four-Topology MOSbius chip]({{ site.baseurl }}/images/projects/chipathon2026/layout.png)
*Top Level Layout Integration by Max*


# Application Example: Inverting Amplifier

![Top-level inverting-amplifier simulation using the 5T OTA]({{ site.baseurl }}/images/projects/chipathon2026/inverting.png)
*Top Level Simulation Test Bench by Eli*


# Team

- Eli Johnson — Team Lead, Schematic and Design Integration/Troubleshooting, Owner of Folded Cascode Design and Layout, Common-Source Design

- Maxwell Drucker — Layout Integration/Troubleshooting, Owner of Scan Chain, Transmission Gates, Programmable Transistor Block (Digital)

- Manuel Garcia — Owner of Telescopic Cascode Design

- Songhang Li — Owner of 5-Transistor Design and Layout, Start Up Circuit Design

# More About Project

- [MOSbius educational chip platform](https://mosbius.org/0_front_matter/intro.html)
- [Four-Topology MOSbius source repository](https://github.com/elijohnsonn/Four-Topology-MOSbius)
- [IEEE SSCS Chipathon 2026 schedule and track information](https://github.com/sscs-ose/sscs-chipathon-2026/tree/main/schedule)



