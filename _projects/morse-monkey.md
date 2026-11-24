---
title: Morse Monkey
order: 2
summary: A USB-pluggable toy monkey that teaches Morse code with lights, a buzzer and a single button.
hero: /assets/img/projects/morse-monkey.jpg
hero_alt: Cover image from the Morse Monkey Instructables write-up, showing a brown, monkey-faced trainer enclosure.
hero_credit: Cover image from the Instructables write-up, published 26 October 2026.
instructable: https://www.instructables.com/MorseMonkey-Why-Dont-You-Know-Morse-Code-a-Toy-Mon/
# TODO: Set `github` to the public repository under https://github.com/bhuvanmakes
# once it is published. Do not link github.com/bhuvanbagwe (those URLs now 404).
# github:
# A fuller post is drafted in _drafts/morse-monkey.md and is not published yet.
---

Morse Monkey is an open Morse-code trainer shaped like a toy rather than a tool. It is built around an ESP32-C3 SuperMini.

A trainer LED flashes the target Morse pattern. A user LED shows your button input. A passive buzzer plays tones for the symbols and for right-or-wrong feedback. The board's BOOT button is the key. The Instructables write-up notes that GPIO 9 is a boot-strapping pin on the ESP32-C3, so the button should not be held while the board is powering on or resetting.

There is no display on purpose. A printed cheatsheet is provided instead, so you learn the sound and rhythm of the code rather than reading letters off a screen.

The [Instructables write-up](https://www.instructables.com/MorseMonkey-Why-Dont-You-Know-Morse-Code-a-Toy-Mon/) was published on 26 October 2026. A longer blog post is drafted and not published yet.
