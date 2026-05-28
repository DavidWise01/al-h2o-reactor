# BOM.md
## AL-H₂O Reactor — Bill of Materials (Reference Design, Passenger Vehicle)

---

> **Note:** These are engineering-estimate costs for a low-volume prototype build.  
> Production scale pricing (>10,000 units/year) would be 30–60% lower on most items.  
> All prices in USD as of 2025.

---

## Section 1: Reaction System

| # | Component | Spec | Supplier (example) | Unit Cost | Qty | Total |
|---|-----------|------|--------------------|-----------|-----|-------|
| 1.1 | Reaction Chamber | 316L SS, 12L, rated 5 bar | Custom fabrication | $800 | 1 | $800 |
| 1.2 | Chamber flanges | 316L SS, 1.4" dia, 8-bolt | Custom | $120 | 2 | $240 |
| 1.3 | Borosilicate viewport | 80mm dia, 4 bar rated | Sight Glass Depot | $95 | 1 | $95 |
| 1.4 | Thermal jacket (silicone blanket) | 200W, 12V, 40×40cm | Omega Engineering | $65 | 1 | $65 |
| 1.5 | PT100 sensors (chamber) | 4× axial, 0–150°C | Omega / RS Components | $18 | 4 | $72 |
| 1.6 | PRV (pressure relief valve) | 2.5 bar, ¾" NPT, 316 SS | Swagelok R3A | $145 | 1 | $145 |
| 1.7 | Burst disk (backup) | 4 bar, ¾" NPT | Fike Corp | $55 | 1 | $55 |
| 1.8 | Mineral wool insulation | 25mm, 0.5 m² sheet | Rockwool | $22 | 2 | $44 |
| 1.9 | Structural frame (chamber mount) | 6061 aluminum extrusion | McMaster-Carr | $85 | 1 | $85 |
| | | | | **Subtotal** | | **$1,601** |

---

## Section 2: Pellet Feed System

| # | Component | Spec | Supplier | Unit Cost | Qty | Total |
|---|-----------|------|----------|-----------|-----|-------|
| 2.1 | Pellet hopper cartridge (shell) | HDPE, 40L, bayonet lock | Custom injection mold | $180 | 1 | $180 |
| 2.2 | Twin-screw auger assembly | 316 SS, 12 kg/hr max | Custom / Flexicon | $450 | 1 | $450 |
| 2.3 | Auger drive motor | 12V DC brushless, 50W | Maxon EC-flat | $185 | 1 | $185 |
| 2.4 | Auger motor controller | PWM, 0–100% throttle | Roboteq BDC2460 | $120 | 1 | $120 |
| 2.5 | Shaft seal (dry/wet side) | PTFE lip seal, 316 shaft | Parker | $35 | 2 | $70 |
| 2.6 | Pellet level sensor | Capacitive, HDPE-compatible | Gems Sensors | $55 | 1 | $55 |
| 2.7 | Bayonet lock ring | Anodized 6061 Al | Custom CNC | $45 | 2 | $90 |
| 2.8 | Cartridge O-ring seal | Viton, 80mm ID | Parker | $8 | 3 | $24 |
| | | | | **Subtotal** | | **$1,174** |

---

## Section 3: Water & Catalyst System

| # | Component | Spec | Supplier | Unit Cost | Qty | Total |
|---|-----------|------|----------|-----------|-----|-------|
| 3.1 | Water storage tank | HDPE, 25L, potable-safe | Ronco / custom | $45 | 1 | $45 |
| 3.2 | Water pump | 12V centrifugal, 8 L/min, 2 bar | Shurflo 4048 | $75 | 1 | $75 |
| 3.3 | Pre-filter (50 micron) | 316 SS housing, polyester element | Parker Hannifin | $35 | 1 | $35 |
| 3.4 | Fine filter (5 micron) | Polypropylene housing + element | Pentek | $22 | 1 | $22 |
| 3.5 | Water solenoid valve | 12V NC, ½" NPT, 316 SS | Bürkert 6013 | $88 | 1 | $88 |
| 3.6 | Water level sensor | Ultrasonic, 25L tank | Gems Sensors | $42 | 1 | $42 |
| 3.7 | Catalyst reservoir | 316 SS, 500mL, sealed | Swagelok | $95 | 1 | $95 |
| 3.8 | Catalyst micropump | Peristaltic, 0.1–2 mL/min | Cole-Parmer | $165 | 1 | $165 |
| 3.9 | Imidazole (concentrate) | Industrial grade, 100g | Sigma-Aldrich | $45 | 1 | $45 |
| 3.10 | Water plumbing (¼" & ½" SS tubing) | 316 SS, 3m each | Swagelok | $35 | 4 | $140 |
| 3.11 | Push-fit fittings (assorted) | 316 SS | Swagelok | $12 | 20 | $240 |
| | | | | **Subtotal** | | **$992** |

---

## Section 4: H₂ Separation & Delivery

| # | Component | Spec | Supplier | Unit Cost | Qty | Total |
|---|-----------|------|----------|-----------|-----|-------|
| 4.1 | Hollow-fiber H₂ membrane separator | Polysulfone, 0.5 m² effective | Compact Membrane Systems | $1,200 | 1 | $1,200 |
| 4.2 | Membrane housing | 316 SS, 4 bar rated | Custom / off-shelf | $180 | 1 | $180 |
| 4.3 | H₂ delivery tubing | 316 SS ¼" OD, H₂-rated, 2m | Swagelok | $28 | 3 | $84 |
| 4.4 | H₂ flow sensor | Thermal mass, 0–50 slpm | Alicat M-series | $320 | 1 | $320 |
| 4.5 | H₂ shut-off solenoid | 12V NC, 316 SS, H₂ service | Bürkert 6011 | $145 | 1 | $145 |
| 4.6 | H₂ sensor (LEL) | Catalytic bead, 0–100% LEL | City Technology FC | $85 | 2 | $170 |
| 4.7 | H₂ alarm controller | Dual-channel, relay output | GFG EC910 | $220 | 1 | $220 |
| | | | | **Subtotal** | | **$2,319** |

---

## Section 5: GaIn Recovery System

| # | Component | Spec | Supplier | Unit Cost | Qty | Total |
|---|-----------|------|----------|-----------|-----|-------|
| 5.1 | GaIn alloy (initial charge) | 75% Ga / 25% In, 300g | Rotometals | $380 | 1 | $380 |
| 5.2 | GaIn reservoir | 316 SS, 500mL | Swagelok | $95 | 1 | $95 |
| 5.3 | GaIn recirculation pump | Peristaltic, chemical resistant | Cole-Parmer | $185 | 1 | $185 |
| 5.4 | Settling column (separation) | 316 SS, 2L, with drain | Custom | $120 | 1 | $120 |
| 5.5 | Temperature control (GaIn stays liquid) | 12V PTC heater, 20W | Minco | $45 | 1 | $45 |
| | | | | **Subtotal** | | **$825** |

---

## Section 6: PEM Fuel Cell Stack

| # | Component | Spec | Supplier | Unit Cost | Qty | Total |
|---|-----------|------|----------|-----------|-----|-------|
| 6.1 | PEM fuel cell stack | 30 kW, 200–400V output | Ballard FCGen-LCS | $8,500 | 1 | $8,500 |
| 6.2 | Air compressor (cathode) | Centrifugal, 1.5 bar, 12V | Mann+Hummel | $650 | 1 | $650 |
| 6.3 | Air humidifier (cathode) | Membrane type | PermaPure | $280 | 1 | $280 |
| 6.4 | Coolant pump (FC cooling) | 12V, 8 L/min | Bosch | $95 | 1 | $95 |
| 6.5 | DC-DC converter (FC to bus) | 200–400V → 400V, 98% eff | Vicor | $1,200 | 1 | $1,200 |
| 6.6 | Stack monitoring board | Cell voltage monitoring, 80 cells | Analog Devices | $350 | 1 | $350 |
| | | | | **Subtotal** | | **$11,075** |

---

## Section 7: Boehmite Collection

| # | Component | Spec | Supplier | Unit Cost | Qty | Total |
|---|-----------|------|----------|-----------|-----|-------|
| 7.1 | Boehmite collection tank | HDPE, 15L, bayonet swap | Custom | $65 | 1 | $65 |
| 7.2 | Slurry pump | Peristaltic, PTFE, 2 L/min | Verderflex | $280 | 1 | $280 |
| 7.3 | Level sensor (boehmite tank) | Float switch, HDPE-safe | Gems | $28 | 1 | $28 |
| 7.4 | Full-tank alarm + display | 12V LED + buzzer | — | $12 | 1 | $12 |
| | | | | **Subtotal** | | **$385** |

---

## Section 8: Control & Safety Electronics

| # | Component | Spec | Supplier | Unit Cost | Qty | Total |
|---|-----------|------|----------|-----------|-----|-------|
| 8.1 | Main controller (ECU) | ARM Cortex-M4, CAN bus | STMicro STM32F4 | $45 | 1 | $45 |
| 8.2 | G-sensor (crash detect) | 3-axis, ±50g | Bosch BMA400 | $8 | 2 | $16 |
| 8.3 | Emergency stop relay | 12V, 40A, automotive grade | Tyco | $12 | 3 | $36 |
| 8.4 | Thermal fuse (physical) | 85°C, irreversible | Bourns | $4 | 3 | $12 |
| 8.5 | CAN bus harness | Automotive shielded | — | $85 | 1 | $85 |
| 8.6 | Driver display | 4" LCD, CAN-fed | Nextion | $55 | 1 | $55 |
| 8.7 | Power distribution board | 12V, 10-channel fused | — | $65 | 1 | $65 |
| 8.8 | Wiring loom (reactor zone) | ATEX-rated, 10m | Lapp Kabel | $120 | 1 | $120 |
| | | | | **Subtotal** | | **$434** |

---

## Section 9: Structural & Mechanical

| # | Component | Spec | Supplier | Unit Cost | Qty | Total |
|---|-----------|------|----------|-----------|-----|-------|
| 9.1 | Chassis mounting frame | 6061 Al welded, powder coat | Custom fab | $350 | 1 | $350 |
| 9.2 | Vibration isolators | Natural rubber, M8 | Paulstra | $12 | 8 | $96 |
| 9.3 | Fasteners (M6–M10 316 SS) | Full kit | McMaster-Carr | $65 | 1 | $65 |
| 9.4 | Pipe clamps and brackets | 316 SS, assorted | McMaster-Carr | $45 | 1 | $45 |
| 9.5 | Thread seal tape (PTFE) | H₂ service rated, yellow | — | $8 | 5 | $40 |
| | | | | **Subtotal** | | **$596** |

---

## Cost Summary

```
Section                            Cost
────────────────────────────────────────
1. Reaction System               $1,601
2. Pellet Feed System            $1,174
3. Water & Catalyst System         $992
4. H₂ Separation & Delivery     $2,319
5. GaIn Recovery                   $825
6. PEM Fuel Cell Stack          $11,075
7. Boehmite Collection             $385
8. Control & Safety Electronics    $434
9. Structural & Mechanical         $596
────────────────────────────────────────
TOTAL (prototype, single unit): $19,401

Engineering labour (200 hrs @ $85/hr):  $17,000
────────────────────────────────────────
Complete prototype build:        ~$36,400
```

---

## Production Cost Projection (10,000 units/year)

```
Reaction system:         $600    (custom → high-volume fab)
Pellet feed:             $350    (auger → injection mold + high-vol motor)
Water/catalyst:          $280    (commodity pumps at volume)
H₂ separation:           $400    (membrane module at volume)
GaIn recovery:           $250    (simplified station-side)
Fuel cell (30 kW):     $3,000    (2025 trajectory: ~$100/kW @ volume)
Boehmite collection:     $100
Electronics:             $150
Structure:               $200
────────────────────────────────
Production COGS estimate: ~$5,330 per unit

Target retail:           ~$8,000–$12,000 per system installed
```

---

## Consumables Per 400 km

```
Aluminum pellets (36 kg @ recycled price $0.40/kg):  $14.40
Imidazole catalyst makeup:                            $0.50
Water (if purchased, 72L):                            $0.05
GaIn makeup (5% loss × $300/kg recovery):             $2.70
────────────────────────────────────────────────────────────
Gross consumable cost per 400 km:                    $17.65

Boehmite byproduct credit (80 kg @ $0.50/kg):       -$40.00
────────────────────────────────────────────────────────────
NET consumable cost per 400 km:                    -$22.35 (POSITIVE)
```

> At current recycled aluminum and boehmite prices, the byproduct revenue **exceeds** the input cost. The fuel is profitable before accounting for the cartridge swap service margin.

---

*Bill of materials by David Lee Wise (ROOT0) / TriPod LLC, 2024–2026.*  
*Prices are reference estimates, subject to supplier negotiation, volume discounts, and market fluctuations.*
