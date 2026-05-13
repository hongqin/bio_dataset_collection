# Catalog Index

Human-readable index of resources catalogued under `catalog/`. Each row links
to the structured YAML file that is the source of truth. See
[`schema.yaml`](schema.yaml) for field definitions and the controlled
vocabularies for `access_mode`, `research_themes`, and `data_modalities`.

Entries are organized first by **species**, then sorted so that the **most
openly accessible** resources appear at the top of each table — public-open
first, then tiered, then controlled.

---

## Human (*Homo sapiens*) — genotype + phenotype resources

### Fully public (no application)

| Resource | Data | Themes | File |
|---|---|---|---|
| [gnomAD](https://gnomad.broadinstitute.org/) | 730k exomes + 76k genomes (allele frequencies, constraint, SVs) | population genetics, variant interpretation, rare disease | [`human/gnomad.yaml`](human/gnomad.yaml) |
| [1000 Genomes / IGSR](https://www.internationalgenome.org/) | 3,202 high-coverage WGS, 26 populations, phased haplotypes | reference panel, population genetics | [`human/1000_genomes.yaml`](human/1000_genomes.yaml) |
| [HGDP + harmonized 1kGP+HGDP](https://www.internationalgenome.org/data-portal/data-collection/hgdp) | 929 HGDP genomes; 4,094 harmonized 30x WGS | diversity panel, human evolution | [`human/hgdp.yaml`](human/hgdp.yaml) |
| [NHGRI-EBI GWAS Catalog](https://www.ebi.ac.uk/gwas/) | 85k+ summary-stats files across 5,000+ traits | GWAS, polygenic risk, phenotype ontology | [`human/gwas_catalog.yaml`](human/gwas_catalog.yaml) |
| [Pan-UK Biobank](https://pan.ukbb.broadinstitute.org/) | 16,131 GWAS × 6 ancestries × 7,228 phenotypes | multi-ancestry GWAS | [`human/pan_ukbb.yaml`](human/pan_ukbb.yaml) |
| [Open Targets Platform](https://platform.opentargets.org/) | target–disease evidence, L2G, GWAS coloc (CC0) | drug discovery, variant-to-function | [`human/open_targets.yaml`](human/open_targets.yaml) |
| [BioBank Japan PheWeb](https://pheweb.jp/) | hundreds of phenotype GWAS in Japanese ancestry | East Asian population genetics, cardiometabolic | [`human/biobank_japan.yaml`](human/biobank_japan.yaml) |
| [SEA-AD](https://portal.brain-map.org/explore/seattle-alzheimers-disease) | snRNA-seq + snATAC-seq + MERFISH + neuropathology from ~80 AD-continuum brains | single-cell, Alzheimer's disease | [`human/sea_ad.yaml`](human/sea_ad.yaml) |

### Tiered (public summary + controlled individual-level)

| Resource | Public tier | Controlled tier | File |
|---|---|---|---|
| [GTEx](https://www.gtexportal.org/) | expression matrices, eQTLs/sQTLs across 54 tissues | individual genotypes + RNA-seq BAMs via dbGaP | [`human/gtex.yaml`](human/gtex.yaml) |
| [FinnGen](https://www.finngen.fi/) | GWAS summary stats (form-gated, no DAC) for ~500k Finns | individual-level via Finnish biobanks | [`human/finngen.yaml`](human/finngen.yaml) |
| [Mexico City Prospective Study](https://mcps-epcm.org/study.html) | variant browser ([RGC-MCPS](https://rgc-mcps.regeneron.com)) | WGS/WES/genotyping + EHR on DNAnexus, DAC review | [`human/mcps.yaml`](human/mcps.yaml) |
| [All of Us](https://www.researchallofus.org/) | Data Browser aggregates (no registration) | WGS + EHR + wearable on Researcher Workbench, DUA + IRB-style training | [`human/all_of_us.yaml`](human/all_of_us.yaml) |

---

## Dog (*Canis lupus familiaris*)

| Resource | Access | Themes | File |
|---|---|---|---|
| [Dog Aging Project](https://dogagingproject.org/data-access) | DUA + Terra; tiered | geroscience, genomics, microbiome | [`dog/dog_aging_project.yaml`](dog/dog_aging_project.yaml) |
| [Darwin's Ark](https://darwinsark.org/) | public (citizen science) | ancestry, behavior genetics, companion-animal health | [`dog/darwins_ark.yaml`](dog/darwins_ark.yaml) |

---

## Microbes & viruses

| Resource | Access | Themes | File |
|---|---|---|---|
| [GISAID](https://gisaid.org/) | registration + DAA (free, identity-gated) | viral genomics, pathogen surveillance, public health | [`microbes/gisaid.yaml`](microbes/gisaid.yaml) |

---

## Multi-species / comparative

| Resource | Access | Themes | File |
|---|---|---|---|
| [DOE JGI](https://data.jgi.doe.gov/) | public, click-through data-use policy | microbial/fungal/plant genomics, metagenomics, bioenergy | [`multi_species/jgi.yaml`](multi_species/jgi.yaml) |
| [GGBN + Smithsonian GGI](https://www.ggbn.org/) | metadata public; physical samples via MTA | biodiversity genomics, conservation, taxonomy | [`multi_species/ggbn.yaml`](multi_species/ggbn.yaml) |

---

*This index is intended to be regenerated from the YAML files. For now it is
maintained by hand; a `scripts/build_index.py` will replace this once the
catalog grows further.*
