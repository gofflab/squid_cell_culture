# Track 2: Cell Line Immortalization

## Version 2.0

---

## Aim

Establish a continuously growing cell line from E. berryi white body tissue that retains either neural stem cell identity or neurogenic differentiation capacity.

---

## Rationale

No cephalopod cell line has ever been established. The broader marine invertebrate field has essentially no permanent cell lines, with one partial sponge success (Hesp et al. 2023). However, the white body offers a unique advantage: its cells are highly mitotic in vivo, with stathmokinetic indices exceeding 20% and ~40% of cells in telophase (Necco & Martin 1963). If this proliferative state can be maintained in culture, spontaneous or assisted immortalization becomes substantially more plausible than for quiescent marine invertebrate cells.

**Critical dependency**: All DNA-dependent strategies require a functional delivery method (Track 4). mRNA-based and small molecule strategies can proceed independently.

---

## Strategies (Prioritized by Feasibility)

### Strategy 1: Small Molecule Lifespan Extension

**Start**: Month 1 (no DNA delivery required).

**Rationale**: Pharmacological maintenance of proliferative capacity without genetic manipulation. Not true immortalization, but may extend culture lifespan sufficiently for experimental use and provide a window for spontaneous immortalization events.

**Protocol**:
1. Establish white body cultures per Track 1 optimized conditions.
2. Supplement with the following cocktails (each in triplicate, 24-well):

| Cocktail | Components | Rationale |
|---|---|---|
| NSC maintenance | CHIR99021 3 uM + Y-27632 10 uM + VPA 0.5 mM | Wnt activation + anti-anoikis + HDAC inhibition. Delays differentiation and senescence. |
| Dual inhibition | CHIR99021 3 uM + PD0325901 1 uM (Tocris, 4192) | Wnt activation + MEK inhibition. 2i-like conditions that maintain pluripotency in mouse ESCs. |
| Senolytic | ABT-263 (navitoclax) 1 uM (Selleckchem, S1001) + rapamycin 10 nM (Sigma, R0395) | Removes senescent cells + mTOR inhibition to delay senescence onset. |
| Telomerase activator | Cycloastragenol (TA-65) 10 uM (Sigma, SML0986) | Small molecule telomerase activator. Unproven in invertebrates, low toxicity. |

3. Culture for 30 days with media changes every 2-3 days.
4. Monitor cell counts weekly. At Days 7, 14, 21, 28: F-ara-EdU incorporation (1 uM, 4h pulse), viability, RT-qPCR for Sox2, Ascl1, Pcna, Elav.
5. If any cocktail maintains viable, proliferating cells beyond 14 days, prioritize for expansion and attempt passage.

### Strategy 2: mRNA-Based Transient Proliferation Induction

**Start**: Month 2-3 (after mRNA synthesis/procurement).

**Rationale**: mRNA transfection works at 1-5% efficiency in squid cells (Kim et al. 2025). Deliver proliferation-inducing factors as mRNA to bypass the DNA delivery problem. Transient expression requires repeated transfection.

**mRNAs to prepare** (IVT with N1-methylpseudouridine, Cap1, 120-nt poly(A)):
- Human c-Myc (wild-type)
- Human c-Myc T58A (stabilized mutant)
- SV40 Large T antigen
- E. berryi TERT (clone from transcriptome sequence, Gavriouchkina et al. 2025)

**Protocol**:
1. Plate white body cells at 70-90% confluence.
2. Wash 2x with Media C without antibiotics.
3. Prepare mRNA-lipid complexes: 500 ng mRNA + Lipofectamine MessengerMAX (Thermo Fisher, LMRNA003) per well (24-well), following manufacturer protocol. Complexes are formed in Opti-MEM (Thermo Fisher, 31985062).
4. Add complexes to cells in Media C without antibiotics. Incubate 24 hours at 22C.
5. Replace with growth media.
6. Re-transfect every 3-4 days.

**Readouts**:
- Day 1 post-transfection: confirm expression by RT-qPCR (c-Myc, LargeT) or immunostaining (if validated antibody available).
- Day 2 post-transfection: F-ara-EdU pulse (1 uM, 4 hours). Compare EdU incorporation in transfected vs. untransfected cells.
- Day 7: cell count relative to Day 0. Any increase indicates proliferation induction.

### Strategy 3: mRNA-Transposase + SV40 Large T Donor

**Start**: Month 3-5.

**Rationale**: The most promising path to stable integration in non-dividing or slowly dividing cells. The transposase enzyme is delivered as mRNA (which works), and it mobilizes a DNA transposon cassette into the genome.

**Construct design**:

Transposon donor (flanked by PiggyBac ITRs):
```
[5' ITR] - [Promoter] - [SV40 LargeT] - [T2A] - [PuroR or eGFP] - [polyA] - [3' ITR]
```

Promoter options (test in parallel):
- OsHV IE1 (bivalve viral, Yoon et al. 2022)
- E. berryi EF1alpha homolog (from reference transcriptome)
- CAG (mammalian benchmark)

Transposase: hyPBase (hyperactive PiggyBac transposase), IVT mRNA.

**Protocol**:
1. Co-transfect 250 ng hyPBase mRNA + 250 ng linearized transposon donor + Lipofectamine MessengerMAX.
2. Incubate 24 hours. Replace with growth media.
3. At Day 3: begin puromycin selection (if PuroR cassette). Determine kill curve on untransfected cells first (test 0.25, 0.5, 1, 2, 4, 8 ug/mL; use lowest dose that kills 100% by Day 7). Or FACS sort GFP+ cells (if eGFP cassette).
4. Expand resistant/GFP+ cells.
5. Validate: genomic PCR across ITR-transgene junction; RT-qPCR for LargeT; growth curve assessment.

### Strategy 4: mRNA-Transposase + E. berryi TERT Donor

**Start**: Month 4-6 (after cloning TERT).

Same as Strategy 3, substituting E. berryi TERT for SV40 LargeT. Run in parallel with Strategy 3 if constructs are ready.

### Strategy 5: Combined LargeT + TERT

**Start**: Month 6+ (if Strategy 3 or 4 produces integrants).

Deliver both transgenes via dual transposon cassettes or a single bicistronic construct.

### Strategy 6: Nucleofection

**Start**: Contingent on Track 4 demonstrating functional nucleofection.

Deliver LargeT or TERT expression plasmids directly via Lonza 4D-Nucleofector. See Track 4 for nucleofection optimization protocol.

### Strategy 7: Spontaneous Immortalization

**Start**: Month 1 (ongoing).

1. Establish 20-30 independent white body cultures from individual hatchlings.
2. Maintain in best growth media from Track 1.
3. Passage when confluent (typically 7-14 days if proliferating).
4. Document passage number, growth rate, and morphology at every passage.
5. If any culture shows accelerated growth, ring-clone the fastest-growing colony and expand separately.
6. At passage 20: assess senescence markers (SA-beta-galactosidase staining).
7. At passage 30+: consider immortalization confirmed. Full characterization (see below).

---

## Characterization of Candidate Immortalized Lines

If any strategy produces continuously growing cells (>20 population doublings), characterize:

1. **Growth curve**: cumulative PDL vs. time over 30+ passages.
2. **Morphology**: phase contrast + phalloidin/DAPI at passages 5, 10, 20, 30.
3. **Molecular identity**: RT-qPCR for the full marker panel (Sox2, Ascl1, Pcna, Elav, Nkx2.5). Bulk RNA-seq at passages 5, 15, 30 compared to fresh white body tissue.
4. **Karyotype**: chromosome spreads at passages 5, 15, 30. E. berryi karyotype may need de novo establishment.
5. **Ploidy**: DNA content by flow cytometry (PI staining in MBSS-based buffer) at passages 5, 15, 30.
6. **Telomerase activity**: TRAP assay.
7. **Differentiation capacity**: can the immortalized line still undergo neurogenic differentiation when growth factors are withdrawn (Track 3, Arm 3B)?
8. **Anchorage-independent growth**: soft agar assay (0.3% low-melting agarose in Media D, 1000 cells/well, score colonies at 3-4 weeks).
9. **Species verification**: COI barcoding PCR to confirm cells are E. berryi (not a contaminant).
10. **Mycoplasma**: PCR-based detection (Lonza MycoAlert) at passages 5, 15.

---

## Risk Assessment

| Risk | Probability | Impact | Mitigation |
|---|---|---|---|
| Cells enter quiescence before any strategy can act | HIGH (50%) | Blocks all strategies | Start Strategies 1, 2, and 7 simultaneously at the earliest possible timepoint |
| DNA delivery fails (blocks Strategies 3-6) | MODERATE (40%) | Limits to mRNA and small molecule approaches | Track 4 diagnostic experiment identifies mechanism; mRNA-transposase may bypass |
| SV40 LargeT does not interact with squid p53/Rb | MODERATE (30%) | Strategy 3 fails | Test human p53DD (dominant-negative p53) as alternative; CRISPR p53 knockout if delivery works |
| Immortalized cells lose neurogenic identity | HIGH (50%) | Line exists but lacks biological utility | Characterize early passages; freeze early stocks; consider conditional systems (tet-off TERT) |
| Spontaneous immortalization never occurs | HIGH (60%) | Strategy 7 fails (expected) | This is a low-investment background strategy; genetic approaches are the primary path |
