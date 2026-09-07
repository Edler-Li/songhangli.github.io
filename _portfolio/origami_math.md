---
title: "Rigid-Foldable Thick Origami by Volume Trimming"
excerpt: "Constructing degree-4 rigid-foldable origami vertices from thick materials using axially varying volume trimming, mathematical hinge geometry, laser-cut layouts, and physical prototypes. <br/>"
collection: portfolio
date: 2023-01-01
role: Mathematical Modeling and Fabrication
institution: Franklin & Marshall College · MAT 372 Origami Mathematics
read_time: true
authors:
  - Songhang Li
teaser: /images/projects/origami/bird-foot-prototype.jpg
---

{% if page.authors %}
<div class="page__meta" style="margin: 0 0 1rem 0;">
  <strong>Author:</strong> {{ page.authors | join: ", " }}<br>
  <strong>Advisor:</strong> Professor Thomas C. Hull
</div>
{% endif %}

{% include toc %}

# Project Overview

<!-- Origami often relies on the assumption of using ideal zero-thickness paper or film. This allows for folding various crease patterns like flat-foldable degree 4 vertices. However, there are some challenges when using rigid material to fold, such as metal, wood, and plastic. The panels will collide into each other along the crease line and not fold properly due to the adding thickness. During folding, especially towards smaller dihedral angles, the material on either side of a crease interferes the folding motion and potentially damages the material. This physical restriction means that the simple angle relationships (like Kawasaki's theorem for flat-foldability) cannot be applied directly to the thick folding. The material thickness fundamentally alters the geometry at the hinges. Therefore, techniques such as volume trimming are essential to create the necessary space for panels to fold without collision.


Many thick material folding techniques exist. In this paper, I will focus on volume trimming technique to overcome the challenge of thick origami. Volume trimming, first proposed by Tachi, is a method for constructing hinges by removing material near the fold lines. While simple to fabricate, the original method had limitations, particularly delamination, where stiff layers detach from the folding layer due to external forces. 
To address delamination in the folding, Jason Ku developed \textbf{axially varying volume trimming} to improve the strength of the hinge.

I will demonstrate volume trimming, the improvement by axial variation, and its application to construct degree 4 vertices as shown in the Figure \ref{fig:degree4V} using laser-cut wood and Acrylic.

----  -->

Mathematical origami commonly models paper as a zero-thickness surface. Under that assumption, crease patterns such as flat-foldable degree-4 vertices can move without the panels colliding. Engineering structures made from acrylic, wood, metal, or composite panels behave differently: the physical thickness near a hinge interferes with the folding motion, particularly as the dihedral angle becomes small.  This physical restriction means that the simple angle relationships (like Kawasaki's theorem for flat-foldability) cannot be applied directly to the thick folding.

This project studied **volume trimming**, a method that removes the interfering material near a fold line, and its stronger extension, **axially varying volume trimming**. The method was then applied to three degree-4 vertices. Their cutting layouts were generated computationally and fabricated as rigid-foldable prototypes using laser-cut panels and a flexible folding layer.

![Three degree-4 origami vertices used in the project]({{ site.baseurl }}/images/projects/origami/degree-4-vertices.png)

# Why Thick Origami Is Difficult

For ideal paper, both sides of a crease share the same geometric line. Thick panels occupy volume on either side of the folding layer. As the panels rotate, their inner corners approach one another and eventually collide unless the hinge geometry is modified.

The zero-thickness angle relationships therefore remain useful for describing the crease pattern, but they are not sufficient for specifying a manufacturable thick mechanism. The hinge must provide clearance while preserving the intended axis and avoiding additional unwanted degrees of freedom.

# Existing Thick-Folding Techniques

Several strategies have been developed for adapting origami to thick materials:

| Technique | Folding|
|---|---|
| Hinge shift | Move the hinge axis outside the panel midplane | 
| Volume trimming | Remove material that would collide near the crease |
| Offset panel | Move the rigid panels away from the folding plane | 
| Offset crease | Replace one crease with two separated creases | 
| Rolling contact | Use shaped elements that roll against one another | 
| Strained joint | Form a compliant hinge within a continuous thick sheet | 

![Comparison of hinge shift, volume trimming, offset-panel, and offset-crease methods]({{ site.baseurl }}/images/projects/origami/thick-folding-methods.png)

Volume trimming was selected because it can preserve the intended crease axis and can be fabricated using planar cutting processes.

# Original Volume Trimming

**Volume trimming** enables rigid folding by removing the volumes of material that would otherwise interfere near the hinge line.

![Cross-section of the original volume-trimming method]({{ site.baseurl }}/images/projects/origami/volume-trimming.png)

The original constant trim solves the collision problem, but it creates a structural weakness. When material is removed uniformly along the hinge, the flexible folding layer is no longer fully supported—or **contained**—between rigid panels. Loads applied to the panels can then peel the stiff layer away from the folding layer, producing delamination.

![Delamination caused by an uncontained folding layer]({{ site.baseurl }}/images/projects/origami/delamination.png)

# Axially Varying Volume Trimming

Jason Ku's axially varying method addresses delamination by alternating the retained material along the hinge axis. Instead of removing the same side continuously, the trim switches sides in a piecewise-constant pattern. The resulting interlocking “teeth” keep the flexible layer contained while maintaining clearance for folding.

![One, two, and many axial alternations in the volume-trimming pattern]({{ site.baseurl }}/images/projects/origami/axial-teeth.png)

A single alternation provides limited support. Two or more alternations distribute the retaining geometry along the crease and improve hinge stability.

# Trimming Geometry

## Small fold angles

Let $t$ be the panel thickness, $\gamma$ the target fold angle, and $d$ the required trimming distance from the crease. For $0^\circ < \gamma \leq 90^\circ$, the right-triangle geometry gives

$$
\tan(\gamma)=\frac{t}{d}.
$$

Therefore,

$$
d=\frac{t}{\tan(\gamma)}=t\cot(\gamma).
$$

![Geometry of volume trimming for fold angles up to 90 degrees]({{ site.baseurl }}/images/projects/origami/small-angle-trimming.png)

The result captures an important physical trend: smaller fold angles require more clearance. As $\gamma$ decreases, $\cot(\gamma)$ increases and a larger portion of the panel must be removed.

## Large fold angles

For $90^\circ < \gamma \leq 180^\circ$, trimming only one inner side is no longer sufficient to keep the folding layer contained. Material must be removed from both inner surfaces. The corresponding distances are expressed using the supplementary angle $\pi-\gamma$; one of the horizontal clearance terms is

$$
d=t\cot(\pi-\gamma).
$$

![Required trimming distances for fold angles greater than 90 degrees]({{ site.baseurl }}/images/projects/origami/large-angle-trimming.png)

These relations convert the desired fold angle and material thickness into fabrication dimensions.

# Degree-4 Vertex Designs

A **degree-4 vertex** is a point at which exactly four crease lines meet. Degree-4 vertices are fundamental building blocks in flat-foldable origami, but reproducing them with thick panels requires compatible clearance at all four creases near the central vertex.

Three vertex geometries were selected:

1. Bird-foot vertex: $\alpha=45^\circ$, $\beta=135^\circ$.
2. Four-quarters vertex: $\alpha=90^\circ$, $\beta=90^\circ$.
3. Asymmetric vertex: $\alpha=45^\circ$, $\beta=90^\circ$.

Here, $\alpha$ is the smallest sector angle and $\beta$ is the adjacent sector angle. The cutting patterns were generated with Jason Ku's *Four Crease Hinge Layout* tool. Each design incorporates axial alternation along the creases and additional clearance near the central vertex.

## Bird-foot vertex

<div class="responsive-row">
  <div class="row-media" style="--image-max-width: 440px; --image-flex: 1;">
    <figure>
      <img src="{{ site.baseurl }}/images/projects/origami/bird-foot-layout.png" alt="Axially varying hinge layout for the bird-foot vertex">
      <figcaption>Generated layout for $\alpha=45^\circ$ and $\beta=135^\circ$.</figcaption>
    </figure>
  </div>
  <div class="row-media" style="--image-max-width: 440px; --image-flex: 1;">
    <figure>
      <img src="{{ site.baseurl }}/images/projects/origami/bird-foot-prototype.jpg" alt="Fabricated rigid-foldable bird-foot vertex">
      <figcaption>Fabricated bird-foot vertex in a folded configuration.</figcaption>
    </figure>
  </div>
</div>

## Four-quarters vertex

<div class="responsive-row">
  <div class="row-media" style="--image-max-width: 440px; --image-flex: 1;">
    <figure>
      <img src="{{ site.baseurl }}/images/projects/origami/four-quarters-layout.png" alt="Axially varying hinge layout for the four-quarters vertex">
      <figcaption>Generated layout for $\alpha=90^\circ$ and $\beta=90^\circ$.</figcaption>
    </figure>
  </div>
  <div class="row-media" style="--image-max-width: 440px; --image-flex: 1;">
    <figure>
      <img src="{{ site.baseurl }}/images/projects/origami/four-quarters-prototype.jpg" alt="Fabricated rigid-foldable four-quarters vertex">
      <figcaption>Fabricated four-quarters vertex in a folded configuration.</figcaption>
    </figure>
  </div>
</div>

## 45°-90° vertex

<div class="responsive-row">
  <div class="row-media" style="--image-max-width: 440px; --image-flex: 1;">
    <figure>
      <img src="{{ site.baseurl }}/images/projects/origami/45-90-layout.png" alt="Axially varying hinge layout for the 45-degree 90-degree vertex">
      <figcaption>Generated layout for $\alpha=45^\circ$ and $\beta=90^\circ$.</figcaption>
    </figure>
  </div>
  <div class="row-media" style="--image-max-width: 440px; --image-flex: 1;">
    <figure>
      <img src="{{ site.baseurl }}/images/projects/origami/45-90-prototype.jpg" alt="Fabricated rigid-foldable 45-degree 90-degree vertex">
      <figcaption>Fabricated asymmetric degree-4 vertex.</figcaption>
    </figure>
  </div>
</div>

# Fabrication Workflow

The mathematical hinge layouts were converted into planar patterns suitable for digital fabrication:

1. Choose the degree-4 sector angles and target fold range.
2. Specify the panel thickness and hinge parameters in the layout generator.
3. Export the front and back cutting geometry.
4. Laser cut the rigid panel layers from acrylic or wood.
5. Align the patterned layers around a flexible folding layer.
6. Bond the laminate while preserving the alternating teeth and central clearance.
7. Fold the vertex through its intended range and inspect for collision, peeling, and loss of alignment.

The fabricated examples demonstrated that the alternating material retained along the hinge could support the folding layer while allowing thick panels to rotate around a degree-4 vertex.

# Conclusions

- Panel thickness turns an ideal crease into a three-dimensional collision problem.
- Constant volume trimming provides clearance but may leave the flexible layer uncontained and susceptible to delamination.
- Axially varying teeth retain support on alternating sides of the hinge and improve structural integrity.
- The relation $d=t\cot(\gamma)$ links material thickness and fold angle to the required trim distance for small-angle folds.
- The three fabricated degree-4 vertices validated a workflow from mathematical crease geometry to laser-cut thick-panel mechanisms.

This approach extends origami design beyond paper and toward deployable structures, architectural systems, robotics, and other mechanisms in which rigid panels must compactly fold without collision.

# Acknowledgment

Professor Thomas C. Hull provided guidance throughout this project and the MAT 372 Origami Mathematics course.

# References

1. J. S. Ku, “Folding Thick Materials Using Axially Varying Volume Trimming,” *Proceedings of the ASME 2017 International Design Engineering Technical Conferences and Computers and Information in Engineering Conference*, DETC2017-67577, 2017.
2. I. L. Delimont, S. P. Magleby, and L. L. Howell, “A Family of Dual-Segment Compliant Joints Suitable for Use as Surrogate Folds,” *Journal of Mechanical Design*, vol. 137, no. 9, 2015.
3. R. J. Lang, T. Nelson, S. Magleby, and L. Howell, “Thick Rigidly Foldable Origami Mechanisms Based on Synchronized Offset Rolling Contact Elements,” *Proceedings of IDETC/CIE 2016*, DETC2016-59747, 2016.
4. T. C. Hull, *Origametry: Mathematical Methods in Paper Folding*, Cambridge University Press, 2020.
5. J. S. Ku, “Four Crease Hinge Layout,” web tool, accessed April 23, 2025.
