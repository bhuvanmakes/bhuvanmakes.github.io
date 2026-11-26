---
title: HL-VAWT — Helical Lift-Based Vertical Axis Wind Turbine
date: 2028-01-13
summary: An open-source, mostly 3D-printed helical lift-based vertical-axis wind turbine designed for higher-wind locations and prototyping with accessible parts.
intro: >-
  HL-VAWT explores a helical, lift-based vertical-axis wind turbine using 3D-printed airfoils and readily available hardware. The prototype is intended for higher-wind environments such as highway slipstreams, railway corridors and hilly regions.
lede: A 3D-printable helical turbine concept for harvesting wind in high-wind locations.
hero: /assets/img/hl-vawt/cover.jpg
hero_alt: HL-VAWT helical lift-based vertical axis wind turbine prototype.
hero_credit: Cover photograph from the original Instructable. The PDF lists its publication date as 13 January 2028.
instructable: https://www.instructables.com/An-Open-Source-Hi-VAWT-Helical-Lift-Based-Vertical/
youtube: CX2byGHOR
tags:
  - Wind energy
  - VAWT
  - 3D printing
---
I started this project to explore vertical-axis wind turbines and develop a design suited to a particular use case: harvesting wind from the slipstream around high-speed vehicles on highways and trains along railway tracks.

The design is a helical, lift-based vertical-axis wind turbine. I wanted to make it mostly from 3D-printed parts and easily sourced components so that other makers could reproduce and improve it.

## Airfoil and operating range

Rather than using a conventional drag-based VAWT profile, I selected the DU 06-W-200 airfoil for the turbine blades. The Instructable gives an estimated minimum starting speed of 3.5 m/s and an operating range of 5–7 m/s, making the design more suitable for high-wind locations than low-wind urban conditions.

## Modular blades

The first prototype was designed around common 3D-printer bed sizes. Each blade is split into 150 mm sections; three sections stack to form a blade about 450 mm tall. The complete rotor uses nine printed airfoil sections across three different blade designs.

I designed the parts in Fusion 360 and supplied STL files so the sections can be printed and assembled.

## Generator and rectifier

I salvaged a NEMA 17 stepper motor from an old Ender 3 to use as the generator. The stepper produces AC as it rotates, so the output is passed through full-bridge rectifier circuits made with 1N4001 diodes. The rectified outputs are combined and smoothed with a 1000 µF, 25 V capacitor.

The Instructable describes an expected DC output of around 6–12 V at moderate rotation speeds; this is a design estimate, not a guaranteed output under all wind conditions.

## Assembly and testing

The three turbine stages are attached to their central mounts using printed dowels, joined to the main rings and placed on the central shaft. The blade sections are aligned and fitted together.

For the initial test I used a 240 mm fan at maximum speed and measured the output with a multimeter. The prototype is still being refined. Typical outdoor wind speeds in Mumbai were noted as around 2–3 m/s, below the estimated operating range, so the next test was planned for a higher-wind location.

**Original build:** [HL-VAWT on Instructables](https://www.instructables.com/An-Open-Source-Hi-VAWT-Helical-Lift-Based-Vertical/). The attached PDF lists 13 January 2028 as its publication date.
