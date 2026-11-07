# Public-data replication

Read this for stage 11. Use it only with the author's approval: reanalysing other teams' data changes the paper's scope, and it may overlap with other planned work.

When no new samples can be taken, public data are the only test of whether a result holds elsewhere.

1. **Get approval.** Ask the author first, and record the decision.
2. **Find data sets.** Look in three places:
   - the data-availability statements of the closest papers;
   - BioProject searches through E-utilities, using the system's terms;
   - the ENA study search.

   For each candidate, record its data type and its primers or protocol, the sample types and number of samples, the metadata available, the release date and whether a paper describes it. Keep this list as a table in the project.
3. **Fix the rules in advance.** Before examining any community or outcome data, write the following into the project's records, with dates:
   - the analysis criterion, unchanged from the manuscript;
   - the treatment and reference sides of each data set, taken from the published descriptions or from the metadata alone;
   - for each sample type, a positive control that uses no part of the criterion being tested. For example, require diagnostic features to be detectably elevated on the treatment side;
   - the statistics of every secondary claim, exactly as in the manuscript.

   Then label every later test pre-specified, added or exploratory. A control defined after looking at one data set counts as pre-specified only for the others.
4. **Download safely.** Put the reads in a new empty folder. Record any partial download, for example the first part of each run, and keep the run lists so that the reads can be fetched again.
5. **Process every data set the same way.** Use one pipeline for all of them.
   - If the usual denoiser or classifier is not installed, do not download and run binaries. Use or write an implementation in an installed language instead.
   - Validate it against a plain implementation on test sequences, and document how it differs from the standard tool.
6. **Validate on the project's own data first.** Before the analysis script is applied to anyone else's data, it must reproduce the published values exactly from the project's original tables.
7. **Run the controls and then the criterion.** A data set that fails the positive control is uninformative, not a failed replication, and is reported as uninformative.
8. **Calibrate and check.**
   - Small sample sizes may force a weakened rule. Calibrate it on all other splits of the same samples, and on the project's own data at the same sizes.
   - Run the criterion between sites that lack the effect, so that its behaviour without a contrast is known.
   - Look for contamination and implausible samples.
9. **Test alternative explanations of a positive result.** Rate each one as unlikely, not the cause, open, or plausible but untested:
   - contamination: check the blanks;
   - primers or pipeline: compare data sets that differ in both;
   - closure: use log-ratio statistics;
   - a shared environment: use partial correlations after removing the measured variables, with every comparable feature as a baseline;
   - transport or dilution from a single source;
   - a biological interaction, which is usually untestable with composition data;
   - dependence running in the reverse direction;
   - an unsampled reservoir.
10. **Report each claim** as replicated, not testable (the control failed), dependent on the scale of the comparison, or exploratory. Give totals by data set when one data set dominates. Remember that samples from one profile or site are not independent.
11. **Write the record and check priority.** Write the public-data record (structure in [Records and templates](records-and-templates.md)), with the recommended manuscript changes and the effect on novelty and competition. Then run the grey-literature check for every deposit used. If a deposit's own authors have already reported the result, a reanalysis of their data is not an independent replication.
