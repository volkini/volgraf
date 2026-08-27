---
title: "Organic Mesh to NURBS: Rebuilding a Shape for Injection Moulding"
description: "A polygonal mesh rebuilt as a clean, watertight NURBS solid with draft, parting line and undercuts resolved — the conversion that stands between a concept and a mould."
summary_tr: "Poligon mesh modelin, eğim açısı, ayırma çizgisi ve geri kalma sorunları çözülerek temiz ve su geçirmez NURBS katıya dönüştürülmesi — konsept ile kalıp arasındaki adım."
date: 2025-07-04
image: /assets/images/case-injection-moulded-vase.jpg
category: portfolio
discipline: moulding
tags: [reverse engineering, mesh to NURBS conversion, STEP file for tooling, injection molding design, draft angle analysis, parting line design, surface modeling, DFM]
---

The client had the shape they wanted. What they did not have was a shape a
mould maker could accept.

## The problem

A polygonal mesh and a manufacturing solid are different things:

- **A mesh is faceted.** Scaled up to a moulded part, facet edges become visible
  defects on a glossy surface.
- **Meshes are rarely watertight**, and a mould tool cannot be cut from geometry
  with holes in it.
- **None of the moulding requirements exist in the mesh.** Draft angles, parting
  line, undercuts — the mesh has no opinion about any of them, and all three
  decide whether the part can leave the tool.
- **The shape still has to match.** Rebuilding it is not licence to redesign it;
  the client's form had to survive the process.

## The approach

- **Rebuild rather than convert.** Automatic mesh-to-solid conversion carries the
  faceting through. The surfaces were reconstructed as continuous NURBS matching
  the original form.
- **Parting line chosen before surfacing**, because where the tool splits
  determines which surfaces need draft and in which direction.
- **Draft applied as part of the geometry**, not added afterwards as a fix,
  keeping the visible form consistent as it tapers.
- **Undercuts removed or acknowledged.** Anything that would need a side action
  was resolved in geometry or flagged so the tooling cost was a decision rather
  than a surprise.
- **Delivered watertight**, as a STEP file that opens cleanly in the mould
  maker's CAM.

## The result

A fully editable NURBS model and a high-precision STEP file matching the
original organic shape, developed through two iterations.

## Where this applies

Any product that starts life as a sculpt, a scan or an artist's mesh and has to
end up in a steel tool. This conversion is where most concept models stall.

*I convert scans and meshes into manufacturable NURBS models with tooling
constraints resolved.*
**[Request a quote](/contact/)** or see [all services](/services/).
