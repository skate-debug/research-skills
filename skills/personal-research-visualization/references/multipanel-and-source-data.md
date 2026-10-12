# Multipanel revisions and source data

Read when planning a figure set, revising compact layouts, auditing duplicate panels or preparing a figure/source-data release. Retain the author's current project choices rather than imposing a fixed figure count, palette or panel template.

## Scientific narrative and panel roles

Plan main and supplementary figures together. Define the study's central contribution, the strongest completed comparisons, the biological context and the material sensitivities. An ML-led study can still require genome catalogues, phylogenetic trees, diversity, community structure and association networks. Include each when it explains a substantive part of the argument.

Assign each proposed panel a question, data source, analytical unit, transformation, encoding and unique role. Consolidate related questions into one main figure when the composition remains readable. Use supporting figures for necessary detail or sensitivity, rather than weaker repeats of main panels. Keep one-sentence counts and low-information summaries in prose or captions.

A sampling map or workflow can be a main contextual figure or a graphical abstract. Choose according to the author's intended narrative and target journal; do not automatically classify every overview as a main result. If a graphical abstract is deferred, continue the other authorized revisions without redesigning it.

## Compact composition

Follow a reference image's compositional principles, not its unrelated measurements or claims. Use lowercase letters, minimal titles, restrained legends, small inter-panel gaps and aligned plotting regions. Allocate size by information content. Many small panels are useful only when each is readable and contributes distinct evidence.

Crop excess whitespace and check both inner axes and outer panel bounds. Align side-by-side panels at their actual plotting areas, accounting for unequal tick labels, legends and colour bars. Keep trees, annotation tracks and heatmaps close with a common tip/order mapping. Equal geometric scale matters for ordinations; equal panel width alone does not establish it.

Workflows should be detailed enough to show real dependencies and compact enough to read at publication size. Use purposeful biological or data glyphs, short labels and clear connectors. Put lengthy software, runtime and implementation explanations in the caption or Methods unless explicitly requested in the artwork. Check north arrows, map scales and workflow connectors against the frame.

Ordination improvements may use clear marker fills/outlines, shape redundancy, zero reference lines, direct labels or linked diversity encodings. Preserve the underlying coordinates, correction convention and explained variation. Co-encoding multiple attributes can replace repeated coordinate views when both remain legible. Do not add unsupported ecological cluster names or explanatory arrows to imitate a reference.

Palette changes and layout changes are separate edits. Preserve an approved composition during a palette-only revision, and preserve an approved palette during a layout-only revision. Use compatible categorical and continuous scales with explicit meanings. Avoid unnecessary brown or other dominant tones when the author prefers a restrained alternative; do not turn that project preference into a universal colour ban.

## Semantic duplication

Audit the entire main and supplementary set, including internal subplots within a lettered panel. Compare question, source records, model/procedure, aggregation, transformation and visual encoding.

- The same measurements recoloured or rearranged to make the same point are usually redundant.
- Observations and prediction residuals answer different questions, even when their rows and columns match.
- Aggregate performance and held-out-group heterogeneity can be complementary when the latter exposes an otherwise hidden result.
- Shared trees, sample ordering, baselines or observed distances are acceptable context for distinct measurements. Preserve their consistent identities.
- An ordination with chronological paths can add temporal structure to the same coordinates. A second colour treatment needs a comparably clear contribution.
- Two error metrics or positivity partitions are distinct only if their mathematical meaning adds information; changing labels is insufficient.

For genuine redundancy, remove a panel, combine encodings or replace it with a supported complementary analysis already available. Do not generate a new statistical experiment solely to fill the space. Map changed panel letters and caption references after every removal or consolidation.

Record decisions in a concise panel ledger for a substantial set-wide audit. Explain intentional shared data and distinguish semantic review from optional perceptual-image screening. Never claim panels are independent merely because their pixel hashes differ.

## Source data and captions

Map every panel to exact source records, stable identifiers, transformations and display order. Preserve full scientific precision, relevant missingness and all underlying records when the plot shows only a subset. Missing, ineligible and undefined values must remain distinguishable from zero.

Provide suitable machine-readable tables and, where needed, exact trees, alignments, clustering orders and geographic assets. A workbook per figure is useful when it improves navigation, but do not duplicate a table within that workbook for every panel that uses it. Include a panel index and useful field definitions, units, denominators and procedure keys.

Large matrices may use complete compressed TSV companions alongside Excel summaries. Document the companion files, counts and identifiers so they are integral, discoverable dataset components. Do not silently truncate rows, predictions, controls or tuning records to fit a workbook. Keep internal absolute paths and unrelated private project content out of reader-facing source files.

Captions must explain the final marks actually present: colours, shapes, outlines, scales, thresholds, transformations, denominators, averaging, uncertainty and omitted/missing values. Define biological annotations and computational procedures at the level needed to interpret them. Describe descriptive ranges as ranges, not confidence intervals, and conditional ranks as ranks unless an inferential test was performed.

Check confirmed chemistry units and nutrient mass bases across all figures and source dictionaries. Label pairwise quantities whose pairs share samples, evaluations of the same cohort under multiple schemes, candidate host evidence and study-wide references accurately. Preserve negative or inconvenient controls and qualified conclusions.

## Revision and delivery

Preserve earlier releases by default. Keep rendering reproducible from the recorded analysis and frozen assets. Version figures, captions and source data together. When the user explicitly requests an in-place correction, update the named current release and its affected source/legend files rather than creating an unsolicited new version.

Use the project's established figure directory and organize main figures, supporting figures, editable exports, captions, source data and review records for easy browsing. A local gallery or contact sheet can help review a large set; it does not replace the final figure files.

Inspect every final panel at the intended physical size. Check 600-DPI pixel dimensions as well as metadata, lossless raster integrity and editable vector content. Verify source joins and consequential numerical summaries in proportion to the revision, without refitting authorized finished analyses. Deliver a clear account of what changed and any concrete unresolved issue.
