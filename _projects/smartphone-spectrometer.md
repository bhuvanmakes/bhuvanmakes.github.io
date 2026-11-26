---
title: A Smartphone-Attached Spectrometer
date: 2024-07-29
summary: A compact 3D-printed diffraction-grating attachment that turns a smartphone camera into a simple tool for observing light spectra.
intro: >-
  I designed a small spectrometer that clips onto a smartphone and aligns a diffraction grating with its camera. After multiple design iterations and printed prototypes, the final enclosure holds the grating in a dedicated slot without adhesive.
lede: A clip-on spectrometer for exploring the colours hidden inside light.
hero: /assets/img/smartphone-spectrometer/cover.jpg
hero_alt: The smartphone-attached spectrometer prototype.
hero_credit: Cover photograph from the original Instructable, published 29 July 2024.
instructable: https://www.instructables.com/A-Smartphone-Attached-Spectrometer-Education-With-/
tags:
  - Spectroscopy
  - Optics
  - 3D printing
---
A spectrum is more than a band of colours. It can reveal information about the light source that produced it. I wanted to make spectroscopy easier to explore with a device many people already own: a smartphone.

The result is a small 3D-printed module that clips over a smartphone camera and holds a diffraction grating in front of the lens.

## The idea

A diffraction grating separates incoming light into its component colours. The smartphone camera records the resulting spectrum, which can then be inspected using an application.

The goal was a compact enclosure that could attach to different smartphones while keeping the grating aligned with the camera.

## Materials

- Diffraction grating element, or diffraction glasses used for laser shows
- Different light sources for observation
- Lasers of different wavelengths for experiments and calibration
- 3D printer, or access to laser cutting for an alternative enclosure

## Design and prototyping

I designed the enclosure in Fusion 360. The main challenge was the clip geometry: it had to fit different phones while positioning the grating correctly over the camera.

I went through more than six design iterations and printed around eight to ten prototypes. These iterations helped refine the overall size, clip and optical alignment.

The final design is split into three parts: `Base_body`, `Cover_body` and `Text`. The original project supplies the `Base_body.stl` and `Cover_body.stl` files.

## Installing the grating

Some early prototypes used adhesive, which could damage the diffraction grating. I changed the design to use a dedicated slit so the grating slides into place without adhesive.

## Recording spectra

Attach the module to the smartphone and align it with the primary or macro camera. I used a smartphone stand to keep the phone steady while recording.

The original build uses the SpectraUPB application on Android or iOS to process captured images into spectra. I started with a standard LED bulb, then experimented with a green laser and other light sources.

At the time of publishing, I was also working on an alternative application based on OpenCV for direct spectrum observation on smartphones. That software was still a work in progress.

**Original build:** [A Smartphone Attached Spectrometer! Education With Colors of the Rainbow](https://www.instructables.com/A-Smartphone-Attached-Spectrometer-Education-With-/), published 29 July 2024.
