<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=bash,c,cpp,linux,git,docker,cmake,vscode,vim" />
  </a>
</p>
<p align="right">
  <a href="https://www.linkedin.com/in/nbordoni01/">
    <img src="https://img.shields.io/badge/LinkedIn-blue?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge"/>
  </a>
</p>

# DNAfx Pedal Mod — Smart Looper & Tuner Controller

Hardware extension project for the **DNAfx GiT** multi-effects pedal.

This project explores how to extend a closed commercial guitar pedal without modifying its firmware, by adding an external programmable control layer using GPIO, USB HID, and relay-based switching.

The work started as a learning exercise in electronics and embedded systems, coming from a software development background.

---

## Overview

The mod exposes looper and tuner control through external hardware, allowing remote operation and automation while preserving the original pedal electronics.

Key capabilities:

- External looper control
- Looper track import workflow
- Remote control via Raspberry Pi + Android client
- Dual interface:
  - USB HID communication
  - GPIO hardware triggering
- Relay-based footswitch emulation
- Internal mounting with custom 3D-printed backplate
- Stable enough for live performance usage

---

## Design Approach

The system interacts with the pedal  at the **hardware interface level**, emulating physical switch presses, and at the **firmware level**, sending payload-bytes throught serial port.

Goals:

- Non-invasive modification
- Electrical safety
- Hardware isolation
- Reproducibility with accessible components

---

## System Architecture
Android App
->
Raspberry Pi (Python service)
->
( GPIO -> Relay switching layer ) || USB HID
->
DNAfx GiT pedal

📦 Repo --> [DNAfx_Hack](https://github.com/jblackiex/DNAfx_Hack)

