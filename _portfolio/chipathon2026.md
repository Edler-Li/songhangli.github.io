---
title: "The MOSbius Project - Chips Design and Tape Out"
excerpt: "From schematic to tapeout. Design and optimization of a five-transistor OTA, with emphasis on gain, bandwidth, offset, and gm/ID-based transistor sizing. <br/>"
collection: portfolio
date: 2026-08-01
role: Analog IC Designer
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

---
# Project Overview
To design and fabricate a chip containing several of the most common
amplifier topologies, all with accessible pins, so that a student can wire up, test,
characterize, and compare each amplifier.
Students measure DC gain, GBW, slew rate, stability, PSRR, etc. for each
amplifier, learning the trade-offs through hands-on experimentation

# Chip Infomation

## Pins
**Total Required Pins**: 17 -- Power 1, Analog 12 (8 Inputs, 4 Outputs), Digital 4 (3 Inputs, 1 Output) -- We have a 'VSS' Pin in top-level, but this is just ground, which is taken care of in the pad ring. So, it is not listed here.

*------insert top.png here

## Area
**Area**: 500um x 400um

## Programmable Transistor

*------insert programmable_pfet.png here

# Schematics

# Layout

*------insert layout.png here

## DRC

## LVS

## PEX

## ESD 

# Tape Out in Progress

## Manufacture

### Global Foundaries GF180MCU

# Simulations

# Applications

## Inverting Op Amp
*------insert inverting.png here

## Transient Measurement

# Team

- Eli Johnson — Team Lead, Schematic and Design Integration/Troubleshooting, Owner of Folded Cascode Design and Layout, Common-Source Design

- Maxwell Drucker — Layout Integration/Troubleshooting, Owner of Scan Chain, Transmission Gates, Programmable Transistor Block (Digital)

- Manuel Garcia — Owner of Telescopic Cascode Design

- Songhang Li — Owner of 5-Transistor Design and Layout, Start Up Circuit Design

## Goal: 


## Schematic
<img width="654" height="831" alt="image" src="https://github.com/user-attachments/assets/83773d0b-c978-4ad5-b898-aacc39b016dd" />

## Transient
<img width="1459" height="800" alt="5tOTA_tb_tran_SR_sch" src="https://github.com/user-attachments/assets/e7007055-aa13-4432-8116-18e185ad2f91" />

## AC Open Loop
<img width="1728" height="700" alt="programmable_5tota_tb_ac_open_loop_sch" src="https://github.com/user-attachments/assets/af34017a-9155-40c1-ae54-a3738d5ad3fb" />

## Top Level
<img width="1728" height="694" alt="5t_inverting_sin_3x_sch" src="https://github.com/user-attachments/assets/0dba2685-81f2-4301-8b47-5b65ed2f870c" />

## More About Chipathon 2026 and our team

https://github.com/sscs-ose/sscs-chipathon-2026/tree/main/schedule

https://github.com/elijohnsonn/Four-Topology-MOSbius

https://mosbius.org/0_front_matter/intro.html

