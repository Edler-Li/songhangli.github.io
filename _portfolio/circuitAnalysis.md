---
title: "ELEN 3201 Circuit Analysis Lab"
excerpt: "Short description of ELEN 3201 Circuit Analysis <br/>"
collection: portfolio
permalink: /portfolio/ELEN3201-Experiment4/
---


<figure id="fig:placeholder" data-latex-placement="H">
<img src="{{ site.baseurl }}/images/ELEN3201Exp4/part1Schematic.png" style="width:75.0%" />
<figcaption>Caption</figcaption>
</figure>


# ELEN 3201 Circuit Analysis Experiment 4  
*November 2025*

---

# Part 1

---

## (a) Underdamped Case

Given:

$$
R_1 = R_2 = R_3 = R_4 = R_5 = R_6 = R_7 = R_8 = 1\,\text{M}\Omega
$$

$$
C_1 = C_2 = 1\,\mu\text{F}
$$

Natural frequency:

$$
\omega_0
= \sqrt{\frac{K_1}{\tau_1 \tau_2}}
= \sqrt{\frac{R_5}{R_6} \cdot \frac{1}{R_1 C_1 R_2 C_2}}
= 1
$$

Damping:

$$
\alpha = \frac{1}{2}
\quad\quad
\omega_d = \frac{\sqrt{3}}{2}
$$

Since $\zeta = 0.5 < 1$, the system is **underdamped**.

Final response:

$$
x(t)
=
1 -
e^{-0.5t}
\left[
\cos\left(\frac{\sqrt{3}}{2}t\right)
+
\frac{1}{\sqrt{3}}
\sin\left(\frac{\sqrt{3}}{2}t\right)
\right]
$$

---

<figure>
<img src="{{ site.baseurl }}/images/ELEN3201Exp4/part1Schematic.png" style="width:75%">
<figcaption>Part 1 Schematic</figcaption>
</figure>

<figure>
<img src="{{ site.baseurl }}/images/ELEN3201Exp4/part1aSimulation.png" style="width:100%">
<figcaption>Simulation (green) vs Ideal (red)</figcaption>
</figure>

<figure>
<img src="{{ site.baseurl }}/images/ELEN3201Exp4/part1aMeasurement.png" style="width:50%">
<figcaption>Measurement</figcaption>
</figure>

---

## (b) Shorting $R_3$

Shorting $R_3$ removes damping ($\zeta = 0$).  
The system oscillates indefinitely (ideal case).

<figure>
<img src="{{ site.baseurl }}/images/ELEN3201Exp4/part1bSimulation.png" style="width:100%">
<figcaption>Simulation – Shorted R3</figcaption>
</figure>

---

## (c) Critically Damped

To achieve $\zeta = 1$:

$$
Q = \frac{1}{2}
\quad \Rightarrow \quad
K_3 = 2
$$

$$
R_3 = 2\,\text{M}\Omega
$$

<figure>
<img src="{{ site.baseurl }}/images/ELEN3201Exp4/part1cSimulation.png" style="width:100%">
<figcaption>Critically Damped ($R_3 = 2M\Omega$)</figcaption>
</figure>

---

## (d) Scaling to $\omega_0 = 100$

Maintain:

$$
Q = \frac{1}{2}
$$

Then:

$$
K_3 = 200
$$

Modify:

$$
C_2 = 0.1\,\text{nF}
$$

Choose:

- $R_4 = 2k\Omega$
- $R_3 = 400k\Omega$ (critical)
- $R_3 = 40k\Omega$ (underdamped)
- $R_3 = 4M\Omega$ (overdamped)

---

## (e) AC Analysis

<figure>
<img src="{{ site.baseurl }}/images/ELEN3201Exp4/part1e.png" style="width:100%">
<figcaption>AC Simulation</figcaption>
</figure>

For $\zeta = 1$:

- Low freq: $|H| \approx 1$
- At $\omega_0$: $|H| = 0.5$
- High freq: $|H| \sim (\omega_0/\omega)^2$

---

## (f) $Q = 10$

Reduce $K_3$ by factor of 20.

<figure>
<img src="{{ site.baseurl }}/images/ELEN3201Exp4/part1f_Q10.png" style="width:100%">
<figcaption>High-Q Response</figcaption>
</figure>

- Sharp resonance at $\approx 100$ rad/s  
- Peak gain ≈ 10 (20 dB)  
- Narrow bandwidth  

---

## (g) U1 Output (Bandpass)

<figure>
<img src="{{ site.baseurl }}/images/ELEN3201Exp4/part1gU1output.png" style="width:100%">
<figcaption>U1 Frequency Response</figcaption>
</figure>

Behavior:

- Low freq → 0  
- Peak at $\omega_0$  
- High freq → 0  

---

## (h) Transfer Function

$$
H_{U1}(\omega)
=
\frac{-j\omega \cdot 100}
{-\omega^2 + j\omega \cdot 10 + 10000}
$$

Bandpass behavior centered at $\omega_0 = 100$ rad/s.

---

## (i) Second Resonance

<figure>
<img src="{{ site.baseurl }}/images/ELEN3201Exp4/part1i1GHz.png" style="width:100%">
<figcaption>Extended Frequency Sweep</figcaption>
</figure>

Second resonance near 100 kHz.

---


