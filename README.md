# quant_20 gene miscount lookup

A self-contained, searchable report covering all 19,408 canonical genes from the `quant_20` long-read RNA-seq quantification benchmark. For each gene, it shows how StringTie, bambu, oarfish, and lr-kallisto quantified it against:

- **Exp 1 / 1A (n=0)** — canonical-only reference
- **Exp 2 / 2A (n=20)** — canonical + 20 non-canonical isoforms/gene reference

## Features

- **Gene search** — look up any gene by name or Ensembl ID, see per-tool status (correct / zero / under-count / over-count) and read counts for both experiments, plus flags for isoform-corruption events and known causes (gene overlap, sequence paralog).
- **Browse by tool** — click any of the 4 tools to open a sortable, filterable table of every gene it miscounted in either experiment.

No build step, no server — `index.html` is fully self-contained (data embedded inline).

## Data source

Generated from the `longread-analysis` pipeline's `quant_20` experiment (`1B_2B_analysis/correctness_with_neighbors_and_paralogs.csv`).
