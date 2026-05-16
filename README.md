# V0 Bedfans Heatshield – Bedfan Mount with Heatshield for Voron V0 + Fysetc CNC Bed Carrier

[Deutsch](README.de.md) · **English**

> *Bedfans that leave your bed sensor alone.*
>
> Integrated bedfan mount with a heatshield on top, for the **Voron V0 with Fysetc CNC bed carrier**. Three printed parts: a holder for two 3010 blowers, an opposing Wago holder for the wiring, and a heatshield directly on top of the fans. The shield leaves a narrow side gap (~3 mm) below the heat mat, so the bedfan airflow exits sideways instead of blowing straight up into the centrally located bed thermistor.

![Hero](Images/hero.jpg)

> *Inspired by the Voron V0 design (CC-BY-SA 4.0). All parts in this mod are original designs.*

---

## ⚠️ Compatibility – read first

This mod only fits and only makes sense on:

- **Voron V0** with the **Fysetc CNC bed carrier** – the carrier's geometry (heat-mat cutout + side through-holes) is required for the sandwich mount described below
- **Heat mats with a centrally placed thermistor** – e.g. the Formbot V0 kit mat. If your thermistor sits at the edge of the heat mat, you don't have the problem this mod solves

If you run a different V0 bed carrier or your sensor isn't in the airflow path, this mod is the wrong solution.

---

## What this mod fixes

On a V0 with a Fysetc CNC bed carrier and a heat mat with a **centrally placed thermistor**, standard bedfan mounts blow the fan airflow straight up into the underside of the heat mat. The central thermistor sits right in that airflow and gets actively cooled – it reports a temperature far below the real bed temperature. The printer heats at 100 % trying to compensate, but the reported temperature doesn't rise, and Klipper aborts with `heater not heating at expected rate`.

This mod adds a **heatshield directly on top of the fans**. The shield closes off the upward path and deflects the airflow sideways. Roughly 3 mm of gap between the shield and the heat mat underside lets the air exit horizontally under the bed. The thermistor stays out of the airflow, the fans still recirculate chamber air – heatsoak on the V0 noticeably speeds up.

---

## Print Settings

| Setting | Value |
|---|---|
| Material | **PC PBT GF** required – ABS/ASA is borderline at this distance to the heat mat. Creed PC PBT GF works well; other PC-PBT-GF brands should be fine too. |
| Layer height | 0.2 mm |
| Walls | 4 |
| Top/bottom layers | 4 |
| Infill | 40 % |
| **Speed** | **Print slowly.** PC PBT GF doesn't like high speeds – stay conservative, don't use a standard ABS speed profile. |
| Nozzle | **Hardened steel or ruby required** – glass fiber is abrasive, a brass nozzle will wear out noticeably while printing these parts |
| Supports | **None needed** – geometry is support-free |

---

## What this mod does

### Three printed parts

- **Fan holder** sits centered in the heat-mat cutout of the Fysetc CNC bed carrier. Holds **2× 3010 blower fans, 24 V** (GDSTime recommended).
- **Wago holder** sits on the opposite side of the heat-mat cutout. Holds **4× Wago 221-412 (2-pole)** lever connectors. Two are used for the fans, two are left free for whatever wiring you need.
- **Heatshield** sits directly on top of the fans, closes off the upward airflow, leaves ~3 mm of side gap to the heat mat.

### Sandwich mount – one screw axis holds everything

The Fysetc CNC bed carrier has two **through-holes** (no threads) on the side of the heat-mat cutout. A single M3×20 screw enters **from the outside** through the Wago holder, passes through the carrier's through-hole, and threads into a heat-set insert in the fan holder. Two screws (one per side) clamp the Wago holder, the bed carrier, and the fan holder together as one sandwich. No tapping into aluminum required.

### Heatshield stack

The shield sits on the fans and is held by **8× M3×16 BHCS** that enter from below, through the fan holder, through the fans' corner mounting holes, into 8× M3 heat-set inserts in the shield. Four screws per fan – this single screw line holds both the fans in the holder and the shield on top in one move.

### Tight clearance

The gap between the shield and the heat-mat underside is ~3 mm. The material choice (PC PBT GF) is what makes this clearance work long-term – the shield stays dimensionally stable at the temperatures it sees right under a hot bed.

---

## Bill of Materials

### Hardware

| Part | Qty | Note |
|---|---|---|
| 3010 blower fan, 24 V | 2 | **GDSTime recommended** |
| Wago 221-412 (2-pole) | 4 | 2 for the fans, 2 free for your own wiring |

### Screws

| Type | Qty | Use |
|---|---|---|
| M3×20 button head (BHCS, ISO 7380) | 2 | sandwich mount – Wago holder ↔ bed carrier ↔ fan holder (one per side) |
| M3×16 button head (BHCS, ISO 7380) | 8 | heatshield stack – from below, through the fan holder, through the fans, into the shield inserts (4 per fan) |

### Heat-Set Inserts

| Position | Qty |
|---|---|
| M3 in the fan holder (side) | 2 |
| M3 in the heatshield (top, 4 per fan position) | 8 |
| **M3 heat-set inserts total** | **10** |

Voron-standard M3 brass inserts, OD ≈ 5 mm, L ≈ 4 mm.

### Required on the printer

| Part | Note |
|---|---|
| **Fysetc CNC bed carrier** | Provides the two side through-holes for the sandwich mount. The mod won't fit other carriers without modification. |
| **Heat mat with a centrally placed thermistor** | The shield only makes sense if the thermistor sits in the path of the bedfan airflow |

---

## Assembly

### Preparation

1. Press the heat-set inserts:
   - **2× M3** into the side of the fan holder (for the sandwich mount)
   - **8× M3** into the heatshield (four per fan position, from the top side of the shield)
2. Place the **2× 3010 fans** into the fan holder.

### Heatshield stack

3. Place the heatshield on top of the fans. Align the holes.
4. From **below**, drive **8× M3×16 BHCS** up through the fan holder, through each fan's corner holes, into the shield's inserts. Tighten evenly. The fans are now clamped between the holder and the shield in one sandwich.

### Mounting to the bed carrier

5. Route the fan wires towards the side where the Wago holder will sit.
6. Place the **fan holder** centered in the heat-mat cutout of the Fysetc CNC bed carrier.
7. Place the **Wago holder** on the opposite side of the cutout.
8. From the outside of the Wago holder, drive **2× M3×20 BHCS** (one per side) through the Wago holder, through the bed carrier's through-hole, and into the M3 insert in the fan holder. Tighten both sides evenly.
9. Insert the **4× Wago 221-412** connectors into their slots in the Wago holder.

> After mounting, slowly home Z and verify the shield clears the heat mat. The intended gap is ~3 mm – it's tight, but designed in.

---

## Wiring

**4× Wago 221-412 (2-pole), 24 V** for the fans.

- The two 3010 fans connect in parallel via two of the Wagos (one for V+, one for GND), then go to any free 24 V fan output on the printer.
- The remaining two Wagos are unused on purpose – use them for whatever else you want to clean up near the bed (heat-mat wiring, sensor lines, …). That's a setup decision, not part of the mod.

No specific connector, no Klipper config snippet – whatever your printer setup expects is what you wire up.

---

## Print Files

In the [`/3MF`](3MF/) folder – **1 file:**

| File | Contents |
|---|---|
| `V0-Bedfans-Heatshield.3mf` | fan holder + Wago holder + heatshield (all three parts in one file) |

---

## Source CAD

- **STEP:** [`/STEP`](STEP/) – editable in any CAD tool (Fusion, FreeCAD, OnShape, SolidWorks)
- **Fusion 360 native:** [`/CAD`](CAD/) – with full parametric tree
- **No STL** – the 3MF is slicer-independent and contains all parts cleanly

---

## License

[**CC-BY-SA 4.0**](LICENSE) – the Voron ecosystem standard.

Forks, remixes and reposts welcome – but please under the same license and with a reference back to the original.

---

## Credits

- **Design:** Wh'sFortune
- **Inspired by:** [Voron V0](https://docs.vorondesign.com) (CC-BY-SA 4.0)
- **Companion mods:** [Aegis Chamber](https://github.com/WhsFortune/Projekt-Aegis) (insulated panel set for the V0.2) · [Filtra](https://github.com/WhsFortune/filtra) (in-chamber recirculating filter for the V0)

Issues and feedback welcome on GitHub.
