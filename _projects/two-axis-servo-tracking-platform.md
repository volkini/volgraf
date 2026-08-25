---
title: "Two-Axis Servo Tracking Platform with Geared Drive and Pneumatics"
description: "A high-speed pan-and-tilt platform built on an aluminium extrusion frame — gear reduction, catalogue servos and SKF bearings selected so the client could source every part."
summary_tr: "Alüminyum profil şasi üzerine kurulu iki eksenli hızlı takip platformu: dişli redüksiyon, katalog servolar ve SKF rulmanlarla her parçası piyasadan temin edilebilir şekilde tasarlandı."
date: 2025-09-12
image: /assets/images/case-servo-tracking-rig.jpg
category: portfolio
tags: [motion control hardware, servo drive design, gear train design, aluminium extrusion frame, pneumatic actuator integration, mechatronics design, machine design, SolidWorks assembly]
---

A two-axis motion platform: one horizontal axis, two synchronised servos on the
vertical axis, geared reduction, pneumatic actuators, and a frame built from
aluminium extrusion.

## The problem

The client had studied the motion they wanted and specified the drive
electronics themselves — roughly 1200 W on the horizontal axis and two 400 W
servos on the vertical, synchronised over EtherCAT for high-resolution,
responsive motion. What they needed was the mechanical half:

- **Torque and inertia have to match the chosen servos**, or the drives are
  either overloaded or wasted.
- **Two servos on one axis must not fight each other**, which puts the burden on
  the mechanical stiffness of the vertical assembly.
- **Fast direction changes punish backlash.** A gear train that is fine for
  steady motion becomes the limiting factor when the platform reverses quickly.
- **Everything had to be sourceable.** This was a first prototype iteration
  built by the client, not by a machine shop with a standard parts crib.

## The approach

- **Standard-frame servo bodies** chosen so the mechanical design does not depend
  on one supplier's motor — the client can buy to a frame size rather than a part
  number.
- **Catalogue SKF bearings, named in the file structure.** Bearing models are
  carried in the CAD part names so nothing has to be reverse-identified at
  assembly time.
- **Gear ratios matched to the reference motion**, with the drive train sized to
  the torque the selected servos can deliver.
- **Selective lightening.** Pockets were machined into the upper gears to reduce
  inertia where it matters, while the bottom gear was deliberately left solid —
  there, the extra mass helps.
- **Pneumatic actuation, correctly identified.** The actuators are pneumatic, not
  hydraulic, with a third small cylinder added for an auxiliary function.
- **Scope limits stated up front.** Certain regulated components were excluded
  from the CAD as a matter of policy; the client was told this before work
  started rather than discovering it at delivery.

## The result

A complete mechanical design across five iterations — frame, geared drive,
bearing selection, servo mounting and pneumatic integration — with 3D files and
2D drawings delivered as a buildable package.

## Where this applies

Motion platforms, pan-tilt rigs, geared servo axes and any machine where an
electrical specification exists and the mechanics have to meet it. Matching
inertia, backlash and stiffness to the chosen drive is the whole job.

*I design servo-driven mechanisms and machine frames around the drives you have
already chosen.*
**[Request a quote](/contact/)** or see [all services](/services/).
