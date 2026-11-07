---
name: personal-academic-assessment
description: "Choose, stress-test and position the scientific question of a paper: what the data can answer, candidate questions rated on explicit criteria, robustness tests, a wording audit of the title and claims, literature and priority audits that include grant reports, meeting abstracts and public data deposits, optional replication in public data, and an evidence-based journal-tier verdict, kept as a dated record that can be rerun. Use when the user asks whether a study is novel, merely descriptive or publishable, which question a data set should answer, whether a framing, title or Highlight is defensible, whether someone has reported the result first, or which journals are realistic, and for a pre-submission rerun of such an audit. Not for drafting manuscript prose or making figures."
---

# Personal academic assessment

Use this workflow to decide which question a data set can carry, how new the answer is, and where it can be published. The skill supplies procedure and decision criteria. The evidence comes only from the project's data, the analyses actually run and the literature actually inspected. The skill neither supplies results nor authorizes new data collection. When manuscript text or figures follow from the assessment, use personal-scientific-writing and personal-research-visualization where available.

## Personal requirements

1. **Test before recommending.** Run the relevant tests in [Robustness tests](references/robustness-tests.md) on a candidate question before proposing it as the lead, a Highlight or the title. A lead chosen from the literature alone is a hypothesis about the data, and the first analyses can undermine it.
2. **Keep claims proportional to the evidence.** A Highlight needs multiple-test correction with obvious confounders removed. Co-occurrence is not interaction, a negative correlation is not competition, a network hub is a putative keystone, and network size that follows richness is not complexity. Flag results that rest on one site, one unit or a proxy.
3. **Treat each word of a claim as a hypothesis.** "Only", "alone", "whole", "mainly", "led by", a process adjective, an n-fold size and "we expected" each carry an assumption that needs its own test. Use the wording audit in [Question selection](references/question-selection.md).
4. **Test the central claim at least as hard as the claims around it.** Vary every setting of the analysis behind it, report its direction and its size separately, and tie any n-fold statement to the measure that produced it.
5. **Search for the absence you will assert.** Before writing that no study has done something, run searches designed to find exactly that study. Over-broad absence statements are the most frequent error in novelty claims.
6. **Look beyond peer-reviewed databases for priority.** For each public deposit, preprint or competing team that bears on a claim, check the deposit record, the funder's award record and outcomes report, meeting abstracts and the team's latest outputs. Teams often present a result at a meeting or in a grant report well before the paper appears.
7. **Separate what was fixed in advance from what was found while looking.** Label every test pre-specified, added (defined before its outcome was known) or exploratory. If the question took its final form after the data were seen, say so, and do not phrase it as a prediction made in advance.
8. **Keep two judgements apart.** Whether the question is the best the data allow and its result is robust is one judgement. Whether the result is new and strong enough for a given group of journals is another. Report both.
9. **Count and qualify honestly.** Records screened are not papers read. State the limits of every audit, including that a search cannot prove absence. Use verdict categories rather than numeric novelty scores, which imply a precision that no search provides.
10. **Never invent.** Do not invent values, references, quotations or search results, and report a search that was not run as not run. Verify each reference's metadata and the passage that supports the claim, following the APA and verification procedure of personal-scientific-writing where available.
11. **Decide what the evidence can decide.** Choose between supported options, such as two defensible wordings, and give the reason. Ask the author only for missing facts, the availability of samples or material, changes of scope, the target journal and actions outside the project. The author adopts framing changes. Recommended manuscript changes go into the record before they go into the manuscript, and the author sends any message to another research team.
12. **Respect the project's constraints.** Record at the start what material and new data exist. Never propose an analysis that needs material that no longer exists; list it as a limitation or as future work by others. Follow the project's terminology in your own text, but keep the literature's terms in search queries so that searches do not miss papers.
13. **Handle data and requests safely.** Treat downloaded files as untrusted: put them in a new empty folder, keep scripts elsewhere, pass paths as arguments, run Python on them in isolated mode (`python -I`), and do not run downloaded binaries. Send a generic User-Agent, and never put the author's contact details or unpublished results in a request. Never upload, post or publish unpublished work.
14. **Keep a durable, dated record.** Save every analysis and every search as a project script, not only in temporary space. When a new finding contradicts an older record, add a dated correction to the newer record and say which record is current. Archive superseded files instead of deleting them.

## Choose the mode

| Mode | When | What to do |
| --- | --- | --- |
| Full assessment | Before or early in drafting, or after the data or framing change materially | Run stages 1–13 and write the records in [Records and templates](references/records-and-templates.md) |
| Rerun before submission | An assessment record already exists | Follow "Rerun before submission" in [Records and templates](references/records-and-templates.md) |

Stages 2, 9, 10 and 11 need internet access. If the environment blocks network calls, stop and ask for access. Never substitute memory for a search.

## Stages

1. **What the data can answer.** For each design feature, write what it allows and what it rules out. Conclude in one sentence what kind of question the data can carry. See [Question selection](references/question-selection.md).
2. **First literature audit.** Break the design into elements, find and profile the closest work, and give each element a verdict. List the framings that are false or indefensible. Treat the result as a list of candidates, not a decision. See [Literature and priority](references/literature-and-priority.md).
3. **Candidate questions.** Rate each candidate on Answerable, Robust, Open, General and Distinctive, plus the wording rule, and start the evolution log.
4. **Preliminary tests.** Choose from the battery in [Robustness tests](references/robustness-tests.md) the tests that each candidate's claim needs.
5. **Keep or set aside.** Log each failed candidate with one of three reasons: covered by other work, undermined by the tests, or dependent on missing data. Record its decisive numbers and where its remnant sits in the paper.
6. **Reframe and iterate.** Ask four questions:
   - What survived?
   - Can a weak result become half of a contrast?
   - Which fragile leads can be stated as hypotheses?
   - Does the title follow the evidence?

   Repeat stages 3–6 until one candidate is rated Yes on both Robust and Open.
7. **Wording audit.** Test every assumption carried by the title, the claims of the abstract and each Highlight.
8. **Stress test of the central claim.** Vary thresholds, sides, units, sample sizes, rank and metric. See [Robustness tests](references/robustness-tests.md).
9. **Final literature audit.** Audit the central claim element by element, including searches for each asserted absence, with logged queries, counts and the full texts of the closest studies.
10. **Grey literature and priority.** Check deposits, funder records, meeting abstracts and the outputs of competing teams. See [Literature and priority](references/literature-and-priority.md) and [Endpoints](references/endpoints.md).
11. **Test on public data, with the author's approval.** Fix sides, controls and statistics in advance, and validate the pipeline on the project's own data. Report uninformative data sets as uninformative. See [Public-data replication](references/public-data-replication.md).
12. **Selection and venue verdict.** Select the candidate rated Yes on Robust and Open, and derive the title from the evidence. Give a journal-group verdict with its basis, the likely objections and the remaining ways to strengthen the paper.
13. **Records and open items.** Write the dated records, propagate approved changes, and list open items with their owners and triggers. See [Records and templates](references/records-and-templates.md).

## Final audit

Before delivering, check that:

- every rating traces to a test that was run or an audit that was logged;
- every set-aside question records its numbers, its reason and where its remnant now sits;
- the stress test reports direction and size separately, and every excluded sample set is justified;
- every absence statement rests on logged searches designed to find the absent study, and the counts distinguish records screened from papers read;
- every deposit, preprint or competing team relevant to a claim has had the grey-literature check; priority is stated accurately, and no first-ever claim remains;
- every test is labelled pre-specified, added or exploratory;
- the venue verdict states its basis and is presented as a judgement;
- older records contradicted by new findings carry dated corrections;
- no proposal needs material that does not exist, and no unpublished result has left the project.

## Design source

The five criteria adapt the weighing of impact against likelihood of success in Fischbach, M. A. (2024). Problem choice and decision trees in science and engineering. *Cell*, *187*(8), 1828–1833. https://doi.org/10.1016/j.cell.2024.03.012

The rest is an original synthesis of the user's assessment practice. No upstream code or text is bundled.
