---
title: "ELEN 3802 Digital System Lab 1"
excerpt: "Short description of ELEN 3802 Digital System Lab 1<br/>"
collection: portfolio
---
# Q1 Noise Margin

<figure id="fig:placeholder" data-latex-placement="H">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q1.png" style="width:75.0%" />
<figcaption>Q1 XY mode</figcaption>
</figure>

- *V*<sub>*IH*</sub> = 1.469 V

- *V*<sub>*IL*</sub> = 1.183 V

- *V*<sub>*OH*</sub> = 4.07 V

- *V*<sub>*OL*</sub> = 0.233 V

- *NM*<sub>*H*</sub> = *V*<sub>*OH*</sub> − *V*<sub>*IH*</sub> = 4.07 − 1.469 = 2.601 V

- *NM*<sub>*L*</sub> = *V*<sub>*IL*</sub> − *V*<sub>*OL*</sub> = 1.183 − 0.233 = 0.950 V

Capacitance only resists changes in AC, meaning that it affects the
speed of the gate, not the final voltage levels it reaches.

# Q2 Delay Measurement

## 66pF:

- *t*<sub>*p**H**L*</sub> = 7.820 ns

- *t*<sub>*p**L**H*</sub> = 28.140 ns

<figure id="fig:66_parallel" data-latex-placement="H">
<figure id="fig:66_tpLH">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q2_66_tpLH.png" />
<figcaption>Q2 66 tpLH</figcaption>
</figure>
<figure id="fig:66_tpHL">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q2_66_tpHL.png" />
<figcaption>Q2 66 tpHL</figcaption>
</figure>
<figcaption>Q2 66 propagation delay comparison</figcaption>
</figure>

## 0.1 uF:

- *t*<sub>*p**H**L*</sub> = 7.040 ns

- *t*<sub>*p**L**H*</sub> = 25.000 ns

These values are given by *Δ*X shown on the oscilloscope.

<figure id="fig:0.1_parallel" data-latex-placement="H">
<figure id="fig:0.1_tpLH">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q2_0.1_tpLH.png" />
<figcaption>Q2 0.1 tpLH</figcaption>
</figure>
<figure id="fig:0.1_tpHL">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q2_0.1_tpHL.png" />
<figcaption>Q2 0.1 tpHL</figcaption>
</figure>
<figcaption>Q2 0.1 propagation delay comparison</figcaption>
</figure>

# Q3 74HC00 Noise Margin

- *V*<sub>*IH*</sub> = 2.317 V

- *V*<sub>*IL*</sub> = 2.15 V

- *V*<sub>*OH*</sub> = 5.03 V

- *V*<sub>*OL*</sub> = 0.400 V

- *NM*<sub>*H*</sub> = *V*<sub>*OH*</sub> − *V*<sub>*IH*</sub> = 5.03 − 2.317 = 2.713 V

- *NM*<sub>*L*</sub> = *V*<sub>*IL*</sub> − *V*<sub>*OL*</sub> = 2.15 − 0.400 = 1.750 V

<figure id="fig:Q3_74HC00_XY" data-latex-placement="H">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q3_74HC00_XY.png" style="width:75.0%" />
<figcaption>Q3 74HC00 XY plot</figcaption>
</figure>

# Q4 74HC00 Delay Measurement

## 66 pF:

- *t*<sub>*p**H**L*</sub> = 15.620 ns

- *t*<sub>*p**L**H*</sub> = 71.880 ns

<figure id="fig:Q4_66_parallel" data-latex-placement="H">
<figure id="fig:Q4_66_tpLH">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q4_66_tpLH.png" />
<figcaption>Q4 66 tpLH</figcaption>
</figure>
<figure id="fig:Q4_66_tpHL">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q4_66_tpHL.png" />
<figcaption>Q4 66 tpHL</figcaption>
</figure>
<figcaption>Q4 66 propagation delay comparison</figcaption>
</figure>

## 0.1 *μ*F:

- *t*<sub>*p**H**L*</sub> = 12.500 ns

- *t*<sub>*p**L**H*</sub> = 70.320 ns

<figure id="fig:Q4_01_parallel" data-latex-placement="H">
<figure id="fig:Q4_01_tpLH">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q4_0.1_tpLH.png" />
<figcaption>Q4 0.1 tpLH</figcaption>
</figure>
<figure id="fig:Q4_01_tpHL">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q4_0.1_tpHL.png" />
<figcaption>Q4 0.1 tpHL</figcaption>
</figure>
<figcaption>Q4 0.1 propagation delay comparison</figcaption>
</figure>

# Q5

<figure id="fig1:q5" data-latex-placement="H">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q5.png"
style="width:75.0%" />
<figcaption>Q5 Green=input signal. Yellow=output signal</figcaption>
</figure>

The output signal’s frequency is half that of the input signal (500Hz
expected).

As we increased the frequency, the following output is obtained:

<figure id="fig2:q5" data-latex-placement="H">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q5_2.png"
style="width:75.0%" />
<figcaption>Q5 Green=input signal. Yellow=output signal</figcaption>
</figure>

<figure id="fig3:q5" data-latex-placement="H">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q5_3.png"
style="width:75.0%" />
<figcaption>Q5 Green=input signal. Yellow=output signal</figcaption>
</figure>

<figure id="fig4:q5">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q5_4.png"
style="width:75.0%" />
<figcaption>Keep increasing the frequency</figcaption>
</figure>

<figure id="fig5:q5">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q5_5.png"
style="width:75.0%" />
<figcaption>Keep increasing the frequency</figcaption>
</figure>

<figure id="fig6:q5">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q5_6.png"
style="width:75.0%" />
<figcaption>High frequency</figcaption>
</figure>

The chip keeps working because the maximum frequency that the waveform
generator allows is 20MHz but based on the data sheet of the 74F74 the
chip can function up to 100MHz.

If the frequency is too high, breakdowns happen because the new data do
not arrive at the D pin fast enough, causing the flip-flop to fail to
toggle.

Circuit appears to continue functioning at very high frequencies because
the flip-flop may start acting like an amplifier rather than a frequency
divider, producing a sine-like wave that happens to be a multiple of the
input.

# Q6

## Question 6(a)

How does the debouncer operate?

The debouncer bounces between states. It can have multiple states that
are noisy. The SR latch prevents the bouncing. It allows the NAND gate
to work properly without noise when combined with the switch. The images
below show the behavior of R, S, and Q, with the lines of yellow, green,
and blue, respectively.

<figure id="fig:q6_parallel" data-latex-placement="H">
<figure id="fig:q6_pressed">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q6_1.png" />
<figcaption>R and S are high, Q is low. (button is pressed)</figcaption>
</figure>
<figure id="fig:q6_not_pressed">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Q6_2.png" />
<figcaption>R is low, S is high, Q is high. (button not pressed)
</figcaption>
</figure>
<figcaption>Q6 SR latch behavior. R=Yellow, S=Green, Q=Blue</figcaption>
</figure>

When the button is not pressed, the circuit is open. R is low while both
S and Q are high. When the button is pressed, R is high while both S and
Q are low. When the button is slightly pressed, nothing happens because
the debouncer utilizes the latch’s ability to maintain its current state
when both set (S) and reset (R) inputs are low, ignoring the rapid
transitions caused by switch bounce while only changing its output state
once the switch settles on a new and stable position. When the button is
not pressed, R is grounded and S is not, which makes Q high. When the
button is pressed, S is grounded and R is not, which makes Q not go
high, which means Q is low.

# Design Question

<figure id="fig:placeholder" data-latex-placement="H">
<img src="{{ site.baseurl }}/images/ELEN3802/Lab1Design.png" />
<figcaption>Design Schematic</figcaption>
</figure>

We used a Hex binary counter 74AC161, a NAND gate, and a HFC4511
decoder. The clock impulse is fed into CP PIN2 of 74AC161 from the
debouncer. Each press created a clock impulse. After each 10 counts
cycle, we need to reset the counter or it would continue to count until
16. So we need to reset the counter every decade. In other words,
whenever counter output is 1010 (Q1=1 and Q3=1), NAND gate would produce
low output and feeds it to the active low MR PIN of the counter. The
counter restarts a new cycle. The binary output from the counter then
was fed into the decoder and finally presented counts number on the
LEDs.

Note: We tried to use 2 inverters to build a NAND gate using De Morgan’s
Law. However, we cannot achieve this goal during the lab, so we used
74F00 for our NAND gate directly.

<figure id="fig:placeholder" data-latex-placement="H">
<img src="{{ site.baseurl }}/images/ELEN3802/designPic.JPG" style="width:50.0%" />
<figcaption>Circuit</figcaption>
</figure>


