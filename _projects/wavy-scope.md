---
title: Wavy-Scope
date: 2025-10-13
summary: A portable radio-signal finder using a Ku-band LNB and satellite signal-strength meter to explore radio astronomy.
intro: >-
  Wavy-Scope repurposes a satellite dish LNB and an analogue satellite finder into a portable radio astronomy instrument. It is designed to make detecting signals from the Sun, the Moon and artificial satellites accessible and hands-on.
lede: A handheld, retro sci-fi radio-signal finder for curious sky-watchers.
hero: /assets/img/wavy-scope/cover.png
hero_alt: Wavy-Scope handheld radio-signal detector.
hero_credit: Cover photograph from the original Instructable, published 13 October 2025.
instructable: https://www.instructables.com/Wavy-Scope-Handheld-Signal-Finder-to-Detect-the-Su/
tags:
  - Radio astronomy
  - RF
  - 3D printing
---
I wanted to make radio astronomy feel more approachable: a portable instrument that children, students and curious makers could take outside and experiment with.

Wavy-Scope is built around an off-the-shelf Ku-band satellite LNB and a satellite signal-strength meter. The LNB receives microwave signals in the Ku band, amplifies and down-converts them. Instead of using an SDR and software, this build repurposes the analogue meter and buzzer from a satellite finder.

## Parts

- Single-channel Ku-band LNB
- SOLID dB meter or satellite signal-strength finder
- 1 metre RG6 coaxial cable
- Four RG6 male connector adapters
- Four 18650 Li-ion cells
- Two dual-cell 18650 holders
- 18650 Li-ion charger
- 3D-printed enclosure parts
- Optional microcontroller for reading and logging signal values

## Making it portable

A typical LNB and satellite meter are powered by a set-top box. To make Wavy-Scope handheld, I used four 18650 cells in series, giving a nominal pack voltage of about 14.8 V. The Instructable notes that the LNB and finder accept a supply in the 12–18 V range.

## Enclosure

I designed the enclosure in Fusion 360, with a retro science-fiction look. The coaxial cables remain visible and follow their natural curves rather than being forced into tight coils. The V1 files include the battery covers and holder, dB-meter holder and plate, and LNB spacers.

The parts were FDM printed in PLA on a Bambu Lab A1. A Bambu Studio 3MF profile is also included.

## What it detected

I tested Wavy-Scope against several sources:

- **The Sun:** the signal response was clear in the test.
- **The Moon:** I observed a detection spike around the Moon's alt-azimuth coordinates, including during a bright morning.
- **Artificial satellites:** the analogue meter could be adjusted to reveal faint changes while scanning the sky, although the results were weaker and less clear than the Sun and Moon tests.

The device also responds to other high-frequency emitting electronics, such as computers and microwave ovens.

## Next iteration

I was working on reading the satellite finder's meter output with a microcontroller. That would make it possible to log signal strength over time and produce more detailed plots for amateur radio astronomy experiments.

**Original build:** [Wavy-Scope on Instructables](https://www.instructables.com/Wavy-Scope-Handheld-Signal-Finder-to-Detect-the-Su/), published 13 October 2025.
