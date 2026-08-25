---
title: "Eight-Section Expanding Pizza Divider, 13 in Closed"
description: "An expanding pulley mechanism rebuilt from six sections to eight — a 3D-printable divider that opens evenly from a 13-inch closed diameter."
summary_tr: "Altı dilimden sekiz dilime çıkarılan genişleyen kasnak mekanizması: 13 inç kapalı çaptan eşit açılan, 3B baskıya uygun pizza bölücü."
date: 2024-10-23
image: /assets/images/case-pizza-divider.jpg
category: portfolio
tags: [mechanism design, expanding pulley mechanism, 3D printable design, kitchen product design, kinematic design, parametric CAD, consumer product, STL deliverable]
---

The client had found expanding-pulley designs online, built a rough prototype,
and hit the limit: every available design has six sections. They needed eight,
to divide a pizza evenly.

## The problem

Going from six to eight sections is not a matter of adding two more:

- **The whole mechanism is angular.** Six sections means 60° per segment; eight
  means 45°. Every link length, slot angle and pivot position changes.
- **Expansion must stay even.** If the segments do not move together, the slices
  come out unequal — which is the one thing the product exists to prevent.
- **A 13-inch closed diameter** was fixed, so the mechanism had to fold into a
  defined envelope rather than sizing itself.
- **It had to be 3D printable**, which limits how thin the links can be and how
  the pivots can be made.

## The approach

- **Rebuilt parametrically from the segment count**, so the geometry is driven by
  the number of sections rather than adapted from a six-section layout — the
  reason existing designs could not simply be modified.
- **Synchronised expansion through the link geometry**, keeping the segments
  positively coupled so they open together instead of relying on friction.
- **Sections sized for FDM printing**, with pivot features that survive layer
  adhesion and clearances that work at printed tolerance rather than machined
  tolerance.
- **Closed diameter as the driving dimension**, with the open state falling out
  of the mechanism rather than being set independently.

## The result

A working eight-section expanding divider, delivered as printable files
converted to STL at the client's request.

## Where this applies

Iris, expanding and synchronised-segment mechanisms: dividers, apertures,
adjustable frames. Segment count is the parameter everything else derives
from — which is why these designs cannot be edited, only rebuilt.

*I design parametric mechanisms that can be rebuilt at any segment count.*
**[Request a quote](/contact/)** or see [all services](/services/).
