# HTR-Corpus-A

![characters badge](badges/characters.svg) ![regions badge](badges/regions.svg) ![lines badge](badges/lines.svg) ![files badge](badges/files.svg)

## Data
* Bronze-standard corpus, automatically created using models trained on Corpus A. Manual corrections are limited to the OCR of the verses.

The data can be found at `./data/**/*xml` in ALTO format and follow [SegmOnto segmentation standards](https://segmonto.github.io). All data is produced using the eScriptorium interface and cataloged on [HTR-United](https://htr-united.github.io). The ALTO files have undergone no correction.

## Corpus 

* Corpus-B 

file in csv : [`Corpus B.csv`](corpus/Corpus_B.csv)

| Identifier | Segmentation | Transcription | Page | Author | Title | Printer | Date | Place | Library & Call number |
|-----------|--------------|---------------|------|--------|-------|---------|------|-------|----------------------|
| Lefevre_1-Tim_C1-C3-6 | no | no | 21 | Jacques Lefèvre d'Etaples | Commentarii in epistolas d. Pauli | Anonymus | 1512 | Paris | [Regensburg SB – 999/2Script.801](https://mdz-nbn-resolving.de/urn:nbn:de:bvb:12-bsb11059254-9) |
| Bugenhagen_1-Tim_C3-6 | auto | no | 26 | Johannes Bugenhagen | In epistulam Pauli ad Timotheum | Anonymus – Adam Petri? | 1527 | Basel | [München SB – Res/Exeg. 309 b Beibd.3](https://mdz-nbn-resolving.de/urn:nbn:de:bvb:12-bsb00027764-8) |
| Cajetan_1-Tim_C3-C6 | no | no | 9 | Thomas Cajetan | Epistolae Pauli et Aliorum Apostolorum ad Graecam Veritatem Castigatae | Giunta Luca-Antonio | 1531 | Venezia | [München SB – 2 Exeg. 610](https://mdz-nbn-resolving.de/urn:nbn:de:bvb:12-bsb10143002-9) |
| Unbekannt_1-Tim_C1_C3-6 | no | no | 195 | Unbekannt | Commentarius in priorem Timothei epistolam à viro summae pietatis studio conscriptus | Heinrich Petri | 1533 | Basel | [Basel UB – UBH FG VIII2 16:7](https://doi.org/10.3931/e-rara-3101) |
| Pellicanus_1-Tim_C1_C3-6 | no | no | 70 | Pellicanus Conrad | In omnes apostolicas epistolas Pauli commentarii | Atelier Frocher | 1539 | Zurich | [Zürich ZB – III B 14 \| G](https://doi.org/10.3931/e-rara-2604) |
| Calvin_1-Tim_C1_C3-6 | no | no | 82 | Jean Calvin | Commentarii in utranque Pauli epistolam ad Timotheum | Jean Girard | 1548 | Geneve | [Genève BGE – Bb 1493 (2)](https://doi.org/10.3931/e-rara-5708) |
| Lambertus_1-Tim_C3-6 | auto | auto | 422 | Lambert Daneau | Priorem Epistolam ad Timotheum | Eustathius Vignon | 1577 | Genève | [Genève BGE – BGE Cti 1753 / S 22877](https://doi.org/10.3931/e-rara-6338) |
| Hyperius_1-Tim_C2 | no | no | 121 | Hyperius Andreas | Commentarii in epistolas D. Pauli ad Timotheum | Christoph Froschauer | 1582 | Zurich | [Zürich ZB – C 85 \| G](https://doi.org/10.3931/e-rara-62382) |

* auto = data automaticly processed, with no human correction 

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


