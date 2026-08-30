---
title: "SAE Aero Design Competition Preparation"
excerpt: "A power and lift efficient, short-take-off-length 3.8 meters fixed wing plane for water delivery  <br/>"
collection: portfolio
date: 2024-05-01
role: Team Lead, Wing Design, and Fabrication
institution: Franklin & Marshall College · Department of Physics and Astronomy
read_time: true
authors:
  - Songhang Li
  - Yucheng Nie
  - Ryan Zhang
teaser: /images/projects/sae-aero-design/aircraft-final.jpg
---

{% if page.authors %}
<div class="page__meta" style="margin: 0 0 1rem 0;">
  <strong>Authors:</strong> {{ page.authors | join: ", " }}<br>
  <!-- <strong>Advisor:</strong> Professor Ken Krebs -->
</div>
{% endif %}
{% include toc %}


# Project Overview

- Designed a power and lift efficient, short-take-off-length 3.8 meters fixed wing plane for water delivery.
- Calculated the lift of the wing based on the structure of air foil in order to improve the load capacity.
- Fabricated the wings utilizing balsa wood and carbon fiber, employing laser cutter and heat-shrink
covering film application techniques.

# Design Requirements

The aircraft design focused on five primary requirements:

1. Carry a 2 kg payload safely.
2. Generate sufficient lift at low airspeed for short-field takeoff.
3. Minimize structural and empty weight.
4. Maintain stable and controllable flight in roll, pitch, and yaw.
5. Integrate the airframe, propulsion system, electronics, and control surfaces into a testable platform.

The team followed an iterative design-build-test-improve workflow. Analytical estimates and simulation informed the initial geometry; construction and control-integration experience then exposed practical issues that guided the next design revision.

<div style="text-align: center;" markdown="1">
![Iterative engineering design process used for the aircraft]({{ site.baseurl }}/images/projects/sae-aero-design/design-process.png){: width="300px" }
</div>


# Aerodynamic Design

## Lift and drag

The wing had to produce enough lift to support the aircraft and payload at a practical takeoff speed. The first-order design relationship was

$$
L=\frac{1}{2}\rho V^2 S C_L,
$$

where $\rho$ is air density, $V$ is airspeed, $S$ is wing area, and $C_L$ is the lift coefficient. Wing geometry and angle of attack were selected to increase useful lift while limiting profile and lift-induced drag.

<div class="responsive-row">
  <div class="row-media" style="--image-max-width: 520px; --image-flex: 1;">
    <figure>
      <img src="{{ site.baseurl }}/images/projects/sae-aero-design/xflr5-lift.png" alt="XFLR5 lift distribution over the aircraft wing and tail">
      <figcaption>Calculated lift distribution over the wing and tail.</figcaption>
    </figure>
  </div>
  <div class="row-media" style="--image-max-width: 520px; --image-flex: 1;">
    <figure>
      <img src="{{ site.baseurl }}/images/projects/sae-aero-design/xflr5-drag.png" alt="XFLR5 aerodynamic drag visualization">
      <figcaption>Aerodynamic loading and lift-induced drag analysis.</figcaption>
    </figure>
  </div>
</div>

One XFLR5 configuration used during design exploration had the following modeled parameters:

| Parameter | Modeled value |
|---|---:|
| Wing span | 230 cm |
| Root chord | 38 cm |
| Mean aerodynamic chord | 30.3 cm |
| Wing area | 6,785 cm² |
| Aspect ratio | 7.8 |
| Tip twist | -6° |
| Modeled aircraft mass | 5.0 kg |
| Analysis speed | 12 m/s |
| Angle of attack | 5° |
| Lift coefficient, $C_L$ | 0.625 |
| Drag coefficient, $C_D$ | 0.030 |
| Lift-to-drag ratio | 20.5 |
| Static margin | 15% |

These values describe an analyzed configuration rather than every revision of the physical aircraft.

## Stability analysis

XFLR5 was also used to evaluate aircraft stability. The workflow began by defining the geometry, mass distribution, and moments of inertia. Aerodynamic polars were then calculated and post-processed through eigenmode, root-locus, and time-response analysis.

<div style="text-align: center;" markdown="1">
![XFLR5 aircraft stability-analysis workflow]({{ site.baseurl }}/images/projects/sae-aero-design/stability-workflow.png){: width="600px" }
</div>

This process connected geometry choices—such as wing placement, sweep, twist, and tail configuration—to longitudinal and lateral-directional stability before committing to fabrication.

# Wing Construction

The wing structure combined low-mass materials with localized reinforcement. Balsa wood provided the ribs and supporting geometry, while carbon-fiber members carried higher bending loads. Laser-cut components improved dimensional repeatability, and heat-shrink covering film formed the aerodynamic surface.
<div style="text-align: center;" markdown="1">
![Foam-wing structural concept]({{ site.baseurl }}/images/projects/sae-aero-design/foam-wing-structure.png){: width="500px" }
</div>


# CAD and Mechanical Design

Custom mechanical components were modeled for fabrication and integration with the airframe. These included landing-gear connectors, empennage connectors, a front faceplate, and other interfaces that converted the aerodynamic layout into an assembly that could be manufactured and repaired.

<div style="text-align: center;" markdown="1">
![CAD models of custom aircraft components]({{ site.baseurl }}/images/projects/sae-aero-design/cad-components.png){: width="500px" }
</div>

Additive manufacturing was useful for geometrically complex or low-volume parts, while balsa, foam, carbon fiber, and sheet materials were retained where they provided better stiffness-to-weight performance.

# Propulsion and Electronics

The electrical architecture integrated the flight battery, radio receiver, electronic speed controller, propulsion motor, nose-wheel steering, and aerodynamic control servos. Separating the propulsion power path from the control-signal routing made the system easier to assemble and troubleshoot.

<div style="text-align: center;" markdown="1">
![Propulsion, receiver, and servo wiring architecture]({{ site.baseurl }}/images/projects/sae-aero-design/electronics-wiring.jpg){: width="500px" }
</div>

The receiver commanded independent actuators for the ailerons, flaps, elevator, rudder system, and steerable nose wheel. The electronic speed controller regulated motor power in response to the throttle command while also interfacing with the onboard power system.

# Flight Controls

The control-surface layout provided the three fundamental aircraft rotations:

- **Roll:** differential aileron motion changes lift between the left and right wings.
- **Pitch:** elevator deflection changes the tail force and rotates the aircraft nose up or down.
- **Yaw:** rudder deflection produces lateral tail force and turns the aircraft about its vertical axis.

<div style="text-align: center;" markdown="1">
![Aircraft control surfaces and actuator locations]({{ site.baseurl }}/images/projects/sae-aero-design/control-surfaces.jpg){: width="500px" }
</div>

<div style="text-align: center;" markdown="1">
![Relationship between the roll, yaw, and pitch control axes]({{ site.baseurl }}/images/projects/sae-aero-design/roll-yaw-pitch.jpg){: width="500px" }
</div>

The initial airframe relied on coordinated aileron and elevator inputs without a fully implemented rudder. Although this arrangement provided basic control, it limited direct yaw authority and made coordinated turns more difficult.

# Improvements and Future Development


## Increase passive lateral stability

A tilted or dihedral wing configuration was also considered. Raising the wing tips relative to the center section creates a restoring rolling moment during sideslip, improving passive lateral stability and reducing pilot workload.

<div style="text-align: center;" markdown="1">
![Tilted-wing prototype for increased passive stability]({{ site.baseurl }}/images/projects/sae-aero-design/dihedral-wing.jpg){: width="500px" }
</div>

## Continue iterative testing

Future work would combine ground testing, taxi testing, structural load checks, and controlled flight trials. Results from each stage could be used to update the mass model, center-of-gravity location, control throws, propulsion sizing, and XFLR5 analysis.


## Using Wing Helper

[Wing Helper](https://www.winghelper.com/default_j5/) is a 3D CAD program for design of RC plane models.

<img src="{{ site.baseurl }}/images/SAEWing2.jpeg" alt="Description" style="width: 50%; display: block; margin: 0 auto;">

<img src="{{ site.baseurl }}/images/SAEWing.jpeg" alt="Description" style="width: 90%; display: block; margin: 0 auto;">



# Laser Cutter

<div style="display: flex; flex-wrap: wrap; gap: 20px; justify-content: center;" markdown="1">
![Laser Cutter View 1]({{ site.baseurl }}/images/SAEphoto1.JPG){: style="width: 48%; min-width: 300px; height: auto;"}
![Laser Cutter View 2]({{ site.baseurl }}/images/SAEphoto2.JPG){: style="width: 48%; min-width: 300px; height: auto;"}
![Laser Cutter View 3]({{ site.baseurl }}/images/SAEphoto3.jpeg){: style="width: 48%; min-width: 300px; height: auto;"}
![Laser Cutter View 4]({{ site.baseurl }}/images/SAEphoto4.jpeg){: style="width: 48%; min-width: 300px; height: auto;"}
</div>

<!-- ## Using Wing Helper

<div style="display: flex; flex-wrap: wrap; gap: 20px; justify-content: center;" markdown="1">
![Wing Helper View 1]({{ site.baseurl }}/images/SAEWing.jpeg){: style="width: 48%; min-width: 300px; height: auto;"}
![Wing Helper View 2]({{ site.baseurl }}/images/SAEWing2.jpeg){: style="width: 48%; min-width: 300px; height: auto;"}
</div> -->





## Parameter

Laser-cutting trials established practical fabrication settings for several stock thicknesses:

| Material thickness | Glowforge setting |
|---|---|
| 1/4 in (6.25 mm) | Speed 610, full power, 3 passes |
| 1/16 in | Speed 650, full power, 1 pass |
| 1/8 in | Speed 650, full power, 2 passes |
| Scoring | Speed 700, power 20, 1 pass |

The settings served as starting points for the material batches used during construction; test cuts were still required before processing final parts.

# Project Outcome

The project established an aircraft-development workflow spanning aerodynamic modeling, stability analysis, composite and wood construction, CAD, additive manufacturing, propulsion integration, and control-system design.

Poster presented at the Spring 2024 Student Research Fair, Franklin and Marshall College, PA. <br/>

<img src="{{ site.baseurl }}/images/SAEAeroPoster.png" alt="Description" style="width: 80%; display: block; margin: 0 auto;">

