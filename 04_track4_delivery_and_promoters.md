# Track 4: DNA Delivery Diagnostics and Promoter Screening

## Version 2.0

---

## Rationale

Kim et al. (2025) report that all DNA delivery methods failed in E. berryi primary cells: lipofection (Lipofectamine 3000, 2000), electroporation, lentiviral vectors (VSV-G pseudotyped), and AAV, across promoters including CMV, Ubc, SFFV, and OsHV. mRNA delivery via Lipofectamine MessengerMAX succeeded at 1-5% efficiency. This systematic failure of DNA expression is the single most important technical barrier in the program.

However, a critical distinction applies to this program: Kim et al. worked with quiescent optic lobe fibroblasts. White body cells in hatchlings are actively mitotic. Plasmid DNA accesses the nucleus during mitosis when the nuclear envelope breaks down. If culture conditions maintain even partial proliferative activity in white body NSCs, standard transfection methods may succeed where they failed in non-dividing cells. This hypothesis must be tested early.

This track is structured as three sequential phases. Phase 2 and 3 are contingent on Phase 1 results.

---

## Phase 1: DNA Fate Diagnostics (Weeks 1-4)

### Aim

Determine where in the delivery pathway DNA is lost or silenced in squid cells. This is a prerequisite for all downstream delivery optimization.

### Experiment 1: Fluorescent DNA Tracking

**Principle**: Label plasmid DNA with a fluorescent dye and track its fate by confocal microscopy.

**Materials**:
- Label IT Nucleic Acid Labeling Kit, Cy5 (Mirus Bio, MIR3700)
- pEGFP-N1 plasmid (Clontech) or pmaxGFP (Lonza), endotoxin-free prep
- Lipofectamine 3000 (Thermo Fisher, L3000001)
- Hoechst 33342 (Thermo Fisher, 62249)

**Protocol**:
1. Label 5 ug pEGFP-N1 with Cy5 per manufacturer protocol (1 hour, 37C). Purify by spin column.
2. In parallel, label 5 ug GFP mRNA with Cy5 (positive control: mRNA delivery is known to work).
3. Plate white body cells on glass-bottom wells at 50-80% confluence.
4. Transfect with Cy5-labeled DNA (500 ng/well, 24-well) using Lipofectamine 3000.
5. Transfect parallel wells with Cy5-labeled mRNA using Lipofectamine MessengerMAX.
6. At 4, 8, 12, and 24 hours post-transfection:
   - Wash 3x with MBSS.
   - Add Hoechst (1:50,000, 30 min) for nuclear counterstain.
   - Image live by confocal microscopy: Cy5 (DNA/mRNA), Hoechst (nuclei), DIC (morphology).
7. Score each cell as: (a) no Cy5 signal, (b) Cy5 cytoplasmic only, (c) Cy5 nuclear, (d) Cy5 in both.
8. At 24 hours: also check for GFP fluorescence (expression from the pEGFP-N1 construct).

**Interpretation**:

| Observation | Diagnosis | Next step |
|---|---|---|
| Cy5-DNA absent from cells | Membrane crossing failure | Try nucleofection (Phase 2A) |
| Cy5-DNA cytoplasmic, not nuclear | Nuclear import failure | Nucleofection or NLS-conjugated DNA (Phase 2A) |
| Cy5-DNA nuclear, no GFP expression | Transcriptional silencing | Promoter screen justified (Phase 3); test HDAC inhibitors |
| Cy5-DNA signal disappears by 8 hours | Active DNA degradation | Innate immune DNA sensing; test pathway inhibitors (Phase 2B) |
| Cy5-DNA nuclear + GFP expression | It works in WB cells (unlike optic lobe) | Proceed directly to Phase 3 promoter screen |

### Experiment 2: Is DNA Degraded by Innate Immunity? (If Experiment 1 suggests degradation)

**Principle**: Cephalopods have robust innate immunity. If cytoplasmic DNA sensors (cGAS-STING or related pathways) detect foreign DNA and trigger degradation, pharmacological inhibition may rescue expression.

**Protocol**:
1. Pre-treat cells for 24 hours with:
   - Chloroquine 50 uM (Sigma, C6628): inhibits endosomal acidification, blocks TLR signaling
   - BX795 1 uM (Sigma, SML0549): TBK1 inhibitor, blocks cGAS-STING
   - RU.521 10 uM (InvivoGen, inh-ru521): cGAS inhibitor
   - Vehicle control (DMSO)
2. Transfect with Cy5-labeled DNA as in Experiment 1.
3. Compare DNA persistence (Cy5 signal at 12, 24 hours) and GFP expression at 48 hours.

### Experiment 3: Does Mitotic Activity Enable DNA Delivery?

**Principle**: Test whether white body cells (mitotic) show better DNA delivery than optic lobe cells (quiescent).

**Protocol**:
1. Isolate white body cells and optic lobe cells from the same hatchlings (paired comparison).
2. Transfect both with Cy5-labeled pEGFP-N1 using identical conditions (Lipofectamine 3000, 500 ng/well).
3. At 48 hours: quantify GFP+ cells in each population.
4. In parallel: F-ara-EdU pulse (1 uM, 4 hours) on untransfected wells to confirm differential proliferation.

If white body cells show GFP expression where optic lobe cells do not, the mitotic state is enabling nuclear DNA entry.

---

## Phase 2: Targeted Delivery Solutions (Weeks 4-10)

Based on Phase 1 diagnosis, pursue the appropriate strategy.

### Phase 2A: Nucleofection (If Nuclear Import Is the Barrier)

**System**: Lonza 4D-Nucleofector X Unit with 16-well Nucleocuvette Strips.

**Protocol**:
1. Lift white body cells (scraping or gentle trypsinization). Count. Resuspend at 2 x 10^5 cells per 20 uL nucleofection solution.
2. Test Lonza optimization pulse programs (no cephalopod-specific program exists):
   - CM-138 (primary neurons)
   - DS-138 (primary fibroblasts)
   - EH-100 (primary macrophages, relevant since some WB cells are phagocytic)
   - FF-120 (hard-to-transfect cells)
3. Nucleofection solutions: test both P3 Primary Cell and SF Cell Line solutions.
4. Plasmid: 1 ug pmaxGFP per reaction.
5. Immediately post-nucleofection: add 80 uL pre-warmed Media D to cuvette. Transfer to 24-well plate with 500 uL Media D.
6. Assess at 24 and 48 hours: GFP expression (fluorescence microscopy), viability (calcein-AM/EthD-1).
7. Target: >5% GFP+ with >50% viability.

**Osmolality consideration**: Standard nucleofection solutions are ~300 mOsm. White body cells are adapted to ~950 mOsm. The transient hypotonic exposure during the nucleofection pulse may actually aid DNA entry (osmotic swelling opens nuclear pores), but prolonged exposure will be lethal. Minimize time in nucleofection buffer (prepare cells, nucleofect, and return to growth media within 5 minutes). Alternatively, supplement nucleofection solution with NaCl to achieve 600-700 mOsm (a compromise between the Lonza formulation and full marine osmolality).

### Phase 2B: Innate Immune Pathway Inhibition (If DNA Degradation Is the Barrier)

Use the pharmacological inhibitors from Phase 1, Experiment 2, but now applied during transfection with unlabeled DNA:

1. Pre-treat with the most effective inhibitor(s) from Experiment 2 for 12-24 hours.
2. Transfect with pEGFP-N1 via Lipofectamine 3000 while maintaining inhibitor.
3. Assess GFP expression at 24, 48, 72 hours.
4. If successful, determine whether inhibitor is needed only during transfection or must be maintained.

### Phase 2C: mRNA-Transposase Hybrid (Parallel Track, Independent of Phase 1)

This strategy bypasses both nuclear import and promoter barriers for the integration step. The transposase protein (delivered as mRNA to cytoplasm, translated, then enters nucleus using its own NLS) mobilizes the DNA donor into the genome.

See Track 2, Strategy 3 for detailed protocol. Begin construct design during Phase 1. This strategy can proceed regardless of Phase 1 diagnosis.

---

## Phase 3: Promoter Screening (Weeks 10-18, Contingent on Phase 2 Success)

### Prerequisite

A DNA delivery method achieving >5% expression efficiency with >50% viability.

### Candidate Promoter Library

Promoters are prioritized based on likelihood of function in cephalopod cells:

**Priority 1: E. berryi endogenous promoters**

Identify the top 10 most highly and broadly expressed genes in white body cells from the SOLARmap dataset (Stock, Hally et al.). Candidate highly expressed genes include actin, EF1alpha, ubiquitin, ribosomal protein genes, and Pcna. Extract 2 kb upstream of the predicted transcription start site from the E. berryi reference transcriptome/genome. Clone these regions upstream of eGFP-T2A-PuroR in a standard expression backbone.

| Gene | E. berryi ID | Rationale |
|---|---|---|
| EF1alpha homolog | (from transcriptome) | Ubiquitous housekeeping, strong in all WB cells |
| Beta-actin homolog | (from transcriptome) | Ubiquitous, strong |
| Pcna | (from transcriptome) | Highly expressed in proliferating WB cells |
| Ubiquitin | (from transcriptome) | Ubiquitous housekeeping |
| Tubulin (Tubb3b, EB22391) | EB22391 | Neuron-specific, strong in WB |

**Priority 2: Molluscan viral promoter**

- OsHV IE1 (Ostreid herpesvirus immediate early, from Yoon et al. 2022). Only promoter demonstrated to drive expression in any molluscan cell.

**Priority 3: Invertebrate promoters**

- Drosophila Actin5C: strong ubiquitous insect promoter, phylogenetically closer than mammalian.
- Drosophila Ubiquitin-63E: another strong ubiquitous insect promoter.

**Priority 4: Mammalian benchmarks** (low probability, included for completeness)

- CAG: strong synthetic mammalian promoter.
- CMV: failed in Kim et al., but included as negative control.
- EF1alpha (human): failed in Kim et al. under "Ubc" designation.

### Screening Protocol

1. Clone each promoter upstream of eGFP in a standardized backbone. Sequence verify. Prepare endotoxin-free DNA.
2. Deliver by validated method (nucleofection, lipofection if it works in WB cells, or mRNA-transposase).
3. At 48 hours: image for GFP expression. Quantify % GFP+ cells and mean fluorescence intensity (MFI).
4. At Day 7: re-image to assess expression durability.
5. Rank promoters by: expression level (MFI), expression breadth (% GFP+), durability (Day 7 / Day 2 signal).

### Decision Criteria

- Top promoter: use for all subsequent transgene constructs (Track 2 immortalization, lineage reporters).
- If no promoter achieves >5% expression: the problem is not promoter recognition. Consider minicircle DNA (reduced bacterial backbone sequences that trigger silencing), S/MAR elements flanking the transgene, or HDAC inhibitor co-treatment (VPA 1 mM or TSA 100 nM) during transfection.

---

## Risk Assessment

| Risk | Probability | Impact | Mitigation |
|---|---|---|---|
| DNA never enters WB cell nuclei by any method | LOW-MODERATE (25%) | Blocks DNA-dependent strategies | mRNA-transposase provides alternative; microinjection as proof-of-concept |
| Mitotic WB cells enable DNA entry (solves the problem) | MODERATE (35%) | Major acceleration of all tracks | Test early (Phase 1, Experiment 3) to capture this advantage |
| DNA enters nucleus but is silenced | MODERATE (25%) | Need endogenous promoters + chromatin modifiers | SOLARmap data enables endogenous promoter identification; HDAC inhibitors |
| All promoters fail | LOW (15%) | Fundamental barrier | Consider mRNA-only approaches for all applications |
| Nucleofection kills cells | LOW-MODERATE (20%) | Lose best delivery option | Optimize pulse; adjust osmolality; try lower DNA amounts |
