# Rubberized-concrete multi-output datasets (D1–D5)

Five tabular datasets of rubberized concrete compiled from 65 published experimental studies. They are the
rubberized-concrete datasets used in the manuscript *Joint versus independent modeling in multi-output
regression: A controlled same-learner comparison on simulated and real data* (D. Li, J. He, F. Liu).

| Dataset | Samples | Source studies | Outputs |
|---|---|---|---|
| D1 | 184 | 14 | compressive strength, splitting tensile strength, flexural strength |
| D2 | 356 | 27 | compressive strength, splitting tensile strength |
| D3 | 241 | 21 | compressive strength, flexural strength |
| D4 | 329 | 18 | slump, compressive strength |
| D5 | 328 | 24 | compressive strength, splitting tensile strength, flexural strength, slump |

## Columns

Every file in `data/` has the same first eleven columns; the remaining columns are the outputs of that dataset.

| Column | Meaning | Unit |
|---|---|---|
| source_id | Identifier of the source study, see `sources.csv` | – |
| wb_ratio | Water-to-binder ratio | – |
| cement_kg_m3 | Cement content | kg/m³ |
| fine_aggregate_kg_m3 | Fine aggregate content | kg/m³ |
| water_kg_m3 | Water content | kg/m³ |
| coarse_aggregate_kg_m3 | Coarse aggregate content | kg/m³ |
| superplasticizer_kg_m3 | Superplasticizer content | kg/m³ |
| rubber_size_mm | Approximate rubber particle size | mm |
| rubber_mass_kg_m3 | Rubber content | kg/m³ |
| rubber_volume_pct | Rubber volume as a percentage of the total concrete volume | % |
| age_d | Curing age | d |
| compressive_strength_MPa | Compressive strength | MPa |
| splitting_tensile_strength_MPa | Splitting tensile strength | MPa |
| flexural_strength_MPa | Flexural strength | MPa |
| slump_mm | Slump | mm |

## Compilation notes

- Each row is one mix and one curing age reported in a source study; values were read from tables or, where only
  figures were given, digitised from the figures. Rows with any missing input or output were removed.
- Mixes without rubber (rubber content 0) are the control mixes of the same source study.
- The source tests mostly used standard specimens and standard curing, but specimen size, curing conditions and
  testing practice differ between studies and are not recorded as inputs. Cross-study prediction should therefore be
  evaluated with splits grouped by `source_id`.
- `sources.csv` lists every source study. English-language references were checked against Crossref; Chinese-language
  references were checked against the first page of the original article. Source 9 could only be identified from the
  first page of a scanned copy.

## License

The compiled datasets are released under the Creative Commons Attribution 4.0 International license (CC BY 4.0).
The measured values remain the results of the cited source studies; please cite them together with this repository.
