---
title: Morse Monkey
date: 2026-10-26
summary: A toy-like, open-source Morse code trainer with two LEDs, a buzzer and a physical key built around an ESP32-C3 SuperMini.
intro: >-
  Morse Monkey is a small physical Morse code trainer designed to make learning feel more like playing with a toy than using a study app. It uses two LEDs, a passive buzzer and the ESP32-C3 SuperMini's BOOT button as the Morse key.
lede: A little monkey that teaches dots, dashes and the rhythm of Morse code.
hero: /assets/img/morse-monkey/cover.jpg
hero_alt: Morse Monkey trainer enclosure.
hero_credit: Cover photograph from the original Instructable, published 26 October 2026.
instructable: https://www.instructables.com/MorseMonkey-Why-Dont-You-Know-Morse-Code-a-Toy-Mon/
tags:
  - ESP32-C3
  - Electronics
  - Learning
---
Morse code is easy to recognise in the form of SOS, but learning to send it is another matter. Phone apps often use a virtual button on a screen. I wanted a simple, inexpensive physical device that makes learning tactile and audible.

Morse Monkey is designed to look like a toy rather than a tool. The idea is to make practice approachable: play with the little monkey, and learn Morse along the way.

## What it does

Two red LEDs act as the trainer and user indicators. The trainer LED flashes the target Morse pattern; the user LED shows your button input. A passive buzzer plays the tones for Morse symbols and gives feedback when an answer is incorrect.

A short press represents a dot and a longer press represents a dash. When you finish entering a character, the firmware compares the sequence with the target. A correct answer advances the lesson; an incorrect answer repeats the same character.

## Parts

- ESP32-C3 SuperMini
- Two 5 mm LEDs
- Two 330 Ω resistors
- Passive buzzer
- Connecting wires and a suitable prototyping board
- USB cable for programming and power

The BOOT button on the ESP32-C3 SuperMini is reused as the Morse key, so the prototype does not need a separate button.

## Circuit and enclosure

I kept the electronics simple and made a PCB using an online EDA tool. The enclosure was designed in Fusion 360, with printable files supplied in the original project.

**Important:** GPIO 9 is a boot-strapping pin on the ESP32-C3. Avoid holding the BOOT button while powering on or resetting the board.

## Firmware

Open the firmware in Arduino IDE, select the appropriate ESP32-C3 board and upload the sketch. Enable USB CDC On Boot if required by your board configuration.

The firmware handles button timing, dot-and-dash detection, lesson progression and feedback. The lesson sequence can be modified in the code to experiment with different groups of letters.

The original project links the firmware and 3D files here: [Morse Monkey GitHub repository](https://github.com/bhuvanbagwe/Morse_Monkey).

## Why no display?

I intentionally left out a display. Showing the corresponding letter every time would encourage visual memorisation, while Morse is primarily learned and used through sound and rhythm. Instead, I made a printable cheatsheet to use alongside the device.

The Instructable includes demonstration videos and the complete build details.

**Original build:** [Morse Monkey on Instructables](https://www.instructables.com/MorseMonkey-Why-Dont-You-Know-Morse-Code-a-Toy-Mon/), published 26 October 2026.
