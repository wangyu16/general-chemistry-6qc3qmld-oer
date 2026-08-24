# Chapter 11: Intermolecular Forces, Liquids, and Solids

:::info
**Reference:** Yu Wang's General Chemistry Lecture Notes, Chapter 11 (CC BY 4.0)
**Audience:** introductory undergraduate general chemistry, second semester
**Package license:** CC BY 4.0
**Note:** builds on molecular polarity from Chapter 10; facts checked for accuracy against OpenStax *Chemistry 2e* and Wikipedia (used for reference only — no text or figures adapted from either).
:::

:::success
**Chapter Learning Objectives**
- Identify the intermolecular force(s) present between molecules and rank their relative strength.
- Relate intermolecular forces to the properties of liquids: surface tension, viscosity, and water's anomalous behavior.
- Classify a solid as molecular, ionic, covalent-network, or metallic, and describe its expected hardness, melting point, and conductivity.
- Count atoms per unit cell and determine coordination number for simple cubic, body-centered cubic, and face-centered cubic lattices.
- Describe phase changes in terms of energy, apply the Clausius–Clapeyron equation, and interpret a phase diagram.
:::

## Chapter Logic

Chapter 10 established which molecules are polar. This chapter asks: once you know that, what *physical* consequences follow? The answer runs in one direction — from force type, to bulk liquid behavior and solid structure, to the energetics of moving between phases.

{{mermaid
graph TD
  A["Molecular polarity & structure (Ch. 10)"] --> B["Type & strength of intermolecular force"]
  B --> C["Liquid properties:<br/>surface tension, viscosity"]
  B --> D["Solid classification:<br/>molecular / ionic / covalent-network / metallic"]
  B --> E["Phase-change energetics<br/>& phase diagrams"]
  C --> F["Everything in this chapter<br/>traces back to force type"]
  D --> F
  E --> F
}}

**Visual description:** A top-down flowchart. Molecular polarity and structure (from Chapter 10) determines the type and strength of intermolecular force present. That single fact then branches into three consequences covered in this chapter: liquid properties (surface tension, viscosity), solid classification (four solid types), and phase-change energetics (heats of transition, phase diagrams) — all three trace back to the same root cause.

:::warning
Intermolecular forces are attractions **between** separate molecules. Do not confuse them with intramolecular forces — the covalent bonds **within** a molecule — which are 10–100 times stronger and are not what breaks when a substance melts or boils.
:::

## 11.1 Intermolecular Forces{{attrs[#blk-ch11sec01]}}

:::success
**Learning Objectives**
- Distinguish intermolecular from intramolecular forces.
- Identify dipole-dipole forces, dispersion forces, and hydrogen bonds from a molecule's structure.
- Rank ion-dipole, hydrogen-bonding, dipole-dipole, and dispersion forces by relative strength.
:::

**Intermolecular forces** (also called **van der Waals forces**) are the attractive forces *between* molecules. **Intramolecular forces** — the covalent bonds that hold atoms together within one molecule — are a different and much stronger phenomenon. A typical covalent bond takes on the order of 150–1,100 kJ/mol to break; a hydrogen bond, the strongest common intermolecular force, takes only about 10–40 kJ/mol. ==That hundred-fold difference is *why* melting or boiling a substance never breaks its covalent bonds==: ice melts and water boils while every H–O covalent bond in the H₂O molecule stays perfectly intact.

![Six example molecules: three polar hydrogen-bond donors (water, hydrogen fluoride, ammonia) and three nonpolar molecules (methane, carbon tetrachloride, carbon dioxide)](../assets/polar_nonpolar_molecules.svg)
*Figure 11.1 — Polar molecules (top row) each have a permanent dipole and can act as hydrogen-bond donors when H is attached to N, O, or F. Nonpolar molecules (bottom row) either have no polar bonds (CH₄) or have polar bonds arranged so symmetrically that their dipoles cancel (CO₂). Self-generated with RDKit.*

### Dipole-dipole forces

A **polar molecule** has a permanent dipole: a partial positive end and a partial negative end. When two polar molecules approach each other, the positive end of one is attracted to the negative end of the other — a **dipole-dipole force**. Examples: $\ce{HCl}$, $\ce{H2O}$, acetone. These forces exist in addition to, and are generally stronger than, the dispersion forces described next.

### Dispersion forces

Even a completely nonpolar molecule like $\ce{CH4}$ or $\ce{Br2}$ experiences intermolecular attraction — otherwise it could never condense into a liquid at all. The electron cloud around any atom or molecule is in constant motion, and at any instant it may be shifted slightly to one side, creating a momentary **instantaneous dipole**. That instantaneous dipole induces a matching **induced dipole** in a neighboring molecule, and the two weakly attract — a **dispersion force** (also called a London dispersion force).

**Polarizability** — how easily a molecule's electron cloud can be distorted into an instantaneous dipole — increases with:
- **more electrons** (heavier atoms, larger molecules), and
- **a more diffuse electron cloud** (larger atoms/molecules of the same general shape).

This is why dispersion forces, though individually weak, can dominate for large molecules: $\ce{I2}$ (a solid at room temperature) is held together entirely by dispersion forces, yet those forces are strong enough to overcome $\ce{I2}$'s much smaller mass compared to, say, liquid water.

### Hydrogen bonds

A **hydrogen bond** is an especially strong dipole-dipole interaction that occurs specifically when a hydrogen atom is covalently bonded to a small, highly electronegative atom — **N, O, or F** — and is then attracted to a lone pair on a nearby N, O, or F atom. The N–H, O–H, or F–H bond is so polar, and the H atom so small, that the resulting attraction is unusually strong (roughly 10–40 kJ/mol, versus 2–5 kJ/mol for a typical dipole-dipole interaction).

:::warning
"Hydrogen bond" is a common-mistake magnet: **not every molecule containing hydrogen forms hydrogen bonds.** $\ce{CH4}$ has hydrogen atoms, but they are bonded to carbon (not N, O, or F) and are barely polar — no hydrogen bonding. Always check specifically for H bonded *directly* to N, O, or F.
:::

### Ranking the forces

$$\text{ion-dipole} > \text{hydrogen bond} > \text{dipole-dipole} > \text{ion-induced dipole} > \text{dipole-induced dipole} > \text{dispersion force}$$

:::info
This ranking is for *comparable-sized* species. A very large, highly polarizable nonpolar molecule can have *stronger* dispersion forces than a small polar molecule has dipole-dipole forces — size and electron count matter as much as polarity itself.
:::

{{chart
type: bar
title: Typical interaction energy by type (order of magnitude, kJ/mol)
labels: Covalent bond, Ionic lattice, Hydrogen bond, Dipole-dipole, Dispersion (small molecule)
series: kJ/mol (approx.) = 350, 700, 25, 5, 2
}}
**Data summary:** Approximate, illustrative order-of-magnitude energies. Covalent bonds (~350 kJ/mol) and ionic lattice energies (~700 kJ/mol) are intramolecular/ionic-bonding energies shown for scale; among the intermolecular forces, hydrogen bonds (~25 kJ/mol) are markedly stronger than ordinary dipole-dipole (~5 kJ/mol) or dispersion forces between small molecules (~2 kJ/mol). Real values vary considerably by specific substance.

:::: tabs
::: tab Problem
For each pair, identify every intermolecular force present, and state which substance should have the higher boiling point: (a) $\ce{CH3OH}$ (methanol) vs. $\ce{CH3SH}$ (methanethiol); (b) $\ce{Kr}$ vs. $\ce{He}$.
:::
::: tab Solution
**(a)** Methanol has an O–H bond, so it experiences hydrogen bonding, dipole-dipole forces, and dispersion forces. Methanethiol has an S–H bond — sulfur is not N, O, or F, so there is no hydrogen bonding, only dipole-dipole and dispersion forces. Methanol's additional hydrogen bonding makes it the higher-boiling substance (actual values: methanol 64.7 °C, methanethiol 6.2 °C).

**(b)** Both are nonpolar monatomic noble gases, so only dispersion forces apply to either. Kr (36 electrons) is far more polarizable than He (2 electrons), so Kr has the stronger dispersion forces and the higher boiling point (Kr: −153.2 °C vs. He: −268.9 °C).
:::
::::

**Self-check:**
- Does $\ce{HF}$ hydrogen-bond with itself? What about $\ce{CH3F}$?
- Why is $\ce{I2}$ a solid at room temperature while $\ce{Cl2}$ is a gas, given that both are nonpolar diatomic halogens?

## 11.2 Properties of Liquids{{attrs[#blk-ch11sec02]}}

:::success
**Learning Objectives**
- Define surface tension and viscosity, and connect both to intermolecular force strength.
- Distinguish cohesion from adhesion, and explain capillary action.
- Explain water's unusually high melting/boiling point, specific heat, and density-at-4-°C behavior in terms of hydrogen bonding.
:::

### Surface tension

**Surface tension** measures a liquid's resistance to increasing its surface area. A molecule in the interior of a liquid is pulled equally in every direction by its neighbors, but a molecule at the surface is pulled only sideways and downward — a net inward force that makes the surface act like a stretched, elastic skin. **Stronger intermolecular forces produce higher surface tension.**

![A water strider standing on a water surface, supported entirely by surface tension](../assets/water_strider_surface_tension.jpg =700x)
*Figure 11.2 — A water strider's weight is fully supported by the surface tension of water — a direct, everyday consequence of hydrogen bonding between water molecules. Source: NPS Photo, via Wikimedia Commons (public domain).*

**Cohesion** is the attraction between *like* molecules (e.g., water molecules to each other); **adhesion** is the attraction between *unlike* molecules (e.g., water to glass). When adhesion exceeds cohesion, a liquid climbs a narrow tube against gravity — **capillary action** — which is how paper towels wick up spills and how trees pull water upward through narrow xylem vessels.

### Viscosity

**Viscosity** measures a fluid's resistance to flow. Like surface tension, **stronger intermolecular forces mean higher viscosity** — think of honey (extensive hydrogen bonding among its sugar molecules) versus water versus gasoline. Viscosity also decreases as temperature rises, because added thermal energy helps molecules slip past their neighbors' attractive pull.

### Water's anomalous behavior

Each water molecule can form up to **four hydrogen bonds** (two through its own O–H bonds as a donor, two through its oxygen lone pairs as an acceptor) — more than almost any other small molecule. ==This extensive hydrogen-bonding network is the single cause behind every one of water's "anomalous" properties==, which would otherwise be surprising for a molecule as small as $\ce{H2O}$ (molar mass 18 g/mol):

- an unusually **high melting point and boiling point** compared to $\ce{H2S}$, $\ce{NH3}$, or $\ce{HF}$ of similar or larger size (see Figure 11.3, below),
- an unusually **high specific heat** (4.184 J/g·°C — this is why oceans and lakes moderate regional climate), and
- **maximum density at 4 °C**, not at its freezing point — ice's open hydrogen-bonded lattice is actually *less* dense than liquid water, which is why ice floats and lakes freeze from the top down, insulating aquatic life below.

![Line chart comparing normal boiling points of period 2-5 hydrides in groups 14, 15, 16, and 17](../assets/hydride_boiling_points.svg)
*Figure 11.3 — Group 14 hydrides (no hydrogen bonding) follow a smooth, steadily increasing trend with size. NH₃, H₂O, and HF each sit far above where their own group's trend would otherwise put them — the extra lift is hydrogen bonding, and water's is the largest of the three. Self-generated with matplotlib from verified literature boiling points.*

:::info
Water's expansion on freezing is the same hydrogen-bonding effect that gives ice its negative melting-point/pressure slope in the phase diagram — see Section 11.4.
:::

**Self-check:**
- Why does breaking a paper towel's capillary wicking require making adhesion weaker than cohesion (e.g., coating the fibers with wax)?
- If water had no hydrogen bonding at all (imagine a hypothetical nonpolar $\ce{H2O}$), would you expect its boiling point to be higher or lower than −80 °C (roughly where the Group 16 hydride trend predicts it should fall)?

## 11.3 Solids{{attrs[#blk-ch11sec03]}}

:::success
**Learning Objectives**
- Distinguish crystalline solids from amorphous solids.
- Classify a solid as molecular, covalent-network, ionic, or metallic from the bonds holding it together, and predict its hardness, melting point, and conductivity.
- Count atoms per unit cell and calculate coordination number for simple cubic, body-centered cubic, and face-centered cubic lattices.
:::

A **crystalline solid** has long-range, repeating order — its atoms, ions, or molecules occupy specific, predictable positions. An **amorphous solid**, such as glass, lacks that long-range order even though it is rigid.

### Four types of crystalline solids

| Type | Held together by | Hardness | Melting point | Conductivity | Examples |
|---|---|---|---|---|---|
| Molecular | Intermolecular forces | Soft | Low | Poor | $\ce{Ar}$, $\ce{H2O}$ (ice), $\ce{CO2}$ (dry ice) |
| Covalent network | Covalent bonds throughout | Hard | High | Poor (graphite is the exception) | Diamond, graphite, quartz |
| Ionic | Ionic bonds | Hard, brittle | High | Poor solid; good when molten/dissolved | $\ce{NaCl}$, $\ce{MgCl2}$ |
| Metallic | Metallic bonds | Soft to hard | Low to high | Good | $\ce{Fe}$, $\ce{Cu}$, $\ce{Hg}$ |

![Sodium chloride's ionic lattice, shown as a 3D ball-and-stick model](../assets/nacl_ionic_lattice.png =520x)
*Figure 11.4 — In an ionic solid such as NaCl, each ion is surrounded by six oppositely charged ions in a rigid, repeating lattice — the electrostatic attraction extends through the whole crystal, which is why ionic solids are hard, brittle, and high-melting. Source: Benjah-bmm27, via Wikimedia Commons (public domain).*

![A quartz crystal specimen (SiO2), an example of a covalent-network solid](../assets/quartz_crystal.jpg =520x)
*Figure 11.5 — Quartz (SiO₂) is a covalent-network solid: every Si and O atom is linked into one continuous three-dimensional network of covalent bonds, giving it the hardness needed to scratch glass and a melting point above 1,600 °C. Source: Masha Milshina, via Wikimedia Commons, CC BY 4.0.*

### Unit cells

A **unit cell** is the smallest repeating structural unit of a crystal lattice; stacking copies of it in three dimensions builds the entire crystal. There are seven unit-cell shapes in total, but general chemistry focuses on the three **cubic** cells:

![Simple cubic, body-centered cubic, and face-centered cubic unit cells, shown as 3D wireframes with atoms at their lattice positions](../assets/cubic_unit_cells.svg)
*Figure 11.6 — The three cubic unit cells. Corner atoms are shared among 8 adjacent cells; a face atom is shared between 2 cells; a body-centered atom belongs entirely to its own cell. Self-generated with matplotlib.*

| Unit cell | Atoms per cell | Coordination number | How atoms touch |
|---|---|---|---|
| Simple cubic (SCC) | 1 | 6 | along the cell edge |
| Body-centered cubic (BCC) | 2 | 8 | along the cube diagonal |
| Face-centered cubic (FCC) | 4 | 12 | along the face diagonal |

The **coordination number** is the number of nearest neighbors surrounding one atom in the lattice. Counting atoms *per cell* requires accounting for sharing: a corner atom counts $\frac{1}{8}$ toward its cell (shared among 8 cells meeting at that corner), a face atom counts $\frac{1}{2}$ (shared between 2 cells), and a body-centered atom counts fully (not shared at all).

**Close packing** — the most space-efficient way to stack spheres — comes in two forms: hexagonal close-packed (an "ABAB…" stacking pattern) and cubic close-packed (an "ABCABC…" pattern, which is geometrically identical to the FCC unit cell).

:::: tabs
::: tab Problem
Verify the atom count for a body-centered cubic (BCC) unit cell: 8 corner atoms plus 1 body-centered atom. How many atoms belong to the cell in total?
:::
::: tab Solution
Each of the 8 corner atoms is shared among 8 unit cells, so each contributes $\frac{1}{8}$ atom to this cell:

$$8 \times \frac{1}{8} = 1\ \text{atom from the corners}$$

The single body-centered atom is not shared with any other cell, so it contributes a full atom:

$$1 \times 1 = 1\ \text{atom from the center}$$

$$\text{Total} = 1 + 1 = 2\ \text{atoms per BCC unit cell}$$

This matches the table above, and is why the coordination number (8, from the atoms touching along the cube diagonal) is higher than a simple cubic cell's (6) despite BCC having the same corner arrangement — the added body atom touches all 8 corner atoms directly.
:::
::::

**Self-check:**
- How many atoms belong to a face-centered cubic (FCC) unit cell? (Hint: 8 corner atoms + 6 face atoms, using the sharing fractions above.)
- Why is graphite a good electrical conductor even though it is classified as a covalent-network solid, unlike diamond?

## 11.4 Phase Changes and Diagrams{{attrs[#blk-ch11sec04]}}

:::success
**Learning Objectives**
- Define evaporation, condensation, dynamic equilibrium, and equilibrium vapor pressure.
- Calculate heat absorbed or released during a phase change using molar heat of vaporization, fusion, or sublimation.
- Apply the Clausius–Clapeyron equation to relate vapor pressure and temperature.
- Interpret a phase diagram, including the triple point and critical point.
:::

A **phase** is a physically distinct, uniform region of a substance (solid, liquid, or vapor). A **phase change** occurs when energy is added to or removed from a substance, without changing its chemical identity.

### Liquid–vapor equilibrium

At any given temperature, some molecules at a liquid's surface have enough kinetic energy to escape into the vapor phase — **evaporation**. Some vapor molecules simultaneously return to the liquid — **condensation**. In a sealed container, these two rates eventually become equal: a **dynamic equilibrium**, where both processes continue but the *amounts* of liquid and vapor no longer change. The vapor pressure at this equilibrium is the **equilibrium vapor pressure**, and it depends only on temperature and the substance's identity (not on the amount of liquid present).

The **molar heat of vaporization** ($\Delta H_\text{vap}$) is the energy needed to vaporize one mole of liquid — a direct measure of how strongly a liquid's molecules attract each other (larger $\Delta H_\text{vap}$ means stronger intermolecular forces).

:::: tabs
::: tab Problem
The molar heat of vaporization of water is 40.66 kJ/mol. How much heat is absorbed when 10.0 g of water boils away?
:::
::: tab Solution
First convert grams of water to moles:

$$10.0\ \text{g}\ \ce{H2O} \times \frac{1\ \text{mol}\ \ce{H2O}}{18.0\ \text{g}\ \ce{H2O}} = 0.556\ \text{mol}\ \ce{H2O}$$

Then multiply by the molar heat of vaporization:

$$0.556\ \text{mol} \times 40.66\ \text{kJ/mol} = 22.6\ \text{kJ absorbed}$$

Notice the units track exactly as in a Chapter 3 stoichiometry problem or a Chapter 6 enthalpy problem — mass converts to moles, then moles convert to the desired quantity (here, heat) using a per-mole conversion factor ($\Delta H_\text{vap}$).
:::
::::

### The Clausius–Clapeyron equation

Because $\Delta H_\text{vap}$ links a liquid's vapor pressure to its temperature, we can relate vapor pressure at two different temperatures directly:

$$\ln\frac{P_1}{P_2} = \frac{\Delta H_\text{vap}}{R}\left(\frac{T_1 - T_2}{T_1 T_2}\right)$$

{{sp[warning] Reminder}} both $T_1$ and $T_2$ must be in **kelvin** before you substitute — the same habit from Chapter 5's ideal gas law.

![Vapor pressure of diethyl ether plotted against temperature, computed from the Clausius-Clapeyron equation](../assets/vapor_pressure_diethyl_ether.svg)
*Figure 11.7 — The vapor pressure of diethyl ether rises steeply and non-linearly with temperature, crossing 760 mmHg (1 atm, its normal boiling point) at about 35 °C. Curve computed from the Clausius–Clapeyron equation using the worked example's data. Self-generated with matplotlib.*

:::: tabs
::: tab Problem
Diethyl ether ($\ce{CH3CH2OCH2CH3}$) has a vapor pressure of 400 mmHg at 27 °C and a molar heat of vaporization of 26.0 kJ/mol. Calculate its vapor pressure at 77 °C.

{{smiles CCOCC}}
:::
::: tab Solution
Convert both temperatures to kelvin ($T_1 = 300\ \text{K}$, $T_2 = 350\ \text{K}$) and substitute into the Clausius–Clapeyron equation:

$$\ln\left(\frac{400\ \text{mmHg}}{P_2}\right) = \frac{26.0\times10^3\ \text{J/mol}}{8.314\ \text{J/K·mol}}\left(\frac{1}{350\ \text{K}} - \frac{1}{300\ \text{K}}\right)$$

$$\ln\left(\frac{400\ \text{mmHg}}{P_2}\right) = -1.489$$

$$\frac{400\ \text{mmHg}}{P_2} = e^{-1.489} = 0.226$$

$$P_2 = \frac{400\ \text{mmHg}}{0.226} = 1{,}770\ \text{mmHg}$$

As expected, vapor pressure rises sharply with temperature — nearly 4.5-fold from 27 °C to 77 °C for this substance.
:::
::::

### Liquid–solid and solid–vapor equilibrium

The **melting point** (solid → liquid) and **freezing point** (liquid → solid) describe the same equilibrium temperature, and the **molar heat of fusion** ($\Delta H_\text{fus}$) is the energy needed to melt one mole of solid. The **molar heat of sublimation** ($\Delta H_\text{sub}$, solid directly to vapor) follows Hess's law exactly as in Chapter 6:

$$\Delta H_\text{sub} = \Delta H_\text{fus} + \Delta H_\text{vap}$$

### Phase diagrams

A **phase diagram** maps out which phase (solid, liquid, or vapor) is stable at every combination of temperature and pressure.

![Schematic phase diagram of water, with the solid, liquid, and vapor regions labeled and the triple point, normal melting/boiling points, and critical point marked](../assets/water_phase_diagram.svg)
*Figure 11.8 — Phase diagram of water. The solid-liquid boundary has a slight negative slope — unique among common substances — because ice is less dense than liquid water, so increasing pressure favors the denser liquid phase and lowers the melting point. Self-generated with matplotlib; boundary shapes are schematic, but all four labeled points (triple, normal melting, normal boiling, and critical) are real, verified values. Data summary: triple point 0.01 °C at 0.00604 atm; normal melting point 0 °C at 1 atm; normal boiling point 100 °C at 1 atm; critical point 374 °C at 218 atm.*

Two points are worth memorizing conceptually:
- The **triple point** is the single temperature/pressure combination where all three phases coexist in equilibrium simultaneously.
- The **critical point** marks the temperature and pressure above which liquid and vapor become indistinguishable — no amount of pressure can liquefy a gas above its **critical temperature**.

:::warning
Water's negative-sloped solid-liquid boundary is the *exception*, not the rule — for nearly every other substance, increasing pressure on a solid favors the (denser) solid phase and *raises* the melting point. Water is unusual because hydrogen bonding makes its solid phase (ice) *less* dense than its liquid phase.
:::

**Self-check:**
- Using the phase diagram above, what phase change occurs if you start at 0.001 atm and −40 °C and slowly raise the temperature at constant pressure?
- Why does increasing pressure on ice (e.g., under an ice skate) very slightly lower its melting point, while doing the same to a block of paraffin wax would raise its melting point?

## Synthesis

==Every idea in this chapter is downstream of one fact: which intermolecular force (or combination of forces) acts between a substance's particles.== That single fact sets the strength of attraction, and the strength of attraction sets everything measurable that follows — how strongly a liquid resists spreading out (surface tension) or flowing (viscosity), how a solid is classified and how hard and high-melting it is, and how much energy is required to pry the particles apart into a gas (heats of fusion, vaporization, and sublimation, and the shape of the phase diagram itself). Water's unusual behavior throughout this chapter — its high boiling point, its high specific heat, its expansion on freezing, its negative-sloped solid-liquid phase boundary — is not four unrelated facts but one fact (extensive hydrogen bonding) appearing four times.

## Asset and License Record for This Chapter

| Asset | Source URL | License | Attribution |
|---|---|---|---|
| `assets/polar_nonpolar_molecules.svg` | — (self-generated, RDKit) | CC BY 4.0 | Self-generated; released under this package's CC BY 4.0 license. |
| `assets/hydride_boiling_points.svg` | — (self-generated, matplotlib) | CC BY 4.0 | Self-generated from verified literature boiling points; released under this package's CC BY 4.0 license. |
| `assets/water_strider_surface_tension.jpg` | https://commons.wikimedia.org/wiki/File:A_water_strider_stands_on_the_water_because_of_its_light_weight_and_the_surface_tension_of_the_water._(3116c804-0240-4b9a-b937-70fc7c2b156e).jpg | Public domain | NPS Photo, via Wikimedia Commons. |
| `assets/nacl_ionic_lattice.png` | https://commons.wikimedia.org/wiki/File:Lattice-enthalpy-NaCl-3D-ionic.png | Public domain | Benjah-bmm27, via Wikimedia Commons. |
| `assets/quartz_crystal.jpg` | https://commons.wikimedia.org/wiki/File:Grape_quartz_04.jpg | CC BY 4.0 | Masha Milshina, via Wikimedia Commons. |
| `assets/cubic_unit_cells.svg` | — (self-generated, matplotlib) | CC BY 4.0 | Self-generated; released under this package's CC BY 4.0 license. |
| `assets/vapor_pressure_diethyl_ether.svg` | — (self-generated, matplotlib) | CC BY 4.0 | Self-generated from the Clausius–Clapeyron equation and this study guide's own worked-example data; released under this package's CC BY 4.0 license. |
| `assets/water_phase_diagram.svg` | — (self-generated, matplotlib) | CC BY 4.0 | Self-generated; boundary curves schematic, key points from verified real data; released under this package's CC BY 4.0 license. |
