# Project Phantom 

**Phantom** is a professional electric guitar concept built around a simple principle: the instrument must remain a **real guitar first**, while integrating advanced onboard digital processing, a robust hardware control surface, and a clear industrial identity.

This project is not about turning a guitar into a tablet, a toy, or a keyboard substitute. It is about designing a modern performance instrument with a rigid wooden body, per-string audio processing, embedded DSP, and a restrained, stage-appropriate user interface.

---

## Project Vision

Phantom Guitar combines the physical integrity and expressive nuance of a traditional electric guitar with a tightly integrated onboard digital system.

The instrument is designed to:

- preserve the feel and expressive detail of a true electric guitar
- process each string independently in real time
- provide onboard effects, routing, alternate tunings, and utility tools
- avoid MIDI-first workflows and retain the audio character of the strings themselves
- use a physical, hardware-like interface rather than a touchscreen-centric UI
- present a premium, professional stage identity with minimal visual noise

The result is a guitar that behaves like an instrument, not a gadget.

---

## Core Design Philosophy

### 1. Guitar first
NX Guitar is designed as a serious instrument with a rigid body, stable structure, and performance-ready ergonomics. The digital system is integrated into the instrument architecture, but it does not redefine the guitar as a consumer electronics device.

### 2. Audio, not MIDI
The system is built around **real-time audio-domain processing**, not MIDI conversion. The project avoids reducing guitar playing into note events and instead preserves:

- picking dynamics
- string attack
- bends and vibrato
- slides and legato noise
- harmonic complexity
- per-string character

### 3. One process per string
Each string is treated as its own signal path. This enables more precise DSP, cleaner alternate tunings, better harmonization, and far more reliable polyphonic processing than a mixed mono pickup path.

### 4. Hardware UI, not app UI
The control surface is intentionally physical. NX Guitar does not present itself as a guitar with a screen attached. Instead, it uses a dedicated control plate with tactile controls, protected status displays, and single-color illumination suitable for live performance.

### 5. Restrained visual language
The project avoids excessive RGB lighting, large touch displays, and flashy consumer-tech styling. The intended character is premium, dark, minimal, mechanical, and stage-safe.

---

## Instrument Character

- **professional**, not experimental
- **robust**, not fragile
- **precise**, not playful
- **modern**, not futuristic for its own sake
- **integrated**, not assembled from unrelated parts

Its identity sits between three worlds:

- boutique electric guitar design
- embedded DSP hardware
- performance control surface design

The aesthetic target is a guitar that can stand beside professional rack gear, studio hardware, and high-end stage instruments without looking like a novelty product.

---

## UI Philosophy

The Phantom control surface is designed as a **hardware panel embedded into the guitar body**.

It is not a touchscreen interface. It is a tactile control system with protected status displays and a clear live-performance logic.

### Design goals

The UI must be:

- readable at a glance
- usable in low-light environments
- playable without constant visual attention
- resistant to moisture and stage wear
- visually restrained and non-fatiguing

### Lighting strategy

The interface uses **single-color illumination only**. This is intended to reduce distraction on stage and preserve eye comfort during rehearsals, performances, and dark venue conditions.

The preferred visual language is:

- dark charcoal or black control surface
- single accent color for active information and ring illumination
- low-glare display windows
- no RGB effects and no decorative lighting

---

## UI Layout

The front control plate is positioned in the lower bout and mounted flush into the body as a dedicated black metal or carbon-fiber-reinforced module.

### Primary elements

#### 1. Four illuminated rotary controls
A column of four physical rotary controls sits on the left side of the plate.

These are intended to function as:

- fast parameter controls
- contextual encoder controls
- page-aware DSP editing controls
- effect depth, mix, or routing controls depending on mode

They are conceived as illuminated hardware controls rather than decorative LEDs. Their ring illumination communicates active state and orientation while preserving a clean, monochrome visual identity.

#### 2. Two vertical parameter bands
Adjacent to the rotary controls are two narrow parameter zones. These are designed to represent frequency- or parameter-based editing in a clear vertical layout.

The visual language supports:

- EQ shaping
- filter movement
- per-string or grouped parameter editing
- macro visualization
- modulation or routing depth indication

This area should feel closer to studio hardware than to a mobile app.

#### 3. Two protected display windows
The center of the control surface contains two small display modules.

These displays are intentionally limited in size. Their role is to provide focused system feedback without dominating the instrument visually.

Suggested functions include:

- preset name and active mode
- tuner or tuning map
- per-string status
- routing state
- meter activity
- selected parameter context

These displays should be durable, recessed, and protected from impact and incidental moisture.

#### 4. 3×4 assign button matrix
On the right side of the plate is a matrix of twelve physical assign buttons.

This matrix is intended for:

- preset triggering
- scene switching
- effect block assignment
- navigation
- macros
- performance utilities

The matrix should read as a serious hardware input area, not as drum pads or decorative buttons.

### Secondary front controls

Above the control plate, the guitar retains **two conventional body knobs** for immediate performance functions such as:

- master volume
- wet/dry blend
- master tone
- system mix

This separates **playing controls** from **system controls**.

---

## Signal Architecture

NX Guitar is based on a **per-string audio architecture**.

### High-level flow

```text
String Capture (6 independent channels)
→ Low-noise analog front end
→ Multichannel ADC
→ Real-time DSP engine
→ Global stereo mix / routing
→ Main outputs / headphones / auxiliary paths
```

### Why per-string processing matters

Per-string processing makes the system viable as an instrument rather than a novelty. It allows for:

- cleaner alternate tunings
- more accurate pitch shifting
- better harmonization
- per-string dynamics and EQ
- intelligent stereo placement
- improved polyphonic tracking
- greater expressive preservation during DSP processing

This is the foundation that separates NX Guitar from conventional onboard multi-effects systems.

---

## Intended DSP Capabilities

The onboard processing system is intended to support a broad but instrument-focused feature set.

### Core processing

- per-string EQ
- per-string compression
- distortion and saturation paths
- delay and reverb
- chorus, flanger, phaser, modulation
- intelligent stereo routing
- dynamics shaping

### Extended transformation

- alternate tunings without retuning the physical strings
- virtual capo functions
- harmonization
- octave layers
- 12-string style simulation
- baritone-style transformations
- custom response curves per string

### Utility functions

- tuner
n- metronome
- preset management
- performance scenes
- routing control
- parameter macros

The design goal is not “infinite features,” but a focused professional toolkit embedded into the instrument itself.

---

## Mechanical Integration

NX Guitar is mechanically organized into distinct zones so that the instrument remains serviceable and structurally coherent.

### Front zone: playing surface
The upper and central regions of the front body remain dedicated to the guitar itself:

- pickups
- strings and bridge
- picking area
- standard playing controls

This area should remain uncluttered.

### Lower control zone: embedded UI plate
The lower bout houses the flush-mounted control surface.

This plate should be:

- rigid
- mechanically sealed
- visually integrated with the body contour
- easy to service as a subassembly
- resistant to accidental impact and contamination

### Rear service zone
A large rear access hatch provides access to the main electronics cavity.

This cavity is intended to house:

- DSP board
- converter board
- power management
- battery system
- shielding
- internal wiring and service access

This allows the front plate to remain a dedicated human-interface layer, while the rear cavity contains the core electronics.

---

## Materials and Surface Language

The instrument body is intended to remain primarily wooden in character and structural behavior, even when paired with technical materials.

### Intended materials

- painted or satin-finished wooden body
- black anodized aluminum or carbon-reinforced control plate
- protected display windows
- tactile mechanical controls
- optional carbon accent areas where structurally or visually appropriate

### Surface character

The overall visual language should remain:

- dark
- matte or satin
- low-glare
- precise
- professional

The technical elements should feel integrated into the body, not attached after the fact.

---

## Live Performance Character

NX Guitar is meant to succeed in the exact places where many “smart instrument” concepts fail.

It is designed for:

- stage readability
- tactile control without constant menu diving
- low visual fatigue in dark environments
- minimal accidental activation
- clear separation between playing and system editing
- confidence under real performance conditions

The interface should support fast action, not visual distraction.

---

## System Principles

The project should follow these principles throughout development:

### Preserve instrument identity
Every technical decision must support the experience of playing a guitar, not replace it.

### Keep latency extremely low
The instrument only works if the response remains immediate and natural.

### Build for failure safety
The guitar should retain a safe, usable signal path even when the digital system is unavailable.

### Separate audio, control, and power cleanly
Signal integrity, shielding, and internal architecture are central to the success of the instrument.

### Favor physical clarity over software excess
The interface should expose only what matters, with strong tactile logic and minimal visual clutter.

---

## Summary

NX Guitar is a concept for a modern electric guitar with integrated per-string DSP and an embedded physical control surface.

Its defining characteristics are:

- real-guitar feel and structure
- per-string audio-domain processing
- onboard effects and alternate tuning capability
- physical UI with four illuminated rotary controls, two protected displays, and a 3×4 assign matrix
- single-color lighting for stage-safe readability
- premium industrial design with a restrained, professional character

NX Guitar is not a touchscreen guitar, not a MIDI-first controller, and not a novelty concept. It is a serious attempt to define a new category of embedded-performance electric instrument.

---

## Status

This project is currently in the concept and system-design phase.

Current focus areas include:

- industrial design refinement
- UI architecture and control logic
- per-string signal-chain design
- DSP hardware architecture
- enclosure, cavity, and control-plate integration
- practical prototyping strategy

---

## License
I/US Source-Available License 1.0

Copyright (c) 2026 Pezhman Farhangi
I/US Music
