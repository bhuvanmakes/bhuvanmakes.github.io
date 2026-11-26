---
title: Auto-Chef
date: 2025-03-17
summary: A soup-making robot made by repurposing an Ender 3D printer's heated bed, stepper motor, motion system and G-code controls.
intro: >-
  Auto-Chef reuses an old FDM 3D printer as an automatic soup-making robot. Its heated bed warms the cooking vessel, a peristaltic pump dispenses water, the printer's motion system moves a stirrer, and a 3D-printed dispenser handles premixes. The machine is operated through G-code, without adding a separate microcontroller.
lede: What if your old 3D printer could cook soup instead of printing a Benchy?
hero: /assets/img/auto-chef/cover.png
hero_alt: Auto-Chef robot made by repurposing an old 3D printer.
hero_credit: Cover photograph from the original Instructable, published 17 March 2025.
instructable: https://www.instructables.com/Chef-Robot-Made-Using-Old-3d-Printer-Cooking-Soup-/
tags:
  - Robotics
  - 3D printing
  - Automation
---
Auto-Chef started with a simple observation: the hardware needed for a basic automated cooking machine was already sitting in my workshop inside an old 3D printer.

Instead of adding a new controller for every function, I wanted to reuse the printer's existing motion system and G-code workflow.

## Reusing the printer

The Ender 3 provides the main building blocks:

- **Heat source:** the printer's heated bed.
- **Water dispensing:** a peristaltic pump driven using the extruder stepper motor.
- **Stirring:** a stirrer attached to the hot-end carriage, moved by the printer's axes.
- **Ingredient dispensing:** a food-safe 3D-printed attachment controlled by repurposing PWM fan signals.
- **Control:** slicing software and G-code.

The aim was to avoid adding extra microcontrollers, temperature controllers or timers. The cooking sequence is encoded as G-code, much like a print job.

## Food-contact design

I wanted the food made by the machine to be safe to consume, so the design separates the water from the pump's internal mechanism. The peristaltic pump moves liquid through food-safe silicone tubing without the liquid contacting the pump internals.

The spice or premix dispenser is also lined internally with a food-safe plastic sheet, since the dry ingredients remain inside it during operation.

## The dispenser

The dispenser was designed to release two different premixes separately using a single motor. I could not find an off-the-shelf arrangement that fit the requirement, so I designed one around a Tower Pro MG995 servo.

The servo is controlled by repurposing a PWM-controlled fan output on the printer hot end. G-code changes the fan PWM value, which controls the servo position and opens the dispenser. It took more than ten calibration attempts to get reliable control.

## Cleaning and setup

Because the printer is being repurposed for food preparation, it needs a thorough clean before use. I cleaned the idle Ender 3 before installing the cooking attachments.

The original project includes the CAD and assembly details, along with the G-code-based operating approach.

**Original build:** [Auto-Chef on Instructables](https://www.instructables.com/Chef-Robot-Made-Using-Old-3d-Printer-Cooking-Soup-/), published 17 March 2025.
