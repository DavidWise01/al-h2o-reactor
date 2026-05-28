# AL-H₂O REACTOR
### On-Board Aluminum-Water Hydrogen Generation System

> **Engineering Gap = Product.**  
> The chemistry is MIT-published and proven. The gap between lab bench and production vehicle is the entire opportunity.

---

## What This Is

A complete engineering reference and interactive visualization suite for an **on-board hydrogen generation system** that uses aluminum pellets + water to produce hydrogen on demand — no compressed tanks, no cryogenics, no fossil fuel supply chain.

Chemistry discovered and published by MIT (2023–2024). This repo is the engineering translation: specifications, blueprints, bill of materials, safety documentation, and interactive 3D visualizations.

**Author:** David Lee Wise (ROOT0) / TriPod LLC  
**License:** CC-BY-ND-4.0

---

## The Core Reaction

```
2Al + 6H₂O  ──[imidazole + GaIn]──▶  2Al(OH)₃  +  3H₂↑  +  heat
```

| Input | Output |
|-------|--------|
| Recycled aluminum pellets (36 kg / 400 km) | Hydrogen gas (96% yield) |
| Seawater / any water (20 L / full cartridge) | Boehmite Al(OH)₃ (sellable byproduct) |
| Imidazole catalyst (trace) | Electricity via PEM fuel cell |
| GaIn alloy (recycled) | Water vapor (only exhaust) |

---

## Why This Isn't Just Another Hydrogen Concept

| Conventional Hydrogen Vehicle | AL-H₂O Reactor |
|-------------------------------|-----------------|
| 700-bar compressed H₂ tanks | No pressure vessel — metal pellets at room temp |
| Hydrogen refueling infrastructure (non-existent) | Any water + recycled aluminum = fuel |
| Cryogenic storage or compression energy loss | Exothermic reaction — energy-positive start |
| Single-point supply chain | Distributed production from scrap aluminum |
| Specialized refueling stations | Swap cartridge in 3 minutes, anywhere |

---

## Quick Specs

```
Reactor Volume         ~12 liters
Aluminum per 400 km     36 kg (recycled)
H₂ Yield               96%
Reaction Time           5 min (imidazole catalyst) vs 2 hr (no catalyst)
Catalyst Boost         24x acceleration
Water Source           Seawater, brackish, gray water, any
Fuel Cell Efficiency   60–65% (PEM)
Chain Efficiency       ~55–60%
CO₂ per kg H₂          1.45 kg (recycled Al pathway)
Byproduct              Boehmite Al(OH)₃ — commercially valuable
GaIn Alloy Recovery    Yes, via salt ion precipitation
Refuel Time            ~3 minutes (cartridge swap)
Cost Estimate          ~$9/kg H₂ (recycled aluminum feedstock)
```

---

## Repository Structure

```
al-h2o-reactor/
├── README.md               ← You are here
├── CHEMISTRY.md            ← Full reaction chemistry, stoichiometry, thermodynamics
├── SPECS.md                ← Engineering specifications, sizing calculations
├── SAFETY.md               ← Hazard analysis, safety systems, regulatory notes
├── BOM.md                  ← Bill of materials with suppliers and costs
├── .attribution            ← ROOT0 IP attribution record
├── docs/
│   ├── blueprints.svg      ← Engineering schematic (all 6 stages)
│   └── cascade-timeline.md ← The Cascade deployment roadmap
└── viz/
    ├── al-h2o-reactor.html    ← 3D interactive reactor (static view)
    ├── al-h2o-reactor-v2.html ← 3D reactor + live thermodynamics calculator
    └── the-cascade.html       ← Civilization blueprint scroll experience
```

---

## Interactive Visualizations

### `viz/al-h2o-reactor-v2.html` — **Recommended Entry Point**

Full Three.js 3D model of the complete reactor system. Features:
- **Drag / orbit** the reactor model in 3D
- **CUTAWAY** mode — slice the reactor to see internals
- **FLOW** mode — animated particle flow (Al pellets → H₂ → electricity → boehmite)
- **AUTO-ROTATE** — presentation mode
- **Hover tooltips** on every component
- **Live Thermodynamics Panel** — adjust Al feed rate, water temp, and PEM efficiency to see real-time calculated outputs

All math in the thermodynamics panel uses real stoichiometry:
- `2Al + 6H₂O → 2Al(OH)₃ + 3H₂`  
- Al molar mass: 26.98 g/mol | H₂ molar mass: 2.016 g/mol  
- ΔH = −418 kJ/mol Al | H₂ LHV = 120 MJ/kg  
- Arrhenius-curve catalyst effectiveness model (peak at 50°C)

### `viz/the-cascade.html` — **Civilization Deployment Blueprint**

Scroll-reveal experience mapping how this technology propagates from lab to global infrastructure. 16 sections across 3 tiers:

- **Tier 1 (2024–2028):** Disaster response, submarines, remote medical, military field ops
- **Tier 2 (2028–2032):** Off-grid EV charging, desalination + power combo, agricultural electrification
- **Tier 3 (2032–2040+):** Aluminum-as-currency, decentralized grid, developing world access, deep space ops

Includes interactive deployment calculator with full stoichiometry, CO₂, byproduct, and cost calculations.

---

## The 6-Stage System

```
[HOPPER]──▶[AUGER]──▶[REACTION CHAMBER]──▶[H₂ SEPARATOR]──▶[PEM FUEL CELL]──▶[MOTOR]
               ↑              ↑                    ↓
           [GaIn coat]   [Imidazole +          [BOEHMITE]──▶[Collection Tank]
                          Seawater]                ↓
                                               [GaIn Recovery]
```

**Stage 1 — Pellet Feed:** Recycled Al pellets pre-coated with GaIn alloy (strips oxide layer). Gravity-fed hopper cartridge. Auger rate = f(throttle demand).

**Stage 2 — Seawater Injection:** Filtered seawater or any water pumped in. Salt ions in seawater actually *improve* GaIn recovery (MIT finding).

**Stage 3 — Catalytic Reaction:** Imidazole catalyst accelerates the reaction 24x. Self-limiting: rate controlled by feed rate. Exothermic: heat captured by thermal management.

**Stage 4 — H₂ Separation:** Membrane separator. H₂ rises, boehmite settles. >99% purity. Low-pressure delivery — no compression needed.

**Stage 5 — Fuel Cell Conversion:** PEM stack, 60–65% efficiency. Standard EV motor output. Only exhaust: pure water vapor.

**Stage 6 — Byproduct Recovery:** Boehmite collected and sold (semiconductor, catalyst, ceramic markets). GaIn alloy recovered and recirculated. Zero waste loop.

---

## The Engineering Gap

**This is the product.**

The lab chemistry is solved. MIT published it. The gap is:

1. **On-board integration** — packaging a 12L reactor into a vehicle architecture
2. **Thermal management** — capturing exothermic reaction heat usefully
3. **Cartridge standardization** — swap system, station infrastructure, pellet logistics
4. **GaIn recirculation loop** — on-board vs. station-side recovery
5. **Variable-load response** — auger control latency vs. peak power demand spikes
6. **Boehmite handling** — wet slurry management, pump durability, swap interval
7. **Safety certification** — H₂ in confined spaces, pressure relief, fail-safe modes

Each of those is a business. The full system is a platform.

---

## Chemistry Source

Primary research published by MIT:

- Syed Zia Uddin, Nicolas Lamber, et al. — *"Hydrogen generation from water using Al microparticles treated with NaOH"*, MIT 2023
- Follow-on imidazole catalyst work: acceleration of Al–H₂O reaction from ~2 hours to ~5 minutes in seawater using caffeine-derived compound
- GaIn alloy as aluminum oxide-stripping activator — established prior art, MIT materials science

> **Note:** This repository documents the engineering application. Foundational chemistry IP belongs to MIT researchers. TriPod's contribution is the vehicle integration architecture and The Cascade deployment framework.

---

## Attribution

```
Author:     David Lee Wise (ROOT0)
Entity:     TriPod LLC
Date:       2024-present
Framework:  The Cascade (Tier 1 → Tier 2 → Tier 3)
IP Class:   Engineering architecture, deployment framework
License:    CC-BY-ND-4.0
```

All visualizations and documentation in this repository are original works by David Lee Wise / TriPod LLC, built on top of MIT-published open chemistry.

---

## The Philosophy

> *"World = Family. Engineering Gap = Product."*

This is not a grant proposal. It's not a VC deck. It's a blueprint — open, documented, and attributed — for anyone who wants to close one of the gaps.

The reactor doesn't care about geopolitics. Aluminum is the third most abundant element on Earth. Water covers 71% of the surface. The reaction works. 

What comes after is **The Cascade**.

---

*TriPod LLC // Anchor × Bubble × Gravity Well*
