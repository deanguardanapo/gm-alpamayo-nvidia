# GM × NVIDIA — Alpamayo 2 Super Reasoning Platform

An interactive technical reference documenting the integration pathway between GM's Super Cruise ADAS stack and NVIDIA's Alpamayo 2 Super reasoning model, targeting SAE Level 3 highway autonomy.

## Live Demo

[https://deanguardanapo.github.io/gm-alpamayo-nvidia/](https://deanguardanapo.github.io/gm-alpamayo-nvidia/)

## Overview

GM's Super Cruise is a perception-execution system — cameras, LiDAR, and HD maps feed a deterministic planning layer that handles mapped highway environments reliably. It does not produce decision rationale, maintain an internal world model, or generalize to scenarios outside its operational design domain.

SAE Level 3 (Eyes-Off) requires the vehicle, not the driver, to manage the full dynamic driving task within a defined ODD without supervision. The gap between Super Cruise's current capability and Level 3 compliance is primarily a reasoning gap: the ability to interpret ambiguous inputs, simulate outcome probabilities, and produce defensible control decisions under novel conditions.

NVIDIA's Alpamayo 2 Super is an open 32B-parameter Vision–Language–Action model that reasons jointly across perception, planning, and action. This project explores what a phased integration between GM and that toolchain could look like — starting with distilled models on current Orin hardware and scaling to full-stack deployment on DRIVE AGX Thor.

## What's Inside

| Tab | Contents |
|---|---|
| **About** | Platform scope, problem definition, phased integration approach, and Alpamayo 2 Super key parameters |
| **Live Simulation** | Side-by-side telemetry playback comparing Super Cruise and Alpamayo 2 Super across four edge-case scenarios: traffic light outage, lane cut-off, wrong-way driver, and emergency vehicle |
| **Stack Comparison** | Capability ratings across six dimensions for GM Super Cruise Today, the NVIDIA On Ramp configuration (Alpamayo 1.5 Nano on Orin), and the Full Stack configuration (Alpamayo 2 Super on Thor) |
| **Library Reference** | Component-level documentation for fifteen platform components across the On Ramp and Full Stack phases, including hardware, open models, simulation frameworks, datasets, and inference tooling |
| **The Pitch** | Strategic rationale for the integration, a five-stage development timeline, and the why-now case around NHTSA's AV regulatory formation period |

## Disclaimer

This is an educational project built for personal learning purposes. It is not a product announcement, confirmed roadmap commitment, or official communication from NVIDIA or General Motors. All capability ratings, timing estimates, and integration scenarios are illustrative and based on publicly available information.

## Built With

- HTML, CSS, JavaScript — single-file app, zero dependencies
- [Claude Code](https://claude.ai/code) — AI-assisted development throughout

## Background

Built to explore NVIDIA's automotive AI stack following the Alpamayo 2 Super announcement at GTC Taipei in June 2026. The project covers the full Physical AI toolchain — DRIVE AGX Orin and Thor compute platforms, the Alpamayo model family (1.5 Nano, 2 Super, AR1), simulation infrastructure (OmniDreams, AlpaSim, AlpaGym, Omniverse NuRec), and supporting frameworks (Cosmos 3, TensorRT, TAO Toolkit, NeMo, Omniverse Sensor RTX) — and maps each component to a concrete GM integration use case.
