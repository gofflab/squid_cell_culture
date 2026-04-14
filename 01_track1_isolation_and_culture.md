# Track 1: White Body Isolation and Primary Culture

## Version 2.0

---

## Aims

**Aim 1.1**: Establish reliable isolation of white body cells from E. berryi hatchlings with defined cell identity.

**Aim 1.2**: Optimize culture conditions that maintain cell viability, molecular identity, and proliferative capacity.

**Aim 1.3**: Develop passage and cryopreservation protocols.

---

## Aim 1.1: White Body Cell Isolation

### 1.1.1 Animal Selection and Staging

The neurogenic compartment of the white body predominates in hatchlings and diminishes with developmental age (Claes 1996; Stock, Hally et al.). Hatchlings (0-7 days post-hatching) are the primary source material for all neurogenic culture work. Older animals (juveniles 2-4 weeks, subadults 1-3 months) are included for age-comparison studies and to assess how the neurogenic-to-hematopoietic ratio shifts with development.

| Age class | N animals | Primary use |
|---|---|---|
| Hatchlings (0-7 dph) | 30-40 | Primary culture optimization, NSC maintenance, differentiation |
| Juveniles (2-4 weeks) | 15-20 | Age comparison, larger tissue yield |
| Subadults (1-3 months) | 10-15 | Age comparison, hematopoietic enrichment control |

### 1.1.2 Euthanasia

Anesthetize in 1:1 mixture of 7.5% MgCl2 (Fisher Scientific, M33-500) in deionized water and filtered natural seawater (FNSW) for 30 minutes. Confirm cessation of chromatophore activity, loss of righting reflex, and absence of respiratory movements. Confirm death by decapitation or brain destruction.

**Note**: This replaces the 5% ethanol protocol used in Kim et al. (2025). MgCl2 anesthesia has broader regulatory acceptance and does not introduce fixative into tissues. This is the method used in Stock, Hally et al. for all experimental procedures.

### 1.1.3 Pre-Dissociation Wash

Before dissection, wash the intact euthanized animal:
1. Rinse 3x in sterile FNSW.
2. Transfer to sterile sylgard dissection dish.

### 1.1.4 White Body Dissection

The white body is a 4-lobed structure located between the eyes and optic lobes, surrounding the optic stalk. In hatchlings it is pale/whitish, soft, and glandular.

**Procedure:**
1. Pin animal on sylgard dish.
2. Remove the eye by making an incision around the posterior aspect with fine scissors (Vanas Spring Scissors, Fine Science Tools, 15000-08).
3. Identify the optic lobe (posterior to the eye).
4. The white body is medial to the optic lobe. Using Dumostar-Biology Number 55 forceps (Fine Science Tools, 11295-51), carefully separate the white body from surrounding connective tissue.
5. **Separate anterior from posterior white body.** The anterior territory (ventral-anterior) contributes to the supraesophageal brain via the anterior migratory stream. The posterior territory contributes to the optic lobe via the posterior stream. These are molecularly distinct and should be cultured separately.
6. Place each tissue fragment into a separate well of a 24-well glass bottom plate (Cellvis, P24-1.5H-N) containing 500 uL DBSS (see 06_reagents_and_media.md, Section 2.2).
7. Document each dissection with photographs.
8. Repeat for the contralateral side.

**Training requirement**: Practice dissections on at least 10 animals before initiating culture experiments. Fix 5 dissected white bodies in 4% PFA/FNSW for histological validation of tissue identity (paraffin sections, H&E). Score each dissection for optic lobe contamination and white body integrity.

**Expected yield**: From a single hatchling white body (bilateral), expect 0.5-2 x 10^5 total cells after dissociation (estimated from Kim et al. yields for optic lobes, which are comparable in size). Cell numbers will be lower from anterior vs. posterior fragments.

### 1.1.5 Tissue Dissociation and Cell Isolation

Follow the Kim et al. (2025) protocol with modifications:

1. Incubate tissue in DBSS at 22C for 30 minutes with gentle rocking every 5-10 minutes (disinfection step).
2. Transfer tissue to a clean well. Save the DBSS well (cells dissociate during disinfection).
3. Add 500 uL Trypsin-EDTA Solution A (0.25% trypsin, 0.02% EDTA in MCMFS) to tissue. Incubate at 22C for 15 minutes. Gently triturate 5x with a P1000 pipette at the 7-minute mark.
   - **Note**: White body tissue may require longer digestion than optic lobes. If tissue remains largely intact at 15 minutes, extend to 20 minutes maximum.
   - **Alternative enzyme**: If trypsin yields low viability, test collagenase IV (1 mg/mL in MCMFS, 30 minutes, Worthington LS004186) or papain (as used by Maselli et al. 2018 for O. vulgaris neurons).
4. Neutralize with 1 mL Squid Growth Media B.
5. Leave for 15 minutes.
6. Remove tissue fragments with sterile forceps. Transfer fragments to a new well with Media C for 1 hour (additional cell release). Repeat to new well with Media D overnight.
7. Wash all cell-containing wells 2x with Media C to remove debris. Replace with experimental growth media.
8. Culture at 22C, ambient CO2. L-15-based media does not require CO2 supplementation.
9. Check for cell attachment at 2, 6, 12, and 24 hours.

### 1.1.6 Cell Counting and Viability

- Mix 10 uL cell suspension with 10 uL trypan blue (0.4%).
- Count on hemocytometer or automated cell counter.
- Record: total cells, viable cells, viability percentage.
- For adherent cultures: estimate attached cells from 5 random fields at 20x magnification per well.

---

## Aim 1.2: Culture Condition Optimization

### 1.2.1 Experimental Design

Run as a structured optimization across 3-5 animals per experiment. For each animal, plate anterior and posterior white body cells separately.

**Media conditions** (each in duplicate wells):

| Condition | Base media | Supplements | Rationale |
|---|---|---|---|
| A: Baseline | Media D | FGF 10 ng/mL + EGF 100 ng/mL + ITS-G | Kim et al. standard |
| B: Wnt activation | Media D | As A + CHIR99021 3 uM (Tocris, 4423) | Wnt pathway active in WB (Fzd1, Fzd4, Wnt8b); maintains NSC self-renewal |
| C: Combined NSC | Media D | As A + CHIR99021 3 uM + Y-27632 10 uM (Tocris, 1254) | Anti-anoikis + Wnt activation |
| D: Hematopoietic | Media D | As A + SCF 50 ng/mL (PeproTech, 300-07) + TPO 50 ng/mL (PeproTech, 300-18) | Hematopoietic growth factors for the Nkx2.5+ compartment |
| E: Hemolymph | Media D | As A + 5% filtered E. berryi hemolymph plasma | Endogenous niche factors |
| F: High serum | Media D | As A + 10% FBS (R&D Systems, S11150H) | Enhanced survival, broad mitogenic support |
| G: Differentiation permissive | Media C | ITS-G only, no growth factors, no serum | Allow endogenous neurogenic program to proceed |
| H: Growth factor withdrawal + laminin | Media C | ITS-G, laminin-coated substrate (5 ug/mL) | Permissive differentiation on migratory substrate |

**Substrate conditions** (run in Media D, Condition A):

| Substrate | Preparation | Rationale |
|---|---|---|
| Uncoated glass | None | Baseline (Kim et al.) |
| Poly-D-lysine | 100 ug/mL, coat overnight 4C, wash 3x dH2O | Maselli et al. 2018 for O. vulgaris neurons |
| Laminin | 5 ug/mL in MBSS, coat 2 hours 22C | Migratory substrate for neuroblasts |
| Fibronectin | 10 ug/mL in MBSS, coat 2 hours 22C | Alternative ECM |

**Total per animal**: 8 media conditions x 2 (anterior/posterior) x 2 replicates = 32 wells, plus 4 substrate conditions x 2 x 2 = 16 wells. Three to four 24-well plates per animal.

### 1.2.2 Readouts

**Day 1 (24 hours)**:
- Phase contrast imaging: all wells. Document morphology, attachment, spreading.
- F-ara-EdU incorporation: add 1 uM F-ara-EdU (Vector Laboratories, CCT-1403-5) to one replicate of each condition for 4 hours. Fix in 4% PFA/MBSS (15 min, 22C). Perform click chemistry detection (see 05_track5_proliferation_analysis.md for protocol). Counterstain with Hoechst. Quantify percentage F-ara-EdU+ nuclei.

**Day 3 (72 hours)**:
- Phase contrast imaging.
- Live/dead: calcein-AM 2 uM + ethidium homodimer 4 uM (Thermo Fisher, L3224), 30 minutes, 22C. Quantify viability.
- RT-qPCR on remaining replicate: harvest RNA (TRIzol or RNeasy Micro). Assess: Sox2, Ascl1, Pcna, Elav, Nkx2.5, and a housekeeping gene (actin or EF1alpha homolog from E. berryi transcriptome). Normalize to Day 0 (freshly isolated cells).

**Day 5 (120 hours)**:
- Fix all remaining wells in 4% PFA/MBSS.
- HCR for Sox2 + Ascl1 (or Pcna + Elav) to assess spatial distribution of NSC vs. differentiated cells within wells.
- Phase contrast imaging before fixation.

**Day 7** (for conditions with viable cells):
- F-ara-EdU pulse (second replicate if available), same protocol as Day 1.
- RT-qPCR for full marker panel (see 00_project_overview.md, Molecular Identity Panel).

### 1.2.3 Analysis

For each condition, quantify:
1. Cell attachment density (cells/mm^2) at 24 hours.
2. Viability (%) at 72 hours.
3. F-ara-EdU incorporation (% EdU+) at Day 1 and Day 7.
4. NSC retention score: (Sox2 + Ascl1 expression at Day 3) / (Sox2 + Ascl1 expression at Day 0), by RT-qPCR. Values near 1.0 indicate maintained NSC identity; values approaching 0 indicate loss.
5. Differentiation score: Elav expression at Day 3 / Elav expression at Day 0. Values >1 indicate neuronal differentiation proceeding in culture.
6. Hematopoietic drift: Nkx2.5 expression relative to Day 0.

Statistical analysis: Two-way ANOVA (media x region [anterior/posterior]) with biological replicate as random effect. Minimum N = 3 animals.

### 1.2.4 Go/No-Go Criteria

**GO to Tracks 2-4**: At least one condition yields cells that (a) remain attached and viable (>50%) at Day 5, (b) show >0% F-ara-EdU incorporation at Day 1, and (c) express Sox2 or Ascl1 by RT-qPCR at Day 3.

**CONDITIONAL GO**: Cells survive at Day 5 but no F-ara-EdU incorporation. Proceed with modified conditions: test hypoxia (5% O2), 3D culture (Matrigel embedding), or co-culture with brain-derived feeder cells. Return to optimization before advancing other tracks.

**NO-GO**: No condition yields viable attached cells beyond Day 3 across multiple animals. Consider switching to optic lobe cells (Kim et al. validated system) as fallback source.

---

## Aim 1.3: Passage and Cryopreservation

### 1.3.1 Passage Protocol

**Prerequisite**: A culture condition from Aim 1.2 that maintains viable cells for 5+ days with detectable proliferation.

**Method A: Mechanical scraping** (per Kim et al.):
1. Remove media. Wash 1x with Media C.
2. Add 100 uL Media D to the well.
3. Gently scrape entire surface with sterile cell scraper (CELLTREAT, 229310; cut to fit 24-well if needed).
4. Add 400 uL Media D. Pipette 5x to break up clumps.
5. Transfer to new well. Allow 2 hours for re-attachment.
6. Remove media, wash 1x Media C, replace with growth media.

**Method B: Enzymatic passage**:
1. Remove media. Wash 1x with MCMFS.
2. Add 100 uL Trypsin-EDTA Solution B (0.05% trypsin, 0.02% EDTA). Incubate 5-10 minutes at 22C.
3. Neutralize with 400 uL Media B.
4. Pipette gently to dissociate. Transfer to new well.
5. Allow 2 hours for re-attachment. Wash and replace with growth media.

**Method C: Accutase** (gentler alternative):
1. Remove media. Wash 1x with MCMFS.
2. Add 200 uL Accutase (StemCell Technologies, 07920). Incubate 10-15 minutes at 22C.
3. Add 300 uL Media D. Pipette gently. Transfer.

**At each passage, record**: passage number, cell count before and after, viability, population doubling level (PDL = 3.32 x log10[cells harvested / cells seeded]), cumulative PDL, morphological notes with phase contrast images.

### 1.3.2 Cryopreservation

**Three formulations tested in parallel:**

| Formulation | Composition | Rationale |
|---|---|---|
| A: Standard | 90% Media B + 10% DMSO | Standard mammalian protocol, baseline |
| B: Mixed | 90% Media B + 5% DMSO + 5% glycerol | Reduced DMSO toxicity |
| C: Trehalose | 85% Media B + 10% DMSO + 200 mM trehalose | Trehalose is an endogenous invertebrate cryoprotectant |

**Freezing procedure:**
1. Lift cells (scraping or enzymatic). Count. Target: 5 x 10^5 to 1 x 10^6 cells per cryovial.
2. Centrifuge 200 x g, 5 min, 22C.
3. Resuspend in cryoprotectant solution (pre-chilled to 4C). Add dropwise while gently swirling.
4. Transfer 500 uL to cryovials (Nunc CryoTubes, 1.0 mL).
5. Place in Mr. Frosty (-1C/min) at -80C overnight.
6. Transfer to liquid nitrogen for long-term storage.

**Thawing procedure:**
1. Remove cryovial from LN2. Place in 25C water bath (not 37C) until almost thawed.
2. Transfer to 15 mL tube. Add 5 mL pre-warmed (22C) Media B dropwise over 2-3 minutes.
3. Centrifuge 200 x g, 5 min, 22C.
4. Resuspend in 500 uL growth media. Plate.
5. Do not disturb for 4 hours. Then wash 1x with Media C, replace with growth media.

**Assessment**: viability at 24 hours post-thaw (trypan blue), morphology and attachment at 72 hours. Target: >50% viability at 24 hours.

---

## Troubleshooting

| Problem | Likely cause | Solution |
|---|---|---|
| Very low cell yield | Incomplete dissociation; small tissue size in hatchlings | Pool 2-3 animals per plate. Extend trypsin to 20 min. Try collagenase IV or papain. |
| Rapid cell death (<24h) | Osmotic stress or pH drift | Verify osmolality (target 950 mOsm/kg). Verify pH 7.4 after equilibration at 22C. |
| Contamination | Marine gram-negative bacteria | Reinforce sterile technique throughout. Ensure all FNSW and MBSS is freshly filtered. Verify pre-dissociation FNSW rinses are complete. |
| No F-ara-EdU incorporation | Cells entered quiescence | Test additional conditions: CHIR99021 + Notch ligand + FGF. Test hypoxia (5% O2). Test 3D Matrigel culture. |
| All cells differentiate rapidly | NSC state not maintained | Add CHIR99021 + Y-27632. Increase FGF concentration. Test SHH pathway agonist (SAG 1 uM). |
| All cells Nkx2.5+ | Neurogenic compartment lost, only hematopoietic cells survive | Use younger hatchlings (0-2 dph). Dissect more precisely to enrich neurogenic territory. |
| Poor attachment | Wrong substrate | Test PDL, laminin, Matrigel. Add Y-27632 10 uM (anti-anoikis). |
