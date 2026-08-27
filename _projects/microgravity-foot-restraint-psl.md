---
title: "Passive Stability Lock: A Flush Foot Anchor for Microgravity"
description: "A hands-free boot anchor in a Ø101.6 × 38.1 mm cassette — shielded neodymium array armed by a helix cam, dual-lug turntable, damped release. No power, no stray field."
summary_tr: "Ø101,6 × 38,1 mm kaset içine sığan, elle kullanım gerektirmeyen bot sabitleme sistemi: helis kamla devreye giren perdelenmiş neodyum dizisi, çift lokmalı döner tabla ve damperli serbest bırakma. Enerji gerektirmez, kaçak manyetik alan yaratmaz."
date: 2025-11-05
category: portfolio
discipline: machine
tags: [mechanism design, aerospace hardware design, magnetic latch design, cam mechanism, kinematic design, microgravity equipment, LRU modular design, SolidWorks assembly]
---

The most demanding mechanism in this archive: a floor-mounted anchor that
captures a boot in microgravity, lets the wearer pivot freely, and releases
only on a deliberate sequence — with no electronics and no power anywhere in
it.

## The problem

Every requirement contradicts the next:

- **Capture must be hands-free.** Stepping on the disc should secure the foot,
  with no separate latching action.
- **The magnets must be invisible when idle.** A permanent magnet array sitting
  in a station floor would interfere with nearby equipment — so the field cannot
  simply be present all the time.
- **Rotation must feel free**, or the wearer fights the device every time they
  turn.
- **Release must be impossible by accident**, which normally means friction — and
  friction is exactly what makes rotation unpleasant.
- **Everything inside a Ø101.6 × 38.1 mm envelope** (4.0 × 1.50 in), built as a
  modular line-replaceable cassette so a failed unit can be swapped rather than
  serviced in place.

## The approach

The design gives each contradictory duty to a different physical element:

- **A flux shunt for the idle state.** A thickened steel shunt shields the
  neodymium array when the device is not in use, so no stray field exists to
  disturb equipment nearby.
- **A helix cam as the arming mechanism.** Stepping down depresses the floating
  bezel ring by 6.0 mm; that vertical travel drives a helix cam which rotates the
  shunt 25°, exposing the magnet array. Arming is a consequence of standing on
  it — there is no separate control.
- **Alternating pole array (N-S-N)** to produce a tight, short flux loop that
  grips the two boot lugs, spaced 60 mm along the foot, without projecting field
  upward.
- **A urethane O-ring damper** at touchdown, so capture is muted and
  vibration-free rather than a metallic snap.
- **Dual-lug turntable architecture** carrying the rotation, so the wearer turns
  on a bearing surface instead of against the magnets.
- **Damped release at end of travel.** Free rotation continues until a limiter
  engages; only then does further force drive a dashpot, whose slow final motion
  runs a wheel up a ramp and lifts the plate clear of the magnets.

Because the damper engages only after the limiter, the pivot stays effortless
in normal use and deliberate exactly where accidental release would be
dangerous.

## The result

A complete kinematic design and CAD assembly of 49 parts, with a written
technical definition covering the mechanism, magnetic architecture and the
modular cassette configuration.

It was also the project where the honest answer mattered most. As the concept
grew, the recommendation was to simplify the release sequence rather than keep
stacking stages onto a mechanism already at its complexity limit — advice worth
more to the client than another iteration would have been.

## Where this applies

Restraints, latches and safety interlocks that must be effortless in normal use
and deliberate to release — and any design where a magnetic field has to exist
on demand and not otherwise. The engineering is deciding which physical effect
owns which requirement.

*I design mechanisms from first principles: kinematics, magnetics, force paths
and the CAD to build them.*
**[Request a quote](/contact/)** or see [all services](/services/).
