---
layout: default
title: Results
eyebrow: Results
permalink: /results.html
---

# What the data says so far

> Set expectations: these are results on public data plus bench tests. Final results on your own recordings (Corpus 2) come later. Say why false alarms per hour is your main metric.

## Public-data results {#public-data}

> Walk through panels A–D. For each one: what was measured, and what it means for the device. Use the "human-scale" version of false-alarm rates too (e.g. days between false alarms).

![Four-panel figure. A: false alarms per hour rise from 0.67 on held-out STEAD to 1.99 on PNW and 6.18 on PNW accelerometers. B: share of earthquakes caught is 0.411 with a STEAD threshold, 0.814 recalibrated, 0.856 with self-calibrating CFAR. C: EQTransformer and PhaseNet also lose detections across the three datasets. D: 504 hours of accelerometer noise needed versus 38 hours available publicly.](assets/img/results_summary.png)
*Multi-seed results across three datasets.*

## The datasets {#datasets}

> What's in STEAD, PNW, PNW Accelerometers and PNW Noise, and why you need all four.

![Example three-component waveforms from STEAD, PNW, PNW Accelerometers and PNW Noise, with the P-wave onset and one-second positive window marked](assets/img/datasets_overview.png)
*One example trace from each dataset.*

## Test H-1: sensor noise floor {#h1}

> Does the sensor meet its datasheet? What are the peaks between 6 and 13 Hz, and why do they matter for a 2–15 Hz detector?

![Amplitude spectral density of X, Y and Z axes over one hour at rest. The broadband level sits near or below the 25 micro-g per root hertz datasheet line, with resonance peaks of 6 to 13 times the floor inside the 2 to 15 Hz detection band](assets/img/h1_noise_floor.png)
*One hour at rest on foam, breadboard build.*

## Test H-2: gravity check {#h2}

> What does reaching all six gravity extremes show? Panel B labels the +1.28% gap a "sensitivity error". Your later notes (5 Sep) say it might be offset instead and was never measured. Decide what you can honestly claim, and say it.

![Four-panel gravity test. A: three axes steady over 100 seconds. B: total measured acceleration about 9.93 versus true gravity 9.81 meters per second squared. C: histograms of per-axis jitter. D: each axis reaches beyond plus and minus 9.81 in both directions](assets/img/h2_gravity.png)
*The board at rest, and then rotated through all six orientations.*
