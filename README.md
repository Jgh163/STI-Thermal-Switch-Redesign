# STI-Thermal-Switch-Redesign

A novel approach to adjustable temperature sensing for freeze protection — a fail-safe electronic switch with **no-neutral 2-wire design**.

---

## 🔲 Interactive 3D Model

**[▶ View Interactive 3D PCB Model](https://jgh163.github.io/STI-Thermal-Switch-Redesign/)**

> Drag to rotate · Scroll to zoom · Full color PCB with components

---

## What This Does

A 2-wire device wired in series with a 120VAC relay coil. It monitors temperature and controls whether the relay energizes:

- **Warm** (above setpoint) → TRIAC fires → relay pulls in → heater OFF
- **Cold** (below setpoint) → TRIAC off → relay drops out → heater ON

No neutral wire required. The entire 5V logic rail is powered via a capacitive dropper (X2-rated, fails open).

---

## Key Specs

| Parameter | Value |
|---|---|
| Supply | 120VAC, 2-wire series |
| Logic Rail | 5.1V DC (capacitive dropper) |
| Control Device | Z0103MN TRIAC (600V, 1A) |
| Comparator | TLV3691 (75nA quiescent) |
| Sensor | NTC Thermistor (10kΩ) |
| Quiescent Draw | 0.33 mA |
| Neutral Required | **No** |

---

## Design Highlights

- **TRIAC latching delay** (~0.75ms) exploited as a charging window for C3
- **X2 safety film cap** on mains — fails open by design

---

## Files

| File | Description |
|---|---|
| `board.glb` | 3D model (GLTF/GLB) for web viewer |
| `index.html` | GitHub Pages interactive 3D viewer |

---

## Repository

**GitHub:** [Jgh163/STI-Thermal-Switch-Redesign](https://github.com/Jgh163/STI-Thermal-Switch-Redesign)  
**Live 3D Viewer:** [jgh163.github.io/STI-Thermal-Switch-Redesign](https://jgh163.github.io/STI-Thermal-Switch-Redesign/)
