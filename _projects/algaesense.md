---
title: AlgaeSense
order: 1
summary: An autonomous algae cultivation system that uses a USB microscope and on-device vision to watch the culture and drive pumps, lights and aeration.
hero: /assets/img/projects/algaesense.jpg
hero_alt: The AlgaeSense cube tank on a workbench, filled with green culture, with a 3D-printed lid and silicone tubing.
hero_credit: Photo from the Instructables write-up, published 31 August 2026.
instructable: https://www.instructables.com/AlgaeSense-Grow-Algae-Automatically-As-an-Off-Grid/
hackster: https://www.hackster.io/bhuvanmakes/algaesense-using-ai-to-grow-and-harvest-algae-autonomously-fee1dd
blog: /blog/algaesense/
# TODO: Set `github` to the public repository under https://github.com/bhuvanmakes
# once it is published. Do not link github.com/bhuvanbagwe (those URLs now 404).
# github:
---

AlgaeSense is a cube-shaped photobioreactor that grows [Spirulina](https://www.instructables.com/AlgaeSense-Grow-Algae-Automatically-As-an-Off-Grid/) (*Arthrospira*) and watches the culture itself, not only the water around it.

A 3D-printed peristaltic pump periodically draws a small sample into a viewing chamber. A USB microscope photographs the sample. Software on an [Arduino UNO Q](https://www.hackster.io/bhuvanmakes/algaesense-using-ai-to-grow-and-harvest-algae-autonomously-fee1dd) runs OpenCV on the Linux side of the board, while the microcontroller side runs the pumps, growth LEDs and aeration.

The published prototype demonstrates automated sampling and imaging, OpenCV-based detection, pump and aerator control, LED intensity control, communication between the Linux and microcontroller sides, and automatic logging. It is not a toxin detector: the Hackster write-up is clear that it cannot measure microcystins or dissolved chemical contaminants, and that longer-term control from pH, temperature and similar readings is still planned.

A longer write-up is on the [blog](/blog/algaesense/). The build is documented on Instructables (31 August 2026) and Hackster (19 October 2026).
