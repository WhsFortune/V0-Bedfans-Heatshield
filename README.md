# V0 Bedfans Heatshield – Bedfan Mount with Heatshield for Voron V0 + Fysetc CNC Bed Carrier

[Deutsch](README.de.md) · **English**

> *Bedfans that leave your bed sensor alone.*

![Hero](Images/hero.jpg)

Bedfan mount with a heatshield on top, for the **Voron V0 with Fysetc CNC bed carrier**. Three printed parts: a holder for two 3010 blowers, an opposing Wago holder, and a heatshield directly on the fans. The shield closes off the upward airflow and leaves ~3 mm of side gap to the heat mat, so the bedfan air exits sideways instead of blowing straight up against a centrally placed bed thermistor.

> *Inspired by the Voron V0 design (CC-BY-SA 4.0). All parts in this mod are original designs.*

---

## ⚠️ Compatibility

Only fits and only makes sense on:

- **Voron V0** with the **Fysetc CNC bed carrier**
- **Heat mat with a centrally placed thermistor** (e.g. Formbot V0 kit mat)

If your thermistor sits at the edge of the heat mat, you don't have the problem this mod solves.

---

## The problem

Standard bedfan mounts blow air straight up against the underside of the heat mat. A centrally placed thermistor sits right in that airflow and reports a temperature well below the real bed temperature. The printer heats at 100 % but the reading doesn't rise, and Klipper aborts with `heater not heating at expected rate`.

This mod deflects the airflow sideways with a heatshield directly on the fans. Thermistor stays out of the airflow, the bed reads correctly, and the fans still recirculate chamber air – heatsoak on the V0 noticeably speeds up.

---

## Print Settings

| Setting | Value |
|---|---|
| Material | **PC PBT GF** required – ABS/ASA is borderline this close to the heat mat. Creed PC PBT GF works well. |
| Layer height | 0.2 mm |
| Walls | 4 |
| Top/bottom layers | 4 |
| Infill | 40 % |
| Speed | **Print slowly** – PC PBT GF doesn't like high speeds |
| Supports | None needed – geometry is support-free |

---

## Bill of Materials

### Hardware

| Part | Qty |
|---|---|
| 3010 blower fan, 24 V (GDSTime recommended) | 2 |
| Wago 221-412 (2-pole) | 4 |

### Screws

| Type | Qty | Use |
|---|---|---|
| M3×20 BHCS (ISO 7380) | 2 | sandwich mount – one per side |
| M3×16 BHCS (ISO 7380) | 8 | heatshield stack – 4 per fan |

### Heat-Set Inserts

| Position | Qty |
|---|---|
| M3 in the fan holder (side) | 2 |
| M3 in the heatshield (top) | 8 |

---

## Assembly

1. Press the heat-set inserts: 2× M3 into the side of the fan holder, 8× M3 into the heatshield (four per fan position).
2. Place the 2× 3010 fans into the fan holder.
3. Lay the heatshield on top of the fans and drive **8× M3×16 BHCS from below** up through the fan holder, through the fans' corner holes, into the shield's inserts. This single stack holds the fans in the holder and the shield on top.
4. Place the fan holder centered in the heat-mat cutout of the Fysetc CNC bed carrier and the Wago holder on the opposite side.
5. Drive **2× M3×20 BHCS** from the outside of the Wago holder, through the carrier's side through-hole, into the M3 insert in the fan holder. One per side. This sandwich clamps the Wago holder, the bed carrier and the fan holder together – no tapping into aluminum.
6. Insert the 4× Wago 221-412 into the slots in the Wago holder.

After mounting, slowly home Z and verify the shield clears the heat mat. Intended gap is ~3 mm.

---

## Wiring

The two 3010 fans connect to any free 24 V fan output on the printer via the Wagos.

---

## Files

- [`/3MF`](3MF/) – `V0-Bedfans-Heatshield.3mf` (all three parts in one file)
- [`/STEP`](STEP/) – editable in any CAD
- [`/CAD`](CAD/) – Fusion 360 native with full parametric tree

---

## License

[**CC-BY-SA 4.0**](LICENSE) – the Voron ecosystem standard. Forks and remixes welcome under the same license.

---

## Credits

- **Design:** Wh'sFortune
- **Inspired by:** [Voron V0](https://docs.vorondesign.com) (CC-BY-SA 4.0)
- **Companion mods:** [Aegis Chamber](https://github.com/WhsFortune/Projekt-Aegis) · [Filtra](https://github.com/WhsFortune/filtra)

Issues and feedback welcome on GitHub.
