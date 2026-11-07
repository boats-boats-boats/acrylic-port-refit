# CLAUDE.md — Project Context & Engineering Guidelines for `acrylic-port-refit`

## 1. Project Overview
`acrylic-port-refit` documents and automates the fabrication of replacement fixed cabin trunk windows (`16–20 sq ft` total, up to `8 × 1 ft` long curved side ports) for the **2003 Hunter 326** and **2009 Beneteau 40 (*Novella*)**, using **`3/8"` (`9.5 mm`) gray-tinted cell-cast acrylic** (`Piedmont Plastics Order RO42811431R0`), an **OpenCV camera-to-DXF digitization pipeline** ([`process_window_templates.py`](process_window_templates.py)), and **exterior-applied `3M IJ180Cv3` cast marine vinyl halftone frit borders**.

Primary reference document: [`acrylic-window-frit-refit-guide.md`](acrylic-window-frit-refit-guide.md).

---

## 2. Core Material & Engineering Rules (Do Not Violate)

1. **Cell-Cast Acrylic Only (`3/8"` / `9.5 mm` Gray-Tinted PMMA):**
   * Never substitute extruded acrylic (gums/melts during routing and stress-crazes rapidly) or polycarbonate (scratches and yellows under marine UV).
   * Never clean or wipe cast acrylic with acetone, MEK, lacquer thinner, aromatic hydrocarbons, or ammoniated glass cleaners—use only **`70%` Isopropyl Alcohol (IPA) + distilled water** or dedicated plastic cleaner (`Novus 1`).
2. **Pattern Digitization & CAD Accuracy ([`process_window_templates.py`](process_window_templates.py)):**
   * All templates use **`12.0"` (`304.8 mm`) orthogonal `+` calibration crosshairs** along both axes.
   * Output DXFs must remain in **`1:1` real-world inches (`$INSUNITS = 1`)** with closed `LWPOLYLINE` and smoothed periodic `SPLINE` paths suitable for direct Annapolis CNC router import and wide-format vinyl print/cut plotters.
3. **Thermal Forming vs. Cold-Springing:**
   * Only cold-spring `3/8"` acrylic over very gentle single-axis curves where bending stress stays well below crazing limits.
   * For compound or tighter coachroof curvature, thermoform in an insulated **foil-faced polyisocyanurate (`polyiso`) hot box at `275°F–300°F` (`135°C–150°C`)** with slow uniform cooling below `140°F` to eliminate locked-in residual stress.
4. **Frit Emulation (`3M IJ180Cv3` Cast Vinyl + Cast UV Overlaminate — EXTERIOR Application Only):**
   * True ceramic frit (`1,200°F` baked enamel) is strictly glass-only and will liquefy acrylic.
   * Pre-printed architectural dot films fail due to fixed linear geometry and UV/outgassing adhesive breakdown.
   * Always specify **custom-printed `3M IJ180Cv3` (`2 mil` cast Controltac/Comply vinyl) + matched `3M 8518/8520` cast UV overlaminate** with a `100%` solid blackout perimeter band transitioning inward via a halftone dot matrix.
   * **Apply to the EXTERIOR acrylic surface ONLY** (dry center-hinge method, felt squeegee, post-heated at edges to **`195°F` / `90°C`**). Never apply vinyl between the interior acrylic face and the structural bedding sealant (`Sikaflex 295 UV` / `Sika Primer 209 D` / `3M VHB 4991`), and never trap vinyl on the interior where acrylic outgassing causes blistering.
