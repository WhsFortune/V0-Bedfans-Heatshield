# V0 Bedfans Heatshield – Bedfan-Mount mit Hitzeschild für Voron V0 + Fysetc CNC Bedträger

**Deutsch** · [English](README.md)

> *Bedfans, die deinen Bett-Sensor in Ruhe lassen.*
>
> Integrierter Bedfan-Mount mit aufliegendem Hitzeschild, für den **Voron V0 mit Fysetc CNC Bedträger**. Drei Druckteile: ein Halter für zwei 3010er Blower, ein gegenüberliegender Wago-Halter für die Verkabelung, und ein Hitzeschild direkt auf den Lüftern. Der Schild lässt einen schmalen seitlichen Spalt (~3 mm) zur Heizmatten-Unterseite frei – die Luft der Bedfans tritt seitlich aus, statt senkrecht nach oben gegen den mittig sitzenden Bett-Thermistor zu blasen.

![Hero](Images/hero.jpg)

> *Inspired by the Voron V0 design (CC-BY-SA 4.0). All parts in this mod are own designs.*

---

## ⚠️ Kompatibilität – zuerst lesen

Dieser Mod passt und sinnvoll ist er nur auf:

- **Voron V0** mit **Fysetc CNC Bedträger** – die Geometrie des Trägers (Heizmatten-Aussparung + seitliche Durchgangsbohrungen) ist Voraussetzung für die unten beschriebene Sandwich-Befestigung
- **Heizmatten mit mittig sitzendem Thermistor** – z.B. die Formbot V0-Kit-Matte. Wenn dein Thermistor am Rand der Heizmatte sitzt, hast du das Problem, das dieser Mod löst, gar nicht

Wenn du einen anderen V0-Bedträger fährst oder der Sensor nicht im Luftstrom sitzt, ist dieser Mod die falsche Lösung.

---

## Was dieser Mod löst

Auf einem V0 mit Fysetc CNC Bedträger und einer Heizmatte mit **mittig sitzendem Thermistor** blasen Standard-Bedfan-Mounts den Luftstrom direkt nach oben gegen die Heizmatten-Unterseite. Der mittige Thermistor sitzt genau in diesem Luftstrom und wird aktiv heruntergekühlt – er meldet eine Temperatur deutlich unter der tatsächlichen Bett-Temperatur. Der Drucker heizt mit 100 % gegen, die gemessene Temperatur steigt aber nicht, und Klipper bricht ab mit `heater not heating at expected rate`.

Dieser Mod setzt einen **Hitzeschild direkt auf die Lüfter**. Der Schild schließt nach oben ab und lenkt den Luftstrom seitlich um. Mit etwa 3 mm Spalt zwischen Schild und Heizmatten-Unterseite tritt die Luft horizontal unter dem Bett aus. Der Thermistor bleibt aus dem Luftstrom raus, die Lüfter wälzen trotzdem die Kammerluft um – der Heatsoak im V0 wird spürbar beschleunigt.

---

## Print-Settings

| Bereich | Wert |
|---|---|
| Material | **PC PBT GF** erforderlich – ABS/ASA ist bei dem Abstand zur Heizmatte grenzwertig. Creed PC PBT GF funktioniert gut; andere PC-PBT-GF-Marken sollten auch passen. |
| Layer-Höhe | 0,2 mm |
| Wände | 4 |
| Top/Bottom Layers | 4 |
| Infill | 40 % |
| **Druckgeschwindigkeit** | **Eher langsam fahren.** PC PBT GF mag keine hohen Speeds – konservativ bleiben, nicht das Standard-ABS-Profil durchziehen. |
| Düse | **Hardened Steel oder Ruby zwingend** – die Glasfaser ist abrasiv, eine Messing-Düse wird beim Druck der drei Teile messbar ausgeschliffen |
| Stützen | **Keine nötig** – Geometrie ist support-frei |

---

## Was dieser Mod macht

### Drei Druckteile

- **Fan-Halter** sitzt mittig in der Heizmatten-Aussparung des Fysetc CNC Bedträgers. Nimmt **2× 3010 Blower Fans, 24 V** auf (GDSTime empfohlen).
- **Wago-Halter** sitzt gegenüberliegend auf der anderen Seite der Aussparung. Nimmt **4× Wago 221-412 (2-polig)** Hebelklemmen auf. Zwei werden für die Lüfter genutzt, zwei bleiben frei für eigene Verkabelungs-Zwecke.
- **Hitzeschild** liegt direkt auf den Lüftern, schließt nach oben ab und lässt ~3 mm seitlichen Spalt zur Heizmatte.

### Sandwich-Befestigung – eine Schraubenachse hält alles

Der Fysetc CNC Bedträger hat seitlich an der Heizmatten-Aussparung zwei **Durchgangsbohrungen** (kein Gewinde). Je eine M3×20 Schraube geht **von außen** durch den Wago-Halter, durch die Bedträger-Bohrung, in ein Heat-Insert im Fan-Halter. Zwei Schrauben (eine pro Seite) klemmen Wago-Halter, Bedträger und Fan-Halter in einem Sandwich zusammen. Kein Gewindeschneiden ins Aluminium nötig.

### Hitzeschild-Stack

Der Schild liegt auf den Lüftern und wird mit **8× M3×16 BHCS** gehalten, die von unten durch den Fan-Halter, durch die Eck-Bohrungen der Lüfter, in 8× M3 Heat-Inserts im Schild greifen. Vier Schrauben pro Lüfter – eine einzige Schrauben-Linie hält damit gleichzeitig die Lüfter im Halter und den Schild oben drauf.

### Enge Toleranz

Der Spalt zwischen Schild und Heizmatten-Unterseite liegt bei ~3 mm. Die Materialwahl (PC PBT GF) ist der Grund, warum diese Toleranz langfristig stabil bleibt – der Schild bleibt bei den Temperaturen direkt unter dem heißen Bett formstabil.

---

## Bill of Materials

### Hardware

| Position | Menge | Hinweis |
|---|---|---|
| 3010 Blower Fan, 24 V | 2 | **GDSTime empfohlen** |
| Wago 221-412 (2-polig) | 4 | 2 für die Lüfter, 2 bleiben frei für eigene Verkabelung |

### Schrauben

| Typ | Menge | Verwendung |
|---|---|---|
| M3×20 Linsenkopf (BHCS, ISO 7380) | 2 | Sandwich-Befestigung – Wago-Halter ↔ Bedträger ↔ Fan-Halter (eine pro Seite) |
| M3×16 Linsenkopf (BHCS, ISO 7380) | 8 | Hitzeschild-Stack – von unten durch Fan-Halter, durch die Lüfter, in die Schild-Inserts (4 pro Lüfter) |

### Heat-Set Inserts

| Position | Menge |
|---|---|
| M3 im Fan-Halter (seitlich) | 2 |
| M3 im Hitzeschild (oben, 4 pro Lüfter-Position) | 8 |
| **M3 Heat-Set Inserts gesamt** | **10** |

Voron-Standard M3 Messing, OD ≈ 5 mm, L ≈ 4 mm.

### Drucker-seitig benötigt

| Position | Hinweis |
|---|---|
| **Fysetc CNC Bedträger** | Liefert die zwei seitlichen Durchgangsbohrungen für die Sandwich-Befestigung. Auf andere Bedträger passt der Mod ohne Anpassung nicht. |
| **Heizmatte mit mittigem Thermistor** | Der Schild ergibt nur Sinn, wenn der Thermistor im Luftstrom der Bedfans sitzt |

---

## Montage

### Vorbereitung

1. Heat-Set Inserts setzen:
   - **2× M3** seitlich in den Fan-Halter (für die Sandwich-Befestigung)
   - **8× M3** oben in den Hitzeschild (vier pro Lüfter-Position)
2. **2× 3010 Lüfter** in den Fan-Halter einlegen.

### Hitzeschild-Stack

3. Hitzeschild auf die Lüfter legen. Bohrungen ausrichten.
4. Von **unten** **8× M3×16 BHCS** durch Fan-Halter, durch die Eck-Bohrungen der Lüfter, in die Schild-Inserts schrauben. Gleichmäßig anziehen. Die Lüfter sind jetzt zwischen Halter und Schild als Sandwich eingespannt.

### Befestigung am Bedträger

5. Lüfter-Kabel auf die Seite verlegen, an der später der Wago-Halter sitzen wird.
6. **Fan-Halter** mittig in die Heizmatten-Aussparung des Fysetc CNC Bedträgers setzen.
7. **Wago-Halter** auf der gegenüberliegenden Seite der Aussparung ansetzen.
8. Von außen am Wago-Halter **2× M3×20 BHCS** (eine pro Seite) durch den Wago-Halter, durch die Bedträger-Bohrung, in das M3-Insert im Fan-Halter schrauben. Beide Seiten gleichmäßig anziehen.
9. **4× Wago 221-412** in die Slots im Wago-Halter einsetzen.

> Nach der Montage einmal langsam Z homen und prüfen, dass der Schild die Heizmatte nicht berührt. Der designte Spalt beträgt ~3 mm – knapp, aber gewollt.

---

## Verkabelung

**4× Wago 221-412 (2-polig), 24 V** für die Lüfter.

- Die zwei 3010er werden parallel über zwei der Wagos verdrahtet (eine für V+, eine für GND) und dann an einen freien 24-V-Lüfter-Ausgang am Drucker geführt.
- Die anderen beiden Wagos sind bewusst frei – nutze sie für was auch immer du in der Nähe vom Bett sauber verteilt haben willst (Heizmatten-Verkabelung, Sensor-Leitungen, …). Das ist eine Setup-Entscheidung und nicht Teil dieses Mods.

Kein spezifischer Stecker, kein Klipper-Snippet – was dein Drucker-Setup erwartet, klemmst du dran.

---

## Druck-Files

Im Ordner [`/3MF`](3MF/) – **1 File:**

| File | Inhalt |
|---|---|
| `V0-Bedfans-Heatshield.3mf` | Fan-Halter + Wago-Halter + Hitzeschild (alle drei Teile in einer Datei) |

---

## Source-CAD

- **STEP:** [`/STEP`](STEP/) – editierbar in jedem CAD (Fusion, FreeCAD, OnShape, SolidWorks)
- **Fusion 360 native:** [`/CAD`](CAD/) – mit vollem Parameterbaum
- **Kein STL** – das 3MF ist slicer-unabhängig und enthält alle Bauteile sauber strukturiert

---

## Lizenz

[**CC-BY-SA 4.0**](LICENSE) – Standard im Voron-Ökosystem.

Forks, Remixes und Reposts gerne – aber bitte unter gleicher Lizenz und mit Verweis auf das Original.

---

## Credits

- **Design:** Wh'sFortune
- **Inspired by:** [Voron V0](https://docs.vorondesign.com) (CC-BY-SA 4.0)
- **Companion-Mods:** [Aegis Chamber](https://github.com/WhsFortune/Projekt-Aegis) (isolierende Verkleidung für den V0.2) · [Filtra](https://github.com/WhsFortune/filtra) (Innenraum-Filter mit Umluft für den V0)

Issues und Feedback: gerne als GitHub Issue.
