# Design Decisions & Notes

[[**DESIGN-DECISIONS in English**](/DESIGN-DECISIONS.md)]

**25.10.26**

## Werkzeug-Austausch bei m04b: iFixit-Schraubendreher statt Phasenprüfer

**Entscheidung:** In letzter Minute wurde beim Modul `repair-m04b` der Phasenprüfer durch den iFixit-Schraubendreher (4mm Bit-Halter) ersetzt.

- Da die Module zu diesem Zeitpunkt schon verklebt waren, wurde die Aussparung nachträglich mit einem Dremel etwas ausgefräst, damit der iFixit-Schraubendreher hineinpasst.
- Dadurch gibt es für diese Aussparung **keine Laser-Cutting-Datei** – sie wurde händisch angepasst.

---

**17.09.26**

## Papierstärke für den Druck auf die Lochrasterplatte

**Entscheidung:** Dickeres Papier mit **160 g/m²** wird verwendet.

- Scheint robuster zu sein.
- Lässt sich gut kleben.

---

**10.09.26**

## Anschlag beim Kleben des Papiers auf die Lochrasterplatte

**Entscheidung:** Der Anschlag wird **oben rechts** gemacht.

- Das Papier wird **rechts** bündig zur rechten Kante der Lochrasterplatte platziert.
- Das Papier wird **oben** bündig zur oberen Kante der Lochrasterplatte platziert.

---

**08.09.26**

## Bedrucktes Papier auf Lochrasterplatte kleben

**Learning:** Nach dem Aufkleben von bedrucktem Papier (mit den Werkzeugen drauf) auf die Lochrasterplatte muss der Kleber erst **trocknen**, bevor die überstehenden Ränder mit dem Cutter abgeschnitten werden. Schneidet man zu früh (Kleber noch feucht), reißt das Papier an den Rändern ein.

- [x] Nächster Test: **dickeres Papier** ausprobieren. → siehe Entscheidung vom 01.10.26 (160 g/m²).

## Gummis auf den Lochrasterplatten

**Entscheidung:** Rundgummi mit **Durchmesser > 2 mm** ist zu empfehlen.

- Bei Flachgummis schwankt die Qualität sehr stark.

## Transparenz der Drucklayer auf der Lochrasterplatte

**Entscheidung:** Die Drucklayer werden mit **70 % Deckkraft** gedruckt, damit die Items gut erkennbar sind, wenn sie fixiert werden.

- In Inkscape umgesetzt, indem eine **weiße Ebene** darübergelegt wird, die nur **30 % Deckkraft** hat.

---

**24.07.26**

## Verpackung / Kiste (Versandsicherung)

Lösung dafür, wie die Module versandsicher in die Kiste gepackt werden.

## Variante „Schräggelagert 1"

### Anforderungen (Designtreiber)

- **Versandsicher:** Der Koffer soll per Post verschickt werden können, ohne dass Inhalt beschädigt wird oder verrutscht.
- **Einfach verständliches Einräumen:** Es soll möglichst **nur einen Weg** geben, alles einzuräumen, und dieser soll **klar und selbsterklärend** sein – auch für Leute, die damit nicht viel Erfahrung haben.
- **Erweiterbarkeit:** Es soll etwas mehr reinpassen, falls zusätzlicher Inhalt mitgeschickt werden soll (siehe „Mögliche Bestückungen").

  - Neben den 5 normalen Modulen sollen **2 weitere Module auf Lochrasterplatten** in die Kiste passen.
  - Die Aussparung im unteren Schaumstoff wird entsprechend dimensioniert (für 5 normale + 2 Lochraster-Module).

### Mögliche Bestückungen (jetzt möglich):

- **5 Module aus Pappe + 1 A5-Heftbox**
- **6 Module aus Pappe + 1 A5-Heftbox**
- **5 Module aus Pappe + 2 A5-Heftboxen**, oder
- **5 Module aus Pappe + 1 A5-Heftbox + 1–2 Lochraster-Module**

### Teile:

- Ein Schaumstoffteil für den **Boden**.
- Ein Schaumstoffteil **oben** → sichert die Module gegen Hin- und Herrutschen.
- ~~Entscheidung: **2 Keile**.~~ → **Entscheidung zurückgenommen:** Keile werden **nicht** benötigt. Ein oberes und ein unteres Schaumstoffteil reichen aus.
  - An der linken und rechten inneren Schnittkante wurde beim **oberen** Schaumstoffteil der Schnitt **schräg** angesetzt, sodass er sich in die Radien der Pappmodule einfügt.
  - Das sorgt für eine sehr gute Klemmung → die Verrutschsicherung ist dadurch ausreichend.
- **Dünner Schaumstoff im Deckel nicht notwendig**, weil:
  - das obere Schaumstoffteil die Module bereits gegen Verrutschen sichert;
  - selbst bei normal aufrecht stehenden Modulen der dünne Deckel-Schaumstoff keine Klemmung erzeugen würde → ein oberes Schaumstoffteil ist ohnehin zwingend nötig.

### A5-Heftbox – Unterbringung

- 1 A5-Heftbox hinten
- **Seitlich (aktuelles Design): nicht möglich.** Die A5-Heftbox ist zu hoch. Um sie seitlich unterzubringen, müsste das untere (oder obere) Schaumstoffteil an der Stelle deutlich dünner werden (Höhe reduziert). Folgen:
  - schlecht für die Stabilität des unteren Teils;
  - Module wären nicht mehr gegen Hin- und Herrutschen gesichert.
  - **Seitlich mit anderem Design des oberen Teils:** grundsätzlich möglich, wenn das obere Teil anders gestaltet wird.
- **Vorne (vor den Modulen): möglich**, aber nur, **wenn keine zusätzlichen Lochraster-Module** mit drin sind.

---

**02.06.26**

**Lasern von Shadowfoam (3 Schichten, 30 mm) mit dem [xTool](https://www.xtool.com) (Laser-Cutter):**

- Strength: 5, Speed: 15 → zum „Gravieren", schneidet nur die schwarze oberste Schicht (und ein wenig darunter) (eventuell sogar noch etwas mehr Speed)
- Strength: 20, Speed: 15 → zum Schneiden einer der farbigen Schichten
- Strength: 15, Speed: 5 → zum fast vollständigen Durchschneiden bis zum Boden (zwei farbige Schichten)

