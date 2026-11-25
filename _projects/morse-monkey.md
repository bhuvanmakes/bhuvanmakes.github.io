---
title: Morse Monkey
order: 2
summary: A USB toy monkey that teaches Morse code with lights, a buzzer and one button.
intro: >-
  Morse Monkey is a USB toy monkey that teaches Morse code with lights, a buzzer and one button. It's built around an ESP32-C3 SuperMini, and there's no display on purpose — a printed cheatsheet comes with it instead. The Instructables write-up went up on 26 October 2026.
hero: /assets/img/morse-monkey/cover.jpg
hero_alt: Cover image from the Morse Monkey Instructables write-up, showing a brown, monkey-faced trainer enclosure.
hero_credit: Cover image from the Instructables write-up, published 26 October 2026.
instructable: https://www.instructables.com/MorseMonkey-Why-Dont-You-Know-Morse-Code-a-Toy-Mon/
# TODO: Set `github` to the public repository under https://github.com/bhuvanmakes
# once it is published. Do not link github.com/bhuvanbagwe (those URLs now 404).
# github:
# A fuller post is drafted in _drafts/morse-monkey.md and is not published yet.
---

Morse Monkey is a Morse-code trainer shaped like a toy rather than a tool. It's built around an ESP32-C3 SuperMini.

A trainer LED flashes the target Morse pattern. A user LED shows your button input. A passive buzzer plays tones for the symbols and for right-or-wrong feedback. The board's BOOT button is the key. The Instructables write-up notes that GPIO 9 is a boot-strapping pin on the ESP32-C3, so don't hold the button while the board is powering on or resetting.

There's no display, on purpose. A printed cheatsheet comes with it instead, so you learn the sound and rhythm of the code rather than reading letters off a screen.

The [Instructables write-up](https://www.instructables.com/MorseMonkey-Why-Dont-You-Know-Morse-Code-a-Toy-Mon/) went up on 26 October 2026. A longer blog post is drafted and not published yet.
