# SPECS.md
## AL-H₂O Reactor — Engineering Specifications

---

## System Overview

```
┌─────────────────────────────────────────────────────────────────┐
│  AL-H₂O REACTOR SYSTEM — PASSENGER VEHICLE CONFIGURATION        │
│  Total system mass:   ~65 kg (full cartridge, empty tank)        │
│  Total system volume: ~35 liters (all components)               │
│  Peak power output:   ~25–40 kW continuous                      │
│  Refuel time:         ~3 minutes (pellet cartridge + byproduct)  │
│  Range per cartridge: ~400 km (15 kW avg draw, 80 km/h)         │
└─────────────────────────────────────────────────────────────────┘
```

---

## Component Specifications

### 1. Pellet Hopper / Cartridge

| Parameter | Value |
|-----------|-------|
| Capacity | 36 kg aluminum pellets |
| Pellet size | 4–8 mm pebble / granule |
| GaIn pre-coating | ~0.5–1.0% by weight |
| Cartridge material | HDPE or 316 SS |
| Cartridge sealing | Bayonet lock, O-ring sealed |
| Swap time | <90 seconds |
| Storage conditions | Ambient temperature, no special requirements |
| Shelf life | Indefinite (oxide re-coating prevented by GaIn) |
| Empty weight | ~2 kg (HDPE shell) |
| Full weight | ~38 kg |

### 2. Auger Feed Mechanism

| Parameter | Value |
|-----------|-------|
| Type | Twin-screw auger (prevents bridging) |
| Drive | 12V DC brushless motor, 50W |
| Feed rate range | 0.5–8 kg/hr (proportional to throttle) |
| Response latency | ~200 ms from demand signal |
| Pellet throughput | 36 kg per operating cycle |
| Peak rate | 12 kg/hr (burst, sprint demand) |
| Sealing | Dry-side / wet-side separation seal |

### 3. Reaction Chamber

| Parameter | Value |
|-----------|-------|
| Volume | ~12 liters internal |
| Operating pressure | ~1.1–1.3 bar (low, near-ambient) |
| Operating temperature | 40–65°C (self-heating from ΔH = −418 kJ/mol Al) |
| Optimal temperature | ~50°C |
| Maximum temperature | 80°C (catalyst degradation limit) |
| Material | 316L stainless steel (H₂ service) |
| Viewport | Borosilicate glass, 80mm dia. |
| Pressure relief | PRV set at 2.5 bar |
| Inlet connections | ½" NPT × 3 (water in, catalyst in, drain) |
| Outlet connections | ¾" NPT × 2 (H₂ out, boehmite slurry out) |
| Thermal jacket | Silicone heating blanket (cold start assist, 200W) |
| Heat recovery | Coolant loop to cabin HVAC / battery thermal |
| Insulation | 25mm mineral wool wrap |
| Cycle time | ~5 min per batch (continuous operation via staged chambers) |

### 4. H₂ Membrane Separator

| Parameter | Value |
|-----------|-------|
| Type | Hollow-fiber polysulfone membrane |
| Operating pressure | 1.0–1.2 bar feed |
| H₂ purity | >99.9% |
| H₂ recovery | >95% |
| Operating temp range | 20–80°C |
| Membrane area | ~0.5 m² effective |
| Differential pressure | <0.2 bar |
| Permeate delivery | Low-pressure direct to fuel cell |
| Boehmite rejection | >99.99% |
| Replacement interval | 2,000 operating hours |

### 5. GaIn Recovery System

| Parameter | Value |
|-----------|-------|
| Recovery mechanism | Salt-ion assisted phase separation |
| Recovery efficiency | >95% per cycle |
| GaIn reservoir | 500 mL stainless reservoir |
| Separation time | ~10 min settling post-reaction |
| Station-side vs. on-board | Hybrid: partial on-board, full recovery at station |
| GaIn inventory | ~180–360 g per system |
| Cost per replacement | ~$60–100 (makeup for losses) |

### 6. Catalyst (Imidazole) System

| Parameter | Value |
|-----------|-------|
| Catalyst concentration | 1–5 mM in reaction water |
| Injection | Micropump, 0.1–2 mL/min |
| Reservoir capacity | 500 mL concentrate |
| Reservoir life | ~50 full cartridges |
| Catalyst recovery | Partial — dissolved in slurry, partially lost |
| Makeup cost | <$0.50 per cartridge |

### 7. Seawater / Water System

| Parameter | Value |
|-----------|-------|
| Onboard water tank | 25 liters |
| Water consumption | ~2.0 kg per kg Al (~72 L full cartridge) |
| Filtration | 50 micron pre-filter + 5 micron final |
| Pump | 12V centrifugal, 8 L/min |
| Compatible water sources | Seawater, brackish, gray water, tap |
| Salt tolerance | No upper limit (seawater preferred) |
| Temperature range | 5–50°C inlet |

### 8. PEM Fuel Cell Stack

| Parameter | Value |
|-----------|-------|
| Type | Proton Exchange Membrane (PEM) |
| Power output | 25–40 kW (stack sizing TBD by application) |
| Operating efficiency | 60–65% (H₂ LHV to DC electricity) |
| Operating temperature | 60–80°C |
| H₂ inlet pressure | 1.0–1.2 bar (no compression needed) |
| Humidification | Self-humidifying membrane |
| Cooling | Liquid-cooled (shares EV thermal loop) |
| Platinum loading | 0.3–0.5 mg/cm² (standard PEM) |
| Stack lifetime | 10,000–20,000 operating hours |
| Output voltage | 200–400 VDC (dependent on stack size) |
| Air supply | Centrifugal compressor, 1.5–2 bar |

### 9. Boehmite Collection System

| Parameter | Value |
|-----------|-------|
| Collection tank | 15 liters capacity |
| Tank material | HDPE (boehmite is mildly abrasive) |
| Slurry concentration | ~30–40% solids by weight |
| Drain pump | Peristaltic, abrasion-resistant |
| Swap interval | Every pellet cartridge swap |
| Full tank weight | ~12–15 kg |
| Market value | ~$40–100 per tank (per station buyback) |

---

## System Mass Budget

```
Component                    Mass (kg)
──────────────────────────────────────
Reaction chamber (empty)     8.0
H₂ separator                 2.5
Fuel cell stack (25 kW)     20.0
Auger feed mechanism         3.0
Water tank (empty)           1.5
Boehmite tank (empty)        1.0
GaIn reservoir               1.0
Catalyst reservoir           0.5
Plumbing / fittings          2.5
Control electronics          1.5
Thermal insulation           2.0
Structural frame             4.0
──────────────────────────────────────
System dry mass:            47.5 kg

Al cartridge (full):        38.0 kg
Water tank (full):          25.0 kg
──────────────────────────────────────
System wet mass:           110.5 kg
```

Comparison: A 60 kWh lithium battery pack for a comparable BEV weighs ~400–500 kg.

---

## Power Density Analysis

```
Energy in 36 kg Al cartridge:
  H₂ produced    = 3.876 kg (@ 96% yield)
  H₂ energy LHV  = 3.876 × 120 MJ/kg = 465.1 MJ
  Electrical out  = 465.1 × 0.62 = 288.4 MJ = 80.1 kWh

System mass (wet, less byproduct tank):  ~98 kg
Specific energy:  80.1 kWh / 98 kg = 0.817 kWh/kg

Comparison:
  Lithium NMC battery:    0.20–0.27 kWh/kg
  Hydrogen (compressed):  1.5–2.0 kWh/kg (but tank adds mass)
  AL-H₂O system:         0.82 kWh/kg  ← 3–4× better than Li-ion
```

---

## Sizing Calculator Parameters

The live calculator in `viz/al-h2o-reactor-v2.html` implements:

```javascript
// Core constants
alMolar = 26.982 g/mol
h2Molar = 2.016 g/mol
h2oMolar = 18.015 g/mol
boehmiteMolar = 59.989 g/mol
deltaH = 418 kJ/mol Al
h2LHV = 120.0 MJ/kg
yieldEff = 0.96

// Catalyst temperature response (Arrhenius approximation)
catalystBoost(T) = min(1.2, 0.4 + 0.6 × exp(−(T − 50)² / 800))

// H₂ production
h2MolesHr = (alKgHr × 1000 / alMolar) × 1.5
h2KgHr = (h2MolesHr × h2Molar / 1000) × yieldEff × catalystBoost(T)

// Electrical output
elecKW = (h2KgHr × h2LHV / 3.6) × pemEff

// Range
cartridgeKWh = (cartridgeH2 × h2LHV / 3.6) × pemEff
rangeKm = (cartridgeKWh / 15 kW) × 80 km/hr
```

---

## Application Sizing Variants

### Passenger Vehicle (Reference Design)

```
Al cartridge:    36 kg
Range:           ~400 km
Peak power:      ~30 kW
Fuel cell:       30 kW PEM
Reactor:         12 L dual-chamber
System mass:     ~110 kg (loaded)
```

### Light Commercial Van

```
Al cartridge:    72 kg (dual hopper)
Range:           ~600 km
Peak power:      ~60 kW
Fuel cell:       60 kW PEM
Reactor:         24 L (2× parallel)
System mass:     ~200 kg (loaded)
```

### Emergency Generator (Stationary)

```
Al cartridge:    100 kg (drum feed)
Runtime:         ~48 hrs @ 5 kW
Peak power:      15 kW
Fuel cell:       15 kW PEM
Reactor:         8 L (lower pressure, single)
System mass:     ~80 kg (less mobility hardware)
Use case:        Disaster relief, remote medical, off-grid
```

### Marine (Small Vessel)

```
Al cartridge:    200 kg (bunker feed)
Range:           ~800 km @ 10 kW cruise
Peak power:      80 kW
Water source:    Ambient seawater (no tank needed)
Reactor:         40 L continuous feed
Notes:           Seawater as feedstock eliminates water storage
```

---

*Engineering specifications by David Lee Wise (ROOT0) / TriPod LLC, 2024–2026.*  
*All values engineering estimates based on published chemistry data. Prototype validation pending.*
