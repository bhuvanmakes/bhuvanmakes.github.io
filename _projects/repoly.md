---
title: RePoly
date: 2026-06-08
summary: A mild-steel pulltrusion machine that turns cut PET bottle strips into R-PET filament for 3D printing, using standalone PID and motor controllers.
intro: >-
  RePoly is a team-built machine for converting PET bottle strips into 3D-printing filament. It uses a heated pulltrusion process and deliberately avoids custom firmware: temperature and motor speed are controlled with standalone industrial controllers.
lede: Turning discarded PET bottles into filament for another life in a 3D printer.
hero: /assets/img/repoly/cover.png
hero_alt: RePoly PET bottle-to-filament recycling machine.
hero_credit: Cover photograph from the original Instructable, published 8 June 2026.
instructable: https://www.instructables.com/RePoly-a-Machine-to-Recycle-Polythelene-Plastic-80/
tags:
  - Recycling
  - 3D printing
  - PET
---
RePoly is a machine designed to convert plastic bottles into R-PET filament for 3D printing. The idea is to make recycled plastic useful as a material for new objects, rather than limiting it to a single recycled product.

We wanted a durable machine that could be used in workshops and community settings. That is why the frame is made from mild steel rather than being entirely 3D printed.

## How it works

The machine has a PET-strip input and a filament output. PET bottles are cut into strips of a specific width and fed through a heated section. A motor applies constant tension, pulling the softened strip through the hot end in a process described as pulltrusion.

The filament diameter is influenced by the hot-end temperature and the motor's rotational speed. Both parameters can be adjusted to work towards the desired filament size.

## Controls without custom code

A design goal was to make the machine reproducible without requiring electronics or programming experience. RePoly uses standalone PID temperature control and a PWM motor-speed controller rather than a custom microcontroller program.

The Instructable lists a 12 V, 20 A (240 W) power supply, REC-100 digital PID controller, Fotek solid-state relay, 12 V 12 RPM Johnson geared motor, 12 V single-motor speed controller, a salvaged 3D-printer heater element and a K-type thermocouple.

## Design and fabrication

We explored four design variants before selecting one for CAD. The machine was designed in Fusion 360, with dummy models of the components placed to check their fit and the pulltrusion path. The project files are provided with the Instructable and its linked repository.

## The team

RePoly was built through the combined efforts of Ayaan Sayyed, Jash Jain, Kathan Shah and Shoaib Attar. Swayam sponsored the fabrication.

The original Instructable describes the project as open source and invites others to contribute improvements and feedback.

**Original build:** [RePoly on Instructables](https://www.instructables.com/RePoly-a-Machine-to-Recycle-Polythelene-Plastic-80/), published 8 June 2026.
