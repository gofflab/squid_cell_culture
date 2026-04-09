# E. berryi White Body Cell Culture System

## Establishing Primary, Immortalized, and Neurogenic Cell Culture from the *Euprymna berryi* White Body

### Overview

This repository contains the experimental design and detailed protocols for establishing cell culture systems from the white body of the hummingbird bobtail squid, *Euprymna berryi*. The white body is a dual-function organ containing spatially segregated neurogenic and hematopoietic territories. In hatchlings, the neurogenic compartment is dominant and serves as the primary source of new neurons for the expanding post-embryonic brain (Stock, Hally et al.).

The program builds on the primary cell isolation and culture methods of Kim et al. (2025) and is informed by spatially resolved transcriptomic characterization of the white body (Stock, Hally et al.) and the E. berryi single-cell atlas (Gavriouchkina et al. 2025).

### Repository Structure

```
├── README.md                          # This file
├── 00_project_overview.md             # Master experimental design, rationale, timeline
├── 01_track1_isolation_and_culture.md  # White body dissection, cell isolation, culture optimization
├── 02_track2_immortalization.md        # Cell line establishment strategies
├── 03_track3_NSC_and_differentiation.md # Neural stem cell maintenance and neurogenic differentiation
├── 04_track4_delivery_and_promoters.md # DNA delivery diagnostics, transduction, promoter screening
├── 05_track5_proliferation_analysis.md # F-ara-EdU labeling, cell cycle analysis, kinetics
├── 06_reagents_and_media.md           # Complete media formulations, antimicrobial strategy, catalog numbers
└── CHANGELOG.md                       # Version history
```

### Track Summary

| Track | Title | Duration | Dependency |
|-------|-------|----------|------------|
| 1 | White Body Isolation and Primary Culture | Months 1-6 | None |
| 2 | Cell Line Immortalization | Months 6-24 | Track 1 |
| 3 | NSC Maintenance and Neurogenic Differentiation | Months 3-18 | Track 1 |
| 4 | DNA Delivery and Promoter Screening | Months 2-14 | Track 1 (partially independent) |
| 5 | Proliferation Analysis and Cell Cycle Kinetics | Months 1-6 | Integrated into Track 1 |

### Key References

- Kim Y, Tanner HM, Rosenthal JJC, Brangwynne CP (2025). Protocol for the isolation, culture, and transfection of squid primary cells. STAR Protocols 6(3):103994. PMC12347879.
- Stock J, Hally A, Sriworarat C, Palaganas R, Lucey J, Stein-O'Brien G, Albertin CB, Goff LA. Cephalopod post-embryonic brain expansion is driven by long-distance migration from a novel neurogenic tissue outside the central nervous system. (Submitted).
- Gavriouchkina D et al. (2025). A single-cell atlas of the bobtail squid visual and nervous system highlights molecular principles of convergent evolution. Nature Ecology & Evolution 9:1245-1262.
- Rinkevich B, Pomponi SA (2025). Advancing marine invertebrate cell line research: four key knowledge gaps. In Vitro Cell Dev Biol Anim 61(5):493-505.

### Version

Current: v2.0 (Final Draft)

### Contact

Goff Lab, Johns Hopkins University School of Medicine
