# FDM 3D Printing Filament Comparison & Solvent Finishing Guide

A technical reference guide detailing thermal profiles, mechanical characteristics, typical applications, and chemical post-processing guidelines (smoothing and solvent welding) for common fused deposition modeling (FDM) filaments.

---

## 1. Quick Reference Comparison Table

| Filament Name / Type | Distinguishing Properties | Common Use Cases | Nozzle Temp (°C) | Bed Temp (°C) | Best Solvent for Smoothing & Bonding |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **PLA**<br>*(Polylactic Acid)* | • Easiest to print; minimal shrinkage & warping<br>• Low thermal resistance ($T_g \approx 60^\circ\text{C}$)<br>• High tensile strength, but brittle under impact<br>• Plant-derived and biodegradable under industrial conditions | Rapid prototyping, architectural models, display figurines, non-stress jigs & fixtures | 190 – 220 | 40 – 60<br>*(or unheated)* | • **Smoothing:** Ethyl acetate or Tetrahydrofuran (THF) *(resistant to acetone)*<br>• **Bonding:** Cyanoacrylate (super glue) or Dichloromethane (DCM) |
| **PETG**<br>*(Polyethylene Terephthalate Glycol)* | • Strong layer adhesion & high ductility<br>• Resistant to moisture, acids, and alkalis<br>• Moderate heat resistance ($T_g \approx 80^\circ\text{C}$)<br>• Prone to stringing and oozing | Functional mechanical brackets, waterproof enclosures, outdoor fixtures, snap-fit components | 220 – 250 | 70 – 85 | • **Smoothing:** Dichloromethane (DCM) or Cyclohexanone *(difficult to smooth safely)*<br>• **Bonding:** Cyanoacrylate, two-part structural epoxy, or DCM |
| **ABS**<br>*(Acrylonitrile Butadiene Styrene)* | • High impact resistance, durability, and toughness<br>• Heat resistant up to $\approx 100^\circ\text{C}$<br>• High thermal shrinkage; prone to warping/cracking<br>• Emits styrene fumes (requires enclosure/filter) | Automotive interior trim, functional electronics housings, impact-resistant tooling, snap joints | 230 – 260 | 95 – 110<br>*(enclosure recommended)* | • **Smoothing:** Acetone (vapor chamber or brush)<br>• **Bonding:** Acetone (solvent weld / ABS slurry) or cyanoacrylate |
| **ASA**<br>*(Acrylonitrile Styrene Acrylate)* | • Mechanical toughness matching ABS<br>• Superior UV stability and outdoor weathering resistance<br>• High dimensional stability<br>• Enclosure recommended to prevent warping | Outdoor sensor housings, exterior automotive parts, garden equipment, marine fittings | 240 – 260 | 90 – 110<br>*(enclosure recommended)* | • **Smoothing:** Acetone (vapor chamber or brush)<br>• **Bonding:** Acetone (solvent weld / ASA slurry) or cyanoacrylate |
| **TPU / TPE**<br>*(Thermoplastic Polyurethane)* | • High elasticity, flexibility, and elongation (Shore 70A–95A)<br>• Excellent abrasion, tear, and oil/grease resistance<br>• High inter-layer bond strength<br>• Requires direct-drive extruder & slow print speeds | Gaskets, vibration dampeners, protective cases, robotics tracks/wheels, flexible hinges | 210 – 240 | 30 – 60<br>*(or unheated; release agent recommended)* | • **Smoothing:** Ineffective with common solvents *(thermal/flame smoothing only)*<br>• **Bonding:** Cyanoacrylate (flexible CA) or polyurethane contact cement |
| **Nylon (PA)**<br>*(Polyamide 6 / 12)* | • Exceptional tensile strength, toughness, and fatigue life<br>• Low coefficient of friction & high wear resistance<br>• Extremely hygroscopic (requires active drying)<br>• High warping tendency | Functional gears, sliding bushings, bearings, heavy-duty structural brackets, snap assemblies | 240 – 280 | 70 – 100<br>*(requires specialized bed adhesive)* | • **Smoothing:** Formic acid *(extreme chemical hazard; mechanical smoothing preferred)*<br>• **Bonding:** Formic acid, Resorcinol, or high-performance two-part epoxy |
| **PC**<br>*(Polycarbonate)* | • Extreme impact resistance and rigidity<br>• High heat deflection temperature ($T_g \approx 115\text{–}120^\circ\text{C}+$)<br>• Optical clarity potential<br>• Highly prone to moisture absorption and warping | High-temperature housings, structural engineering parts, protective shields, light covers | 270 – 310 | 100 – 125<br>*(heated enclosure required)* | • **Smoothing:** Dichloromethane (DCM / Methylene Chloride)<br>• **Bonding:** Dichloromethane (solvent weld) or structural two-part epoxy |
| **PVB**<br>*(Polyvinyl Butyral)* | • Mechanical rigidity and print ease comparable to PLA<br>• Formulated specifically for safe alcohol vapor smoothing<br>• Burns out cleanly without ash residue | Decorative display prototypes, artistic models, lost-wax/investment casting patterns | 190 – 220 | 50 – 70 | • **Smoothing:** Isopropyl Alcohol (IPA, $\ge 90\%$) via mist or vapor chamber<br>• **Bonding:** Isopropyl alcohol or cyanoacrylate |
| **HIPS**<br>*(High Impact Polystyrene)* | • Lightweight, rigid, and impact-resistant<br>• Chemically dissolves selectively in d-Limonene<br>• Easy to sand, prime, and machine | Dissolvable support material (paired with ABS/ASA), lightweight structural enclosures, models | 230 – 250 | 90 – 110 | • **Smoothing:** d-Limonene (slow dissolution) or Acetone<br>• **Bonding:** Polystyrene cement (MEK/butyl acetate), acetone, or cyanoacrylate |

---

## 2. Chemical Post-Processing & Smoothing Methods

Chemical smoothing dissolves microscopic ridges along the outer layer lines of 3D prints, allowing surface tension to level the plastic into an injection-molded, glossy finish.

### A. Acetone Smoothing (ABS, ASA, HIPS)
* **Cold Vapor Method:** Place the printed component on an elevated platform (e.g., aluminum foil over a wire stand) inside a sealed glass or polypropylene container lined with paper towels soaked in pure acetone. The ambient vapor smooths layer lines gradually over 30 to 90 minutes.
* **Warm Vapor Method:** Heated acetone chambers accelerate vapor generation but significantly increase combustion and flash fire risks. Strictly use dedicated, explosion-proof, temperature-controlled appliances.
* **Curing & Outgassing:** Immediately after smoothing, parts remain soft and sensitive to fingerprints. Allow 12 to 24 hours of ambient curing in a ventilated area for residual acetone to evaporate and polymer hardness to return.

### B. Isopropyl Alcohol (IPA) Smoothing (PVB)
* **Nebulizer / Mist Chamber:** PVB dissolves reliably when exposed to fine aerosols or vapors of high-concentration Isopropyl Alcohol ($\ge 90\%$ IPA). Dedicated commercial units (such as the Polymaker Polysher) atomize IPA into an ultrasonic mist to provide uniform smoothing without harsh chemical exposure.
* **Manual Brush / Wipe:** Gentle brushing with 99% IPA smooths seams and layer artifacts, though care must be taken to prevent pooling.

### C. Chlorinated & Hazardous Solvents (PLA, PETG, PC)
* **PLA:** Standard PLA is chemically resilient to acetone. While Ethyl Acetate and Tetrahydrofuran (THF) soften PLA, and Dichloromethane (DCM) dissolves it rapidly, their low boiling points, volatility, and high toxicity make domestic chemical smoothing ill-advised. Primer-filler and mechanical sanding remain the industry standard for PLA post-finishing.
* **PETG:** PETG is engineered for chemical resilience against acids, bases, and common solvents. Smoothing with Cyclohexanone or DCM requires strict laboratory ventilation and specialized handling.
* **Polycarbonate (PC):** Dichloromethane (DCM) actively softens and welds PC, but rapid surface crystallization can cause clouding or crazing if solvent exposure is unmonitored.

---

## 3. Component Assembly & Bonding Techniques

Joining multi-part assemblies requires choosing between solvent welding (homogeneous fusion) and mechanical/chemical adhesives (interfacial adhesion).

### A. Solvent Welding
* **Mechanism:** Applying solvent directly to joint interfaces dissolves surface polymer chains. When pressed together, the polymer chains entangle across the interface. As the solvent flashes off, the joint cures into a single continuous solid piece with parent-material structural integrity.
* **ABS / ASA Slurry ("Juice"):** Dissolve scraps or cut filament segments of ABS or ASA in pure acetone until a viscous syrup forms. Use this slurry as a color-matched adhesive and gap-filler that sands and paints flush with the print.
* **Welding Syringes & Capillary Action:** For tight-tolerance joints in ABS, ASA, or Acrylic, clamp mating components dry and apply solvent along the seam via a glass syringe or needle applicator. Capillary action draws the liquid into the joint.

### B. Adhesive Bonding
* **Cyanoacrylate (Super Glue):** Excellent general-purpose adhesive for PLA, PETG, ABS, and PVB. For flexible materials like TPU, use rubber-toughened or flexible cyanoacrylate formulations to avoid brittle joint failure.
* **Two-Part Structural Epoxy:** The standard choice for engineering polymers (Nylon, Polycarbonate, PETG). Epoxy cures via a thermoset chemical reaction independent of the substrate, bridging gaps without requiring surface dissolution. Lightly abrade bonding surfaces with 120-grit sandpaper to increase mechanical interlocking.
* **Polyurethane & Contact Cements:** Ideal for flexible TPU parts subjected to cyclic bending, dynamic shock, or peel loads.

---

## 4. Safety Precautions & Handling Standards

Chemical solvents carry flammability, respiratory, and environmental hazards. Adhere to the following laboratory safety protocols:

1. **Respiratory Protection:**
   * Standard particulate masks (N95/FFP2) do **not** filter chemical vapors.
   * Work with volatile organic compounds (Acetone, Ethyl Acetate, MEK) using half-mask or full-face respirators equipped with certified **Organic Vapor (OV) cartridges**.
2. **Skin and Eye Safety:**
   * Solvents extract natural lipids from the skin, causing severe dryness and dermatitis. Certain solvents (e.g., DCM) penetrate standard latex gloves within seconds.
   * Select gloves compatible with the chemical in use (nitrile for brief splash protection with alcohols and acetone; butyl or fluoroelastomer gloves for ketones and halogenated solvents).
   * Wear splash-proof chemical safety goggles at all times.
3. **Ventilation & Airflow:**
   * Perform all chemical vapor smoothing and solvent welding inside a certified laboratory fume hood or in an open, well-ventilated outdoor environment.
   * Avoid processing solvents in residential living areas, basements, or enclosed print enclosures without external exhaust ducting.
4. **Fire Prevention & Storage:**
   * Acetone, IPA, and Ethyl Acetate have extremely low flash points and heavy vapors that sink to floor level.
   * Eliminate all ignition sources: open flames, unsealed heating elements, non-explosion-proof electrical switches, and static discharge risks.
   * Store solvents in designated flammables safety cabinets within original, clearly labeled chemical safety containers.
