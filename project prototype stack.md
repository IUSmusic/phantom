# Project Phantom Prototype Stack

## Purpose

This document defines the **final recommended prototype setup** for **Project Phantom**: a battery-powered, per-string DSP electric guitar with a minimal physical control surface, compact onboard electronics, and a professional stage-oriented design language.

It is intended for GitHub documentation and reflects the **current recommended implementation direction**, not the broader design discussion.

---

## System Architecture

Project Phantom should be built as **three coordinated subsystems**:

1. **Hexaphonic Instrument Front End**  
   Independent capture of all six strings with low noise and minimal crosstalk

2. **Real-Time Audio Engine**  
   Deterministic embedded DSP for per-string processing and stereo output generation

3. **Physical Control Surface**  
   A separate onboard hardware UI using encoders, buttons, and two protected displays

This separation is the correct foundation for reliability, shielding, serviceability, and future iteration.

---

## Prototype Setup

### 1. Per-String Pickup System
Cycfi active hexaphonic platform  
Examples: **Nu**, **Six Pack**, or equivalent Cycfi modular system

#### Role
- Captures all 6 strings independently
- Provides the correct signal source for true per-string DSP
- Preserves string separation for tuning, harmonization, octave processing, and spatial effects

#### Why this is the correct choice
Project Phantom is not a MIDI-first instrument. It is built around **real per-string audio processing**, so the pickup system must begin with true hexaphonic capture.

---

### 2. Main Embedded Audio Core
**For serious prototype:** Analog Devices **SHARC** platform  
Preferred direction: **ADSP-21569**

#### Role
- Runs all real-time audio processing
- Handles parallel per-string DSP chains
- Supports advanced effects and pitch-aware transformations with low latency

#### Target processing scope
Each string path should support:
- EQ
- compression
- distortion / saturation
- modulation
- delay / ambience
- pitch shift
- octave layers
- harmonization
- per-string routing and panning

#### Why this is the correct choice
SHARC is the strongest embedded path for the full Project Phantom feature set and gives the best chance of reaching product-grade performance without compromising responsiveness.

---

### 3. Audio Conversion
**PCM3168A** or equivalent 6-in / 8-out audio codec

#### Role
- Converts 6 independent analog string signals to digital
- Provides output conversion for stereo and additional output paths
- Simplifies integration compared with stitching together smaller converter blocks

#### Why this is the correct choice
Project Phantom naturally maps to a **6-input multichannel audio system**. A codec that already matches this topology reduces PCB complexity and shortens the path to a working prototype.

---

### 4. Output Architecture
- **Stereo main output**
- **Headphone output**
- **Optional aux / monitor path**

#### Design requirement
The output section should prioritize:
- low noise
- compact analog layout
- stage-safe operation
- efficient battery-powered implementation

---

### 5. Control Surface Architecture
** dedicated **control-surface daughterboard**

#### Physical UI elements
- **4 illuminated rotary encoders**
- **3×4 physical button matrix**
- **2 protected small displays**
- **2 main guitar knobs** above the control plate

#### Design principle
The UI is **physical hardware**, not a touchscreen.

The control surface should be mounted behind a **flush recessed metal or carbon control plate** and operate as a dedicated hardware module, separate from the main audio engine.

#### Why this is the correct choice
This keeps the instrument tactile, stage-friendly, low-glare, and consistent with the intended product character.

---

### 6. Display Strategy
Two small monochrome or single-color displays

#### Role
- Preset and parameter context
- tuner / routing / status feedback
- minimal visual load during performance

#### Design requirement
Displays should be:
- recessed
- protected
- readable in low light
- visually restrained
- integrated into the hardware plate without dominating the body design

---

### 7. Power System
**1S** rechargeable lithium system  
Example direction: **1S2P** high-capacity cell arrangement if required

single-cell charger with power-path management

#### Role
- supports battery-powered operation
- allows compact internal integration
- simplifies charging and system power handling

#### Design requirement
The power subsystem must be:
- low heat
- low noise
- compact
- properly filtered between analog and digital domains

---

## Mechanical Integration

### Front Body Layout
The front of the instrument should remain divided into two distinct zones:

#### Instrument Zone
- pickups
- bridge
- picking area
- two main guitar knobs

#### Control Zone
- angled lower-bout control plate
- 4 illuminated encoders
- 2 protected displays
- 3×4 assign button matrix

This preserves the identity of the instrument as a **authentic wooden electric guitar**, while making the DSP system feel integrated and intentional.

---

### Rear Cavity Layout
The rear service cavity should contain:
- main DSP board
- multichannel converter board
- battery pack
- power regulation
- shielding and internal harness routing

The control-surface board should remain localized to the front plate area.

This layout supports:
- cleaner service access
- shorter control wiring
- improved shielding strategy
- better separation between UI and audio electronics

---

## Shielding and Reliability Requirements

Project Phantom must be designed as a professional instrument, not a novelty device.

### Required design priorities
- isolated analog and digital sections
- careful ground strategy
- short analog signal paths from pickup to converter
- low EMI control implementation
- low thermal load
- physically secure internal mounting
- stage-safe mechanical robustness

### Operational requirement
The instrument should remain stable, quiet, and predictable in live conditions.

---

## Recommended Development Path

### Phase 1 — Signal and DSP Validation
Build and validate:
- hex pickup front end
- multichannel conversion
- per-string DSP chains
- stereo output path

### Phase 2 — Hardware UI Prototype
Add:
- control plate
- encoders
- assign buttons
- displays
- preset and navigation logic

### Phase 3 — Full Onboard Integration
Integrate:
- battery power
- charging
- shielding
- rear cavity structure
- production-oriented mechanical layout

This sequence reduces risk and keeps the prototype effort focused on the most important problem first: **audio feel and responsiveness**.

---

## Final Recommendation Summary

### Final prototype stack
- **Hex pickup:** Cycfi active hexaphonic system
- **DSP core:** ADSP-21569 SHARC
- **Audio conversion:** PCM3168A-class 6-in / 8-out codec
- **UI:** dedicated control-surface daughterboard
- **Displays:** two small protected monochrome displays
- **Controls:** 4 illuminated encoders + 3×4 button matrix + 2 master guitar knobs
- **Power:** 1S rechargeable battery architecture with proper power-path management
- **Mechanical structure:** front control plate + rear electronics cavity

---

## Product Character

Project Phantom should feel like:

- a **professional electric guitar**
- a **precision onboard DSP instrument**
- a **minimal hardware-controlled system**
- a **stage-ready object with low visual noise**

It should **not** feel like:
- a tablet embedded in a guitar
- a MIDI controller disguised as an instrument
- a novelty smart-guitar concept

The correct identity is:

> **A true electric guitar with integrated per-string DSP, expressed through a restrained physical control surface and a professional industrial design language.**
