---
layout: default
title: Overview
eyebrow: Science fair project · 2026–27
---

# Catching the first tremor of an earthquake on a tiny, low-cost device

> One or two sentences, in plain language, saying what this project is. Imagine explaining it to a friend who knows nothing about earthquakes.
> - What does the device do?
> - Why does it matter that it's cheap and small?

{% include seismogram.html %}

{% include facts.html %}

## The problem

> - What is a P-wave, and why do the seconds before the S-wave matter?
> - Why don't earthquake early-warning systems reach everyone today?
> - What goes wrong when you put a cheap sensor in a house? (Think of doors, footsteps, washing machines.)

## My approach

> - Two stages: what does each stage do?
> - Why a streaming TCN instead of the windowed models other people use?
> - Why does detection latency matter more than inference time? Say it in your own words.

| Design choice | Value |
|---|---|
| Model | Streaming dilated TCN, causal 1-D convolutions, kernel 3 |
| Layers | 12 (two stacks, dilations 1, 2, 4, 8, 16, 32) |
| Parameters | 22,185 (budget < 30k) |
| Model size | 21.7 KiB INT8 · 6.5 KiB streaming state |
| Input | 100 Hz, 3-axis, 2–15 Hz causal Butterworth bandpass |
| Primary metric | False alarms per hour, with Poisson confidence intervals |
| Headline latency | Detection latency (P-onset to alert), not inference time |

## Where things stand

> A short paragraph on what's done, what you're doing now (for example, Corpus 2 recordings) and what's next. Update it whenever you post a notebook entry.

## Explore

{% include cards.html %}

## About me

> Who you are, your school and grade, and what got you interested in earthquakes. Add your mentor too, if you want.

## How I used AI tools

> ISEF expects you to disclose AI assistance. Say plainly which parts of the work were AI-assisted (coding, literature search, etc.) and how you checked them. Your `docs/AI_USE_LOG.md` is the record to draw on.
