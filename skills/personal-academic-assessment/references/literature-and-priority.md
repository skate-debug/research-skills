# Literature and priority

Read this for stage 2 (the first audit), stage 9 (the final audit of the central claim), stage 10 (grey literature and priority) and the venue screen in stage 12. Endpoint templates are in [Endpoints](endpoints.md).

## Engines and logging

Use several sources, because each misses records that the others find:

- **PubMed**, through E-utilities, with field tags.
- **Europe PMC**, which adds preprints and searchable full text.
- **A semantic search engine**, if one is available. Record its limits, since some return only a few results per query.
- **OpenAlex**, as a backup. It may refuse requests once its daily limit is reached.
- **Curated lists**, such as the author's own literature collections. Verify their labels against the papers themselves, because curated labels can be wrong.
- **The data-availability statements of the closest papers.** These are where related public deposits are usually found.

Log every query with its exact string, engine, date and hit count. Deduplicate the records by DOI and PMID, and report the number of unique records. Keep the queries in a project script or file, so that the audit can later be rerun as a search for new records only.

## Building queries

Break the claim or design into elements: the system or region, the habitats or sample types, the data types, the design features (gradients, references, controls, time) and the analyses. Write a block of synonyms for each element, then combine the blocks:

```
{system}  = ("term A"[tiab] OR "term B"[tiab] OR ...)
{sample}  = (...)
{data}    = (...)
{design}  = (transect[tiab] OR gradient[tiab] OR "distance from"[tiab] OR reference[tiab] OR ...)

E1  {system} AND {sample} AND {data}
E2  {system} AND {design} AND {data}
E3  {system} AND {sample} AND {design}
```

Run each combination three ways in Europe PMC: for all years, for the last five years (`FIRST_PDATE`), and for preprints only (`SRC:PPR`). Add title-only variants to reduce noise, and full-text variants to catch studies whose abstracts omit the design.

For each absence the paper will assert, write a query that describes exactly the study that would contradict it. For a semantic engine, phrase the query as the claim itself, in plain language.

Keep the literature's own vocabulary in queries, including older or broader terms that the project no longer uses in its text.

## First audit

1. Break the design into elements, and search for each element and for combinations of elements.
2. Sort the close papers into tiers:
   - **Tier A:** the same system and data type. These must be cited and differentiated.
   - **Tier B:** neighbours in habitat or method.
   - **Tier C:** precedents elsewhere, for methods or framing.
3. Profile each tier A and tier B paper. Record:
   - its habitat and data types;
   - its sites and design (references, gradients);
   - its analyses;
   - what it did not do;
   - whether the full text or only the abstract was read.

   Verify each DOI.
4. Give each element a verdict (see below).
5. Write down three things:
   - the risk that reviewers call the paper incremental;
   - the lead claims that avoid that risk;
   - the framings that are false or indefensible, such as a first-ever claim that a close paper contradicts.
6. Hand the result on as candidates for stage 3, not as a decision.

## Final audit of the central claim

1. Break the central claim into elements, and write the element and absence queries described above.
2. Screen titles and abstracts. For each relevant record, note what it did against each element.
3. Read the full text of the three to five closest studies. Copy the sentences on design verbatim into the working notes: reference sites, distances, sample types and data types. Statements about what a paper did or did not do should rest on its own words.
4. Check every preprint for a published version, and cite that version if it exists.
5. Give each element a verdict, and correct older records that the audit contradicts. Report the counts and the limits, and schedule a rerun before submission.

### Verdicts

- **Open:** no study was found that answers it, after searches designed to find one.
- **Partly filled:** close studies answer part of it.
- **Not new worldwide, but new for a region or system:** name the region or system.
- **New as a test, with a stated limit:** for example, it rests on one site or one unit.
- **Not new.**
- **Reported first by others:** cite them, including any grey literature.

Do not give numeric novelty scores.

## Grey literature and priority

Apply this check to every public deposit, preprint or competing team relevant to a claim, and to every result the paper will present as new.

1. **Deposit record.** Read the BioProject record, or its equivalent, in full: title, description and stated aims, organisation, release date, grant numbers and linked publications. A recent release whose stated aims resemble the paper's is a strong sign that its team is close to publishing.
2. **Funder records.** Look up each grant in the funder's public award database. For NSF awards, the award API returns the investigators, institution, abstract, project outcomes report and listed publications. Search the awards by title words to find collaborative partner awards. For other funders, use the equivalent public search where one exists.
3. **Meeting abstracts.** Search the web for the title words of the deposit or award, together with the team's names and the relevant meetings. Some abstract pages render only with JavaScript; fetch their JSON instead (the AGU template is in [Endpoints](endpoints.md)).
4. **The team's outputs.** Search for the team's recent work:
   - author searches in PubMed and Europe PMC for each team member over the last three years;
   - their author records in OpenAlex;
   - preprint servers and theses.
5. **Record and rescope.** Record what was found, with its date and a full citation; conference abstracts and outcomes reports count. Rescope the claim honestly as an independent observation, a reanalysis or an extension, and cite the earlier report. Never claim priority.
6. **Follow up.** Put a recheck of every deposit on the submission checklist. If the author wants to contact the team, draft the message for the author to send.

## Venue screen

1. **Screen the leading journals.** Search PubMed for the system's terms, restricted to the field's leading journals (`"Journal Abbreviation"[Journal]` terms joined by OR) over the last three years. Count the records, and read the abstracts of the 15–20 most recent for the kinds of data they rely on.
2. **Compare the closest studies.** List the venues of the closest studies with similar data, and of any that added stronger data. Stronger data does not guarantee a higher tier; the closest similar studies show what is realistic.
3. **Give a verdict for each journal group, with its basis.** Say whether the limit lies in the design or in the writing; rewriting cannot lift a limit set by the design.
4. **List the likely reviewer objections,** with the paper's position on each, and what could still strengthen the paper within the project's constraints.
5. **Present the verdict as a judgement,** because the outcome depends on editors and reviewers.
