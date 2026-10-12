---
name: personal-research-visualization
description: "Design, revise or audit publication-quality scientific figures with compact interconnected panels, minimal text, diverse justified encodings and complete source data. Use for manuscript figures, sampling maps, analytical workflows, networks and trees, including semantic duplication reviews. Not for business dashboards or decorative illustrations."
---

# Personal research visualization

## Core preferences

1. Reserve Figures for complex, information-rich visualizations. A panel must reveal a relationship, distribution, hierarchy, spatial pattern, multivariate structure, or analytical dependency that would be cumbersome to communicate in one sentence. Move isolated counts, simple totals, redundant summaries, and one-sentence findings to the manuscript or caption. Do not fill a figure with low-information panels merely to reach a panel count.
2. Use minimal text inside Figures and emphasize graphical elements. Prefer concise labels, restrained legends, purposeful symbols, and clear visual connections. Put prose, procedural detail, software versions, runtimes, and interpretation in the caption, Methods, or supplement unless explicitly requested inside the figure. Preserve essential units, scales, denominators, uncertainty, and evidence distinctions.
3. Use diverse, complementary plotting styles suited to the research question. Do not default to a sequence of line and bar charts. Consider Sankey/alluvial plots, circular dendrograms, clustered heatmaps, ordinations, bipartite networks, chord diagrams, distribution plots, and spatial maps when justified by the data. Complexity means information content, not ornamentation. Never invent data or impose an unsupported hierarchy to obtain a sophisticated-looking plot.
4. Consolidate related findings into compact multipanel figures with interconnected panels and a clear scientific argument. Prefer numerous well-sized small panels when the evidence warrants them. Information density comes from complementary evidence, not a panel-count target or tiny labels.

A requested study map plus workflow is an appropriate contextual Figure: it communicates geographic design and branching analytical dependencies. It should not become a page of count cards or a methods table in boxes.

## Before drawing

- Read the project handoff, current figure plan, relevant source data, and the user's reference images. Distinguish a style reference from a scientific data source.
- For each proposed panel, identify its scientific question, source, analytical unit, visual encoding, and unique contribution. Reject panels that repeat another panel or only restate one number.
- Identify actual sample sizes, missingness, repeated measures, transformations, and inference limits. Use stable identifiers for joins. Preserve original data and previous figure versions.
- Revisions authorize the requested figure work, not new statistical analyses, rerunning pipelines, or changing the study's conclusions. Ask only when an unresolved choice materially changes scientific meaning.
- For multipanel planning, substantial revisions, source-data releases or duplication audits, read [Multipanel revisions and source data](references/multipanel-and-source-data.md).

## Choose encodings honestly

| Research structure | Candidate visualization | Required checks |
| --- | --- | --- |
| Flows or membership transitions | Sankey or alluvial | Define what ribbon width counts; reconcile totals; handle duplicated entities and nonexclusive membership explicitly. Do not imply conserved quantities where none exist. |
| Computed hierarchy | Circular dendrogram or annotated tree | Use a real clustering/taxonomic/phylogenetic hierarchy; state distance and linkage or tree method; distinguish clustering from phylogeny. Use a rectangular layout if circular labels become unreadable. |
| Many-to-many associations | Bipartite network, chord diagram, adjacency heatmap | Define edges, weights, evidence, filters, and layout; distinguish association from causation; manage density instead of hiding inconvenient edges. |
| Multivariate community structure | Ordination, clustered heatmap, linked annotation tracks | State transformation, distance, explained variation, ordering, and color scale; distinguish observations from model output. |
| Distributions and uncertainty | Raincloud, violin with observations, ridgeline, ECDF, interval plot | Show the observational unit and adequate sample size; do not replace missing values with zero or imply density with too few observations. |
| Space and study context | Sampling map with useful locator insets | Use real coordinates and sourced geography; preserve projection, scale, attribution, and location uncertainty. Never invent coastlines or move sampling sites for aesthetics. |
| Analytical dependencies | Concise workflow with purposeful biological/data glyphs | Arrows must represent real inputs or dependencies, not merely the order tasks happened. Keep legacy, exploratory, and primary branches distinguishable. Icons and arrow widths are schematic unless quantitatively encoded. |

Line charts and bars remain appropriate when they best answer a nontrivial question; do not replace a clear encoding with a misleading complex one just for variety. Across a figure set, vary encodings because questions differ, not to satisfy a chart-type quota.

## Composition and typography

- Give each Figure one coherent scientific message and each panel one distinct role. Use a clear reading order, lowercase panel letters and aligned plotting areas. Omit panel titles by default when axis labels, concise keys and the caption establish the question.
- Use direct labels when they reduce lookup effort. Keep explanatory sentences outside the plotting area. Avoid large headings that repeat the caption and decorative boxes around every item.
- Use a restrained, accessible palette with stable category meanings. Add shape, position, or line-style redundancy when colors carry essential distinctions. Follow the user's reference style without copying unrelated data or claims.
- Set palette from the current project and latest author preference. This skill's UI brand colour does not prescribe plot colours. There is no single mandatory Nature palette. Use a Nature-inspired categorical palette when requested, then preserve an approved palette across related figures. A colour-only revision must not change the approved layout or analysis.
- Allocate space by information content. Resolve crowded text by simplifying or enlarging the panel, not by making labels microscopic.
- Use compact horizontal, vertical or mixed arrangements according to the data and reference figure. Reduce unused margins, align axes and matrix tracks, bring trees close to their associated heatmaps, and keep arrows, legends and labels inside the intended frame. Landscape orientation is a preference when it improves the composition, not a requirement to compress every figure.
- Inspect at intended publication size, not only enlarged on screen. Treat small map credits and compact legends as real typography that must remain readable.

## Reproducibility and export

- Build data plots, maps, and workflows with deterministic scientific plotting or editable vector tools. Do not use generative imagery to fabricate measurements, geographic features, trees, or analytical relationships.
- Keep source data, transformations, scripts, coordinate systems, and third-party credits traceable. Freeze downloaded geographic inputs used for a submitted version.
- Unless the journal or user specifies otherwise, deliver true 600-DPI PNG and lossless TIFF at a stated physical size, plus an editable SVG or vector PDF. Setting a DPI tag alone does not increase resolution; calculate pixel dimensions from physical size and resolution.
- Retain text and linework as vectors where possible. Embed raster assets at adequate native resolution and disclose mixed raster/vector outputs.
- Place detailed scientific explanations, abbreviations, methods, and limitations in an accompanying caption, not as dense text on the figure.
- Put figures in a clearly versioned folder under the project's figure directory, using `09_figures` when that is the established convention. Include concise captions and panel-level source mappings. Preserve the current release unless the user specifically requests an in-place amendment.

## Final review

Check source-to-mark accuracy, sample and edge counts, grouping/order, units, missingness, scale bars, dependency arrows, and absence of fabricated significance. Render the actual deliverable; inspect all panels for overlap, clipping, legibility, color ambiguity, and unnecessary text. Verify physical dimensions, pixel dimensions, DPI metadata, and successful opening of exports. Report unresolved limitations without claiming journal acceptance or universal publication readiness.

Review duplication across the whole main and supplementary set using scientific questions, source records, transformations and encodings. Pixel similarity alone cannot identify semantic duplication. Record intentional shared information and each panel's distinct role; remove or consolidate repeated displays that make the same point. Check that main findings, sensitivity analyses and detailed source tables form a coherent, qualified narrative.

Keep this skill concise and extend it with the user's later feedback. Project-specific counts, filenames, colors, and layouts belong in the relevant project, not as universal rules here.
