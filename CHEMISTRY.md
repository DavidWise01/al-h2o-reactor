# CHEMISTRY.md
## AL-H₂O Reactor — Complete Reaction Chemistry

---

## Primary Reaction

```
2 Al  +  6 H₂O  ──[imidazole, GaIn]──▶  2 Al(OH)₃  +  3 H₂↑  +  ΔH
```

**Reaction type:** Exothermic hydrolysis  
**Conditions:** Aqueous, ~50°C optimal, atmospheric pressure  
**Catalyst:** Imidazole (C₃H₄N₂) + gallium-indium alloy (GaIn)

---

## Molecular Weights

| Species | Formula | Molar Mass (g/mol) |
|---------|---------|-------------------|
| Aluminum | Al | 26.982 |
| Water | H₂O | 18.015 |
| Hydrogen | H₂ | 2.016 |
| Aluminum hydroxide | Al(OH)₃ | 78.004 |
| Boehmite | AlOOH | 59.989 |
| Imidazole | C₃H₄N₂ | 68.077 |

---

## Stoichiometry

**From the balanced equation: `2Al + 6H₂O → 2Al(OH)₃ + 3H₂`**

### Per kg of aluminum:

```
moles Al = 1000 g / 26.982 g/mol = 37.06 mol/kg

H₂ produced = 37.06 × (3/2) = 55.59 mol H₂
             = 55.59 × 2.016 g/mol = 112.1 g/kg Al
             = 0.1121 kg H₂ per kg Al

H₂O consumed = 37.06 × 3 = 111.18 mol H₂O
              = 111.18 × 18.015 = 2002.5 g/kg Al
              = ~2.0 kg water per kg aluminum

Al(OH)₃ produced = 37.06 mol × 78.004 g/mol = 2890.8 g/kg Al
Boehmite (AlOOH) = 37.06 mol × 59.989 g/mol = 2223.7 g/kg Al
```

### For a full 36 kg cartridge:

```
H₂ produced    = 36 × 0.1121 × 0.96 (yield) = 3.876 kg H₂
H₂O consumed   = 36 × 2.0 = 72 kg ≈ 72 liters (carried or ambient)
Boehmite yield = 36 × 2.224 = 80.1 kg (collected, sellable)
```

---

## Thermodynamics

### Enthalpy of Reaction

```
ΔH = −418 kJ per mol Al  (exothermic — heat released)

Per kg Al:
  ΔH = 37.06 mol/kg × 418 kJ/mol = 15,491 kJ/kg Al
     = 15.49 MJ/kg Al
     = 4.30 kWh/kg Al (thermal)
```

### Hydrogen Energy Content

```
H₂ Higher Heating Value (HHV): 141.8 MJ/kg
H₂ Lower Heating Value (LHV):  120.0 MJ/kg  ← used for PEM calculations

Per kg Al (at 96% yield):
  H₂ = 0.1077 kg
  Energy (LHV) = 0.1077 × 120.0 = 12.92 MJ/kg Al

Comparison to gasoline:
  Gasoline LHV: ~44 MJ/kg
  Al (H₂ output, LHV): 12.92 MJ/kg Al → but Al is 3× denser than gasoline
  Volumetric: ~34.8 MJ/L Al vs ~32 MJ/L gasoline  ← comparable
```

### Energy Balance per kg Al

```
Chemical energy stored in H₂ (LHV):       12.92 MJ
Reaction heat released (exothermic):       15.49 MJ
PEM fuel cell conversion (62%):             8.01 MJ → electricity
Motor conversion (95%):                     7.61 MJ → shaft power
Net chain efficiency:                      ~55–60%
```

---

## The Catalyst System

### Gallium-Indium Alloy (GaIn)

Aluminum's natural oxide layer (Al₂O₃) forms within milliseconds of exposure to air and acts as a passivation barrier that prevents water from reaching bare metal.

GaIn alloy (typically ~75% Ga, 25% In by weight) is a liquid metal at room temperature that:
1. Penetrates aluminum grain boundaries
2. Disrupts and dissolves the Al₂O₃ passivation layer
3. Exposes fresh aluminum surface to water continuously throughout reaction

**Recovery:** GaIn does not bond with aluminum products (Al(OH)₃ / boehmite). It precipitates as a distinct liquid metal phase. MIT finding: salt ions in seawater (Na⁺, Cl⁻, Mg²⁺) preferentially complex with boehmite surface, helping GaIn separate cleanly for recovery.

**Dosage:** ~0.5–2% by weight of aluminum pellets  
**Recovery rate:** >95% per cycle  
**Cost:** Gallium ~$200/kg, Indium ~$150/kg — high but recycled nearly completely

### Imidazole Catalyst (C₃H₄N₂)

Imidazole is the bicyclic nitrogen heterocycle that forms the core of histidine, histamine, and is the active subunit of caffeine (via methylation to form methylimidazole components in purine rings).

**Mechanism:** Imidazole acts as a bifunctional proton transfer catalyst in the hydrolysis step:
- Accepts proton from H₂O at N-1 position
- Donates proton to nascent Al-OH intermediate
- Regenerates after each cycle (catalytic, not consumed)

**Effect on kinetics:**
```
Without catalyst (plain seawater):    ~2 hours to completion
With imidazole (1–5 mM):             ~5 minutes to completion
Acceleration factor:                   24×
```

**Temperature dependence (Arrhenius model):**
```
Optimal temperature: ~50°C
Effective range:     10–70°C
Below 10°C:          significantly reduced rate (<0.5× nominal)
Above 70°C:          catalyst degradation begins
```

**Dosage:** 1–5 mM in the reaction water  
**Cost:** Imidazole ~$5–15/kg industrial grade; trace quantities per batch  
**Safety:** Low toxicity, not a controlled substance

---

## Full Reaction with Boehmite Dehydration

The primary product Al(OH)₃ partially dehydrates under reaction conditions:

```
Step 1: 2Al + 6H₂O → 2Al(OH)₃ + 3H₂↑        (primary hydrolysis)
Step 2: Al(OH)₃ → AlOOH + H₂O                 (dehydration to boehmite, 80–100°C)
```

In the reactor, a mix of Al(OH)₃ and AlOOH (boehmite) is produced depending on temperature. Both are commercially valuable — boehmite is the more desirable form for semiconductor and catalyst applications.

---

## Fuel Cell Reaction (PEM)

At the fuel cell, the generated H₂ combines with atmospheric oxygen:

```
2H₂ + O₂ → 2H₂O + electrical energy + heat

Efficiency (PEM, ambient conditions): 60–65%
Operating temp: 60–80°C (PEM)
Catalyst: Platinum on carbon (anode and cathode)
Exhaust: Pure water vapor + low-grade heat
```

The only tailpipe emission is water.

---

## Competitive Chemistry Comparison

| Method | H₂ Cost | CO₂/kg H₂ | Infrastructure | Energy Source |
|--------|---------|-----------|----------------|---------------|
| Steam methane reforming (SMR) | $1–2/kg | 9–12 kg | Existing, fossil | Natural gas |
| Electrolysis (grid) | $4–6/kg | ~20 kg | Build-out needed | Electricity |
| Electrolysis (solar) | $3–5/kg | ~1 kg | Build-out needed | Solar |
| AL-H₂O (recycled Al) | ~$9/kg | 1.45 kg | Al scrap + any water | Aluminum chemical energy |
| AL-H₂O (virgin Al) | ~$15/kg | 8–12 kg | Same | Smelting electricity |

> **Key insight:** AL-H₂O with recycled aluminum has a lower CO₂ footprint than grid electrolysis, no new infrastructure requirement, and the byproduct has a positive market value that offsets cost.

---

## Water Chemistry Notes

### Seawater vs. Freshwater

MIT testing showed seawater is *preferred* over freshwater:

- Cl⁻ ions improve GaIn recovery (forms distinct layer)
- Na⁺ and Mg²⁺ ions assist boehmite flocculation
- Slightly elevated reaction temperature in practice (thermal buffer from dissolved salts)
- No RO or treatment needed — reaction is not salt-sensitive

### Brackish / Gray Water

Any water source with conductivity >1 mS/cm is effective. Industrial wastewater, agricultural runoff, and even brackish groundwater all work. This is a key advantage for land-locked deployments.

---

## Byproduct Markets

### Boehmite (AlOOH)

- **Semiconductor polishing:** CMP slurry abrasive — $800–$2,500/ton
- **Fire retardant filler:** aluminum hydroxide in plastics/composites — $200–$500/ton
- **Catalyst support:** petroleum refining, Claus process — $400–$800/ton
- **Technical ceramics:** thermal management substrates — $600–$1,500/ton

**At 80 kg boehmite per 36 kg Al cartridge, and blended market price ~$500/ton:**
```
Revenue offset = 0.080 ton × $500/ton = $40 per cartridge
Fuel cost (36 kg Al @ $9/kg H₂ equivalent) = ~$324
Net effective cost after byproduct credit = ~$284 per 400 km
```

---

*Chemistry reference compiled by David Lee Wise (ROOT0) / TriPod LLC, 2024–2026.*  
*Primary sources: MIT DMSE publications, Uddin et al. 2023, GaIn prior art in Al activation.*
