---
title: AlgaeSense
order: 1
summary: A cube that grows Spirulina and watches the culture with a USB microscope, then runs the pumps, lights and aeration from what it sees.
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

AlgaeSense is a cube-shaped photobioreactor that grows [Spirulina](https://www.instructables.com/AlgaeSense-Grow-Algae-Automatically-As-an-Off-Grid/) (*Arthrospira*). It looks at the culture itself, not only the water around it.

A 3D-printed peristaltic pump periodically draws a small sample into a viewing chamber. A USB microscope takes a picture. Software on an [Arduino UNO Q](https://www.hackster.io/bhuvanmakes/algaesense-using-ai-to-grow-and-harvest-algae-autonomously-fee1dd) runs OpenCV on the Linux side of the board, and the microcontroller side runs the pumps, growth LEDs and aeration.

The published prototype can do automated sampling and imaging, OpenCV-based detection, pump and aerator control, LED intensity control, talk between the Linux and microcontroller sides, and automatic logging. It is not a toxin detector. The Hackster write-up is clear that it cannot measure microcystins or dissolved chemical contaminants, and that longer-term control from pH, temperature and similar readings is still planned.

There's a longer write-up on the [blog](/blog/algaesense/). The build notes are on Instructables (31 August 2026) and Hackster (19 October 2026).
