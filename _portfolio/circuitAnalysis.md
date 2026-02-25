---
title: "ELEN 3201 Circuit Analysis Lab"
excerpt: "Filter Design & AC Transient Analysis <br/>"
collection: portfolio
---

<div style="text-align:center; font-size:1.2em;">
</div>

<hr>

#  System Parameters

$$
R_i = 1\,\text{M}\Omega
\quad
C_1 = C_2 = 1\,\mu\text{F}
$$

Natural Frequency:

$$
\omega_0 = 1 \text{ rad/s}
$$

Damping:

$$
\zeta = 0.5 \quad (\text{Underdamped})
$$

---

#  Time-Domain Response

Final solution:

$$
x(t)
=1 - e^{-0.5t}
\left[
\cos\left(\frac{\sqrt{3}}{2}t\right)
+
\frac{1}{\sqrt{3}}
\sin\left(\frac{\sqrt{3}}{2}t\right)
\right]
$$

---

<div align="center">
<img src="{{ site.baseurl }}/images/ELEN3201Exp4/part1Schematic.png" width="65%">
<p><em>State Variable Filter Schematic</em></p>
</div>

<br>

<div align="center">
<img src="{{ site.baseurl }}/images/ELEN3201Exp4/part1aSimulation.png" width="85%">
<p><em>Simulation vs Ideal Response</em></p>
</div>

---

#  Damping Control via $R_3$

| Condition | $R_3$ | Behavior |

|-----------|-------|----------|
| Underdamped | 0.2 MΩ | Oscillatory |
| Critical | 2 MΩ | Fastest non-oscillatory |
| Overdamped | 20 MΩ | Slow monotonic |

<div align="center">
<img src="{{ site.baseurl }}/images/ELEN3201Exp4/part1cSimulation.png" width="85%">
<p><em>Critical Damping</em></p>
</div>

---

# Scaling to $\omega_0 = 100$

To maintain critical damping:

$$
Q = \frac{1}{2}
$$

Set:

$$
C_2 = 0.1\,\text{nF}
\quad
K_3 = 200
$$

---

#  AC Response

<div align="center">
<img src="{{ site.baseurl }}/images/ELEN3201Exp4/part1e.png" width="90%">
<p><em>Bode Response (Critical)</em></p>
</div>

Behavior:

- Low freq: $|H| \approx 1$
- At $\omega_0$: $|H| = 0.5$
- High freq: $|H| \sim (\omega_0/\omega)^2$

---

#  High-Q Case ($Q = 10$)

<div align="center">
<img src="{{ site.baseurl }}/images/ELEN3201Exp4/part1f_Q10.png" width="90%">
<p><em>Sharp Resonance for Q=10</em></p>
</div>

- Peak gain ≈ 20 dB  
- Narrow bandwidth  
- Rapid phase shift  

---

#  Transfer Function

$$
H(\omega)
=\frac{-j\omega \cdot 100}
{-\omega^2 + j\omega \cdot 10 + 10000}
$$

Bandpass response centered at:

$$
\omega_0 = 100 \text{ rad/s}
$$

---

# Extended Frequency Sweep

<div align="center">
<img src="{{ site.baseurl }}/images/ELEN3201Exp4/part1i1GHz.png" width="90%">
<p><em>Second Resonant Mode (~100 kHz)</em></p>
</div>

---


