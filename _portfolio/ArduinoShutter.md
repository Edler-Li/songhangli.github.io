---
title: "DC Mechanical Shutter with H Bridget Controller and Arduino"
excerpt: "This subproject was part of the Photon Counting Experiment of Persistent Luminescence in Eu:LAP<br/>

Developed a circuit solution using Arduino to precisely control excitation laser mechanical shutter <br/>"
collection: portfolio
---

# Design goal
Developing a controller using an Arduino and H-bridge module to precisely control an excitation laser mechanical shutter, enabling photon counting of early-state decay.

# Background
In the Photon Counting Experiment of Persistent Luminescence in Eu:LAP with Professor Ken Krebs, 
the excitation time interval and intensity play a significant role in measuring photon emission characteristics. 
The existing spinning disk shutter in the lab, however, has critical limitations: it cannot provide excitation intervals longer than 10 seconds, 
nor can it operate at the microsecond timescales required for time-resolved measurements. 
Specifically, the experiment demands both
- extended dark periods of up to 20 seconds between excitation pulses allowing complete relaxation of the sample back to its ground state and
- ultrashort excitation bursts on the order of microseconds to isolate and capture the photon emission profile during early-state decay.

These two requirements exist at opposite ends of the temporal spectrum and cannot be realized by a single mechanical spinning disk. 
As a result, precise control over excitation timing is lost, introducing uncertainty into the photon counting data and limiting the decay measurements. To overcome these constraints, a new shutter control system is required. 

This project presents the design and implementation of an Arduino-based controller paired with an H-bridge motor driver module 
to operate a mechanical laser shutter with high temporal precision. 
The system is capable of triggering shutter open and close events across a wide dynamic range time, from millisecond excitation pulses to multi-second intervals, offering the flexibility needed for both fast and slow photon counting experiment. 
The design prioritizes low-latency response, repeatability, and ease of integration with existing experimental setups.


<img src="{{ site.baseurl }}/images/DC1.jpeg" alt="Description" style="width: 80%; display: block; margin: 0 auto;">

<img src="{{ site.baseurl }}/images/DC2.jpeg" alt="Description" style="width: 80%; display: block; margin: 0 auto;">

<img src="{{ site.baseurl }}/images/DC3.jpeg" alt="Description" style="width: 80%; display: block; margin: 0 auto;">
