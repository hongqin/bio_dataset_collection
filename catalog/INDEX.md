# Catalog Index

Human-readable index of resources catalogued under `catalog/`. Each row links
to the structured YAML file that is the source of truth. See
[`schema.yaml`](schema.yaml) for field definitions and the controlled vocabularies
for `access_mode`, `research_themes`, and `data_modalities`.

## Human (*Homo sapiens*)

| Resource | Themes | Modalities | Access | File |
|---|---|---|---|---|
| [Mexico City Prospective Study](https://mcps-epcm.org/study.html) | population genetics, cardiometabolic disease, mortality | WGS, WES, genotyping, survey, linked mortality | tiered: public variant browser → DUA → DAC + analysis on DNAnexus | [`human/mcps.yaml`](human/mcps.yaml) |

## Dog (*Canis lupus familiaris*)

| Resource | Themes | Modalities | Access | File |
|---|---|---|---|---|
| [Dog Aging Project](https://dogagingproject.org/data-access) | geroscience, genomics, microbiome | WGS, RNA-seq, metabolomics, microbiome, EHR, survey, wearable, biobank | tiered: DUA + Terra; restricted fields need extra approval | [`dog/dog_aging_project.yaml`](dog/dog_aging_project.yaml) |

---

*This index is intended to be regenerated from the YAML files. For now it is
maintained by hand; a `scripts/build_index.py` will replace this when the
catalog grows.*
