---
title: AlgaeSense
lede: A microscope-driven photobioreactor that watches Spirulina grow, then acts on what it sees.
hero: /assets/img/projects/algaesense.jpg
hero_alt: The AlgaeSense cube tank on a workbench, filled with green culture, with a 3D-printed lid and silicone tubing.
hero_credit: Photo from the Instructables write-up, published 31 August 2026.
instructable: https://www.instructables.com/AlgaeSense-Grow-Algae-Automatically-As-an-Off-Grid/
hackster: https://www.hackster.io/bhuvanmakes/algaesense-using-ai-to-grow-and-harvest-algae-autonomously-fee1dd
# TODO: Set `github` to the public repository under https://github.com/bhuvanmakes
# once it is published. Do not link github.com/bhuvanbagwe (those URLs now 404).
# github:
# No published long YouTube video, Instagram updates, short videos,
# progress tweets or arXiv paper were found for this project as of 24 Nov 2026.
---

AlgaeSense is a machine for growing algae on its own. The Instructables write-up calls it an AI-enabled photobioreactor: a water container with nutrients, light and carbon dioxide, plus something that can make growing decisions as conditions change.

The culture is *Arthrospira*, or Spirulina. The Instructables build is clear that this is not something to scoop from a random pond. Spirulina lives in highly alkaline water, and a wild sample can be contaminated. The write-up treats the reactor as a way to grow a protein-rich food source more carefully, including off-grid.

## Watching the algae, not only the water

Ordinary sensors can report pH, temperature or turbidity. They don't show what is happening to the cells themselves. AlgaeSense periodically pumps a small sample into a viewing chamber and looks at it with a USB microscope.

From those images, the system is described as tracking changes in filament density, morphology and the overall look of the culture, and flagging unusual organisms that may suggest contamination. It can't detect toxins such as microcystins, or heavy metals and dissolved chemical contaminants. The Hackster project page calls this an early warning system, not a chemical assay.

## The cube

The current enclosure is a cube. Electronics sit in a 3D-printed housing above the tank, and the growth lights are built into that housing. I designed the CAD in Fusion 360, then laser-cut acrylic sheets and joined them with silicone adhesive. A 3D-printed peristaltic pump pulls culture through food-safe silicone tubing into the microscope chamber.

The same write-ups say the electronics don't have to live on that particular tank. The probes, aerator and pump lines can be dropped into another container.

Published hardware on the Hackster page includes:

- Arduino UNO Q
- a 3D-printed peristaltic pump driven by a DC motor
- a 12 V aeration motor, also used as an agitator
- four 1 W white growth LEDs
- a USB microscope module
- a USB PD extender hub
- an L298N motor driver

## A split brain

The Arduino UNO Q is used because it has two sides. The microcontroller can run pumps, LEDs, aeration and sensors. The Linux side handles the microscope, OpenCV, logging and higher-level decisions.

The sampling sequence on the Hackster page is:

1. Aeration off
2. Sample pump on
3. Viewing chamber fills
4. Sample settles
5. Microscope captures images
6. Aeration resumes

Aeration is stopped first so bubbles and movement don't spoil the image.

The OpenCV path described there is contrast enhancement, noise reduction, thresholding, morphological filtering, contour detection and measurement. The measurements include algae-covered area, filament count, contour size and approximate morphology changes between samples.

The full monitoring cycle is written as: grow, stop aeration, sample, settle, image, analyse, read sensors, decide, actuate, log, then repeat.

## What the prototype actually shows

The Hackster results list is careful, and it's the one I'm sticking to. The prototype currently demonstrates:

1. Automated culture sampling
2. Controlled microscope imaging
3. OpenCV-based algae detection
4. Pump and aerator control
5. LED intensity control
6. Communication between the Linux and microcontroller sides
7. Automatic logging of measurements

The important part is that these bits run together as one repeatable cycle — not that harvesting or fully automatic yield optimisation is already finished.

The Instructables write-up also has notes on microscope focus, a training set of around 100 images, and a confusion matrix from model training. I'm not repeating accuracy numbers here, because the published extract doesn't give a complete results table.

## What comes next

The next stage described on Hackster is to collect longer-term growth data — pH, temperature, turbidity, light, aeration, an image-derived biomass estimate and growth rate — and use those variables to tune the growing conditions automatically. The larger aim is a compact system that can grow and monitor algae with little day-to-day attention, and that can scale from a desk-sized cube toward larger setups mainly by changing parameters and hardware interfaces.

The build is up as an 11-step Instructable (31 August 2026) and as a Hackster project (19 October 2026). Software for the project has been documented as LGPL-2.1. A public repository under [github.com/bhuvanmakes](https://github.com/bhuvanmakes) is planned and isn't linked here yet.

This is all from those published write-ups. No subscriber counts, contest results or unpublished measurements are included.
