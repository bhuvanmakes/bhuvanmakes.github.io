---
title: Morse Monkey
lede: A USB toy that teaches Morse code with lights, a buzzer and one button — and deliberately no screen.
hero: /assets/img/projects/morse-monkey.jpg
hero_alt: Cover image from the Morse Monkey Instructables write-up, showing a brown, monkey-faced trainer enclosure.
hero_credit: Cover image from the Instructables write-up, published 26 October 2026.
instructable: https://www.instructables.com/MorseMonkey-Why-Dont-You-Know-Morse-Code-a-Toy-Mon/
# TODO: Set `github` to the public repository under https://github.com/bhuvanmakes
# once it is published. Do not link github.com/bhuvanbagwe (those URLs now 404).
# github:
# Draft only. Publish once the write-up is finished and any kit links are verified.
---

This is a draft. It is not on the public blog until it is moved into `_posts`.

Morse Monkey is a USB-pluggable Morse-code trainer. The Instructables write-up, published on 26 October 2026, explains the form: it is meant to look like a toy monkey, not a piece of bench equipment, so using it feels like play rather than practice.

The board is an ESP32-C3 SuperMini. The published parts list is small:

- Trainer LED, which flashes the target Morse pattern
- User LED, which shows your button input
- A passive buzzer for symbol tones and feedback
- The BOOT button as the key

The write-up includes a connection diagram and says a PCB was designed in an online EDA tool. It also warns that GPIO 9 is a boot-strapping pin on the ESP32-C3, so the BOOT button should not be held while the board is powering on or resetting.

Firmware is an Arduino sketch. You open it in Arduino IDE, select a suitable ESP32-C3 board, and upload it.

There is no display. That is intentional. A screen that showed the matching letter would make it too easy to learn Morse visually. A printed cheatsheet is provided instead.

A longer public repository, 3D files and a licence statement are planned under github.com/bhuvanmakes and are not linked from this draft. No YouTube video, tweets, Instagram updates, short videos or arXiv paper were found for this project as of 24 November 2026.

Sources for this draft: the Instructables write-up and the short project description used on this site.
