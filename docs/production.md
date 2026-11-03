
# Produktion der Module aus gelaserter Wellpappe

## Konturen erstellen

- Schnittkonturen für die Teile erstellen.

## Lasern der Einzelteile (Layer)

- Die einzelnen Schichten/Layer lasern.

## Erstellen der Hintergrundbilder

- [ ] TODO: gleicher Prozess wie bei Lochraster (siehe oben) oder abweichend? Bitte bestätigen.

## Kleben

Benötigte Layer (Aufbau von unten nach oben):

1. **Dünne Hintergrundpappe ohne Kontur** – die Basis, wird die Rückseite des Moduls.
2. **Mehrere Lagen gelaserte Wellpappe mit Kontur** – mit jeweils nur den Aussparungen, die auf dieser Tiefe tatsächlich benötigt werden (das tiefste Werkzeug braucht entsprechend in den meisten Lagen eine Aussparung). Hintergrundbild mit Werkzeug (auf Papier gedruckt) wird hier aufgeklebt.
3. **Moosgummi mit Kontur** (oben) – mit den gleichen Aussparungen wie die oberste Pappe-Lage.

Das Gesamtbild (Fotos der Werkzeuge) ist bereits passend auf die einzelnen Lagen aufgeteilt gedruckt: pro Lage klebt man nur den Bildausschnitt der Werkzeuge, deren Aussparung genau auf dieser Tiefe endet. Das vollständige Bild ergibt sich dadurch erst im fertig gestapelten Modul, weil jedes Werkzeug-Foto genau auf der Lage sitzt, auf der sein Aussparungsboden liegt.

### Material

- **Klebtool** (3D-gedruckt; Modell im Repo: [prod/Gluing-Tool.stl](../prod/Gluing-Tool.stl), Quelle: [src/CAD/Gluing-Tool.FCStd](../src/CAD/Gluing-Tool.FCStd))
- **Ponal Express Leim**, aufgetragen mit einer **kleinen Malerrolle** + **Farbwanne**
- **Prittstift** (zum Ankleben der Bildausschnitte)
- Ausgedruckte **Werkzeughintergrundbilder** auf 160 g/m² Papier
- **Cutter**
- **Leuchttisch** (hilfreich, aber nicht zwingend nötig)

### Vorgehen

1. [[[ raus? ]]] Die dünne Hintergrundpappe (ohne Kontur) als Basis auf den Tisch legen.
2. Pro Wellpappe-Lage, von unten nach oben:
   1. Die für diese Tiefe benötigten Pappkonturen aus der gelaserten Wellpappe herausbrechen (nur dort, wo ein Werkzeug genau auf dieser Tiefe eine Aussparung braucht).
   2. Mit dem Cutter die passenden Bildausschnitte aus dem Papier mit den Werkzeughintergrundbildern ausschneiden, mit ordentlichem Rand drumherum – nur die Bilder der Werkzeuge, deren Aussparung genau auf dieser Lage endet. Ein Leuchttisch hilft, die Position genau zu treffen.
   3. Mit dem Prittstift Kleber auf die unbedruckte Rückseite des Papierausschnitts auftragen und von hinten auf die passende Stelle der Pappe-Lage kleben (bedruckte Seite zeigt nach oben).
   4. Die gesamte Rückseite dieser Pappe-Lage mit Ponal Express (Malerrolle + Farbwanne) benetzen und mit dem Klebtool auf den bisherigen Stapel aufkleben. Bei dem ersten (untersten) Papplayer wird dieser auf die dünne Hintergrundpappe ohne Kontur aufgeklebt. 
3. Schritt 2 für alle weiteren Wellpappe-Lagen wiederholen, sodass sich das Modul Lage für Lage aufbaut.
4. Zum Schluss die Moosgummi-Lage mit Kontur oben aufkleben.

---

# Produktion der Module auf Lochraster

Prozess für die Erstellung der Hintergrundbilder, das sandwichmäßige Zusammenkleben der Module und die Herstellung/den Einsatz der Spanngummis.

## Erstellung der Hintergrundbilder für die Lochrasterplatten

### 1. Fotos machen

- Vor dem Fotografieren wird das auf **5 %** ausgedruckte Lochraster-Papier untergelegt.
- Die Items werden darauf so angeordnet, wie sie später auf der Lochrasterplatte tatsächlich liegen würden (gleiche Anordnung/Raster).
- **Weißabgleich:** auf den **schwarzen Hintergrund**, damit eine relativ helle Belichtung entsteht.
  - [ ] Tim: bitte hier noch genau nachtragen, wie der Weißabgleich konkret eingestellt wurde.

### 2. Nachbearbeitung in GIMP

- Mit dem **Kurvenwerkzeug** den Hintergrund auf **komplettes Weiß** bringen.
- Schatten dabei möglichst ebenfalls entfernen/minimieren.
- Datei **gimp-anpass-schablone.png** als Ebene in das Bild ziehen.
  - Wird als Referenz für das **Perspektive-Werkzeug** genutzt, um das Foto ins korrekte Format zu ziehen (entzerren).
- Mit dem **Zuschneiden-Werkzeug (Cropping)** auf das A4-Seitenverhältnis **1,414 : 1** zuschneiden – alles außenherum wegschneiden.
- Auf die korrekte Pixelgröße für **300 dpi bei A4** skalieren: **2480 × 3508 Pixel**.
- **Export als JPG.**

### 3. Weiterverarbeitung in Inkscape

- JPG importieren.
- Eine **weiße Ebene mit 30 % Deckkraft** darüberlegen (siehe [[Design Decisions (& Notes)]] – 70 % Deckkraft der Drucklayer).
- **Export als PDF.**

### 4. Druck

- Druck des PDFs auf **160 g/m²** Papier.
- Der Druck erfolgt **borderless** (randlos).

## Spanngummis (Gummibänder mit T-Splinten)

- Jedes Werkzeug/Item wird mittels **Spanngummis** – Gummibändern mit **T-Splinten an beiden Enden** – fixiert und bekommt so eine feste Position.
- Pro Item kommen meist **zwei Spanngummis** zum Einsatz.
- Werden die Spanngummis selbst hergestellt, müssen sie entsprechend abgelängt werden. Folgende Längen kommen zum Einsatz:
  - 40 mm
  - 70 mm
  - 100 mm
  - 130 mm
  - (selten) 180 mm

## Reihenfolge der Arbeitsschritte

1. Ein Lochrastermodul nehmen und ein passendes Bild (Hintergrundbild, siehe oben) auf die Lochrasterplatte kleben – **trocknen lassen**.
2. Die Löcher an den richtigen Positionen stanzen, z. B. über einem Lichttisch.
3. Die überstehenden Papierränder abschneiden mit einem scharfen Cuttermesser.
4. Die Gummibänder (Spanngummis) entsprechend platzieren.
5. Die einzelnen Layer (Sandwich) verkleben (siehe unten).

## Die einzelnen Layer verkleben

### Aufbau des Sandwich (von oben nach unten)

![](../assets/Pegboard-Module-Materials.jpg)

1. **Papier** mit den aufgedruckten Tools, gedruckt auf **160 g/m²**.
2. **Lochraster-Platine** (MDF).
   - [ ] Link zu den Laser-Cutting-Files noch hinzufügen.
3. **Pappschicht**.
   - [ ] Material- und Lasercutting-Links bzw. Ordner noch hinzufügen.
4. **Moosgummischicht** (unten).

### Vorgehen

1. Die mit dem Hintergrundbild beklebte Lochraster-Platine (MDF) wird mit den Gummibändern bestückt. **Erst danach geht es weiter.**
2. Der nächste Schritt wird am besten mit dem **Klebtool** durchgeführt (3D-Druckdatei liegt im Repo, es geht aber auch ohne).
3. Der Papp-Layer wird auf den Tisch gelegt und die Lochraster-Platine oben darauf platziert. Durch festes Andrücken drücken sich die T-Splinte etwas in die Pappschicht ein und markieren so die Positionen.
4. Die Lochraster-Platine wieder zur Seite nehmen und an den markierten Stellen die Pappschicht durchstechen, z. B. mit der Rückseite eines Stifts. Dadurch können die T-Splinte später dort versenkt werden und sich alles gut zusammenkleben lässt.
5. Moosgummi auf die Pappe kleben.
6. Die Lochraster-Platine oben auf Moosgummi + Pappe legen und kräftig andrücken.
7. Alles gut beschweren und eine Weile trocknen lassen.

### Klebehinweise

- Verwendet wird **Ponal Express Leim**.
- Bewährt hat sich der Auftrag mit einer **kleinen Malerrolle**.
- Möglichst gleichmäßig, und nicht zu viel Leim auftragen – insbesondere die Pappe saugt sich sonst voll und verzieht sich etwas.

---

## Legacy "Production Steps" (from the general Repair-Kit README — needs review)

> **TODO:** Go through this list and check whether anything still needs to be carried over into the sections above. Right now, the 3D-printing of the gluing/stacking tool is the one point that still looks relevant and isn't captured above yet.

The following is the old, general production checklist this section replaced in the main README — kept here for reference until reviewed:

* Ordering all required items.
* Laser-cutting the cardboard layers in the `/prod/` folder.
* Unpacking and checking all items.
* Preparing special items (e.g., cutting hook-and-loop fasteners and rubber bands; cutting and putting together heat shrink tubes; cutting sandpaper).
* Picking items using the provided pick-list (in `BOM.fods`).
* Printing and cutting the photos of the tools.
* Preparing the workspace, including 3D-printing the gluing and stacking tool via `stl` in `/prod/`. (For Bambulab P1S you can use the provided `gcode` example)
* Gluing the layers together. (be aware this takes a lot of time, alternatively you can also skip the laser-cut layer approach and use the grid system, see `/src/CAD/README.md`)
* Final assembly and packing. (assembly documentation will follow)
* Documenting feedback in the issue list.
* If you want to become a case study partner you can either join repami.de in their current unit testing series in Berlin or request a separate project via openculture.agency.
