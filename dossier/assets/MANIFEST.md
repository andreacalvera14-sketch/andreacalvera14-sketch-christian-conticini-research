# Assets Manifest

## Status: EMPTY — zero files retrieved

**This directory contains no downloaded PDFs, images, OCR text or scans.**

The brief asked for downloaded primary material to be saved here with a manifest. The manifest exists. The material does not, and this file exists to say so rather than to disguise it.

## Why

Direct network access to every source host was blocked at DNS level in the execution environment. Both available retrieval mechanisms failed:

```
$ curl -sSL https://gallica.bnf.fr/ark:/12148/bd6t5344993p/f16.item...
curl: (6) Could not resolve host: gallica.bnf.fr

$ curl -sSL https://www.berthomeau.com/search/christian%20conticini/
curl: (6) Could not resolve host: www.berthomeau.com

$ curl -sSL https://catalogue.bnf.fr/ark:/12148/cb444579018
curl: (6) Could not resolve host: catalogue.bnf.fr

$ curl -sSL https://data.bnf.fr/fr/ark:/12148/cb121149081
curl: (6) Could not resolve host: data.bnf.fr

$ curl -sSL https://www.liberation.fr/futurs/1998/04/18/...
curl: (6) Could not resolve host: www.liberation.fr

$ curl -sSL https://www.lexpress.fr/informations/la-maison-conticini-...
curl: (6) Could not resolve host: www.lexpress.fr

$ curl -sSL https://www.agatfilms-exnihilo.com/catalogue/films/toques-a-la-loupe/
curl: (6) Could not resolve host: www.agatfilms-exnihilo.com
```

The agent's dedicated page-fetch tool returned `WebFetchBlockedUrlError: failed to lookup address information: No address associated with hostname` for the same hosts.

**No placeholder, reconstructed or synthesised file has been placed here.** An empty assets directory is an honest record of a failed retrieval. A directory of plausible-looking fabricated documents would not be.

## Manifest table

| File | Source URL | Format | Retrieved | SHA-256 |
|---|---|---|---|---|
| *(none)* | — | — | — | — |

---

## Intended structure, for whoever fills it

When the material is retrieved manually, this layout keeps provenance intact:

```
assets/
├── MANIFEST.md                        ← update the table above with every file
├── gallica_bd6t5344993p/
│   ├── f16.jpg                        ← IIIF page image
│   ├── f16.pdf                        ← page PDF
│   ├── f16_ocr.xml                    ← ALTO OCR
│   ├── f16_ocr.txt                    ← plain text extraction
│   └── oai_record.xml                 ← identifies periodical + date
├── berthomeau/
│   ├── 2021-07_conticini_1994.html    ← save complete, with images
│   ├── 2021-07_conticini_1994.pdf
│   └── search_results.html
├── bnf/
│   ├── cb121149081.pdf                ← data.bnf authority page
│   ├── cb444579018.html               ← "Morue, œuf gras cuit" notice
│   ├── cb444578192.html
│   ├── cb450830921.html
│   └── affinerAut_12114908.html       ← the full works list
├── liberation/
│   ├── 1994-07-12_rebonds.pdf         ← THE PRIORITY DOCUMENT
│   └── 1998-04-18_savez-vous-manger-les-choux.pdf
├── lexpress/
│   └── 1993-05_la-maison-conticini.pdf
├── agatfilms/
│   └── toques-a-la-loupe.html
├── guides/                            ← photographed guide pages
│   ├── michelin_1987..1999_p*.jpg
│   └── gaultmillau_1987..1999_p*.jpg
└── testimony/                         ← primary oral history
    ├── christian_conticini_interview_YYYY-MM-DD.md
    └── waitress_interview_YYYY-MM-DD.md
```

## Rules for adding files here

1. **Record every file in the manifest table above**, with its exact source URL, format, retrieval date and SHA-256.
2. **Keep originals unaltered.** Put any transcription or translation in a separate sibling file.
3. **Copyright.** Period newspaper and guide material remains in copyright. Retain scans for **private research use**; quote only fair-use extracts in the dossier text; **do not republish whole articles**. If this repository is public, consider keeping `assets/` private or `.gitignore`d and holding the scans locally.
4. **Interview transcripts** must carry: interviewee name, role and dates, interview date and place, interviewer, and explicit consent terms. See the protocol in `../07_open_questions_and_leads.md`, Lead 3.3.

## Retrieval priority

1. **`gallica_bd6t5344993p/`** — free, open API, guaranteed to contain the subject's name. Highest yield per minute of effort.
2. **`berthomeau/`** — free, and may reproduce the 1994 Libération text outright.
3. **`bnf/`** — free; closes the bibliography.
4. **`testimony/`** — the only route to genuinely new evidence.
5. **`liberation/1994-07-12`** — the single most important unretrieved document in the project.

Exact commands and query strings for each: see `../07_open_questions_and_leads.md` and `../08_source_map.md` §D.
