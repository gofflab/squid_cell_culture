# Track 3: Neural Stem Cell Maintenance and Neurogenic Differentiation

## Version 2.0

---

## Conceptual Framework

The white body is a neurogenic tissue. In vivo, proliferating neural stem cells (Sox2+/Ascl1+/Pcna+) transition through committed progenitors (Ascl1+/Ngn+) to postmitotic specified neuroblasts (Elav+/Vacht+/Ty3h+) that migrate via defined streams to populate the brain (Stock, Hally et al.). This endogenous program is the biological foundation for this track.

The challenge is not neural induction. It is controlling which part of the trajectory cells occupy in vitro:

- **Arm 3A**: Hold cells in the early, proliferative NSC state (for expansion, banking, and immortalization).
- **Arm 3B**: Allow or support the full trajectory through to mature, functional neurons (for neuroscience applications).

---

## Arm 3A: Neural Stem Cell Maintenance

### Aim

Identify culture conditions that maintain white body cells as proliferating neural stem cells (Sox2+/Pcna+/Ascl1+/Elav-) for at least 7 days, with sustained F-ara-EdU incorporation.

### Rationale

In vivo, NSCs reside in the core of the neurogenic white body and express Sox2, Diachete, Pax6, alongside proliferation markers (Mcm2-7, E2f3, Ki67-like). The signaling environment includes Wnt pathway components (Fzd1, Fzd4, Wnt8b, Apc, Axin1, Gsk3b) and Notch pathway components at mid-pseudotime. Removing cells from this niche likely drives premature differentiation. The goal is to pharmacologically recapitulate the niche signals that maintain the stem cell state.

### Experimental Design

**Source**: Hatchling white body cells, 0-3 days post-hatching (maximum neurogenic activity). Pool anterior and posterior for this screen (larger cell numbers).

**Plating**: 2-5 x 10^4 cells/well on poly-D-lysine-coated 24-well glass bottom plates. Allow 12-24 hours attachment in Media D before switching to experimental conditions.

**Conditions** (each in triplicate, minimum 3 biological replicates = 3 animals):

| # | Condition | Composition | Rationale |
|---|---|---|---|
| 1 | Baseline | Media D (FGF 10 + EGF 100 ng/mL + ITS-G) | Kim et al. standard; reference for all comparisons |
| 2 | Wnt activation | Media D + CHIR99021 3 uM | GSK3beta inhibition activates Wnt; Wnt components expressed in WB |
| 3 | Wnt + anti-anoikis | Media D + CHIR99021 3 uM + Y-27632 10 uM | ROCK inhibition prevents dissociation-induced apoptosis |
| 4 | Notch activation | Media D + recombinant Jagged-1 Fc 1 ug/mL (R&D Systems, 1277-JG) | Notch maintains NSC pools across taxa; Notch expressed in WB mid-pseudotime |
| 5 | Wnt + Notch | Media D + CHIR99021 3 uM + Jagged-1 Fc 1 ug/mL + Y-27632 10 uM | Combined pathway activation |
| 6 | SHH pathway | Media D + SAG 1 uM (Tocris, 4366) | Hedgehog signaling maintains vertebrate neurogenic niches |
| 7 | FGF high dose | Media D with FGF increased to 50 ng/mL | FGF is a conserved NSC mitogen |
| 8 | Hemolymph | Media D + 5% filtered E. berryi hemolymph plasma | Endogenous niche-derived factors |
| 9 | Notch inhibition (negative control) | Media D + DAPT 10 uM (Tocris, 2634) | Gamma-secretase inhibitor should accelerate differentiation; validates assay |

**Media changes**: every 2 days with fresh supplements.

### Readouts

**Day 1, 3, 5, 7 post-switch**:

1. **F-ara-EdU incorporation** (primary readout): 1 uM F-ara-EdU, 4-hour pulse at each timepoint (one replicate per timepoint). Fix, click chemistry, Hoechst counterstain. Quantify % EdU+ nuclei from 5 fields at 20x per well. Automated counting preferred (CellProfiler or equivalent).

2. **RT-qPCR** (Day 3, Day 7): Harvest RNA from one replicate. Assess:
   - NSC markers: Sox2, Ascl1 (EB45560), Pcna
   - Differentiation markers: Ngn (EB09075), Elav (EB33473)
   - Proliferation: Ki67-like (EB12028)
   - Compute NSC retention index = geometric mean(Sox2, Ascl1, Pcna) / Elav. Values >1 = NSC-biased. Values <1 = differentiation-biased.

3. **Phase contrast morphology**: daily imaging. Score cell morphology as round/compact (NSC-like) vs. process-bearing (differentiating neuroblast) vs. spread/flat (fibroblast-like or hemocyte).

### Success Criteria

- At least one condition maintains >15% F-ara-EdU+ cells at Day 5.
- NSC retention index >1 at Day 7 in at least one condition.
- DAPT negative control shows accelerated differentiation (increased Elav, decreased Pcna) relative to baseline, confirming assay sensitivity.

### Expected Outcome

Based on the in vivo biology, Wnt activation (CHIR99021) is the most likely candidate to maintain NSC state, given the strong expression of Wnt pathway components in the neurogenic white body. The combination of CHIR99021 + Y-27632 (Condition 3) may give the best survival and proliferation. If hemolymph (Condition 8) outperforms defined factor conditions, this suggests critical niche signals not yet identified, warranting proteomic analysis of hemolymph plasma.

---

## Arm 3B: Neurogenic Differentiation to Mature Neurons

### Aim

Demonstrate that white body cells can complete the endogenous neurogenic program in vitro, generating postmitotic neurons (Elav+/Pcna-) with process extension, neurotransmitter marker expression, and ideally functional electrical activity.

### Rationale

The in vivo differentiation trajectory proceeds from NSCs through Ascl1/Ngn-expressing committed progenitors to Elav+ neurons that express Vacht (cholinergic) and Ty3h (catecholaminergic). Migrating neuroblasts are postmitotic (Pcna-) but retain Sox2 expression transiently. The key question is whether this trajectory proceeds in vitro when cells are removed from the white body and deprived of their normal migration context.

### Experimental Design

**Step 1: Expansion phase** (Days 0-5): Culture white body cells in the best NSC maintenance condition from Arm 3A. Goal: establish a proliferating population.

**Step 2: Differentiation switch** (Day 5 onwards): Transfer cells to differentiation-permissive conditions:

| # | Condition | Composition | Rationale |
|---|---|---|---|
| 1 | Growth factor withdrawal | Media C + ITS-G (no FGF, no EGF, no serum) | Remove mitogenic signals; allow endogenous program |
| 2 | GF withdrawal + laminin | Media C + ITS-G, on laminin substrate (5 ug/mL) | Laminin supports neurite extension and migration |
| 3 | GF withdrawal + neurotrophins | Media C + ITS-G + BDNF 20 ng/mL (PeproTech, 450-02) + NT-3 20 ng/mL (PeproTech, 450-03) | Neurotrophic support for maturing neurons |
| 4 | Brain-conditioned media | Media C + 10% filtered E. berryi brain homogenate supernatant | Target-derived signals for neuronal maturation |
| 5 | Forskolin + ascorbic acid | Media C + ITS-G + forskolin 10 uM (Tocris, 1099) + ascorbic acid 200 uM | cAMP elevation promotes neuronal maturation; ascorbic acid is neuroprotective |
| 6 | Maintained in NSC conditions (negative control) | Best Arm 3A condition | Should remain undifferentiated; validates assay directionality |

**Prepare brain-conditioned media**: Dissect 5 E. berryi hatchling brains. Homogenize in 1 mL Media C using a pellet pestle. Incubate 24 hours at 22C. Centrifuge 10,000 x g, 10 min. Filter supernatant through 0.20 um. Store at -80C in aliquots. Add 10% v/v to Media C before use.

### Readouts

**Day 1, 3, 7, 14 post-differentiation switch**:

1. **Phase contrast morphology**: Quantify neurite outgrowth.
   - Definition of a neurite: process extending >2x cell body diameter.
   - Measure: % cells with neurites, average neurite length per cell, number of branch points per cell (ImageJ/FIJI, NeuronJ plugin or Simple Neurite Tracer).

2. **RT-qPCR** (Day 3, 7, 14 post-switch): Full pseudotime marker panel:
   - Early (should decrease): Pcna, Ki67-like (EB12028), Mcm6
   - Mid (should peak then decrease): Ascl1, Ascl1m, Sox2
   - Late (should increase): Ngn, Lhx1, Lhx3, Nkx2.1, Nkx2.2, Pax6
   - Terminal (should appear last): Elav (EB33473), Vacht, Ty3h
   
   A successful differentiation recapitulates the in vivo pseudotime ordering: sequential appearance of these markers over the 14-day culture period.

3. **HCR in situ hybridization** (Day 7 and 14): Multiplex for Ascl1 + Elav + Pcna (3 channels). This visualizes the spatial relationship between undifferentiated (Pcna+/Ascl1+) and differentiated (Elav+/Pcna-) cells within the same well.

4. **Calcium imaging** (Day 14):
   - Load with Fluo-4 AM 2-5 uM (Thermo Fisher, F14201) in Media C for 30-45 min at 22C.
   - Wash 3x with recording medium (see electrophysiology solutions below).
   - Image on fluorescence microscope at 1-10 Hz acquisition rate.
   - Stimulate with high K+ (25-50 mM KCl in recording medium, rapid perfusion or bolus addition).
   - Also test: acetylcholine (100 uM), glutamate (100 uM), GABA (100 uM) for neurotransmitter responsiveness.
   - Score: % of cells showing >2x baseline fluorescence increase within 30 seconds of stimulation.

5. **Electrophysiology** (Day 14-21, if process-bearing cells are present):

   **Extracellular recording solution** (adapted for marine invertebrate cells):
   - NaCl 420 mM
   - KCl 10 mM
   - CaCl2 10 mM
   - MgCl2 50 mM
   - HEPES 10 mM
   - pH 7.8, osmolality ~950 mOsm/kg

   **Intracellular recording solution**:
   - K-gluconate 120 mM
   - KCl 20 mM
   - MgCl2 2 mM
   - EGTA 1 mM
   - HEPES 10 mM
   - pH 7.2 (KOH), osmolality ~280 mOsm/kg

   **Note**: The large osmolality difference between extracellular (~950) and intracellular (~280) solutions is correct and reflects the biological reality of marine invertebrate cells, which maintain standard intracellular ionic conditions despite the high-osmolality extracellular environment.

   **Protocol**:
   - Use borosilicate glass electrodes pulled to 3-7 MOhm resistance.
   - Aim for >1 GOhm seal.
   - Whole-cell configuration.
   - Current-clamp: assess resting membrane potential. Inject depolarizing current steps (10-200 pA, 500 ms) to test for action potential generation.
   - Voltage-clamp: step from -80 mV to +40 mV in 10 mV increments. Look for voltage-gated Na+ and K+ currents.

### Success Criteria

- **Morphological**: >20% of cells with neurites (>2x cell body diameter) by Day 14 in at least one condition.
- **Molecular**: Elav expression increases >5-fold relative to Day 0 at Day 14. Pcna expression decreases >5-fold. Pseudotime marker ordering is recapitulated.
- **Functional**: Detectable calcium transients in response to high K+ depolarization in >10% of process-bearing cells.
- **Electrophysiological** (aspirational): Voltage-gated currents or action potentials in at least one recorded cell. This would be a landmark result.

### Subtype-Specific Differentiation

If Arm 3B succeeds, a secondary goal is to assess whether anterior and posterior white body cultures generate different neuronal subtypes:

- Culture anterior and posterior white body cells separately (Track 1 dissection protocol).
- Apply the best differentiation condition from Arm 3B.
- At Day 14: compare expression of regional markers:
  - Anterior-derived: Vvl, Lhx1, Nkx2.1, Foxg1 (supraesophageal brain neuron identity)
  - Posterior-derived: Ems/Emx, Lhx3, Foxn4, Six4 (optic lobe neuron identity)
- If regional identity is maintained in culture, this demonstrates that subtype specification is intrinsic to white body territories and persists ex vivo, consistent with the transplant experiments in vivo (Stock, Hally et al.).

---

## Risk Assessment

| Risk | Probability | Impact | Mitigation |
|---|---|---|---|
| No condition maintains NSC state >5 days (Arm 3A) | MODERATE (40%) | Cannot expand NSCs; limits utility | Test broader condition panel including hypoxia, 3D culture, explant co-culture |
| Cells differentiate too rapidly to capture NSC window | MODERATE (30%) | NSC expansion not possible | Shorten attachment phase; add CHIR99021 from the moment of plating |
| Differentiation stalls at progenitor stage (Arm 3B) | MODERATE (35%) | Get Ascl1+ cells but not Elav+ neurons | Extend culture to 21-28 days; test brain-conditioned media; add cAMP analogs |
| No functional activity (calcium, electrophysiology) | MODERATE (40%) | Morphological but not functional neurons | Extend maturation to 28+ days; optimize substrate (laminin + poly-ornithine); test co-culture with brain tissue |
| Regional identity lost in culture | LOW-MODERATE (25%) | Cannot demonstrate subtype specificity | Shorter culture periods; begin subtype analysis at Day 7 rather than Day 14 |
