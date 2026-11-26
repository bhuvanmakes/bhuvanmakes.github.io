---
title: A Smartphone-Attached Spectrometer
date: 2024-07-29
summary: A compact, 3D-printed spectrometer that clips onto a smartphone and uses a diffraction grating to capture the spectra of different light sources.
intro: >-
  I designed a small spectrometer that attaches to a smartphone, making it easier to explore light and colour using a camera most people already have. After more than six design iterations and around eight to ten prototypes, the final clip-on enclosure holds a diffraction grating in a dedicated slot, without adhesive.
lede: A small clip-on spectrometer for exploring the colours hidden inside light.
hero: /assets/img/smartphone-spectrometer/cover.jpg
hero_alt: The 3D-printed Small Spectro module clipped over a smartphone camera.
hero_credit: Cover image from the Instructables project, published 29 July 2024.
instructable: https://www.instructables.com/A-Smartphone-Attached-Spectrometer-Education-With-/
tags:
  - Spectroscopy
  - 3D printing
  - Optics
---

The spectrum of colours is more than something beautiful to look at. It is also a tool used in spectroscopy. I wanted to make that idea easier to explore with a device people already carry: a smartphone.

The result is a small, 3D-printed spectrometer module designed to clip onto almost any smartphone and align a diffraction grating with its camera.

## The idea

A diffraction grating separates incoming light into its component colours. By placing the grating in front of a smartphone camera, the phone can capture the resulting spectrum for observation and analysis.

The goal was to keep the module compact, easy to make and broadly compatible with smartphones.

## Supplies

- A diffraction grating element, or diffraction glasses used for laser shows
- Different light sources for observation
- Lasers of different wavelengths for calibration and comparison
- A 3D printer for the enclosure, or laser cutting as an alternative

## Step 1: Design process

I designed the enclosure in Fusion 360. The main challenge was making it clip onto different smartphones while keeping the grating aligned with the camera.

I went through multiple design iterations, trying to centre the spectra in the camera view, reduce the overall size and make the module easier to use. I also tried to keep the model files small without affecting the printed output.

## Step 2: Prototyping

I made more than six or seven design iterations and printed around eight to ten prototypes before reaching the final design. The iterations helped refine the clip geometry, the position of the grating and the alignment with the smartphone camera.

## Step 3: 3D printing

The final design is split into three parts:

- `Base_body`
- `Cover_body`
- `Text`

The original project provides the `Base_body.stl` and `Cover_body.stl` files for printing.

## Step 4: Insert the diffraction grating

Some earlier prototypes had a problem: adhesive used during assembly could damage the diffraction grating.

For the final version, I made assembly adhesive-free. The enclosure has a dedicated slit where the diffraction grating can be inserted. This keeps the grating in its intended position and avoids applying adhesive to it.

## Step 5: Start recording

Attach the Small Spectro module to the smartphone and align it with the primary or macro camera. I used a smartphone stand to keep the phone steady while recording.

The original build uses the SpectraUPB Android/iOS application to process the captured images into spectra. I started with a standard LED bulb, then tried a green laser and other light sources.

## Step 6: Outputs and work in progress

The project produced spectra from different light sources. At the time of publishing, I was also working on an alternative application based on OpenCV for direct spectrum observation using smartphones. That software was still in progress.

The hardware is a starting point for making spectroscopy more approachable: a small optical attachment, a smartphone camera and an application for examining the captured spectrum.

---

**Original Instructable:** [A Smartphone Attached Spectrometer! Education With Colors of the Rainbow](https://www.instructables.com/A-Smartphone-Attached-Spectrometer-Education-With-/)

*Originally published on Instructables on 29 July 2024.*
