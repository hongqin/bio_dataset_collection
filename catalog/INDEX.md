# Catalog Index

Human-readable index of resources catalogued under `catalog/`. Each row links
to the structured YAML file that is the source of truth. See
[`schema.yaml`](schema.yaml) for field definitions and the controlled
vocabularies for `access_mode`, `research_themes`, `data_modalities`, and
the structured `counts:` map (for sortable scale comparisons).

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
| [Open Targets Platform](https://platform.opentargets.org/) | 63k targets × 28k diseases (CC0) | drug discovery, variant-to-function | [`human/open_targets.yaml`](human/open_targets.yaml) |
| [BioBank Japan PheWeb](https://pheweb.jp/) | hundreds of phenotype GWAS in Japanese ancestry | East Asian population genetics, cardiometabolic | [`human/biobank_japan.yaml`](human/biobank_japan.yaml) |
| [SEA-AD](https://portal.brain-map.org/explore/seattle-alzheimers-disease) | ~84 donors, ~2.9M nuclei (snRNA + snATAC + MERFISH) | single-cell, Alzheimer's disease | [`human/sea_ad.yaml`](human/sea_ad.yaml) |
| [CZ CELLxGENE Discover / Census](https://cellxgene.cziscience.com/) | ~93M cells aggregated; Census API for cross-dataset queries | single-cell aggregation | [`human/cellxgene_census.yaml`](human/cellxgene_census.yaml) |
| [Tabula Sapiens](https://tabula-sapiens-portal.ds.czbiohub.org/) | 483k cells across 24 tissues / 14 donors (v2: ~1.1M) | reference cell atlas | [`human/tabula_sapiens.yaml`](human/tabula_sapiens.yaml) |
| [Human Cell Atlas](https://www.humancellatlas.org/) | ~50M cells across 200+ harmonized projects | community cell atlases | [`human/human_cell_atlas.yaml`](human/human_cell_atlas.yaml) |

### Tiered (public summary + controlled individual-level)

| Resource | Public tier | Controlled tier | File |
|---|---|---|---|
| [GTEx](https://www.gtexportal.org/) | expression matrices, eQTLs/sQTLs across 54 tissues | individual genotypes + RNA-seq BAMs via dbGaP | [`human/gtex.yaml`](human/gtex.yaml) |
| [FinnGen](https://www.finngen.fi/) | GWAS summary stats (form-gated, no DAC) for ~500k Finns | individual-level via Finnish biobanks | [`human/finngen.yaml`](human/finngen.yaml) |
| [NHANES](https://www.cdc.gov/nchs/nhanes/) | surveys, exam, dietary, lab measurements (open) | DNA specimens + genotype data via NCHS RDC | [`human/nhanes.yaml`](human/nhanes.yaml) |
| [NCHS Linked Mortality Files](https://www.cdc.gov/nchs/data-linkage/mortality.htm) | adult public-use LMF (NHIS/NHANES → NDI) | restricted-use LMF (adults + kids, full ICD) via RDC | [`human/nchs_linked_mortality.yaml`](human/nchs_linked_mortality.yaml) |
| [Mexico City Prospective Study](https://mcps-epcm.org/study.html) | variant browser ([RGC-MCPS](https://rgc-mcps.regeneron.com)) | WGS/WES/genotyping + EHR on DNAnexus, DAC review | [`human/mcps.yaml`](human/mcps.yaml) |
| [All of Us](https://www.researchallofus.org/) | Data Browser aggregates (no registration) | WGS + EHR + wearable on Researcher Workbench, DUA + IRB-style training | [`human/all_of_us.yaml`](human/all_of_us.yaml) |

### Population health & surveillance (US, fully public)

| Resource | Data | Themes | File |
|---|---|---|---|
| [CDC WONDER](https://wonder.cdc.gov/) | aggregate mortality, natality, cancer incidence, infectious disease, environmental | epidemiology, mortality, population health | [`human/cdc_wonder.yaml`](human/cdc_wonder.yaml) |
| [BRFSS](https://www.cdc.gov/brfss/) | 400k+ annual telephone interviews, state-level chronic disease + behavior | behavioral health, chronic disease, health equity | [`human/brfss.yaml`](human/brfss.yaml) |
| [US Census Bureau / ACS](https://www.census.gov/data/developers.html) | decennial + ACS tabulations + PUMS microdata + TIGER/Line + SAHIE | demography, SDOH, population denominators | [`human/us_census_acs.yaml`](human/us_census_acs.yaml) |

---

## Mouse (*Mus musculus*)

| Resource | Data | Themes | File |
|---|---|---|---|
| [MGI](https://www.informatics.jax.org/) | ~50k curated alleles, 1,500+ disease models, gene nomenclature | functional genomics, model organism | [`mouse/mgi.yaml`](mouse/mgi.yaml) |
| [IMPC](https://www.mousephenotype.org/) | systematic KO phenotyping; 85M data points, 9,000+ genes phenotyped | knockout phenotyping, disease models | [`mouse/impc.yaml`](mouse/impc.yaml) |
| [Mouse Phenome Database](https://phenome.jax.org/) | quantitative phenotypes across >6,000 strains (CC, DO, inbred) | quantitative genetics, GWAS, aging | [`mouse/mpd.yaml`](mouse/mpd.yaml) |
| [Tabula Muris (Senis)](https://tabula-muris.ds.czbiohub.org/) | 100k cells, 20 tissues (Muris); 529k cells, 6 ages (Senis) | single-cell, aging, reference atlas | [`mouse/tabula_muris.yaml`](mouse/tabula_muris.yaml) |

---

## Chicken (*Gallus gallus*) and other livestock

| Resource | Data | Themes | File |
|---|---|---|---|
| [Animal QTLdb](https://www.animalgenome.org/cgi-bin/QTLdb/index) | ~158,500 QTL/association records across cattle, pig, **chicken**, sheep, horse, goat, trout | livestock genomics, animal breeding | [`multi_species/animal_qtldb.yaml`](multi_species/animal_qtldb.yaml) |

---

## Plants

| Resource | Species | Data | File |
|---|---|---|---|
| [1001 Genomes](https://1001genomes.org/) | *Arabidopsis thaliana* | 1,135 accessions, ~5M SNPs + AraPheno phenotypes | [`plants/arabidopsis_1001.yaml`](plants/arabidopsis_1001.yaml) |
| [3000 Rice Genomes](https://iric.irri.org/projects/3000-rice-genomes-project) | *Oryza sativa* | 3,024 accessions from 89 countries, ~20M SNPs | [`plants/rice_3000.yaml`](plants/rice_3000.yaml) |

---

## Yeast (*Saccharomyces cerevisiae*)

| Resource | Data | Themes | File |
|---|---|---|---|
| [SGD](https://www.yeastgenome.org/) | reference genome + curated phenotype/GO/interaction annotations | functional genomics, phenotype ontology | [`yeast/sgd.yaml`](yeast/sgd.yaml) |
| [1002 Yeast Genomes](http://1002genomes.u-strasbg.fr/) | 1,011 natural isolates resequenced + high-throughput phenotyping | population genetics, GWAS | [`yeast/yeast_1002.yaml`](yeast/yeast_1002.yaml) |

---

## Bacteria & archaea

| Resource | Data | Themes | File |
|---|---|---|---|
| [GTDB](https://gtdb.ecogenomic.org/) | 901,341 genomes (878,998 bacterial + 22,343 archaeal), phylogenomic taxonomy | microbial taxonomy, phylogenomics | [`bacteria/gtdb.yaml`](bacteria/gtdb.yaml) |
| [BV-BRC](https://www.bv-brc.org/) | 1.3M bacterial + 15M viral genomes with consistent RASTtk annotation + AMR | infectious disease, AMR, pathogen surveillance | [`bacteria/bv_brc.yaml`](bacteria/bv_brc.yaml) |

---

## Dog (*Canis lupus familiaris*)

| Resource | Access | Themes | File |
|---|---|---|---|
| [Dog Aging Project](https://dogagingproject.org/data-access) | DUA + Terra; tiered | geroscience, genomics, microbiome | [`dog/dog_aging_project.yaml`](dog/dog_aging_project.yaml) |
| [Darwin's Ark](https://darwinsark.org/) | public (citizen science) | ancestry, behavior genetics, companion-animal health | [`dog/darwins_ark.yaml`](dog/darwins_ark.yaml) |

---

## Microbes & viruses (pathogen-focused)

| Resource | Access | Themes | File |
|---|---|---|---|
| [GISAID](https://gisaid.org/) | registration + DAA (free, identity-gated) | viral genomics, pathogen surveillance, public health | [`microbes/gisaid.yaml`](microbes/gisaid.yaml) |

---

## Protein structures & cryo-EM

### Experimental and integrative structures

| Resource | Data | Access | File |
|---|---|---|---|
| [PDB / RCSB / wwPDB](https://www.rcsb.org/) | 227k experimental structures + 1M CSMs | public, CC0 | [`proteins/pdb.yaml`](proteins/pdb.yaml) |
| [PDB-IHM](https://pdb-ihm.org/) | 382 integrative/hybrid models (formerly PDB-Dev) | public, CC0 | [`proteins/pdb_ihm.yaml`](proteins/pdb_ihm.yaml) |

### Predicted structures

| Resource | Data | Access | File |
|---|---|---|---|
| [AlphaFold DB](https://alphafold.ebi.ac.uk/) | ~261M predicted structures covering UniProt | public, CC-BY 4.0 | [`proteins/alphafold_db.yaml`](proteins/alphafold_db.yaml) |
| [ESM Metagenomic Atlas](https://esmatlas.com/) | ~617M ESMFold predictions of metagenomic proteins | public, CC-BY 4.0 | [`proteins/esm_atlas.yaml`](proteins/esm_atlas.yaml) |
| [ModelArchive](https://www.modelarchive.org/) | Non-AlphaFold predicted structures and complexes (RoseTTAFold, homology, ab initio) | public | [`proteins/model_archive.yaml`](proteins/model_archive.yaml) |

### Cryo-EM and cryo-ET

| Resource | Data | Access | File |
|---|---|---|---|
| [EMDB](https://www.ebi.ac.uk/emdb/) | 57k+ cryo-EM 3D reconstructions | public, CC0 | [`proteins/emdb.yaml`](proteins/emdb.yaml) |
| [EMPIAR](https://www.ebi.ac.uk/empiar/) | 2,900 raw cryo-EM image datasets (8.5 PiB) | public, CC0 | [`proteins/empiar.yaml`](proteins/empiar.yaml) |
| [CZ CryoET Data Portal](https://cryoetdataportal.czscience.com/) | >17,000 tomograms, 45 species, ML-ready annotations | public, CC-BY 4.0 | [`proteins/cryoet_data_portal.yaml`](proteins/cryoet_data_portal.yaml) |
| [ETDB-Caltech](https://etdb.caltech.edu/) | >11,000 cellular cryo-ET datasets (Jensen Lab), 100+ microbial species | public | [`proteins/etdb_caltech.yaml`](proteins/etdb_caltech.yaml) |
| [CryoBench](https://cryobench.cs.princeton.edu/) | 5 simulated benchmarks for heterogeneous reconstruction (NeurIPS 2024) | public, CC-BY | [`proteins/cryobench.yaml`](proteins/cryobench.yaml) |

---

## Clinical / EHR & medical imaging

### EHR / clinical

| Resource | Access | Scale | File |
|---|---|---|---|
| [Synthea / SyntheticMass](https://synthea.mitre.org/) | fully public (synthetic, Apache 2.0) | ~1M synthetic MA patients + generator | [`medical/synthea.yaml`](medical/synthea.yaml) |
| [MIMIC-IV](https://physionet.org/content/mimiciv/) | credentialed (CITI training + DUA), free | ~300k patients, BIDMC 2008–2022 | [`medical/mimic_iv.yaml`](medical/mimic_iv.yaml) |
| [eICU-CRD](https://eicu-crd.mit.edu/) | credentialed (PhysioNet) | ~200k ICU admissions, ~208 US hospitals | [`medical/eicu_crd.yaml`](medical/eicu_crd.yaml) |
| [N3C COVID Enclave](https://covid.cd2h.org/) | institutional DUA + cloud-only analysis | ~22M patients across 75+ sites | [`medical/n3c.yaml`](medical/n3c.yaml) |

### Medical imaging

| Resource | Access | Scale | File |
|---|---|---|---|
| [TCIA](https://www.cancerimagingarchive.net/) | mostly public (per-collection DOI) | 175+ collections, ~80k patients, multi-modal | [`medical/tcia.yaml`](medical/tcia.yaml) |
| [NIH ChestX-ray14](https://nihcc.app.box.com/v/ChestXray-NIHCC) | public, attribution only | 112,120 X-rays, 30,805 patients | [`medical/chestxray14.yaml`](medical/chestxray14.yaml) |
| [CheXpert](https://aimi.stanford.edu/datasets/chexpert-chest-x-rays) | request + Stanford non-commercial license | 224,316 X-rays, 65,240 patients | [`medical/chexpert.yaml`](medical/chexpert.yaml) |

---

## Bioimaging & volumetric image archives

| Resource | Data | Scale | File |
|---|---|---|---|
| [BioImage Archive](https://www.ebi.ac.uk/bioimage-archive/) | cross-modality umbrella (light + EM + MRI + microCT + more) | ~1,500 studies; 10s of PB | [`imaging/bioimage_archive.yaml`](imaging/bioimage_archive.yaml) |
| [IDR (Cell-IDR + Tissue-IDR)](https://idr.openmicroscopy.org/) | curated light microscopy + high-content screens | ~100 reference studies; 100s TB | [`imaging/idr.yaml`](imaging/idr.yaml) |
| [OpenOrganelle (Janelia COSEM)](https://openorganelle.janelia.org/) | FIB-SEM volumes of whole cells @ 4nm/voxel, 35 organelle classes | ~30 datasets | [`imaging/openorganelle.yaml`](imaging/openorganelle.yaml) |
| [Allen Cell Imaging Collections](https://www.allencell.org/) | 3D live-cell fluorescence on 25 gene-edited WTC-11 hiPS lines | ~200k cell volumes | [`imaging/allen_cell.yaml`](imaging/allen_cell.yaml) |
| [MorphoSource](https://www.morphosource.org/) | microCT specimens (largely vertebrate skeletal) | ~27,000 models (~13k open-access) | [`imaging/morphosource.yaml`](imaging/morphosource.yaml) |
| [WormAtlas + WormWiring + OpenWorm](https://www.wormatlas.org/) | C. elegans connectomes, EM, anatomy, lineage | 302 neurons; 8+ published connectomes | [`imaging/wormatlas.yaml`](imaging/wormatlas.yaml) |

> **Gap:** I did not find a consolidated public database for **plant microCT / volumetric imaging**. Most plant-root microCT data lives in per-paper supplementary materials (e.g., DIRT/3D for maize root crowns, synchrotron Arabidopsis root studies) rather than a single repository. The closest umbrella resources that DO accept plant imaging submissions are [BioImage Archive](https://www.ebi.ac.uk/bioimage-archive/) and (for community deposition) [Plant Image Analysis (plant-image-analysis.org)](https://www.plant-image-analysis.org/) — neither is a centralized microCT database.

---

## AI / ML foundation models (single-cell)

These are pre-trained model resources, not datasets — included because they
are part of the same data ecosystem (trained on CELLxGENE) and surfaced on
the CZ Virtual Cells Platform.

| Model | Training scale | License | File |
|---|---|---|---|
| [scGPT](https://virtualcellmodels.cziscience.com/model/scgpt) | ~33M cells (human + mouse) | CC-BY-NC-ND on checkpoints, MIT code | [`models/scgpt.yaml`](models/scgpt.yaml) |
| [UCE — Universal Cell Embeddings](https://virtualcellmodels.cziscience.com/model/uce) | ~36M cells across 8 species; zero-shot cross-species | MIT | [`models/uce.yaml`](models/uce.yaml) |
| [TranscriptFormer](https://virtualcellmodels.cziscience.com/model/transcriptformer) | 112M cells × 12 species spanning 1.5B years of evolution | open weights | [`models/transcriptformer.yaml`](models/transcriptformer.yaml) |
| [Geneformer](https://huggingface.co/ctheodoris/Geneformer) | 30M (V1) → 104M (V2) human non-cancer cells | Apache 2.0 (most permissive) | [`models/geneformer.yaml`](models/geneformer.yaml) |

---

## Multi-species / comparative

| Resource | Access | Themes | File |
|---|---|---|---|
| [DOE JGI](https://data.jgi.doe.gov/) | public, click-through data-use policy | microbial/fungal/plant genomics, metagenomics, bioenergy | [`multi_species/jgi.yaml`](multi_species/jgi.yaml) |
| [GGBN + Smithsonian GGI](https://www.ggbn.org/) | metadata public; physical samples via MTA | biodiversity genomics, conservation, taxonomy | [`multi_species/ggbn.yaml`](multi_species/ggbn.yaml) |
| [Animal QTLdb](https://www.animalgenome.org/cgi-bin/QTLdb/index) | public | livestock QTL across 7 species | [`multi_species/animal_qtldb.yaml`](multi_species/animal_qtldb.yaml) |
| [Zebrahub](https://zebrahub.ds.czbiohub.org/) | public | zebrafish development scRNA-seq (~120k cells, 10 stages) | [`multi_species/zebrahub.yaml`](multi_species/zebrahub.yaml) |

---

*This index is intended to be regenerated from the YAML files. For now it is
maintained by hand; a `scripts/build_index.py` will replace this once the
catalog grows further.*
