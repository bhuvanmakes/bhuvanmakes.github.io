---
title: Receiving NOAA 15 with an RTL-SDR
date: 2024-06-20
summary: Trying to pull weather images from NOAA 15 with a home-built telescopic V-dipole and a cheap RTL-SDR.
intro: >-
  I wanted to receive weather images straight from a satellite in orbit, using an antenna I designed myself and a cheap RTL-SDR. After a couple of messy attempts on the terrace, I got a pass from NOAA 15 and an image of the Indian subcontinent. Next I want to try NOAA 18 or 19, and use a Raspberry Pi instead of my laptop.
lede: Trying to pull weather images from NOAA 15 with a telescopic V-dipole and a cheap RTL-SDR.
hero: /assets/img/rtl-sdr-noaa-15/cover.jpg
hero_alt: YouTube thumbnail for the video, showing a received weather-satellite image of India's west coast with the title I hacked data from satellite.
hero_credit: Thumbnail from the YouTube video, published 20 June 2024.
youtube: Lps8Qj2zblw
tags:
  - RTL-SDR
  - Satellites
  - NOAA
---

This is how Earth looks from about the Indian subcontinent, and the picture is special to me because I captured it directly from a satellite in orbit, with an antenna I designed myself.

The images we usually see on Google Earth come from Google's database, and those can be blurred where someone doesn't want you to look. In this case there are no blurs, at least technically — you see what the satellite sees. As far as I know, receiving these broadcasts is perfectly legal.

## The antenna

I started with the antenna. I didn't want a terrace full of different-sized V-shaped antennas, and I live in a building, so I can't leave one up permanently anyway. The neighbours wouldn't like that.

The useful trick is that frequency is inversely proportional to wavelength, and the size of a V-dipole follows the wavelength. If the two arms are telescopic, I can change their length and retune the antenna for different bands.

I don't have a VNA, so I couldn't measure it properly. I went ahead anyway. I also 3D-printed an enclosure to keep the wiring tidy. The whole antenna can be made for less than $10, and I made a separate video guide for building it.

## A cheap receiver

NOAA weather satellites transmit around 137 MHz. A "proper" software-defined radio was more than I wanted to spend, so I used a DVB-tuner RTL-SDR instead. It's a small USB stick. You can listen to FM on a computer with it, and you can even receive some geostationary signals — in theory you could watch TV on the computer with one, though that's less of a party trick these days.

While I was in the SDR rabbit hole I also started looking at submarine signals from various ground stations. I had some luck receiving a transmission station in Australia — the kind of place that shows up in spooky alien documentaries because of how it looks. That's really just a very large antenna. At very low frequencies the antenna has to get a lot longer.

## First pass: too hot, then the wrong input

I found out that a satellite was going to pass over my area in about 30 minutes, so I quickly assembled the antenna, put it on a tripod and went up to the terrace.

I could already hear the signal on 137.100 MHz, and the laptop was receiving it from the antenna. The problem was the heat. It was a very hot day, this is my work laptop, and I don't have a spare. I got worried it was getting cooked, so I stopped the reception and went back inside.

Six hours later I went up again, set everything up, and started recording. I was about five minutes late, so I missed the first five minutes of the pass, which was fine. When the recording finished I hit auto-process in the image-decoding software… and the picture came out dark. I tried an IR filter. Same thing.

I listened to the raw audio and realised the software had been recording from the laptop's microphone, not from the SDR. There's a virtual-cable setup for this, and I'm sure I had it right in the morning, but this time it had defaulted back to the microphone. That's why the image was black. A bit sad. I left it for the next day.

## The next day

The following day I recorded from the terrace again. I arrived ten minutes early this time, and I set up on the topmost part of the terrace so walls wouldn't get in the way. I wanted the whole pass.

The full transmission came in, and the images were much better. I really like them, though they aren't perfect. These are from NOAA 15, which is a much older satellite. From what I've read on a few subreddits, the images from NOAA 18 and NOAA 19 are better quality.

## What's next

The next thing I want to do is record NOAA 18 or NOAA 19, and I planned to do that with a Raspberry Pi instead of the laptop. It should be easier to leave a Pi on the terrace and control it from there.

For later passes I also planned to post the images on my YouTube Community tab, rather than making a full video every time.

The video this write-up follows is on [YouTube](https://www.youtube.com/watch?v=Lps8Qj2zblw), published 20 June 2024.
