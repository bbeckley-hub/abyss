<div align="center">

<img src="images/abyss_banner.png" alt="ABYSS banner" width="100%">

# 🌊 ABYSS

**Acinetobacter baumannii Yielding Surveillance System**

*One resource. Pasteur MLST, IC lineages, capsule typing, carbapenemases, and full metadata — free and open.*

[![Live Site](https://img.shields.io/badge/🌐_Live_Site-bbeckley--hub.github.io/abyss-0d9488?style=for-the-badge)](https://bbeckley-hub.github.io/abyss/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)
[![Genomes](https://img.shields.io/badge/Genomes-48,038_typed-blue?style=for-the-badge)](https://bbeckley-hub.github.io/abyss/)
[![Pages](https://img.shields.io/badge/Pages-12-purple?style=for-the-badge)](https://bbeckley-hub.github.io/abyss/)
[![Countries](https://img.shields.io/badge/Countries-100+-0891b2?style=for-the-badge)](https://bbeckley-hub.github.io/abyss/geography.html)
[![Part of ARGUS](https://img.shields.io/badge/Part%20of-ARGUS-0a1628?style=for-the-badge)](https://github.com/bbeckley-hub/argus)
[![Status](https://img.shields.io/badge/Status-v0.1-brightgreen?style=for-the-badge)](https://github.com/bbeckley-hub/abyss/releases)

[**🏠 Home**](https://bbeckley-hub.github.io/abyss/) ·
[**🧬 MLST**](https://bbeckley-hub.github.io/abyss/pages/mlst.html) ·
[**💊 AMR**](https://bbeckley-hub.github.io/abyss/pages/amr.html) ·
[**📊 Statistics**](https://bbeckley-hub.github.io/abyss/statistics.html) ·
[**🌍 Geography**](https://bbeckley-hub.github.io/abyss/geography.html) ·
[**👑 Lineages**](https://bbeckley-hub.github.io/abyss/lineages.html) ·
[**📥 Downloads**](https://bbeckley-hub.github.io/abyss/downloads.html) ·
[**ℹ️ About**](https://bbeckley-hub.github.io/abyss/about.html)

</div>

---

## 📖 What is ABYSS?

**ABYSS** is an open-access genomic resource that integrates every major *Acinetobacter baumannii* typing and gene-annotation scheme — **plus country, isolation source, host, and collection year** — into a single, queryable interface:

| Category | Modules |
|---|---|
| **Typing** | Pasteur MLST · International Clones (IC1–IC12) · OXA-51 variants · Kaptive KL + OCL capsule |
| **Genes** | AMR (carbapenemase-aware) · Virulence (VFDB) · Plasmid replicons |
| **Epidemiology** | Country · isolation source · host · collection year |
| **Lineage context** | Data-derived IC catalogue with live counts |
| **Retrieval** | Search → filter → export accession lists in one click |

No login, no API key, no install. Runs entirely in your browser over HTTPS.

> **The core deliverable is accession retrieval.** Every page lets you filter by genotype *and* geography and download the exact list of genome accessions that match — ready to feed to `datasets download genome accession`.

---

## 👁️ Part of the ARGUS family

ABYSS is the **third resource** of **ARGUS** — *Antimicrobial Resistance Genomic Unified Surveillance* — a family of independent, open genomic surveillance sites, each dedicated to one of the WHO priority ESKAPE pathogens. Every resource shares the same architecture: accession-first, metadata-integrated, no login, no install, MIT-licensed. Each has its own name, its own DOI, and its own community.

Named for **Argus Panoptes** — the hundred-eyed giant of Greek myth who never slept — the umbrella is a bet that AMR surveillance has to be *unified* to be useful, and that the pathogens driving the crisis deserve the same treatment.

| Resource | Pathogen | Status |
|---|---|---|
| 🦖 **SAURUS** | *Staphylococcus aureus* | [Live](https://bbeckley-hub.github.io/saurus/) |
| 🌑 **ECLIPSE** | *Escherichia coli* | [Live](https://bbeckley-hub.github.io/eclipse/) |
| 🌊 **ABYSS** | *Acinetobacter baumannii* | **This repo** — [live](https://bbeckley-hub.github.io/abyss/) |
| 🏆 **KLEOS** | *Klebsiella pneumoniae* | Planned |
| 💧 **PSEUDA** | *Pseudomonas aeruginosa* | Planned |
| 👑 **EMPIRE** | *Enterococcus faecium* | Planned |
| 🌀 **ENTROPY** | *Enterobacter* spp. | Planned |

Every sibling is built on the same architecture — a static site, accession-first design, with a shared generator template. That means once one resource works, the next one ships in weeks rather than months, and every resource benefits from improvements made in any other.

---

## 🌊 The name

> ***abyss*** (n.) — *an immeasurably deep gulf or great space.*

*Acinetobacter baumannii* lives in the abyss. Not the deep ocean — the deep hospital. The ventilator tubing. The mattress rail. The dry surface at 3am that nobody swabbed. The gap between equipment that infection control has stopped looking at.

These are the overlooked reservoirs of the ICU — the small, dark spaces where carbapenem-resistant *A. baumannii* survives for weeks, colonises the next patient, and waits. Surveillance fails in exactly those places, because we tend to look where we've always looked.

**ABYSS descends into those spaces.** From the genomes already sequenced and already public, the resource yields the surveillance that routine ICU rounds miss — every respiratory isolate, every bloodstream infection, every catheter tip, every dry-surface swab. It is a watch kept over the parts of the hospital nobody thinks to watch.

---

## 🎯 Project goal — annotate the full public *A. baumannii* collection

ABYSS is being built incrementally toward a single milestone: **complete typing annotation of every public *A. baumannii* genome** in the NCBI Assembly database.

| Milestone | Scope | Status |
|---|---|---|
| **v0.1** | 59,160 accessions · metadata + typing layer · 12 pages | ✅ **live** |
| **v0.3** | + remaining GCF (RefSeq) genomes | 🔜 **next** |
| **v0.4** | + GCA (GenBank) genomes | 📋 planned |
| **v0.5** | + Shelenkov-only GenBank | 📋 planned |
| **v1.0** | **Full collection · frozen release · citable DOI** | 🎯 target |

See the [**Roadmap**](#-roadmap) below for details.

---

## ✨ Features

<table>
<tr>
<td width="50%" valign="top">

### 🔬 Interactive typing pages

- **Live search** with exact-match operators (`ST2`, `IC2`, `KL2`)
- **Multi-column filters** — combine ST + IC + OXA-51 + KL + OCL + **Country + Source + Year**
- **Column visibility toggle** — persisted per browser
- **Row selection** with select-all-visible
- **Sortable columns** — numeric-aware
- **Pagination** — 20 / 50 / 100 rows per page
- **Export** — TSV · CSV · JSON · **accession-only**

</td>
<td width="50%" valign="top">

### 🌍 Geography &amp; Metadata

- **59,160 BioSample records** with country, source, host, year
- **96% country · 83% source · 91% host · 95% year** coverage
- **ICU lens** — source categories collapsed into epidemiological super-groups
- **4 interactive charts** — countries, sources, timeline, hosts
- **5 filters** — country · source · host · year · assembly level
- Full provenance — raw submitter strings preserved

</td>
</tr>
<tr>
<td valign="top">

### 🧬 Gene retrieval pages

- **Carbapenemase-aware** — OXA-23 · OXA-24/40 · OXA-58 · OXA-143 · NDM · KPC · VIM · IMP
- **Up to 5 genes per query**
- **ANY / ALL** match logic
- **Curated headline genes** for AMR, virulence, plasmid
- One-click **accession list export**
- **Click-to-copy** accession per row

</td>
<td valign="top">

### 👑 Lineage catalogue

- IC1–IC12 · **data-derived**, not curated from a static DB
- **Live sample counts** from the current dataset
- **Top STs per IC** — expanded view lists up to 60
- **OXA-51 variants observed** per IC
- **KL + OCL associations** joined from capsule
- **Export all accessions** per IC

</td>
</tr>
<tr>
<td valign="top">

### 📊 Statistics dashboard

- Distribution donuts — IC · KL · OCL · coverage
- Top 20 Pasteur STs · top 20 countries
- **Crosstab explorer** — pick any two dimensions
- Timeline of collection years
- Fully filter-aware — every chart responds

</td>
<td valign="top">

### 📥 Bulk downloads

- Every merged TSV as `.tsv.gz`
- Row counts + file sizes at a glance
- **`abyss_metadata.tsv.gz`** — full BioSample table
- **Long-format gene tables** — pivot-ready
- **Bulk ZIP** — one archive, everything inside

</td>
</tr>
</table>

---

## 🚀 Quick start

**Just visit the live site:**

### 👉 **https://bbeckley-hub.github.io/abyss/**

### Example workflow — get all IC2 carbapenem-resistant blood isolates from West Africa

1. Open [**MLST**](https://bbeckley-hub.github.io/abyss/pages/mlst.html) → filter:
   - `IC = IC2`
   - `Country = Ghana` (or `Nigeria`, `Senegal`, …)
   - `Source = blood`
2. Open [**AMR**](https://bbeckley-hub.github.io/abyss/pages/amr.html) → search `OXA-23`
3. Click **🧬 Accessions** → save the `.txt` file
4. Feed it to NCBI:

   ```bash
   datasets download genome accession --inputfile accessions.txt
   ```

5. ✅ You have the exact genomes you want, filtered by genotype *and* geography

Or start from the [**Geography page**](https://bbeckley-hub.github.io/abyss/geography.html) to browse the collection by country, source, host, or year.

---

## 🗺️ Roadmap

<details>
<summary><b>v0.1 — Foundation + typing layer</b> ✅ live</summary>

- [x] 12 pages live: index · about · mlst · capsule · master · amr · vfdb · plasmid · statistics · geography · lineages · downloads
- [x] 59,160 accessions indexed with full BioSample metadata
- [x] 48,038 genomes typed — Pasteur ST · IC1–IC12 · OXA-51 · Kaptive KL + OCL
- [x] Gene content — AMR · VFDB · plasmid replicons
- [x] Interactive statistics dashboard with crosstab explorer
- [x] Data-derived IC catalogue with per-IC accession export
- [x] Gzipped bulk downloads + single-archive ZIP
- [x] GitHub Pages deployment + Zenodo DOI

**Dataset:** Shelenkov 2024 (47,738) + AcinetoScope supplement (300)

</details>

<details open>
<summary><b>v0.3 — Complete RefSeq coverage</b> 🔜 next</summary>

- [ ] Fetch full RefSeq (GCF) assembly manifest for *A. baumannii* (taxonomy ID 470)
- [ ] Dedupe by numeric accession stem, GCF-preferred
- [ ] Type the remaining GCF genomes through AcinetoScope
- [ ] Merge new batches into `mlst_all.tsv` and `capsule_all.tsv`
- [ ] Regenerate all pages — every count picks up the new samples automatically

</details>

<details>
<summary><b>v0.4 — GenBank expansion</b> 📋 planned</summary>

- [ ] Type the full GenBank (GCA) collection
- [ ] Per-batch provenance tracking — users see which batch contributed each genome
- [ ] Handle GCA ↔ GCF paired accessions cleanly
- [ ] Merge into unified master table

</details>

<details>
<summary><b>v0.5 — Shelenkov-only GenBank</b> 📋 planned</summary>

- [ ] Include GCA genomes present only in Shelenkov 2024 but not typed here
- [ ] Deduplication pass
- [ ] AMR / VFDB / plasmid annotations carried forward

</details>

<details>
<summary><b>v1.0 — Full resource</b> 🎯 target</summary>

- [ ] **Every public *A. baumannii* genome** typed
- [ ] Cross-module filter UI — IC + ST + KL + OCL + country + source + any gene
- [ ] Boolean query builder for advanced users
- [ ] **Frozen, versioned release**
- [ ] **Zenodo DOI** for citable archive
- [ ] Database article submitted (*Microbial Genomics* or *Database* — Oxford)

</details>

---

## 🧬 Data sources

| Layer | Source | Coverage |
|---|---|---|
| **Typing** | [AcinetoScope](https://doi.org/10.1038/s41598-026-70189-y) (Beckley et al., *Sci Rep* 2026) | 300 supplement |
| **Typing + gene matrices** | [Shelenkov et al. 2024](https://doi.org/10.3390/data9020022) (*Data*, MDPI) | 47,738 genomes |
| **Metadata** | [NCBI BioSample](https://www.ncbi.nlm.nih.gov/biosample/) via `datasets summary genome` | 59,160 records |
| **AMR genes** | Shelenkov 2024 (AMRFinderPlus + ABRicate) | 45,000+ |
| **Virulence (VFDB)** | Shelenkov 2024 | 45,000+ |
| **Plasmid replicons** | Shelenkov 2024 (PlasmidFinder + APT) | 45,000+ |

All genome identifiers use the standard `GCA_XXXXXXXXX.Y` or `GCF_XXXXXXXXX.Y` format. Gene tables are GCA-keyed. Metadata is GCF-preferred. All joins go through the numeric accession stem.

---

## 📁 Repository structure

```
abyss/
├── README.md
├── LICENSE
├── images/
│   └── abyss_banner.png
└── docs/                          ← GitHub Pages site (source: main /docs)
    ├── .nojekyll
    ├── index.html                 ← landing page
    ├── about.html                 ← project + team + methods
    ├── statistics.html            ← interactive dashboard + crosstab
    ├── geography.html             ← metadata browser + ICU lens
    ├── lineages.html              ← IC1–IC12 data-derived catalogue
    ├── downloads.html             ← bulk data index
    ├── master.html                ← all typings, one view
    ├── assets/
    │   └── chart.min.js           ← Chart.js (bundled locally)
    ├── data/                      ← bulk .tsv.gz downloads + lazy JSON
    │   ├── *.tsv.gz               ← typing + gene tables
    │   ├── abyss_metadata.tsv.gz  ← BioSample metadata
    │   ├── master_samples.json    ← lazy-loaded master
    │   └── abyss_data_all.zip     ← everything, one archive
    └── pages/
        ├── mlst.html              ← Pasteur ST + IC + OXA-51
        ├── capsule.html           ← Kaptive KL + OCL
        ├── amr.html               ← carbapenemase-aware retrieval
        ├── vfdb.html              ← virulence gene retrieval
        ├── plasmid.html           ← replicon retrieval
        └── data/                  ← per-page JSON indexes
```

> `merged/`, `batches/`, and `logs/` are git-ignored — they hold the local pipeline.

---

## 🛠️ Running locally

**Prerequisites:** Python 3.9+

```bash
git clone https://github.com/bbeckley-hub/abyss.git
cd abyss/docs
python3 -m http.server 8000
```

Open **http://localhost:8000/**.

> ⚠️ **HTTP required.** The per-page samples use `fetch()` to load JSON. Browsers block this from `file://` URLs. Served over HTTP (or from GitHub Pages), it just works.

---

## 🧪 Regenerating pages

Each page is produced by a self-contained Python script in `merged/`. The recommended sequence:

```bash
cd merged/

# Supporting pages
python3 generate_index.py                -o ../docs/index.html
python3 generate_statistics.py           -o ../docs/statistics.html
python3 generate_lineages.py             -o ../docs/lineages.html
python3 generate_downloads.py            -o ../docs/downloads.html
python3 generate_about.py                -o ../docs/about.html

# Typing + gene pages (pre-existing)
python3 generate_mlst.py                 -o ../docs/pages/mlst.html
python3 generate_capsule.py              -o ../docs/pages/capsule.html
python3 generate_gene_page.py --db all   --outdir ../docs/pages/ --datadir ../docs/pages/data
python3 generate_master.py               -o ../docs/master.html
python3 generate_geography.py            -o ../docs/geography.html
```

The `generate_downloads.py` step also gzips every merged TSV and rebuilds the bulk ZIP. Run it **last** so the archive reflects the latest data.

---

## 🤝 Contributing

We welcome:

- 🐛 **Bug reports** — [open an issue](https://github.com/bbeckley-hub/abyss/issues)
- 💡 **Feature suggestions** — [start a discussion](https://github.com/bbeckley-hub/abyss/discussions)
- 🧬 **Data corrections** — if you spot a lineage call that doesn't match the literature
- 📊 **New metadata sources** — geographic crosswalks, country name normalizations

Please keep pages **self-contained** (one script per page) and preserve the shared visual style. The `.argus-nav` and `.argus-footer` CSS class names are family-wide — do not rename them.

---

## 📚 Citation

If you use ABYSS in your research, please cite the typing pipeline and the source gene dataset.

### Typing pipeline

> **Beckley B, Amarh V, Lopes BS, et al.** AcinetoScope: a computational pipeline for rapid, comprehensive *Acinetobacter baumannii* outbreak investigation and resistance gene tracking. *Scientific Reports*. 2026.
> [doi:10.1038/s41598-026-70189-y](https://doi.org/10.1038/s41598-026-70189-y)

### Gene + typing dataset

> **Shelenkov A, Mikhaylova Y, Akimkin V.** Genomic Epidemiology Dataset for the Important Nosocomial Pathogenic Bacterium *Acinetobacter baumannii*. *Data*. 2024;9(2):22.
> [doi:10.3390/data9020022](https://doi.org/10.3390/data9020022)

### Metadata source

> **NCBI BioSample** — country, isolation source, host, and collection date attributes attached to each assembly.

### Cite ABYSS itself

> **Beckley B.** ABYSS: *Acinetobacter baumannii* Yielding Surveillance System. 2026.
> [github.com/bbeckley-hub/abyss](https://github.com/bbeckley-hub/abyss)

---

## 🙏 Acknowledgements

ABYSS stands on the shoulders of the open-source genomics community. We thank:

- **Brown Beckley & Vincent Amarh** — for AcinetoScope, the typing engine
- **Andrey Shelenkov & colleagues** — for publishing their genomic epidemiology dataset openly
- **NCBI** — for the `datasets` CLI, AMRFinderPlus, and the Assembly + BioSample databases
- **Torsten Seemann** — for `mlst`, `ABRicate`, and a decade of pipeline standards
- **Kelly Wyres, Ryan Wick & the Kaptive team** — for `Kaptive 3` and the *A. baumannii* K-locus database
- **Ruth Hall, Mehrad Hamidian & the APT team** — for `APT` (Acinetobacter Plasmid Typing)
- **Center for Genomic Epidemiology (DTU)** — for `ResFinder`
- **PubMLST & the Oxford MLST team** — for allele and ST reference databases
- **The CARD, VFDB, MEGARes, ARG-ANNOT, and BacMet teams** — for their reference databases
- **The Python scientific stack** — pandas, numpy, Chart.js, and every dependency in between

---

## 📄 License

**MIT License** — free to use, modify, and redistribute. Attribution appreciated.

See [LICENSE](LICENSE) for details.

---

<div align="center">

**Built with 🌊 at the University of Ghana Medical School**

*Watching the parts of the hospital nobody thinks to watch.*

**[⭐ Star this repo](https://github.com/bbeckley-hub/abyss)** if you find it useful.

</div>
