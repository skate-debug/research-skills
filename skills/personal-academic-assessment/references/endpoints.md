# Endpoints

Templates for literature, deposit, funder and meeting-abstract lookups. All were tested on 6 November 2026. Services change, so when a template fails, check the service's current documentation before improvising.

Etiquette:

- Send a generic User-Agent and no personal contact details.
- Pause about half a second between E-utilities calls; NCBI allows three requests per second without an API key.
- Retry failed calls with increasing waits.
- Save raw responses before parsing them.

| Service | Use | Template |
| --- | --- | --- |
| PubMed search | Records for a query | `https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?db=pubmed&term=<query>&retmode=json&retmax=400&sort=pub_date`. For a date limit, add `&datetype=pdat&mindate=YYYY/MM/DD&maxdate=3000` |
| PubMed summaries | Title, journal, date and DOI | `…/esummary.fcgi?db=pubmed&id=<pmid,pmid,…>&retmode=json` |
| PubMed abstracts | Abstract text | `…/efetch.fcgi?db=pubmed&id=<pmids>&rettype=abstract&retmode=text` |
| Europe PMC search | Records, preprints and abstracts | `https://www.ebi.ac.uk/europepmc/webservices/rest/search?query=<query>&format=json&pageSize=300&resultType=lite`. Use `resultType=core` for abstracts. Fields: `TITLE_ABS:`, `TITLE:`, `AUTH:"Surname AB"`, `DOI:"<doi>"`, `FIRST_PDATE:[YYYY-MM-DD TO YYYY-MM-DD]`, `SRC:PPR` |
| Europe PMC full text | Full text of open-access PMC articles | `https://www.ebi.ac.uk/europepmc/webservices/rest/<PMCID>/fullTextXML` |
| Crossref | Reference metadata | `https://api.crossref.org/works/<doi>`, or `https://api.crossref.org/works?query.bibliographic=<title words>&rows=3` |
| OpenAlex | Keyword search and author works | `https://api.openalex.org/works?search=<words>&per-page=12&sort=publication_date:desc`. Returns HTTP 429 once its daily limit is reached; fall back on Europe PMC |
| bioRxiv | Whether a preprint has been published | `https://api.biorxiv.org/details/biorxiv/<doi>`. The field `published` holds the journal DOI, or `NA` |
| NCBI BioProject | Deposit description, grants and organisation | esearch `db=bioproject&term=<accession>[Project Accession]`, then esummary `db=bioproject&id=<uid>&retmode=json`, then efetch `db=bioproject&id=<uid>&retmode=xml` |
| NCBI BioSample | Per-sample attributes | `…/efetch.fcgi?db=biosample&id=<biosample accession>&retmode=xml` |
| SRA run table | Runs of a project | `https://trace.ncbi.nlm.nih.gov/Traces/sra-db-be/runinfo?acc=<project accession>` (CSV) |
| SRA reads | FASTQ of one run | `https://trace.ncbi.nlm.nih.gov/Traces/sra-reads-be/fastq?acc=<run accession>` (with simplified quality values) |
| ENA run table | Runs, file sizes and sample titles | `https://www.ebi.ac.uk/ena/portal/api/filereport?accession=<project accession>&result=read_run&fields=run_accession,sample_accession,sample_alias,sample_title,experiment_title,library_strategy,library_layout,instrument_model,read_count,fastq_bytes,fastq_ftp&format=tsv&limit=0` |
| ENA study search | Finding deposits | `https://www.ebi.ac.uk/ena/portal/api/search?result=study&query=<query>&fields=study_accession,secondary_study_accession,study_title&format=tsv&limit=60`. Example query: `study_title="*term*" AND description="*term*"` |
| NSF award | Investigators, institution, outcomes report and publications | `https://api.nsf.gov/services/v1/awards/<award id>.json?printFields=id,title,pdPIName,coPDPI,awardeeName,startDate,expDate,abstractText,projectOutComesReport,publicationResearch` |
| NSF award search | Collaborative partner awards | `https://api.nsf.gov/services/v1/awards.json?keyword="<award title>"&printFields=id,title,pdPIName,awardeeName` |
| AGU abstracts | Abstract text and authors as JSON | `https://studio.m-anage.com/agu/<meeting>/meetingapi.cgi/Paper/<paper id>` (key `Abstract`). The reading page `…/meetingapp.cgi/Paper/<paper id>` needs JavaScript |
