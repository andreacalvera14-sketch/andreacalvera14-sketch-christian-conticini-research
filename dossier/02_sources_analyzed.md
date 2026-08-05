# 02 — Sources Analysed, One by One

## How to read this file

Each entry gives: **full citation → retrieval status → what it says → quoted passages → analysis**.

**A standing caveat that applies to every entry below.** The agent could not open any of these URLs directly (see `00_executive_summary.md`). What it had was an indexed search tool that returns a synthesised summary with source citations attached. So:

- Where a passage is marked **[SUMMARY-DERIVED]**, it is text produced by the search tool *about* the source, in French. It is **not a transcription of the source**. It reflects the source's content as indexed. Treat it as a lead, not as a quotation.
- Where a passage is marked **[INDEXED SNIPPET]**, it is a fragment that appears to reproduce the source's own catalogue/title text as indexed.
- **Nowhere in this dossier is a sentence presented as a verbatim quotation from a source the agent did not read.** Where the brief asked for original French plus English translation of key passages, and the French original could not be obtained, that is stated in place of the quotation rather than filled in.

This is the point at which a dossier of this kind normally goes wrong. It is being made explicit so that it does not.

---

## SOURCE 1 — Berthomeau, search index for "christian conticini"

**Citation:** *Le blog de Jacques Berthomeau*, site search results for "christian conticini". https://www.berthomeau.com/search/christian%20conticini/

**Retrieval:** **[COULD-NOT-ACCESS]** — `curl: (6) Could not resolve host: www.berthomeau.com`. Not retrieved in any format.

**What it is:** Jacques Berthomeau is a French wine and food commentator and prolific blogger, a former French agriculture-ministry official known for the 2001 "Rapport Berthomeau" on French wine. His blog reproduces and comments on period press material. As an aggregator of pre-digital French food journalism he is a genuinely useful secondary route into material that is otherwise offline.

**What it would give:** the complete inventory of Berthomeau's posts mentioning Christian — potentially more than the single 1994 post named in the brief, and potentially reproducing further Libération text.

**Analysis:** this is the highest-value *accessible-to-a-human* source in the entire brief. It is a free public blog with no paywall. A human with an unrestricted browser can retrieve it in seconds. Its unavailability here is purely an artefact of the sandbox. **Priority 1 for manual retrieval.**

---

## SOURCE 2 — Berthomeau, post of July 2021 on the 12 July 1994 article

**Citation:** Jacques Berthomeau, *"Le 12 juillet 1994 Christian Conticini dézingue le culte du produit sain, authentique et naturel, nous en reparlerons avec Bruno Verjus"*, berthomeau.com, July 2021.
https://www.berthomeau.com/2021/07/le-12-juillet-1994-christian-conticini-dezingue-le-culte-du-produit-sain-authentique-et-naturel-nous-en-reparlerons-avec-bruno-verju

**Retrieval:** **[COULD-NOT-ACCESS]** — DNS blocked. Confirmed to exist and be indexed; also listed in the blog's July 2021 archive page (berthomeau.com/archive/2021-07/).

**What it says [SUMMARY-DERIVED]:**

> « Le 12 juillet 1994, Christian Conticini a livré une critique incisive du "culte du produit sain, authentique et naturel" dans un article publié dans la rubrique **"Rebonds" de Libération**. Sa prise de position a été mentionnée par Jacques Berthomeau sur son blog, qui souligne qu'à l'époque, Conticini "dézingue" la vision idéalisée de ces notions… »

English: *"On 12 July 1994, Christian Conticini delivered an incisive critique of the 'cult of the healthy, authentic and natural product' in an article published in Libération's 'Rebonds' section. His stance was taken up by Jacques Berthomeau on his blog, who stresses that at the time Conticini 'shot down' the idealised vision of these notions…"*

Further, [SUMMARY-DERIVED]: the original text of Conticini's critique is **not fully available online**; Berthomeau links the position forward to contemporary product-first chefs, naming **Bruno Verjus**; and Berthomeau's suggestion for finding the original is to search *Libération*'s archives under the **Rebonds** rubric.

**The one word we can rely on from the source itself:** **« dézingue »** — it is in the post's own URL slug, so it is Berthomeau's word, not a paraphrase. It is strong, colloquial French: to shoot down, to trash, to demolish. English: *"guns down."* Berthomeau chose a violent verb to characterise Christian's 1994 intervention. That is a real, retrievable signal about the tone of the piece.

**Analysis.** Three things of substance emerge even without the article.

1. **A precise archival coordinate.** *Libération*, **12 July 1994**, **Rebonds** section. Rebonds is Libération's opinion/op-ed page — signed argument, not reportage. That tells us Christian was writing as an *opinion contributor*, which is a different and higher-status thing than being interviewed.
2. **A datable intellectual position.** In 1994, at the height of the French terroir-and-authenticity turn, a starred Paris chef publicly attacked the ideology of the natural product. That is a contrarian position, taken early, by a working chef. It is the single most distinctive intellectual fact in this dossier.
3. **Berthomeau's own framing** — reaching back to it in 2021 to set against Bruno Verjus — shows a knowledgeable French food commentator treating the 1994 piece as *still worth arguing with* twenty-seven years later. That is an independent judgement of its significance, made by someone with no stake in Christian's reputation.

**Caution.** Everything above about the article's *content* is second-hand. We do not know Christian's actual argument, only its target and its temperature. Do not attribute specific reasoning to him on this basis.

---

## SOURCE 3 — Gallica, ark:/12148/bd6t5344993p, folio 16

**Citation:** Gallica (BnF digital library), document ark:/12148/bd6t5344993p, view f16, search term "christian conticini".
https://gallica.bnf.fr/ark:/12148/bd6t5344993p/f16.item.r=christian%20conticini

**Retrieval:** **[COULD-NOT-ACCESS]** — `curl: (6) Could not resolve host: gallica.bnf.fr`. No PDF, no IIIF image, no OCR text obtained.

**What it is:** the `bd6t` prefix in a Gallica ARK denotes a **microform-derived digitisation** — typically periodicals scanned from microfilm. The URL points at **page 16** of the document, hit on a full-text search for "christian conticini," which means Gallica's OCR layer contains that string on that page. Almost certainly, therefore: **a page of a periodical containing a passage naming Christian Conticini.**

**What could not be determined:** the title of the periodical, its date, the nature of the item on f16, or the surrounding text. A search attempt on the bare ARK returned only speculation about Philippe, which is unreliable and is not recorded here as fact.

**Analysis.** This is the most frustrating entry in the dossier and the most tractable for a human. Gallica is **fully open**: it exposes IIIF, OCR text and PDF export without authentication. Every one of the following would have worked from an unrestricted machine, and is recorded here so a human can run them:

```
# Metadata (OAI) — identifies the periodical and date
https://gallica.bnf.fr/services/OAIRecord?ark=bd6t5344993p

# Pagination / structure
https://gallica.bnf.fr/services/Pagination?ark=bd6t5344993p

# OCR text of page 16
https://gallica.bnf.fr/RequestDigitalElement?O=bd6t5344993p&E=ALTO&Deb=16

# Page image, IIIF
https://gallica.bnf.fr/iiif/ark:/12148/bd6t5344993p/f16/full/full/0/native.jpg

# IIIF manifest (full structure + metadata)
https://gallica.bnf.fr/iiif/ark:/12148/bd6t5344993p/manifest.json

# PDF of a page range
https://gallica.bnf.fr/ark:/12148/bd6t5344993p.f16n1.pdf
```

**This is the single highest-yield unretrieved item in the brief**, because unlike the newspaper sources it is (a) free, (b) machine-retrievable, (c) already known to contain the subject's name, and (d) likely to be period press that no other route reaches. **Priority 1, jointly with Source 1.**

---

## SOURCE 4 — BnF catalogue, author refinement, "Conticini, Christian"

**Citation:** BnF Catalogue général, author-refinement query, `nomAuteur=Conticini, Christian`, `index0=AUT3;12114908`.
https://catalogue.bnf.fr/affinerAut.do?nomAuteur=Conticini%2C+Christian&index0=AUT3%3B12114908

**Retrieval:** **[COULD-NOT-ACCESS]** — DNS blocked.

**What it is:** a filtered results view listing every BnF record attached to authority ID **12114908** — the machine identifier for Christian Conticini as an author/contributor. The definitive works list.

**Analysis.** The authority number 12114908 is the key that unlocks the rest of the BnF material, and it is confirmed: it is embedded in this URL and matches the data.bnf.fr ARK cb**12114908**1 (Source 7). The existence of a distinct BnF authority record is itself meaningful — **the French national library treats Christian Conticini as a distinct catalogued creator, not as a variant of his brother.** That is an institutional fact and it settles the "is he a real distinct figure" question independently of any press.

Note also, from indexed search: BnF's catalogue is currently undergoing a **cataloguing-tool migration causing display and data-retrieval disruptions**, publicly acknowledged on their site. A human retrieving these records should be aware that a blank or partial record may be a transient system fault rather than an absence of data — and should retry.

---

## SOURCE 5 — Agat Films / Ex Nihilo, *Toques à la loupe*

**Citation:** Agat Films & Cie – Ex Nihilo, catalogue entry, *Toques à la loupe*.
https://www.agatfilms-exnihilo.com/catalogue/films/toques-a-la-loupe/

**Retrieval:** **[COULD-NOT-ACCESS]** — DNS blocked. Content known via indexed summary of the producer's own page.

**What it says [SUMMARY-DERIVED]:**

> « La série documentaire "Toques à la loupe" produite par Agat Films – Ex Nihilo est une collection de **26 épisodes de 13 minutes**, réalisée par **Philippe Tourancheau** en **1997**. Cette série … mêle l'expertise du chef **Christian Conticini** avec celle du chimiste **Hervé This** … Chaque épisode est une leçon où ils explorent et expliquent les processus chimiques à l'œuvre lors de la cuisson des aliments … »

English: *"The documentary series 'Toques à la loupe', produced by Agat Films – Ex Nihilo, is a collection of 26 episodes of 13 minutes, directed by Philippe Tourancheau in 1997. The series combines the expertise of chef Christian Conticini with that of the chemist Hervé This… Each episode is a lesson in which they explore and explain the chemical processes at work in the cooking of food…"*

Additionally [SUMMARY-DERIVED]: broadcast on **La Cinquième** (later France 5); described as one of the first popularising programmes on molecular gastronomy on French television; distribution associated with **Doc & Film International**; traces survive via **INA** notices and documentary catalogues.

**Analysis — this is the dossier's pivotal source.** It is the producer's own catalogue, i.e. as close to a primary record as a production credit gets. It establishes, with names, dates and format:

- Christian Conticini as **the cook** in a national television series about the science of cooking;
- opposite **Hervé This**, co-founder of molecular gastronomy with Nicholas Kurti — an association that places Christian inside the most consequential French culinary-intellectual project of the period;
- in **1997**, i.e. *while still running the Table d'Anvers kitchen*;
- across **26 episodes**, which is a substantial commitment, not a cameo.

It also explains the shape of his BnF record (Sources 6, 8, 9) and dissolves the "1997 recipe series" misreading.

**Note on the title.** The brief writes *"Toqués à la loupe"*; the producer's URL slug is `toques-a-la-loupe`. *Toque* is the chef's hat (hence, by metonymy, a chef); *toqué* means "crazy/cracked." Either is a plausible pun and the accent may simply be dropped in the slug. **The exact orthography of the on-screen title is unresolved** and both spellings should be tried when searching INA.

---

## SOURCE 6 — BnF catalogue, ark:/12148/cb444579018

**Citation:** BnF Catalogue général, notice ark:/12148/cb444579018.
https://catalogue.bnf.fr/ark:/12148/cb444579018

**Retrieval:** **[COULD-NOT-ACCESS]** — DNS blocked.

**What it is [INDEXED SNIPPET].** The indexed title of this record reads:

> « Notice bibliographique **Morue, œuf gras cuit / Philippe Tourancheau réal.** … »

English: *"Bibliographic record — Cod, fat-cooked egg / Philippe Tourancheau, dir. …"*

**Analysis — the correction that reframes the bibliography.** This fragment is short but decisive. `réal.` is the standard BnF abbreviation for *réalisateur*, director. A record whose primary statement of responsibility is a **director credit** is an **audiovisual** record.

Therefore *Morue, œuf gras cuit* — previously catalogued in earlier research as a 1997 recipe co-authored by Christian Conticini and Hervé This — is **an episode of *Toques à la loupe***, directed by Philippe Tourancheau, in which Christian Conticini cooks.

By extension, the whole list of 1997 "works" attached to Christian's BnF authority record is an **episode list**. This is stated in `00`, `01`, `04` and `05` because it invalidates a conclusion that earlier attempts had already committed to paper.

**Confidence:** the inference from `réal.` is strong and the corroboration from the producer's catalogue (Source 5) is independent. But the full notice was not read, and the exact BnF material designation (videocassette? broadcast deposit? DVD?) is unknown.

---

## SOURCE 7 — data.bnf.fr, ark:/12148/cb121149081

**Citation:** data.bnf.fr, *Christian Conticini*, ark:/12148/cb121149081 (authority 12114908).
https://data.bnf.fr/fr/ark:/12148/cb121149081 · PDF form: `.../cb121149081.pdf`

**Retrieval:** **[COULD-NOT-ACCESS]** — DNS blocked. The `.pdf` variant is confirmed to exist and be indexed but was not downloaded.

**What it says [SUMMARY-DERIVED]:**

> « Le livre "La cuisine gourmande des stars" figure bien parmi les œuvres listées pour Christian Conticini sur data.bnf.fr. Il apparaît que ce titre date de **1989** … Christian Conticini a également collaboré sur plusieurs [œuvres] de **1997** en collaboration avec **Hervé This** … »

English: *"The book 'La cuisine gourmande des stars' does appear among the works listed for Christian Conticini on data.bnf.fr. This title dates from 1989… Christian Conticini also collaborated on several 1997 [works] in collaboration with Hervé This…"*

**Analysis.** Confirms: the authority record exists; it carries 1989 and 1997 material; the 1997 material is linked to Hervé This. Read together with Source 6, "1997 works with Hervé This" resolves to "1997 television episodes with Hervé This."

**An important limitation to state.** The `.pdf` at this address is a **PDF rendering of the catalogue page**, not a repository of article scans. There are no press-article PDFs behind a data.bnf.fr authority URL. This was already correctly identified in the prior conversation and is confirmed as the right reading. Anyone expecting to "download all the articles" from this link should reset that expectation: it is metadata, and the route to actual documents runs through the Gallica/INA links that hang off it.

---

## SOURCE 8 — BnF catalogue, ark:/12148/cb444578192

**Citation:** BnF Catalogue général, notice ark:/12148/cb444578192.
https://catalogue.bnf.fr/ark:/12148/cb444578192

**Retrieval:** **[COULD-NOT-ACCESS]** — DNS blocked. No record-specific content retrieved.

**Analysis.** The ARK is numerically adjacent to Source 6 (cb4445790… / cb4445781…), which in BnF practice indicates records **created in the same cataloguing batch**. Given Source 6 is a *Toques à la loupe* episode, this is with high probability **another episode of the same series**. **[PARTIAL — inference from ARK adjacency, not from the record.]** A human should confirm the episode title and hold what remains.

---

## SOURCE 9 — BnF catalogue, notice list ark:/12148/cb450830921

**Citation:** BnF Catalogue général, `liste-de-notices.do?arkNotice=ark:/12148/cb450830921`.
https://catalogue.bnf.fr/liste-de-notices.do?arkNotice=ark%3A%2F12148%2Fcb450830921

**Retrieval:** **[COULD-NOT-ACCESS]** — DNS blocked.

**Analysis.** The `liste-de-notices` endpoint returns a **set** of records rather than one, which typically indicates a **collection-level or serial record** with constituent parts. The ARK block (cb4508…) is distinct from the cb4445… block of Sources 6 and 8, so this is probably a **different deposit** — plausibly the series-level record for *Toques à la loupe*, or a separate work entirely. **Unresolved.** Genuinely worth a human's time, because a series-level record would list all 26 episodes in one place and complete the filmography.

---

## SOURCE 10 — *Libération*, 18 April 1998

**Citation:** *"Savez-vous manger les choux ? Christian Conticini détaille quelques recettes de son cru"*, **Libération**, 18 April 1998.
https://www.liberation.fr/futurs/1998/04/18/savez-vous-manger-les-choux-christian-conticini-detaille-quelques-recettes-de-son-cru_233485/

**Retrieval:** **[COULD-NOT-ACCESS]** — DNS blocked; additionally understood to be behind Libération's archive paywall. Body text never seen.

**What is established:** the article exists; it is dated **18 April 1998**; its subject is **cabbage**; Christian Conticini is the named author of recipes described as *"de son cru"* (of his own devising); it sits in Libération's **"futurs"** URL section; Libération's archive index for that date exists at `liberation.fr/archives/1998/04/18/`. **[PARTIAL]**

**What is NOT established:** the text, the recipes, the length, whether it is one of a series.

**Analysis.** Two points of real weight.

1. **The word *"chou"* is a trap that must be flagged.** A search for Conticini + choux collapses instantly into **Philippe's *pâte à choux*** — choux pastry, Paris-Brest, chouquettes. The search tool did exactly this: asked for the 1998 Libération cabbage article, it returned a Philippe Conticini choux-pastry recipe. **These are different words for different things** (*le chou* the vegetable; *la pâte à choux* the pastry) and this is a live contamination risk for anyone researching Christian. Recorded here as a methodological warning.
2. **The URL section is "futurs."** In 1998 Libération's *Futurs* pages covered science and technology. A chef's recipe column filed under *Futurs* rather than a lifestyle section is a meaningful signal: it is consistent with the **Hervé This / science-of-cooking** register Christian was working in that same year on television. That the 1997 TV series and the 1998 science-section byline point the same way is the closest thing this dossier has to independent corroboration of his intellectual position.

**On the "recurring column" question.** The brief asks for an enumeration of every by-lined Libération piece. **Two dated pieces are now known — 12 July 1994 and 18 April 1998.** Two data points four years apart are consistent with a recurring column but **do not demonstrate one**. The claim of a regular column remains **[UNVERIFIED]**; what is verified is that he was published in Libération at least twice, in different registers (op-ed; recipes).

---

## SOURCE 11 — *L'Express*, May 1993

**Citation:** *"La maison Conticini, de fils en père"*, **L'Express**, May 1993.
https://www.lexpress.fr/informations/la-maison-conticini-de-fils-en-pere_594231.html

**Retrieval:** **[COULD-NOT-ACCESS]** — DNS blocked; L'Express archive likely paywalled.

**What it says [SUMMARY-DERIVED]:**

> « … contrairement à la tradition où "les fils quittent les pères", c'est **Roger Conticini**, le patriarche, qui a d'abord aidé ses deux fils à faire de **La Table d'Anvers** l'une des tables reconnues de Paris, avant de partir ouvrir sa propre maison. L'article vante l'ambiance conviviale et la cuisine traditionnelle de cette adresse, située à deux pas du **Champ-de-Mars**, dans un esprit de "cantine à l'ancienne" avec "plats canailles et bons petits vins"… »

English: *"…contrary to the tradition in which 'sons leave fathers', it is Roger Conticini, the patriarch, who first helped his two sons make La Table d'Anvers one of the recognised tables of Paris, before leaving to open his own house. The article praises the convivial atmosphere and traditional cooking of this address, a step from the Champ-de-Mars, in the spirit of an old-fashioned canteen with 'hearty dishes and good little wines'…"*

**Analysis.** Four extractable facts, all **[PARTIAL]**: the father is named **Roger**; he **worked at La Table d'Anvers** helping his sons before opening his own place; **Roger's own subsequent establishment — not La Table d'Anvers** — is a traditional bistro **near the Champ-de-Mars** (7th arrondissement); and by 1993 La Table d'Anvers was described as *"one of the recognised tables of Paris."*

**Do not conflate the two addresses.** La Table d'Anvers is at **2 place d'Anvers, 75009** (9th arrondissement, at the foot of Montmartre). The Champ-de-Mars bistro is **Roger's separate venture** in the 7th, a different neighbourhood entirely, and has no bearing on the location or character of the restaurant that is this dossier's subject.

That last phrase, if it is the article's own, is a **1993 third-party assessment of the restaurant's standing** from a national newsweekly — and therefore, since Christian ran the savoury kitchen, an assessment of his cooking. It is the closest thing in this dossier to a period critical judgement. **It must be handled carefully: the phrasing reaches us through a summary, not the page.**

**Interpretive caution.** The article is about *the family and the father's new restaurant*. It is not a Christian profile. It should not be over-read as evidence about Christian specifically beyond the four facts above.

---

## Cross-cutting assessment

**What the eleven sources, taken together, actually establish.**

Christian Conticini is documented in three independent institutional registers:

1. **Institutional/bibliographic** — a BnF authority record (12114908) with attached works. The national library treats him as a distinct creator.
2. **Audiovisual** — a 26-episode 1997 national television series in which he is the cook, produced by a serious documentary house, opposite the co-founder of molecular gastronomy.
3. **Journalistic** — at least two by-lined pieces in a national daily, in 1994 (op-ed polemic) and 1998 (recipes, science section), plus family/restaurant coverage in a national newsweekly in 1993, plus a blogger returning to his 1994 argument in 2021.

That is a considerably firmer footing than "Philippe Conticini's less famous brother."

**What they do not establish.** Anything about his formation, his birth, his post-1998 life, his clientele, his relationship with Ducasse, or any claim of primacy in fusion cuisine. And, critically, **not one of the eleven was read in original form by this agent.** The evidentiary floor under this entire dossier is indexed summary. A human with a browser can raise that floor substantially in under an hour, starting with Sources 1, 2 and 3, none of which are paywalled.
