# Bio Dataset Collection

An agentic search system for discovering and cataloging datasets and databases used in bioinformatics research. The agent surveys public registries, consortium portals, and curated repositories, then organizes results so researchers can quickly judge whether a resource fits their study.

## What This Project Does

- **Agentic discovery** — uses LLM-driven agents to search across bioinformatics data portals, publication supplements, and consortium websites.
- **Structured cataloging** — each dataset/database entry is captured with consistent metadata so resources can be compared side-by-side.
- **Access-mode triage** — flags barriers to access (public download vs. controlled access) up front, so users know what approvals they will need before starting.
- **Thematic organization** — groups resources by species and research theme so a user can ask "what human single-cell atlases exist?" or "what mouse epigenomics data is open?" and get a focused answer.

## Catalog Schema

Every entry in the catalog includes the following fields:

| Field | Description |
|---|---|
| `name` | Dataset or database name |
| `url` | Primary access URL |
| `provider` | Hosting institution or consortium |
| `species` | Organism(s) covered (e.g., *Homo sapiens*, *Mus musculus*, multi-species) |
| `research_themes` | Topics covered (e.g., cancer genomics, single-cell, microbiome) |
| `data_modalities` | Types of data (bulk RNA-seq, scRNA-seq, WGS, proteomics, imaging, EHR, etc.) |
| `access_mode` | See "Access Modes" below |
| `size` | Approximate scale (samples, cells, patients, terabytes) |
| `last_updated` | Most recent release or update date |
| `citation` | Primary publication / DOI |
| `notes` | Caveats, license terms, embargo periods |

## Access Modes

Datasets are tagged with one or more of the following access modes:

- **Public / Open** — Free download, no registration. Examples: NCBI GEO, Ensembl, UniProt.
- **Registration Required** — Free account creation needed; no formal review. Examples: cBioPortal API keys, some bulk download endpoints.
- **Usage Agreement / DUA** — Click-through or signed Data Use Agreement before download. Examples: UK Biobank summary stats, some TCGA derived data.
- **Controlled Access (DAC Approval)** — Application to a Data Access Committee with project description. Examples: dbGaP, EGA, UKB individual-level data.
- **IRB Approval Required** — Local Institutional Review Board approval needed in addition to DAC. Typical for identifiable human genomic + clinical data.
- **Institutional Membership** — Requires affiliation with a member institution or paid subscription. Examples: COSMIC commercial license, some clinical registries.
- **Embargoed** — Public after a stated release date; pre-embargo access via consortium membership.
- **Tiered Access** — Multiple levels (e.g., open summary statistics + controlled individual-level data).

## Organization by Species

The catalog is structured to support filtering by species, with primary groupings for:

- **Human** (*Homo sapiens*) — population genomics, clinical cohorts, cell atlases, cancer
- **Model organisms** — mouse, rat, zebrafish, fly, worm, yeast, *Arabidopsis*
- **Microbes** — bacteria, archaea, viruses (including pathogen surveillance)
- **Multi-species / comparative** — Ensembl, UCSC, NCBI taxonomy-spanning resources
- **Environmental / metagenomic** — soil, marine, host-associated microbiomes

## Organization by Research Theme

Entries are also indexed by research theme, including:

- **Genomics** — reference genomes, variation, population genetics
- **Transcriptomics** — bulk RNA-seq, single-cell RNA-seq, spatial transcriptomics
- **Epigenomics** — ChIP-seq, ATAC-seq, DNA methylation, Hi-C
- **Proteomics & Structural Biology** — mass spec, protein structures, interactions
- **Cancer Genomics** — somatic mutations, copy number, clinical outcomes
- **Clinical & EHR** — patient cohorts, biobanks, registries
- **Microbiome & Metagenomics** — 16S, shotgun metagenomics, MAGs
- **Imaging** — histopathology, radiology, microscopy
- **Drug Discovery & Chemoinformatics** — bioactivity, ADMET, chemical libraries
- **Phenotype & Ontology** — HPO, MONDO, GO, disease classifications

## How the Agentic Search Works

1. **Seeding** — the agent starts from curated lists (e.g., the Nucleic Acids Research Database Issue, FAIRsharing, re3data).
2. **Expansion** — follows references and "related resources" links from each entry.
3. **Extraction** — pulls metadata into the schema above using a mix of structured APIs and LLM-based extraction from landing pages.
4. **Normalization** — maps species names to NCBI taxonomy IDs and themes to controlled vocabularies.
5. **Verification** — flags entries whose URLs or access modes have changed since last crawl.

## Repository Layout

```
bio_dataset_collection/
├── README.md              # this file
├── catalog/               # per-resource metadata files
├── agents/                # agent prompts and search strategies
├── scripts/               # ingestion, normalization, validation
└── memory/                # session memory for the agent
```

## Status

Early development. The catalog schema and access-mode taxonomy are defined; agent-driven population is in progress.

## Contributing

Suggestions for resources to include, corrections to access modes, or theme tagging refinements are welcome via issue or PR.
