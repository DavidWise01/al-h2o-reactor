# SAFETY.md
## AL-H₂O Reactor — Hazard Analysis & Safety Systems

---

## Safety Profile Overview

The AL-H₂O system has a fundamentally different risk profile from conventional hydrogen vehicles:

| Risk | Conventional H₂ Vehicle | AL-H₂O Reactor |
|------|--------------------------|-----------------|
| On-board H₂ storage | **700 bar compressed tank** (catastrophic failure potential) | No storage — generated on demand at 1.1–1.3 bar |
| Fuel volatility | Compressed gas — immediate release on breach | Solid aluminum pellets — no release without water |
| Refuel hazard | High-pressure H₂ transfer | Metal pellet swap — no gas transfer |
| Runaway risk | Rapid tank depressurization | Self-limiting reaction: stop water → stop H₂ |
| Crash scenario | Tank rupture / H₂ fire | Pellets spill (inert), water spills, reaction halts |

**Primary safety advantage:** The reaction requires *both* aluminum AND water AND catalyst together. Removing any one input stops hydrogen generation within seconds.

---

## Hazard Identification (HAZID)

### H1 — Hydrogen Gas Accumulation

**Hazard:** H₂ is flammable (4–75% v/v in air, autoignition 500°C).  
**Likelihood:** Low — H₂ generated at low pressure, delivered directly to fuel cell without storage.

**Controls:**
- [ ] Continuous H₂ gas sensors in engine bay (LEL monitoring, 10% LEL alarm)
- [ ] Forced ventilation system: 10 air changes/hr minimum in H₂ zone
- [ ] Automatic shut-off: auger stops + water valve closes on >20% LEL alarm
- [ ] Purge valve: inert N₂ or CO₂ purge on sensor trigger
- [ ] All electrical components in H₂ zone: ATEX/IECEx Zone 1 rated
- [ ] No ignition sources within 500mm of H₂ plumbing

**Residual risk:** Low

---

### H2 — Reaction Runaway (Thermal)

**Hazard:** Exothermic reaction ΔH = −418 kJ/mol Al. Uncontrolled pellet feed could generate excessive heat.

**Controls:**
- [ ] Thermal sensor on reaction chamber (4-point PT100)
- [ ] Emergency stop: auger de-energized at >75°C chamber temp
- [ ] PRV (pressure relief valve) set at 2.5 bar — vents to safe external exhaust
- [ ] Water feed kill valve: solenoid-controlled, normally open (failsafe off)
- [ ] Physical thermal fuse: irreversible trip at 85°C (backup to electronic)
- [ ] Overpressure burst disk downstream of PRV (2nd layer)

**Residual risk:** Very Low

---

### H3 — GaIn Alloy Toxicity

**Hazard:** Gallium and indium are mildly toxic if ingested. GaIn alloy is liquid at room temperature (melting point ~15.7°C). Spill during cartridge swap.

**Controls:**
- [ ] Sealed cartridge system: GaIn-coated pellets enclosed in hopper
- [ ] Glove requirement for cartridge swap (nitrile, minimum)
- [ ] Station-side GaIn recovery performed by trained operators
- [ ] SDS provided at all service points
- [ ] No oral/dermal exposure route in normal operation

**MSDS Notes:**
- Gallium: LD50 (oral rat) >5000 mg/kg — practically non-toxic
- Indium compounds: TLV 0.1 mg/m³ (respirable) — avoid inhalation of dust
- GaIn alloy: main risk is skin absorption with prolonged contact

**Residual risk:** Low

---

### H4 — Imidazole Exposure

**Hazard:** Imidazole is an irritant (skin, eyes). Concentrated solution in catalyst reservoir.

**Controls:**
- [ ] Catalyst reservoir: sealed pressurized vessel, pump-only access
- [ ] Secondary containment tray under reservoir
- [ ] SDS provided; PPE (safety glasses, nitrile gloves) for service
- [ ] Dilution in reaction water reduces final concentration to 1–5 mM (benign)

**Regulatory status:** Not a controlled substance. REACH registered. Low environmental concern at use concentrations.

**Residual risk:** Negligible in normal operation

---

### H5 — Boehmite Slurry Handling

**Hazard:** Boehmite slurry (Al(OH)₃ / AlOOH in water) is mildly abrasive and alkaline (pH ~8–9).

**Controls:**
- [ ] Slurry collection tank sealed; exchange at service station
- [ ] Pump internals rated for abrasive slurry duty (ceramic or PTFE lined)
- [ ] Collection tank over-fill sensor + alarm
- [ ] Spill kit in vehicle for collection tank exchange

**Environmental note:** Boehmite is environmentally benign — it's the feedstock for commercial aluminum oxide production. It does NOT contaminate groundwater or stormwater in typical spill quantities.

**Residual risk:** Negligible

---

### H6 — Electrical Hazards (Fuel Cell High Voltage)

**Hazard:** PEM fuel cell stack outputs 200–400 VDC. Standard EV electrical hazard class.

**Controls:**
- [ ] All high-voltage wiring orange-insulated, HV-rated (1 kV class)
- [ ] Automatic disconnect on crash signal (airbag deployment / G-sensor)
- [ ] Service interlock: manual HV disconnect before maintenance access
- [ ] HV enclosures: IP67 rated
- [ ] Arc flash protection: current-limiting fuses at stack output

**Standards applicable:** ISO 26262, UN ECE R100, FMVSS 305

**Residual risk:** Low (same as any BEV)

---

### H7 — Crash / Impact Scenario

**Hazard:** Vehicle collision during operation.

**Controls:**
- [ ] Pellet hopper: reinforced polymer housing, pellets remain contained
- [ ] Reaction chamber: isolated from crumple zones, mounted to chassis rail
- [ ] Emergency shutdown: G-sensor (>8g) immediately cuts auger, water valve, fuel cell
- [ ] H₂ generation ceases within 5 seconds of water valve closure
- [ ] Remaining H₂ in lines (<50 mL total): purged via PRV to atmosphere
- [ ] No compressed gas tanks to rupture

**Key advantage vs. compressed H₂:** A breached 700-bar tank can propel the vehicle and ignite a sustained fire. The AL-H₂O system in a crash simply stops generating. The aluminum pellets are inert without water contact.

**Residual risk:** Low

---

## Emergency Procedures

### H₂ Sensor Alarm (Low Level — 10% LEL)

```
1. Audible/visual alert in cabin
2. Auger feed rate reduced 50%
3. Ventilation forced to maximum
4. Monitor: if alarm clears in 60s, resume normal
5. If persistent: proceed to HIGH LEVEL procedure
```

### H₂ Sensor Alarm (High Level — 25% LEL)

```
1. Auger STOP (immediate)
2. Water valve CLOSE (immediate)
3. H₂ generation ceases
4. N₂/CO₂ purge activates (if equipped)
5. Warning to driver: reduce speed, find safe stop
6. Do not re-enter vehicle until H₂ sensor clears
7. Service required before restart
```

### Thermal Runaway Response

```
1. Electronic shutdown at 75°C
2. Physical fuse trips at 85°C (requires replacement)
3. PRV vents excess pressure
4. Allow 30 min cooling before access
5. Inspect reaction chamber before returning to service
```

### Cartridge Swap (Normal Operation)

```
1. Engine off / fuel cell in standby
2. Allow 5 min cooldown (reaction chamber)
3. Don nitrile gloves
4. Disconnect boehmite collection tank → station exchange
5. Unlock pellet hopper cartridge (bayonet, quarter-turn)
6. Remove spent cartridge (empty, ~2 kg)
7. Insert fresh cartridge — audible lock click
8. Add water to reservoir if needed (check gauge)
9. System self-tests on startup
```

---

## Regulatory Framework

### Current Standards (Apply by Analogy)

| Standard | Applicability |
|----------|--------------|
| SAE J2578 | General fuel cell vehicle safety |
| SAE J2600 | Hydrogen fueling connection — modified for solid fuel |
| ISO 26262 | Functional safety (electronic controls) |
| UN ECE R134 | Hydrogen-powered vehicles (framework) |
| FMVSS 305 | Electrical safety for electric vehicles |
| ATEX Directive | Explosive atmosphere equipment (EU) |
| IEC 62282 | Fuel cell technologies |

### Gaps Requiring New Standards

1. Solid aluminum fuel cartridge safety standard (no current equivalent)
2. On-board H₂ generation (all current standards assume stored H₂)
3. GaIn-treated metal fuel handling and disposal
4. Boehmite slurry waste classification and transport

> **Note:** The absence of applicable standards is not a safety problem — it's a regulatory opportunity. The system is inherently safer than compressed H₂ vehicles that already have certification pathways.

---

## Environmental Profile

### Per 400 km Journey

```
CO₂ equivalent:
  Aluminum smelting (recycled, grid average): 1.45 kg CO₂/kg H₂
  H₂ produced: 3.876 kg
  Total CO₂: 5.62 kg per 400 km = 14.1 g CO₂/km

Comparison:
  Petrol vehicle (EU avg):     ~120 g CO₂/km
  BEV (EU grid avg):           ~50–70 g CO₂/km
  AL-H₂O (recycled Al):        ~14 g CO₂/km
  AL-H₂O (100% renewable Al):  ~2 g CO₂/km (electrolysis with solar)

Solid waste:   Zero (boehmite is commercially recovered)
Water output:  ~70 L pure water vapor (fuel cell exhaust, condensed)
GaIn:          Recovered and recycled, no waste stream
```

---

*Safety documentation by David Lee Wise (ROOT0) / TriPod LLC, 2024–2026.*  
*This document is a preliminary engineering hazard analysis. Full HAZOP, FMEA, and regulatory submission required before commercial deployment.*
