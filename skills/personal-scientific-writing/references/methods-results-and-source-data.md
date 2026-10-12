# Methods, results and source data

Read for substantial Materials and Methods or Results drafting, mathematical exposition, or manuscript integration after figures and supplementary data are finalized. Project-specific numbers, units, procedures and exceptions come from the current project record.

## Publication prose and working records

Describe the research as the study actually conducted. Shared samples or methodological precedents do not require introductory sentences positioning every analysis relative to a companion paper. Use the author's confirmed sampling and laboratory record to write a self-contained account, with appropriate citations for adopted methods, software and borrowed concepts.

A published companion paper and an unpublished draft may help recover shared field or laboratory details when the author confirms their applicability. Distinguish this documentary use from bibliographic evidence. Do not automatically cite an unpublished working draft as a publication. Disclose related manuscripts under consideration or in press when the journal requires it, including sample or analytical overlap, through the appropriate submission materials. Avoid concealing overlap or implying that reused samples are newly collected.

Resolve conflicting methods using the author's corrections and confirmed source priority. Do not invent equipment, transport conditions, subsampling, extraction, assay or sequencing details. When a parameter remains untraceable, omit unnecessary precision and retain the uncertainty in the author-query record; do not substitute an unsupported instrument or coordinate datum.

Keep internal folder names, handoff references, transcription-correction histories, recovery steps, failed preliminary runs and editorial rationales outside manuscript prose. Report an exclusion, failed validation or other negative finding when it affects scientific interpretation, the reported analytical design or reproducibility. A supplementary section is not a destination for every pipeline log.

Use Supplementary Methods when detailed procedures genuinely need a separate home under the intended journal's current requirements or the user's chosen structure. Keep the main Methods sufficient to understand the study. Do not create a separate Supplementary Methods document merely because a prior draft became long. Verify current journal instructions when submission formatting becomes part of the task.

## Mathematical explanation

Add an equation when readers need its definition to reproduce or interpret the analysis. Typical useful components are:

- Closure, zero handling and square-root or centred-log-ratio transformations.
- Environmental, contextual, viral and host-aggregated predictor definitions.
- A fitting objective with its penalty, kernel or latent-component specification.
- Grouped outer validation, nested training selection and decoding rules.
- Primary and complementary errors, paired improvements and conditional-control ranks.
- Support, richness or diversity diagnostics when their definitions affect conclusions.

Choose only the components used by the study. Do not add a generic catalogue of formulas or introduce a different model while rewriting its Methods.

Introduce what an equation does, show it near the relevant procedure, define every symbol and index, and explain the practical consequence. Identify input dimensions, units, denominators, averaging order, zero replacement, thresholds, tie handling and fallback rules where applicable. Use consistent notation throughout Methods, captions and source-data dictionaries.

Preserve mathematically different quantities: the mean of squared distances is not the square of their mean; a per-coordinate error contribution needs the correct aggregation; unsquared and squared objectives can have different optima. State whether a tuning objective differs from the reported evaluation metric. Check equations against the implemented procedure and saved numerical outputs. Equations explain reproducibility; their number is not a measure of rigor.

## Predictive and ecological evidence

Keep software names, versions, key settings, reference-database versions and reproducible selection rules where they support the performed analysis. Separate catalogue construction from fold-local processing. Identify which transformations, eligibility filters, imputations and hyperparameters are learned from training data, and which references were assembled study-wide.

Define the observational unit, repeated measurements, held-out groups and evaluation target. Two validation schemes applied to the same samples do not create two independent sample cohorts. Within-year interpolation and site holdout do not establish future forecasting or external-population validation.

Compare against the strongest available environmental and contextual baselines. Match predictor access when assessing host encodings; explain how links, unlinked abundance and excluded features enter the model. Distinguish annotated candidate hosts from validated infections and conditional-control ranks from inferential P values. Do not frame separate follow-up experiments as a fully crossed design.

Retain genomic catalogues, phylogenetic context, diversity, community geometry and association networks when they establish the biological question or explain prediction behavior. Interpret improvements together with biological fidelity, support/zero behavior and sensitivity results. A machine-learning emphasis does not remove the need for the underlying bioinformatics evidence.

## Units, accessions and supplementary materials

Use author-confirmed units and mass bases. Distinguish salinity scale, nutrient ion or molecule mass, and concentrations expressed as an element. A combined channel needs its own confirmed definition; do not infer a conversion or difference from its label alone. Apply these definitions consistently in prose, figures, tables and dictionaries. Do not transfer one project's reporting units to another.

Associate each sequence accession with the correct assay and dataset. Metagenomic and marker-gene accessions are not interchangeable. Keep unresolved repository or code-release details in the submission checklist until confirmed; do not present them as already deposited.

Give supplementary tables, datasets and figure source data distinct functions:

- A supplementary table communicates a concise scientific comparison or complete statistical summary.
- A supplementary dataset retains the full catalogue, observations, predictions, settings or diagnostics needed for reuse.
- Figure source data identify the precise records, transformations and display order underlying every panel.

Choose Excel, TSV/CSV and document formats according to current journal requirements and the reader's task. Keep long matrices machine-readable rather than forcing them into Word tables. Complete compressed TSV companions are appropriate when they make workbooks manageable, with explicit file and field dictionaries and no silent record loss. Preserve identifiers and seeds exactly, full numerical precision, and the distinction between zero and unavailable values.

Verify stable joins, row counts, fold membership, units, key numerical summaries and source-to-panel mappings before changing manuscript references. Store a repeated table once when practical and map all relevant panels to it. After confirmation, revise the relevant Methods and Results passages and cross-references proportionately; retain correct existing prose.
