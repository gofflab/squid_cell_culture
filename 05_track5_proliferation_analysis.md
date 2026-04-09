# Track 5: Proliferation Analysis and Cell Cycle Kinetics

## Version 2.0

---

## Rationale

Quantitative assessment of cell proliferation is the single most important readout for evaluating culture quality across all tracks. This track establishes F-ara-EdU pulse labeling and cell cycle analysis as core methods, integrated into Tracks 1-4 as a standard readout rather than a standalone effort.

F-ara-EdU is validated as non-toxic in E. berryi at concentrations up to 100 uM for 3+ days continuous exposure (Stock, Hally et al.). The in vivo labeling protocol (1 uM, 4-hour pulse) provides the baseline parameters for in vitro adaptation.

---

## 5.1: F-ara-EdU Pulse Labeling Protocol (In Vitro)

### Materials

| Reagent | Supplier | Catalog # | Storage |
|---|---|---|---|
| F-ara-EdU | Vector Laboratories | CCT-1403-5 | -20C, protect from light |
| CuSO4 | Sigma-Aldrich | C7631 | RT |
| Fluorescent azide (AF488 or AF647) | Vector Laboratories | CCT-1284-1 (647) or CCT-1488-1 (488) | -20C, protect from light |
| Sodium ascorbate | Sigma-Aldrich | 11140 | Make fresh |
| DMSO | Sigma-Aldrich | D2438 | RT |
| Hoechst 33342 | Thermo Fisher | 62249 | 4C, protect from light |
| 16% Paraformaldehyde | Electron Microscopy Sciences | 15714-S | RT |

### Stock Solutions

- **F-ara-EdU**: 50 mM in DMSO. Aliquot 20 uL. Store at -20C protected from light. Stable 6 months.
- **Working concentration**: Dilute to 1 uM in growth media immediately before use (1:50,000 dilution of stock).

### Labeling Protocol

1. Add F-ara-EdU to culture media at 1 uM final concentration.
2. Incubate for 4 hours at 22C (standard pulse; this is the validated in vivo condition).
3. Remove media. Wash 2x with MBSS.
4. Fix in 4% PFA in MBSS for 15 minutes at 22C (for cultured cells on glass).
   - Alternative for whole-mount or thick samples: fix in 4% PFA in FNSW at 4C for 2-5 days, then permeabilize with acetone and detergent solution per Stock, Hally et al.
5. Wash 3x with PBS or MBSS.

### Click Chemistry Detection

**Validated conditions from Stock, Hally et al.:**

1. Permeabilize: 0.5% Triton X-100 in PBS, 10 minutes at RT. (For cultured cells on glass, this is sufficient. For thicker samples, use the full detergent solution from Stock, Hally et al.: 12 mM sodium deoxycholate, 50 mM Tris pH 7.5, 1 mM EDTA, 150 mM NaCl, 1% SDS.)
2. Wash 2x with PBS.
3. Prepare click reaction mix fresh (per well, 24-well plate, 300 uL):
   - PBS: 270 uL
   - 100 mM CuSO4: 6 uL (final 2 mM)
   - Fluorescent azide (1 mM stock): 1.2 uL (final 4 uM)
   - DMSO: 30 uL (final 10%)
   - 100 mM sodium ascorbate (prepared fresh in dH2O): add LAST, 30 uL (final 10 mM)
4. Incubate 30 minutes at RT for cultured cells. (Stock, Hally et al. use 2 hours for whole-mount tissue; shorter is sufficient for monolayer cultures.)
5. Wash 3x with PBS.
6. Counterstain with Hoechst 33342 (1:50,000 in MBSS or high-salt PBS) for 15 minutes at RT.
7. Wash 2x. Image or store at 4C in PBS protected from light.

### Quantification

- Image 5 random fields per well at 20x magnification (fluorescence: EdU channel + Hoechst).
- Count total nuclei (Hoechst+) and F-ara-EdU+ nuclei per field.
- Calculate: % EdU+ = (F-ara-EdU+ nuclei / total nuclei) x 100.
- Automated counting: use CellProfiler or FIJI/ImageJ with thresholding on both channels.

### Controls

- **Positive control**: F-ara-EdU-treated E. berryi hatchling white body cryosections (known high proliferation).
- **Negative control**: cells not exposed to F-ara-EdU, processed through full click chemistry (background signal).
- **Background control**: cells exposed to F-ara-EdU but click chemistry performed without fluorescent azide (non-specific CuSO4/ascorbate staining).

---

## 5.2: In Vivo vs. In Vitro Proliferation Comparison

This is the most informative single experiment for evaluating culture quality.

### Protocol

1. **In vivo baseline** (from Stock, Hally et al. data): % F-ara-EdU+ cells in white body after 4-hour, 1 uM pulse in hatchlings. This value is already established.

2. **In vitro time course**: Isolate white body cells into culture (Track 1 conditions). At 6, 24, 48, and 72 hours post-plating:
   - Add 1 uM F-ara-EdU for 4 hours.
   - Fix and process by click chemistry.
   - Quantify % EdU+ cells.

3. **Compute proliferation retention ratio**: (% EdU+ in vitro at time T) / (% EdU+ in vivo baseline).

### Interpretation

| Retention ratio | Assessment | Action |
|---|---|---|
| >50% at 24h, >25% at 72h | Good proliferation retention | Proceed with culture expansion and Track 2 |
| 10-50% at 24h, declining | Partial retention, cells entering quiescence | Optimize: add CHIR99021, test hypoxia, increase FGF |
| <10% at 24h | Rapid quiescence | Fundamental culture condition failure; return to Track 1 optimization |

---

## 5.3: Cell Cycle Phase Distribution (Flow Cytometry)

### Osmolality Considerations

Standard flow cytometry buffers (PBS, ~300 mOsm) are dramatically hypotonic relative to 950 mOsm culture media. Cells will swell and lyse. Two approaches:

**Approach A: Fixed-cell analysis in MBSS-based buffer (recommended)**
- Fixation in 70% ethanol (osmolality-independent, solvent-based fixation) stabilizes cells.
- All subsequent washes use MBSS instead of PBS.
- PI/RNase A staining in MBSS: 50 ug/mL propidium iodide (BD Biosciences, 51-66211E) + 100 ug/mL RNase A (Thermo Fisher, EN0531) in MBSS. 30 min at 37C protected from light.
- Run on flow cytometer within 2 hours.
- Gate: FSC-A vs FSC-H for singlets. PI histogram for DNA content (G0/G1 = 2N, S = 2N-4N, G2/M = 4N).

**Approach B: Imaging-based analysis (alternative, avoids lifting cells)**
- Fix cells in situ (4% PFA/MBSS).
- Stain with Hoechst 33342 (1 ug/mL, 30 min).
- Image nuclei by fluorescence microscopy.
- Measure integrated Hoechst fluorescence intensity per nucleus using CellProfiler.
- Histogram of nuclear intensities reveals G1 (2N peak), S (intermediate), and G2/M (4N peak) populations.
- Advantage: no osmotic perturbation, no cell loss from lifting, compatible with co-staining.

### Protocol for Combined F-ara-EdU + DNA Content Analysis

This dual-parameter analysis (analogous to BrdU/PI plots) reveals which cell cycle phase cells are in when labeled.

1. Pulse with 1 uM F-ara-EdU for 4 hours.
2. Fix in 4% PFA/MBSS, 15 min.
3. Permeabilize: 0.5% Triton X-100, 10 min.
4. Click chemistry for F-ara-EdU detection (AF488 azide).
5. Stain with Hoechst 33342 (1 ug/mL, 30 min).
6. Image: EdU (488 nm) + Hoechst (UV/405 nm).
7. Plot: EdU intensity vs. Hoechst intensity per cell (2D scatter).
   - G0/G1: low Hoechst, EdU-negative
   - S-phase: intermediate Hoechst, EdU-positive
   - G2/M: high Hoechst, EdU-negative (if not in S during pulse) or EdU-positive (if transited through S during pulse)

---

## 5.4: Pulse-Chase Kinetics

### Aim

Determine cell cycle transit times and identify distinct proliferative subpopulations within white body cultures.

### Protocol

1. Pulse cells with 1 uM F-ara-EdU for 2 hours (shorter pulse for kinetic resolution).
2. Wash 3x with warm growth media. Replace with F-ara-EdU-free media.
3. Fix replicate wells at chase timepoints: 0, 2, 4, 6, 8, 12, 18, 24, 36, 48 hours post-pulse.
4. Process all timepoints in a single batch (click chemistry + Hoechst).
5. Quantify: % EdU+ cells, mean EdU intensity, and Hoechst intensity per cell at each timepoint.

### Analysis

- **At chase = 0**: EdU+ cells are in S-phase. Their Hoechst intensity ranges from 2N to 4N.
- **As chase progresses**: EdU+ cells complete S-phase (Hoechst increases to 4N), pass through G2/M (Hoechst returns to 2N as daughter cells), and re-enter G1.
- **Labeled mitotic figures**: At early chase times (2-6 hours), EdU+ cells with 4N DNA content and condensed chromosomes are in G2/M. The time from pulse to first appearance of labeled mitoses estimates G2 duration.
- **Labeled doublets**: Appearance of paired EdU+ cells with 2N content indicates completed division. Time to first doublets estimates G2+M duration.

### Mathematical Modeling

Fit pulse-chase data to standard cell cycle kinetic models:
- T_S (S-phase duration): estimated from the duration of EdU+ population at 2N-4N intermediate Hoechst intensities.
- T_G2+M: estimated from time between end of pulse and appearance of labeled 2N cells.
- T_total (total cycle time): estimated from time between pulse and re-entry of labeled cells into S-phase (if cells are cycling continuously).

### Growth Fraction

From continuous labeling experiment (1 uM F-ara-EdU maintained continuously):
- Fix replicate wells at 2, 4, 8, 12, 24, 48, 72 hours.
- Plot cumulative % EdU+ cells over time.
- Plateau value = growth fraction (% of cells that are cycling).
- Time to plateau estimates the duration of the longest cell cycle phase.

---

## 5.5: Application-Specific Protocols

### For Track 2 (Immortalization Validation)

Compare primary cells (early passage) vs. candidate immortalized lines:
- Weekly F-ara-EdU incorporation (1 uM, 4h pulse) over 4-6 weeks.
- Growth fraction measurement (continuous labeling) at passage 5 and passage 20.
- Cell cycle phase distribution at passages 5, 10, 20.
- Criteria for immortalization: growth fraction >50% at passage 20, sustained EdU incorporation, no increase in G0/G1 fraction over passages.

### For Track 3 (Differentiation Monitoring)

Track cell cycle exit during neurogenic differentiation:
- F-ara-EdU pulse at Days 0, 3, 7, 14 post-differentiation switch.
- Co-stain with HCR for Elav + Pcna.
- A successfully differentiating culture should show: decreasing % EdU+ over time, increasing Elav+/Pcna- population, and EdU+ cells should be Pcna+/Elav- (proliferating cells are NSCs, not neurons).
- Differentiation efficiency = % Elav+/Pcna- cells at Day 14.

### For Track 1 (Culture Optimization)

F-ara-EdU incorporation is the primary quantitative readout for all Track 1 media optimization experiments (see Track 1, Section 1.2.2).

---

## Quality Control

| Control | Purpose | Expected result |
|---|---|---|
| No F-ara-EdU + full click chemistry | Click chemistry background | <1% false-positive "EdU+" cells |
| F-ara-EdU + click without azide | Non-specific copper/ascorbate staining | <1% false-positive |
| In vivo pulse (hatchling white body section) | Positive control for labeling and detection | Robust EdU signal in white body |
| Serum-starved cells (0% FBS, 48h) + EdU pulse | Quiescence control | <5% EdU+ (most cells in G0) |
| Known proliferative mammalian cell line (HEK293T or similar, if available) | Protocol positive control (different species) | >30% EdU+ |
