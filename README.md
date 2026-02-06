# HTR-Corpus-A

![characters badge](badges/characters.svg) ![regions badge](badges/regions.svg) ![lines badge](badges/lines.svg) ![files badge](badges/files.svg)

## Data
Gold-standard corpus (manually corrected), used as a training dataset for the models.

The data can be found at `./data/**/*xml` in ALTO format and follow [SegmOnto segmentation standards](https://segmonto.github.io). All data is produced using the eScriptorium interface and cataloged on [HTR-United](https://htr-united.github.io). The ALTO files have undergone manual correction, and the segmentation and transcription from the HTR are currently under review.

## Corpus 

* Corpus-A 

file in csv : [`Corpus A.csv`](corpus/Corpus_A.csv)

| Identifier | Segmentation | Transcription | Page | Author | Title | Printer | Date | Place | Library & Call number |
|-----------|--------------|---------------|------|--------|-------|---------|------|-------|----------------------|
| Lefevre_1-Tim_C2 | gold | gold | 3 | Jacques Lefèvre d'Etaples | Commentarii in epistolas d. Pauli | Anonymus | 1512 | Paris | [Regensburg SB – 999/2Script.801](https://mdz-nbn-resolving.de/urn:nbn:de:bvb:12-bsb11059254-9) |
| Bucer_Eph_test | gold | gold | 41 | Jacques Lefèvre d'Etaples | Commentarii in epistolas d. Pauli | Anonymus | 1512 | Paris | [Regensburg SB – 999/2Script.801](https://mdz-nbn-resolving.de/urn:nbn:de:bvb:12-bsb11059254-9) |
| Bugenhagen_1-Tim_C2 | gold | gold | 18 | Johannes Bugenhagen | In epistulam Pauli ad Timotheum | Anonymus – Adam Petri? | 1524 | Basel | [München SB – Res/Exeg. 309 b Beibd.3](https://mdz-nbn-resolving.de/urn:nbn:de:bvb:12-bsb00027764-8) |
| Lefevre_Rm_test | gold | gold | 19 | Martin Brucer | Epistolam ad Ephesios | Anonymus | 1527 | Strasbourg | [München SB – Polem. 408 Beibd.2](https://mdz-nbn-resolving.de/urn:nbn:de:bvb:12-bsb00035303-6) |
| Cajetan_1-Tim_C2 | gold | gold | 6 | Thomas Cajetan | Epistolae Pauli et Aliorum Apostolorum ad Graecam Veritatem Castigatae | Giunta Luca-Antonio | 1531 | Venezia | [München SB – 2 Exeg. 610](https://mdz-nbn-resolving.de/urn:nbn:de:bvb:12-bsb10143002-9) |
| Unbekannt_1-Tim_C2 | gold | gold | 24 | Unbekannt | Commentarius in priorem Timothei epistolam à viro summae pietatis studio conscriptus | Heinrich Petri | 1533 | Basel | [Basel UB – UBH FG VIII2 16:7](https://doi.org/10.3931/e-rara-3101) |
| Bullinger_1-Tim_C2 | gold | gold | 32 | Heinrich Bullinger | In D. Apostoli Pauli ad Thessalonicenses Timotheum Titum & Philemonem epistolas | Christoph Froschauer | 1536 | Zürich | [Zürich ZB – VD 16 B 5144 Vischer C 251](https://doi.org/10.3931/e-rara-23723) |
| Bucer_Rm_test | gold | gold | 19 | Martin Bucer | Metaphrases et enarrationem in Epistolam ad Romanos | Wendelin Rihel | 1536 | Strassbourg | [Regensburg SB – 999/2Script.662](https://mdz-nbn-resolving.de/urn:nbn:de:bvb:12-bsb11059175-0) |
| Pellicanus_1-Tim_C2 | gold | gold | 11 | Pellicanus Conrad | In omnes apostolicas epistolas Pauli commentarii | atelier Frocher | 1539 | Zurich | [Zürich ZB – III B 14 \| G](https://doi.org/10.3931/e-rara-2604) |
| Calvin_1-Tim_C2 | gold | gold | 15 | Jean Calvin | Commentarii in utranque Pauli epistolam ad Timotheum | Jean Girard | 1548 | Geneve | [Genève BGE – Bb 1493 (2)](https://doi.org/10.3931/e-rara-5708) |
| Lambertus_1-Tim_C1-2 | gold | gold | 225 | Lambert Daneau | priorem Epistolam ad Timotheum | Eustathius Vignon | 1577 | Genève | [Genève BGE – BGE Cti 1753 / BGE S 22877](https://doi.org/10.3931/e-rara-6338) |
| Aretius_1-Tim | gold | gold | 163 | Benedictus Aretius | in Epistolas ad Timotheum ad Titum et ad Philemonem | Jean Le Preux | 1580 | Morges | [München ZB – Exeg. 53 Beibd.1](https://mdz-nbn-resolving.de/urn:nbn:de:bvb:12-bsb10313792-3) |
| Hyperius_1-Tim_C2 | gold | gold | 12 | Hyperius Andreas | Commentarii in epistolas D. Pauli ad Timotheum | Christoph Froschauer | 1582 | Zurich | [Zürich ZB – C 85 \| G](https://doi.org/10.3931/e-rara-62382) |
| Total |  |  | **588** |  |  |  |  |  |  |

---

# File Nomenclature Guide

## 1. Directory Naming Convention

```
[exegete's name]_[epistle abbreviation]_[optional suffix]
```

### Components 

| Component | Description | Examples |
|-----------|-------------|----------|
| **Exegete's name** | Commentator name | `Aretius`, `Bucer`, `Bullinger` |
| **Epistle** | Abbreviated Latin Vulgate name | `1-Tim`, `Eph`, `Rm` |
| **Optional suffix** | Additional specification | `C_2`, `01`, `test` |

### Optional Suffix Types

- **`C_[chapter number]`** → For commentaries focusing on a single chapter
  - Example: `C_2` (Chapter 2)
  
- **`test`** → For PhD student dataset
  - Example: `test`

- **`[number]`** →  for iteration of the same commentary with the same author
  - Example: `01`, `02`
---

### Directory Examples

```
Aretius_1-Tim 
	└─Aretius commentary on 1 Timothy

Aretius_1-Tim_01
   └─ Aretius commentary on 1 Timothy, version 1

Bucer_Eph_test
   └─ Bucer commentary on Ephesians, test dataset

Bullinger_1-Tim_C_2
   └─ Bullinger commentary on 1 Timothy, Chapter 2
```
---
##  2. File Naming Convention

* Source: MDZ (Münchener Digitalisierungs Zentrum) : [URN of book]_[URN of page].xml
* Source: e-rara : [URN of page].xml

### File example 

| Source | Pattern | Example |
|--------|---------|---------|
| **MDZ** | `[book]_[page].xml` | `bsb10313792_00016.xml` |
| **e-rara** | `[page].xml` | `16892668.xml` |

---

## How to cite 

```bibtex
@misc{Goy_HTR-Corpus-A_16thExegesis,
  author={Floriane Goy, Noemi Schürmann, Benjamin Manig, Matteo Colombo },
  title={HTR of Latin printed book from 16th Century},
  version={1.0},
  address={Genève},
  publisher={université de Genève},
  year={2023-2026},
  url={https://github.com/16thExegesisDH/HTR-Corpus-A},
}
```


