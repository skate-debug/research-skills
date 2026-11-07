# Records and templates

Read this for stage 13, and for a rerun before submission.

## Main record

Name the record after the paper, for example `docs/<PAPER>_QUESTION_SELECTION.md`, and date it. Give it these sections:

1. **Summary:**
   - the question;
   - the reasons it was chosen;
   - the central numbers;
   - how many questions were set aside, and why;
   - the two judgements, kept apart;
   - the effect of any public-data test.
2. **What the data can answer** (T1).
3. **How each candidate was judged** (T2), with the wording rule.
4. **How the question evolved** (T5), ending with whether the final question is exploratory.
5. **Questions set aside** (T13), grouped by the three reasons.
6. **Academic evaluations:**
   - literature audits (T3);
   - robustness tests (T4);
   - the stress test of the central claim (T7), with its weakest point and the share of any named group;
   - novelty after the final audit (T12), with corrections and limits;
   - the test on public data.
7. **Why this question was selected** (T6 and prose), including the title wording.
8. **Whether the narrative is strong enough:**
   - the limits that remain;
   - the venue verdict (T8);
   - the likely objections (T9);
   - what could still strengthen the paper.
9. **What the next version still needs:** numbered open items, each with an owner and a trigger.
10. **Records:** the scripts and output folders behind every number.

End with the references, in the project's citation style, each one verified.

## Public-data record

Start with the date, scope, corrections and purpose. Then give:

1. a summary;
2. the data used;
3. what was fixed in advance (T10);
4. the results, by claim;
5. what the results do and do not show (T11);
6. the recommended changes to the manuscript;
7. the effect on novelty and competition;
8. the limits;
9. the records;
10. the references.

## Propagation

- **Manuscript changes.** Put recommended changes into the record first, and into the manuscript only when the author asks. Afterwards, rebuild any generated manuscript package.
- **Reader-facing summary.** If the project keeps a summary of the assessment for readers, such as a web page built from lists in a script, update those lists and rebuild it whenever the record changes.
- **Project map.** Update the project's README, and keep the open items current.

## Table templates

| ID | Table | Columns |
| --- | --- | --- |
| T1 | Design | Design feature · What it allows · What it rules out |
| T2 | Criteria | Criterion · Question asked |
| T3 | Literature audits | Round · Date · Scope (engines, queries, records) · Result |
| T4 | Robustness tests | Test · Purpose · Result |
| T5 | Evolution | Date · Leading question · Outcome |
| T6 | Selection | Candidate · Answerable · Robust · Open · General · Distinctive |
| T7 | Central-claim stress test | Check · One column per group compared |
| T8 | Venue | Journal group · Assessment · Basis |
| T9 | Objections | Likely objection · Position |
| T10 | Pre-specification | Test · When defined · Standing (pre-specified, added or exploratory) |
| T11 | Alternative explanations | Explanation · Evidence · Standing |
| T12 | Novelty | Element · Closest work · Verdict |
| T13 | Set aside | Question · What the tests showed · Why set aside · Where it sits now |
| T14 | Wording | Wording · Assumption · Test · Result · Decision |
| T15 | Close-paper profile | Paper (DOI) · Habitat · Data types · Sites and design · Analyses · What it did not do · Read in full or abstract only |

## Rerun before submission

1. **Start from the records.** Read the main record, the public-data record and the open items. Check which open items the current manuscript has already resolved.
2. **Search for new records only.** Rerun the logged queries from the date of the last audit, compare the hit counts with the logged baseline, and screen every new record.
3. **Rerun the venue screen** from the date of the last screen.
4. **Recheck every deposit and competing team:** linked publications, funder records (outcomes reports and publication lists), meeting abstracts and author searches. If a competing paper has appeared:
   - replace any citation of its abstract or report with the paper;
   - revise the affected sections;
   - update any draft message to the team before the author sends it.
5. **Check every cited preprint** for a published version.
6. **Search the last authors of the closest studies,** combined with the system's terms, from the date of the last audit.
7. **Screen new entries** in any curated lists used before.
8. **Close the round.**
   - Add a dated row for this round to the audit table, and correct any statement it overturns.
   - Apply the approved changes.
   - Rebuild the generated outputs.

## Failure modes this workflow guards against

| Failure | Guard |
| --- | --- |
| A lead recommended from the literature before any test, then undermined by the first analyses | Test before recommending |
| Agreement between two data sets that mostly reflects a shared gradient | Shared-gradient control |
| An over-broad statement that no study had done something | Search for the absence you will assert |
| A hoped-for Highlight that fails multiple-test correction | Correction with confounders removed |
| A pattern that rests on one unit | Leave one unit out |
| Wording that carries untested assumptions | Wording audit |
| A central claim tested less than the claims around it, or an n-fold size that depends on the method | Stress test of the central claim |
| A competing team's meeting abstract or grant report missed by peer-reviewed searches | Grey-literature check |
| A mislabelled entry in a curated literature list | Verify curated labels against the papers |
| A search engine that returns only a handful of results per query | Several engines |
| Analysis or search scripts lost with temporary files | Keep every script in the project |
