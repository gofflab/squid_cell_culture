# Project Overview: E. berryi White Body Cell Culture Systems

## Version 2.0

---

## Background and Rationale

The cephalopod white body has historically been characterized as the primary hematopoietic organ in squid and octopus. Recent work (Stock, Hally et al.) has revealed that the white body is a dual-function organ containing spatially segregated neurogenic and hematopoietic territories. In *E. berryi* hatchlings, the neurogenic compartment is dominant. It contains proliferating neural stem cells (NSCs) expressing canonical markers (Ascl1, Sox2, Pax6, Ngn) that give rise to postmitotic neuroblasts that migrate via defined anterior and posterior streams to populate the expanding brain. This tissue is the primary source of new neurons during post-embryonic brain expansion, with the brain increasing more than 200-fold in mass during the first months of life.

The white body offers exceptional advantages as a source for cell culture:

1. **High endogenous proliferative rate.** White body cells in hatchlings show stathmokinetic indices exceeding 20%, with ~40% of cells in telophase in early in vitro observations (Necco & Martin 1963). F-ara-EdU pulse labeling confirms extensive S-phase activity within 4 hours of exposure (Stock, Hally et al.). This is a fundamental advantage over other marine invertebrate tissues, where primary cells universally enter quiescence within 24-72 hours in vitro (Rinkevich & Pomponi 2025).

2. **Well-characterized cell states.** Spatial transcriptomics (SOLARmap, 839 genes, 221,576 cells) provides a comprehensive molecular atlas of cell states along the neurogenic trajectory, from proliferating stem cells through committed progenitors to specified neuroblasts. This atlas enables precise molecular tracking of cell identity in culture.

3. **Defined differentiation trajectory.** Pseudotime analysis reveals an ordered developmental sequence: proliferating NSCs (Mcm2-7, E2f3, Ki67-like) transition through proneural commitment (Ascl1, Ascl1m) to specified neuroblasts (Ngn, Lhx family, Nkx2.1/2.2) that begin neurotransmitter specification (Vacht, Ty3h) before leaving the white body. This endogenous program can potentially be recapitulated in vitro.

4. **Regional specialization.** Anterior white body territories (Vvl, Fzd1, Lhx1, Nkx2.1, Foxg1) generate neurons for the supraesophageal brain; posterior territories (Wnt8b, Ems/Emx, Runx, Lhx3, Foxn4, Pax6) generate neurons for the optic lobes. Regional identity is intrinsic and maintained after transplantation, enabling subtype-specific neuronal cultures.

This program builds on the primary cell isolation methods of Kim et al. (2025), who established protocols for isolating fibroblast-like cells from *E. berryi* optic lobes, eyes, and gills. Their key findings relevant to this program: cells are viable for 3-5 days, can be passaged by mechanical scraping with cell loss, mRNA transfection works at 1-5% efficiency via Lipofectamine MessengerMAX, and all DNA delivery methods tested (lipofection, electroporation, lentiviral, AAV) failed. No cell division events were observed in their optic lobe cultures.

---

## Experimental Tracks

### Track 1: White Body Isolation and Primary Culture

**Goal**: Establish reliable isolation of white body cells from E. berryi hatchlings and optimize culture conditions that maintain cell viability, identity, and proliferative capacity.

**Key elements**: Dissection protocol separating anterior and posterior white body; culture optimization using Kim et al. media formulations supplemented with pathway-informed growth factors (Wnt, Notch, FGF/EGF); molecular identity tracking using the SOLARmap-validated marker gene panel; F-ara-EdU proliferation assessment integrated from the outset.

**Duration**: Months 1-6.
**Dependency**: None. Foundation track.

### Track 2: Cell Line Immortalization

**Goal**: Establish a continuously growing cell line from white body tissue via multiple parallel strategies.

**Key elements**: Small molecule lifespan extension (CHIR99021, Y-27632, VPA); mRNA-based transient proliferation induction (c-Myc, SV40 Large T mRNA); mRNA-transposase stable integration (hyPBase mRNA + transposon donor carrying SV40 LargeT or E. berryi TERT); nucleofection (contingent on Track 4); spontaneous immortalization by long-term culture with clonal selection.

**Duration**: Months 6-24.
**Dependency**: Track 1 (optimized primary culture conditions).

### Track 3: Neural Stem Cell Maintenance and Neurogenic Differentiation

**Goal**: Two-armed track. Arm 3A: maintain white body NSCs in a proliferative, undifferentiated state. Arm 3B: allow the endogenous neurogenic differentiation program to proceed to terminal neuronal maturity in vitro.

**Key elements**: Arm 3A screens Wnt/Notch/FGF pathway modulation for NSC maintenance, monitored by Sox2/Ascl1/Pcna expression and F-ara-EdU incorporation. Arm 3B uses growth factor withdrawal and permissive substrates (laminin) to allow endogenous differentiation, monitored by pseudotime-ordered marker gene expression and functional readouts (calcium imaging, electrophysiology).

**Duration**: Months 3-18.
**Dependency**: Track 1 (established cultures).

### Track 4: DNA Delivery Diagnostics and Promoter Screening

**Goal**: Diagnose why DNA delivery fails in squid cells, solve it, and then screen promoters for transgene expression.

**Key elements**: Phase 1 (diagnostic): Cy5-labeled DNA fate tracking to determine whether failure occurs at membrane crossing, nuclear import, or transcriptional silencing. Phase 2 (targeted solution): nucleofection, mRNA-transposase hybrid, or innate immune pathway inhibition, depending on Phase 1 results. Phase 3 (promoter screen): endogenous E. berryi promoters from SOLARmap data, OsHV bivalve viral promoter, invertebrate promoters, mammalian benchmarks.

**Duration**: Months 2-14.
**Dependency**: Track 1 (cells for transfection); partially independent.

### Track 5: Proliferation Analysis and Cell Cycle Kinetics

**Goal**: Quantitative characterization of cell proliferation dynamics using F-ara-EdU pulse labeling and flow cytometric analysis, integrated into all other tracks as a core readout.

**Key elements**: F-ara-EdU parameters validated by Stock, Hally et al. (1 uM, 4-hour pulse); click chemistry (2 mM CuSO4, 4 uM azide, 10 mM ascorbate); in vivo vs. in vitro proliferation rate comparison; cell cycle phase distribution by DNA content analysis; pulse-chase kinetics for transit time estimation.

**Duration**: Months 1-6, then ongoing as core readout.
**Dependency**: Track 1 (primary cultures). Integrated into Tracks 1-4 as standard readout.

---

## Molecular Identity Panel

All culture conditions and experiments are evaluated using the following E. berryi-validated marker gene panel, derived from the SOLARmap spatial transcriptomics dataset (Stock, Hally et al.).

| Cell state | Marker genes | Detection method |
|---|---|---|
| Proliferating NSC | Pcna, Ki67-like (EB12028), E2f3, Mcm2, Mcm6, Cenpe, Kif11 | RT-qPCR, HCR |
| Neural stem cell identity | Sox2 (EB22657), Diachete, Pax6 (EB23886), Ascl1 (EB45560), Ascl1m (EB46007) | RT-qPCR, HCR |
| Committed neuroblast | Ngn (EB09075), Erm, Lhx1, Lhx3, Lhx9, Nkx2.1 (scro), Nkx2.2 (vnd) | RT-qPCR |
| Migrating neuroblast | Sxl (EB29273), Sox2, Runx (EB17597) | RT-qPCR, HCR |
| Mature neuron | Elav (EB33473), Vacht, Ty3h | RT-qPCR, HCR |
| Hematopoietic | Nkx2.5, SoxF, Pdia6 | RT-qPCR (contamination/drift monitor) |
| Anterior WB identity | Vvl, Fzd1, Lhx1, Nkx2.1, Foxg1, Hbn | RT-qPCR |
| Posterior WB identity | Wnt8b, Ems/Emx, Ap2a, Runx, Lhx3, Foxn4, Six4 | RT-qPCR |

RT-qPCR primer sets should be designed against the E. berryi reference transcriptome (Gavriouchkina et al. 2025) during Month 1 of the program. HCR probes can be designed using HCR 3.0 Probe Maker, following the methods established in Stock, Hally et al.

---

## Timeline

### Phase 1: Foundation (Months 1-3)
- Design and validate RT-qPCR primers for marker panel.
- Optimize white body dissection (anterior vs. posterior).
- Establish baseline primary culture (Track 1 optimization matrix).
- Begin F-ara-EdU in vitro proliferation comparison (Track 5).
- DNA fate diagnostic experiment (Track 4, Phase 1).
- Begin small molecule lifespan extension screen (Track 2, Strategy 1).
- Begin long-term spontaneous immortalization cultures (Track 2, Strategy 7).

### Phase 2: Culture Optimization and Delivery (Months 3-8)
- NSC maintenance screening (Track 3, Arm 3A).
- Neurogenic differentiation characterization (Track 3, Arm 3B).
- Targeted DNA delivery solution (Track 4, Phase 2).
- Cryopreservation optimization.
- mRNA-based immortalization attempts (Track 2, Strategies 2-4).

### Phase 3: Advanced Applications (Months 8-18)
- Promoter validation (Track 4, Phase 3).
- Genetic immortalization (Track 2, Strategies 3-6).
- Functional neuronal characterization (electrophysiology, calcium imaging).
- scRNA-seq comparison of cultured vs. in vivo white body cells.

### Phase 4: Validation and Scaling (Months 18-24)
- Cell line characterization (if immortalization succeeds).
- Multi-investigator protocol validation.
- Manuscript preparation.

---

## Risk Assessment

| Track | Probability of success | Primary risk | Mitigation |
|---|---|---|---|
| Track 1 (Primary culture) | 75-85% | Cells enter quiescence in vitro despite high in vivo proliferative rate | Broad condition screen; pathway-informed media optimization |
| Track 2 (Immortalization) | 30-50% | No precedent for any cephalopod cell line; DNA delivery unsolved | Multiple parallel strategies; small molecule and mRNA approaches bypass DNA delivery |
| Track 3A (NSC maintenance) | 50-60% | Maintaining stem cells outside their niche is challenging across systems | Systematic Wnt/Notch/FGF screening; quantitative F-ara-EdU readout |
| Track 3B (Neurogenic differentiation) | 70-80% | Endogenous program may not proceed ex vivo | Growth factor withdrawal; permissive substrates; the intrinsic transcriptional cascade is strong |
| Track 4 (DNA delivery) | 40-60% | Systematic failure in Kim et al.; mechanism unknown | Diagnostic experiment first; nucleofection and mRNA-transposase as novel approaches |
| Track 5 (Proliferation analysis) | >90% | Technical only; F-ara-EdU validated in vivo | Direct adoption of Stock, Hally et al. parameters |

**Overall program**: There is a high probability (>80%) that the program will establish short-term (5-14 day) white body primary cultures with defined molecular identity and some degree of proliferation. There is a moderate probability (50-70%) of achieving neurogenic differentiation in vitro. There is a lower but meaningful probability (30-50%) of establishing a continuously growing cell line within 24 months.

---

## Resource Requirements

### Personnel Expertise
- Cell culturist with marine organism experience (1.0 FTE)
- Molecular biologist for cloning, vector construction, qPCR (0.5 FTE)
- Technician or graduate student for routine culture and imaging (0.5 FTE)

### Equipment
- Cell culture facility with 22ºC incubator (ambient CO2, L-15-based media)
- Vapor pressure osmometer (Knauer K-7000 or equivalent) [optional]
- Stereomicroscope with camera for dissection
- Inverted fluorescence microscope with DIC, phase contrast, and live imaging capability
- Confocal microscope (for HCR imaging) (Neuro imaging core)
- Flow cytometer with UV, violet, blue, and red lasers (FACS Aria in lab)
- Lonza 4D-Nucleofector (for Track 4) [optional if lipofection or other methods do not work]
- Patch-clamp electrophysiology rig (for Track 3B functional characterization) [this will have to be done in collaboration with Neill lab or others in Neuro dept]
- qPCR instrument [lightcycler @ MRB? or ABI system somewhere]
- Controlled-rate freezer (for cryopreservation) [or Mr. Frosty system]

### Animals
- ~200 E. berryi hatchlings and juveniles across developmental stages for all tracks
- Active breeding colony required [looking to Kavli for support]
- All animal work per institutional IACUC protocols

### Estimated Annual Reagent Budget
- Cell culture consumables and media components: $15,000
- Growth factors, small molecules, supplements: $10,000
- Molecular biology (qPCR, cloning, mRNA synthesis): $12,000
- F-ara-EdU and click chemistry reagents: $3,000
- HCR probes and reagents: $5,000
- Nucleofection supplies: $5,000 [optional]
- Sequencing (scRNA-seq, if performed): $30,000-45,000 [not currently budgeted for or available]
- Total: ~$80,000-95,000/year
