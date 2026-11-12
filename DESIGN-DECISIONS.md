# Design Decisions & Notes

[[**DESIGN-DECISIONS auf Deutsch**](/DESIGN-DECISIONS.de.md)]

**25.10.26**

## Tool Swap for m04b: iFixit Screwdriver Instead of the Voltage Tester

**Decision:** At the last minute, the voltage tester (Phasenprüfer) in the `repair-m04b` module was replaced with the iFixit screwdriver (4mm bit holder).

- Since the modules were already glued at that point, the recess was milled out afterwards with a Dremel to fit the iFixit screwdriver.
- As a result, there is **no laser-cutting file** for this recess – it was adjusted by hand.

---

**17.09.26**

## Paper Thickness for Printing on the Pegboard

**Decision:** Thicker paper at **160 g/m²** is used.

- Seems more robust.
- Glues well.

---

**10.09.26**

## Alignment When Gluing the Paper onto the Pegboard

**Decision:** The paper is aligned to the **top right**.

- The paper is placed flush with the right edge of the pegboard.
- The paper is placed flush with the top edge of the pegboard.

---

**08.09.26**

## Gluing Printed Paper onto the Pegboard

**Learning:** After gluing printed paper (with the tools printed on it) onto the pegboard, the glue must **dry** before trimming the overhanging edges with the cutter. Cutting too early (while the glue is still wet) tears the paper at the edges.

- [x] Next test: try **thicker paper**. → see decision from 01.10.26 (160 g/m²).

## Rubber Bands on the Pegboards

**Decision:** Round rubber cord with a **diameter > 2 mm** is recommended.

- Flat rubber bands vary a lot in quality.

## Transparency of the Print Layer on the Pegboard

**Decision:** The print layers are printed at **70% opacity**, so the items are clearly visible once they're mounted.

- Implemented in Inkscape by placing a **white layer** on top that only has **30% opacity**.

---

**24.07.26**

## Packaging / Crate (Shipping Protection)

Solution for how the modules are packed securely for shipping in the crate.

## Variant "Angled Bedding 1"

### Requirements (Design Drivers)

- **Shipping-safe:** The case should be shippable by post without the contents being damaged or shifting.
- **Easy-to-understand packing:** There should ideally be **only one way** to pack everything, and it should be **clear and self-explanatory** — even for people without much experience.
- **Expandability:** It should fit a bit more, in case additional content needs to be shipped along (see "Possible Configurations").

  - Besides the 5 normal modules, **2 additional modules on pegboards** should also fit in the crate.
  - The recess in the bottom foam is dimensioned accordingly (for 5 normal + 2 pegboard modules).

### Possible Configurations (now possible):

- **5 cardboard modules + 1 A5 folder box**
- **6 cardboard modules + 1 A5 folder box**
- **5 cardboard modules + 2 A5 folder boxes**, or
- **5 cardboard modules + 1 A5 folder box + 1–2 pegboard modules**

### Parts:

- One foam part for the **bottom**.
- One foam part **on top** → secures the modules against sliding back and forth.
- ~~Decision: **2 wedges**.~~ → **Decision reversed:** wedges are **not** needed. A top and bottom foam part are enough.
  - On the left and right inner cut edge, the cut on the **top** foam part was angled, so that it fits into the radii of the cardboard modules.
  - This creates a very good clamping effect → the anti-slip protection is sufficient as a result.
- **Thin foam in the lid is not necessary**, because:
  - the top foam part already secures the modules against sliding;
  - even with modules standing normally upright, the thin lid foam wouldn't create any clamping effect anyway → a top foam part is mandatory regardless.

### A5 Folder Box – Placement

- 1 A5 folder box at the back
- **On the side (current design): not possible.** The A5 folder box is too tall. To fit it on the side, the bottom (or top) foam part would need to be noticeably thinner there (reduced height). Consequences:
  - bad for the stability of the bottom part;
  - modules would no longer be secured against sliding back and forth.
  - **On the side with a different design of the top part:** possible in principle, if the top part is designed differently.
- **In front (in front of the modules): possible**, but only **if there are no additional pegboard modules** included.

---

**02.06.26**

**Laser-cutting Shadowfoam (3 layers, 30 mm) with the [xTool](https://www.xtool.com) (laser cutter):**

- Strength: 5, Speed: 15 → for "engraving", cuts only the black top layer (and a little underneath) (maybe even a bit more speed)
- Strength: 20, Speed: 15 → for cutting one of the colored layers
- Strength: 15, Speed: 5 → for cutting almost to the bottom (two colored layers)
