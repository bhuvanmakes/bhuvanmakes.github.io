---
title: AlgaeSense
date: 2026-08-31
summary: An autonomous Spirulina photobioreactor that samples its culture, images it through a USB microscope and adjusts its growing environment.
intro: >-
  AlgaeSense is an off-grid photobioreactor concept built around a simple question: can a machine grow and monitor Spirulina with as little daily intervention as possible? This prototype uses an Arduino UNO Q, LED lighting, aeration, a DIY peristaltic pump and a USB microscope to sample and inspect the culture.
lede: A small autonomous photobioreactor that grows and monitors Spirulina.
hero: /assets/img/algaesense/cover.jpg
hero_alt: AlgaeSense photobioreactor prototype.
hero_credit: Cover photograph from the original Instructable, published 31 August 2026.
instructable: https://www.instructables.com/AlgaeSense-Grow-Algae-Automatically-As-an-Off-Grid/
tags:
  - Spirulina
  - Photobioreactor
  - Arduino UNO Q
---
Food independence is one of the harder parts of living off-grid. AlgaeSense explores a compact alternative to conventional crop growing: cultivating Spirulina, a fast-growing photosynthetic cyanobacterium, in a controlled tank.

The goal is an autonomous photobioreactor. LEDs provide light, an aerator mixes the culture and introduces air, and nutrients support growth. The prototype is designed around a 10-litre culture system.

## Hardware

The Instructable lists an Arduino UNO Q, a BO motor used for the peristaltic pump, an aerator motor, four 5 V 1 W COB LEDs and a temperature probe. A pH sensor and TDS sensor are listed as future additions.

I sourced a 50 ml Spirulina mother culture and nutrients from Algreen. The write-up recommends starting with a clean mother culture rather than collecting unknown algae from the wild.

## Building the tank

I designed the enclosure in Fusion 360 and laser-cut the acrylic sheets. The first attempt to join the sheets with silicone adhesive leaked repeatedly, so sealing the tank became an iterative part of the build. The CAD files are included with the original project.

## Sampling the culture

One of the central ideas is a dedicated 3D-printed viewing chamber. Food-safe tubing runs from the tank through a DIY peristaltic pump and into the chamber. An acrylic viewing slit lets the USB microscope observe the sample.

The pump fills the chamber, then stops for five seconds so the sample can settle. The microscope captures multiple frames for analysis before the culture is returned to its normal aeration cycle.

## Microscope and image analysis

I modified the focus of an inexpensive USB electronics microscope by shifting its focus position. This produced images usable for the project's video object-detection model.

The Instructable describes a dataset of around 100 manually labelled images, including Spirulina at different sizes and orientations, as well as possible contaminants. The model is used to detect Spirulina, identify possible contaminants and assess the sample using its appearance and coverage.

## Current operating sequence

The published algorithm:
1. Checks day/night timing and culture age.
2. Runs the LEDs during the configured day period.
3. Keeps aeration running to mix the culture.
4. Samples at fixed intervals using the peristaltic pump.
5. Waits for the microscope sample to settle.
6. Captures several microscope images.
7. Detects Spirulina and possible contaminants.
8. Counts detections and estimates algae area or coverage.
9. Compares results with earlier samples to estimate growth stage.
10. Adjusts lighting, logs results and repeats the cycle.

The Instructable presents this as a working autonomous prototype. It also notes that pH and TDS sensing are future additions. The longer-term aim is to make the reactor more capable of optimising growth with less manual attention.

**Original build:** [AlgaeSense on Instructables](https://www.instructables.com/AlgaeSense-Grow-Algae-Automatically-As-an-Off-Grid/), published 31 August 2026.
