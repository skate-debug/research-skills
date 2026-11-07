# Robustness tests

Read this for stage 4, the preliminary tests of each candidate, and for stage 8, the stress test of the central claim.

Run each test as a project script with a fixed random seed. Write its outputs as tables in the project's results folder, with a short README entry, so that a later rerun gives the same numbers.

## Battery for candidate claims

Choose the tests that a candidate's claim needs.

| Test | Use when | How | The claim fails when |
| --- | --- | --- | --- |
| Restricted permutations | Samples are nested in blocks such as sites, plots, profiles, cores or subjects | Permute only within blocks, or use the blocks as strata | The effect disappears under the restriction |
| Shared-gradient control | Two matrices or variables both follow a gradient such as depth, distance or time | Partial Mantel test or partial correlation with the gradient removed; repeat inside blocks | The association largely disappears |
| Independent selection | A signature is defined from the same samples it is tested on | Define it from the end members or a training subset, then test it on the other samples | The signal appears only in the samples used to define it |
| Circularity removal | A response axis is built from the same features that are classified along it | Classify on an axis built from independent data, and among features not used to build the axis | The response disappears |
| Closure | Compositional data contain a dominant group | Remove the dominant group from the denominator; use log-ratio statistics | The peak or trend vanishes |
| Leave one unit out; unit fixed effects | A result could rest on one site, unit or subject | Drop each unit in turn. Fit unit fixed effects, rotating the axis within units by cyclic shifts so that autocorrelation is kept | The result disappears without one unit |
| Correction with confounders removed | Many associations are tested, and obvious confounders exist | Partial correlations within strata, then Holm or Benjamini–Hochberg adjustment | Adjusted significance is lost |
| Sensitivity without a dominant non-target group | A group outside the claim, such as host, plant or animal reads, dominates the data | Rerun without that group, re-rarefied to equal depth | The claim depends on that group |
| Matched random null | A reduction or overlap might occur for any set of features | Random feature sets matched in number and abundance | The observed value lies inside the null range |
| Dilution and mixture | Intermediate samples lie on a gradient between end members | Expected shares if an end member were diluted. Mixture models fitted by expectation–maximisation, benchmarked against mixtures from within the same unit | The observation matches dilution |
| Baseline | A pattern is described as special | How often comparable features show the pattern without the proposed cause | The pattern turns out to be common |
| Competing geometry | A pattern could follow an absolute coordinate or one relative to a putative source | Compare the fit of both coordinates | Neither can be preferred, so say so |
| Proxy check | A condition is inferred from a proxy | Look where the proxy and the inference disagree | The inference is contradicted, so drop it |

A failed test does not erase a result. It sets the result's standing:

- kept as a supporting result;
- reduced to a description of one unit;
- stated as a hypothesis;
- or set aside, following the set-aside log in [Question selection](question-selection.md).

## Stress test of the central claim

Vary every setting of the analysis behind the central claim:

1. **Base.** Run the analysis exactly as in the manuscript, including every selection criterion and its thresholds.
2. **Thresholds.** Vary each threshold over a wide range, for example from half to four times its value.
3. **Sides.** Vary which samples form each side of the comparison:
   - each unit alone;
   - meaningful subsets;
   - the reference widened;
   - each station or site left out in turn;
   - the doubtful samples alone, and added to the base.
4. **Power.** Redraw the better-sampled group many times (for example 999) at the sample sizes of the other group, so that a contrast cannot reflect unequal sampling.
5. **Rank.** Repeat the analysis at a coarser taxonomic or categorical rank.
6. **Symmetry.** Apply the mirror criterion, to features that fall rather than rise.
7. **Selection-free measures.** Compute a whole-community effect size, such as PERMANOVA R², and compare the dissimilarities between groups with those within groups.
8. **Sensitivity.** Rerun without any dominant non-target group.
9. **Composition.** Record the share of any named group in the response under every setting, and the sample or feature behind each low value.

Report the direction and the size separately. The direction is secure only if it holds under every setting; the size depends on the measure.

Justify in the manuscript any sample set left out of the base. Name the weakest point explicitly.

Check odd values for artefacts before interpreting them, such as a dominant feature that drops out because it has no name at the chosen rank.
