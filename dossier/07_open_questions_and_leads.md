# 07 — Open Questions and Prioritised Leads

This is the working file. It is ordered by **expected yield per unit of effort**, not by importance of the question.

Effort key: **🟢 minutes, free, from a browser** · **🟡 hours, or needs a subscription** · **🔴 on-site visit, correspondence, or paid reproduction**

---

## TIER 1 — Do these first. Free, fast, and blocked here only by the sandbox.

Everything in this tier failed in this environment purely because of DNS blocking. A human with an ordinary browser can clear the entire tier in **under an hour**, and it would move a large share of this dossier from [PARTIAL] to [VERIFIED].

### Lead 1.1 🟢 — Gallica ark bd6t5344993p, page 16

**Question:** what periodical is this, from what date, and what does it say about Christian Conticini?

**Why first:** Gallica is completely open — no login, no paywall, with public APIs for OCR, IIIF images and PDF. The page is *already known* to contain the string "christian conticini" in its OCR layer, because that is how the URL in the brief was constructed. This is a guaranteed hit on period press, and it is free.

**Exact steps:**
```
1. Identify the document:
   https://gallica.bnf.fr/services/OAIRecord?ark=bd6t5344993p
   → gives title, date, publisher, type.

2. Full IIIF manifest (structure + metadata):
   https://gallica.bnf.fr/iiif/ark:/12148/bd6t5344993p/manifest.json

3. OCR text of page 16:
   https://gallica.bnf.fr/RequestDigitalElement?O=bd6t5344993p&E=ALTO&Deb=16

4. Page image (full resolution):
   https://gallica.bnf.fr/iiif/ark:/12148/bd6t5344993p/f16/full/full/0/native.jpg

5. PDF of the page:
   https://gallica.bnf.fr/ark:/12148/bd6t5344993p.f16n1.pdf

6. Re-run the in-document search to find EVERY page mentioning him, not just f16:
   https://gallica.bnf.fr/ark:/12148/bd6t5344993p/f1.texteBrut
   (then Ctrl-F), or use the "Recherche dans le document" panel in the viewer.
```
**Save to:** `/dossier/assets/gallica_bd6t5344993p/`

### Lead 1.2 🟢 — Berthomeau, the 1994 article

**Question:** what did Christian Conticini actually argue on 12 July 1994? Does Berthomeau reproduce the text?

**Why:** this is the intellectual core of the dossier (`06`), and it currently rests entirely on a summary. Berthomeau's blog is free and public.

**Exact steps:**
1. Open the post: `https://www.berthomeau.com/2021/07/le-12-juillet-1994-christian-conticini-dezingue-le-culte-du-produit-sain-authentique-et-naturel-nous-en-reparlerons-avec-bruno-verju`
2. **Save the complete text and any images.** If Berthomeau reproduces the Libération article (he often reproduces period material), that single act resolves the largest open question here.
3. Then run the site search: `https://www.berthomeau.com/search/christian%20conticini/` and **enumerate every post**. There may be more than one.
4. Also try `https://www.berthomeau.com/search/conticini/` — broader, catches posts naming only the surname.
5. Check the July 2021 archive page (`/archive/2021-07/`) for related posts in the same run of argument.
6. **Consider emailing Berthomeau.** He is an engaged blogger who has demonstrably taken an interest in this exact article. He may have the clipping, or remember where he got it. Low cost, potentially decisive.

### Lead 1.3 🟢 — The BnF records, read properly

**Question:** the complete, accurate works list, and the resolution of the 1989 attribution.

**Exact steps:**
1. `https://catalogue.bnf.fr/affinerAut.do?nomAuteur=Conticini,+Christian&index0=AUT3;12114908` → **export the full list of attached records.**
2. Open each: `cb444579018`, `cb444578192`, `cb450830921`. Note for each: title, statement of responsibility, material type, date, shelf mark.
3. `https://data.bnf.fr/fr/ark:/12148/cb121149081` and its `.pdf`. Also try the RDF/JSON export for a machine-readable works list.
4. **For *La Cuisine gourmande des stars* (1989): read the transcribed statement of responsibility, the ISBN and the publisher.** That is what settles Christian vs Philippe. See Lead 2.4.
5. Also run `https://catalogue.bnf.fr` author search on **"Conticini"** alone, unfiltered, to catch records misfiled between the brothers.

**Note:** BnF has acknowledged disruptions from a cataloguing-system migration. If a record renders blank, **retry** rather than concluding it is absent.

### Lead 1.4 🟢 — Agat Films, and the full episode list

**Steps:**
1. `https://www.agatfilms-exnihilo.com/catalogue/films/toques-a-la-loupe/` — save the page; note synopsis, credits, and any episode list or stills.
2. Search the **Doc & Film International** catalogue for the series sales sheet.
3. **Email Agat Films.** Ask for: the full 26-episode list, the exact on-screen title spelling, broadcast dates, Christian Conticini's precise credit, and whether any stills or press kit survive. They are an active company and this is an ordinary archival enquiry.

---

## TIER 2 — Subscription or paid archives. High yield.

### Lead 2.1 🟡 — RetroNews (BnF press archive)

RetroNews is the BnF's digitised press platform. Subscription, with free trials; also **free on-site at the BnF**.

**Queries, in priority order.** Use exact-phrase quoting; start broad, then facet by title and date.

**A. Identity — run first, no date filter:**
```
"Christian Conticini"
```
Then use the left-hand facets (title, date, document type) to narrow. This surfaces bylines that keyword+date queries miss.

**B. The restaurant:**
```
"Table d'Anvers" "Conticini"                          [1986-2000]
"Table d'Anvers" "étoile"                             [1986-1999]
"Table d'Anvers" "place d'Anvers"
"Table d'Anvers" (alone — then facet)                 [1986-2000]
```

**C. The Libération column (see also 2.2):**
```
"Conticini" "Rebonds"                                 [1994]
"Conticini" "chronique"
"Conticini" "recette"                                 [1990-1999]
```

**D. Fusion / Peru:**
```
"Conticini" "ceviche"
"Table d'Anvers" "péruvien"
"Table d'Anvers" "Pérou"
"Conticini" "fusion"
"Table d'Anvers" "cuisine du monde"
```

**E. Science / Hervé This:**
```
"Conticini" "Hervé This"
"Conticini" "gastronomie moléculaire"
"Toques à la loupe"        AND        "Toqués à la loupe"
```

**F. Training:**
```
"Conticini" "Martinez"                                [1975-1990]
"Conticini" "Cannes"                                  [1975-1990]
"Christian Conticini" "chef"                          [1980-1990]
```

**G. Clientele (see §Tier 4 for the health warning):**
```
"Table d'Anvers" "Fujimori"
"Table d'Anvers" "Brad Pitt"
"Table d'Anvers" "Jennifer Aniston"
```

**Titles to prioritise in faceting:** Libération, Le Monde, Le Figaro, Le Quotidien de Paris, L'Express, Le Point, L'Humanité, La Croix.

### Lead 2.2 🟡 — The Libération archive, directly

**Question:** the full inventory of by-lined Christian Conticini pieces. Was there really a recurring column?

**Known anchors:**
- 12 July 1994 — *Rebonds*
- 18 April 1998 — *"Savez-vous manger les choux ?"*, in the **futurs** section, `.../futurs/1998/04/18/...-recettes-de-son-cru_233485/`

**Method:**
1. Retrieve both articles in full. Save as PDF and text.
2. **Exploit the URL structure.** Libération's archive is browsable by date: `https://www.liberation.fr/archives/1998/04/18/`. If the recipe pieces were a **weekly column**, they will sit on a **regular weekday**. 18 April 1998 was a **Saturday**. **Therefore: browse the Saturday archive index for consecutive weeks around April 1998** — say January to July 1998 — and look for further Conticini bylines. This is the single most efficient way to test the column hypothesis, and it needs only the free archive index pages.
3. Do the same around 12 July 1994 for the Rebonds slot.
4. Search the site for `Conticini` restricted to 1990–2000.
5. **Fallback if the online archive is thin:** Libération's pre-2000 archive is poorly digitised. The complete run exists on **microfilm at the BnF** and can be consulted on site. Once a date is known, the microfilm is definitive.

### Lead 2.3 🔴 — Michelin and Gault & Millau guide runs

**Question:** the year the star appeared, the years it was held, the actual 17/20, and — crucially — **the G&M written notice, which is a review**.

**Method:** consult the annual guides, **1987–1999**, at the BnF or a large French municipal library. Look up Paris 9e, **2 place d'Anvers**. Photograph each relevant page.

**This is the highest-value on-site action after the INAthèque**, because the G&M notice would supply the period critical text that `03` records as entirely missing.

### Lead 2.4 🟡 — *La Cuisine gourmande des stars* (1989), a physical copy

**Question:** who actually wrote it?

**Method:** BnF notice first (Lead 1.3), for ISBN and publisher. Then hunt a second-hand copy: **abebooks.fr, rakuten.fr, leboncoin.fr, chapitre.com, Amazon Marketplace FR**. An illustrated 50-page 1989 French cookery title should be cheap and findable. **The title page settles the attribution.**

---

## TIER 3 — Living witnesses. Potentially the highest yield of all.

These are the leads that generate **new** evidence rather than recovering old evidence. They are listed last only because they require correspondence.

### Lead 3.1 🔴 — Hervé This

He worked beside Christian for 26 episodes. He is alive, active and publishes prolifically.

**Ask:** How did the collaboration come about? What was Christian like technically? What did Christian understand about the science? Does he have materials, stills, notes? What became of Christian? Does he recall the 1994 Libération piece? Was the ceviche Christian's own?

**Also:** search This's own extensive bibliography and blog for "Conticini" — he has written the history of molecular gastronomy repeatedly and may already have published an account.

### Lead 3.2 🔴 — Philippe Tourancheau, director

He filmed Christian across 26 episodes. A working French documentarian. He is a direct professional witness to Christian at the stove, and — unlike almost everyone else in the record — has **no stake in the Philippe Conticini narrative**.

**Ask:** the full episode list, broadcast dates, surviving materials and stills, and his personal recollection of Christian.

### Lead 3.3 🔴 — Christian Conticini himself, and the former waitress

The user has access to both. **This is the most valuable untapped source in the entire project.** Oral testimony from named participants is legitimate historical evidence — it simply must be *captured properly* to be citable.

**Protocol for making the testimony citable:**

1. **Record it** (audio, with explicit consent), and transcribe.
2. **Log the metadata**: full name of interviewee, role and dates in that role, date and place of interview, interviewer, and consent terms.
3. **Ask open questions before named ones.** Critical: ask *"Which well-known people ate at the restaurant?"* **before** ever mentioning Fujimori, Pitt or Aniston. Naming them first contaminates the answer — a witness will very often confirm a name they have just been handed. This is the same failure mode that has been corrupting the AI searches; it corrupts human memory too.
4. **Anchor every claim in specifics**: what year? what season? who else was present? what was served? who took the booking? was there a reservation book, a photograph, a signed menu, a press cutting?
5. **Chase the paper.** Reservation books, guest books, signed menus, photographs, invoices — any of these converts oral testimony into documentary evidence in a single step. **Ask explicitly whether any survive.**
6. **Interview the two witnesses separately.** Independent corroboration is worth far more than a joint account.
7. **Store the transcript in this repository** as a dated primary source, and cite it as such.

**Suggested question set for Christian:**
- Date and place of birth; where in the family order relative to Philippe.
- Full apprenticeship history, house by house, with dates. **Was the Hôtel Martinez, Cannes, among them?**
- How and why La Table d'Anvers came about; the exact opening date in 1986.
- The division of labour with Philippe, in his own words.
- The Michelin star: which year, how it felt, how long held. The Gault & Millau 17/20.
- **The 12 July 1994 Libération piece: what was he arguing, and why then?** Does he have a copy?
- Was there a regular Libération column? How many pieces? Over what period?
- How did *Toques à la loupe* come about? How was Hervé This to work with?
- Was ceviche ever on the menu at Anvers? From when? What else was outside the French repertoire?
- Did he know Alain Ducasse? How well?
- What happened after 1998?
- **Does he have: menus, press cuttings, photographs, the reservation book, a copy of the 1989 book?** Anything physical he holds is a primary source and should be scanned into `/dossier/assets/`.

---

## TIER 4 — Claims that need discipline, not searching

### The clientele claim

**Status: [UNVERIFIED]. No published source of any kind.**

This must be handled carefully, and the reason is documented in the conversation history behind this dossier: **repeated AI searches have returned confident paragraphs naming Fujimori, Brad Pitt and Jennifer Aniston with zero citations attached.** That is not confirmation. That is the model repeating names it was given. It has now happened across multiple sessions and it will happen again.

**The rule for this project:** a claim about clientele is admissible only with (a) a dated published source, or (b) properly captured first-hand testimony per Lead 3.3. An uncited AI paragraph is neither, however confident its tone.

**Documentary routes worth trying:**
- Society and gossip columns of the period: *Le Figaro* "Carnet", *Point de Vue*, *Gala*, *Paris Match*, *Voici* — for the years the named figures were in Paris.
- **Spanish-language Peruvian press** for a presidential visit: `"Table d'Anvers" Fujimori`, `"Table d'Anvers" presidente`, `Fujimori París restaurante` — try the *El Comercio* archive.
- Fujimori's presidential travel is a matter of public record; establishing **which years he was in Paris** narrows the search enormously and is easy to do.
- Michelin-starred Paris restaurants of the period were routinely name-checked in celebrity-in-Paris features. Worth a RetroNews sweep independent of the named individuals.

### The Ducasse friendship

**[UNVERIFIED].** Only circumstantial contemporaneity (Le Louis XV, 1987; La Table d'Anvers, 1986).

**Routes:** Ducasse has published memoirs and given a very large number of interviews — search his published work for "Conticini". Ask Christian directly (Lead 3.3). Do not assert it meanwhile.

### The Martinez training

**[FAMILY TESTIMONY] — the substance is now settled; only the documentation is outstanding.** Christian trained at the Hôtel Martinez, Cannes, under **Chef Duparc**, then under **Chef Christian Willer**. See `01` §2.

The search environment remains **actively contaminated** by name-collision with **Christian Sinicropi**, the Martinez's later starred chef. Any search result linking "Christian" + "Martinez" must be screened for this before being believed — it is why earlier passes found nothing.

**Routes to a citable document:** the Hôtel Martinez / Hyatt heritage and press office, for brigade records c. 1980–1986; tribute and obituary coverage of Christian Willer (d. 2020), which often lists brigade alumni by name; period profile interviews (RetroNews Lead 2.1F), as French guides of the era printed a chef's training houses.

**One question to the family closes the remaining ambiguity:** *Chef Duparc's first name and approximate years.* No published source places a Duparc at the Martinez immediately before Willer — the indexed record ties a Sylvain Duparc to the **Carlton**, Cannes, in the same period — so either the tenure is simply undocumented online, or this is a different Duparc.

### The fusion primacy claim

**[UNVERIFIED] and probably unprovable as stated.** Use the defensible reformulation in `03` §3. What would move it: a **dated menu** from La Table d'Anvers, or a period review naming Peruvian dishes.

---

## Prioritised summary

| # | Lead | Effort | Expected yield |
|---|---|---|---|
| 1 | Gallica bd6t5344993p — OCR, image, PDF | 🟢 | **Very high** — free, guaranteed hit on period press |
| 2 | Berthomeau: the 1994 post + full site search | 🟢 | **Very high** — may contain the 1994 text itself |
| 3 | BnF records read properly; full works list | 🟢 | High — closes the bibliography |
| 4 | Agat Films page + direct enquiry | 🟢 | High — full episode list, exact title |
| 5 | **Interview Christian and the waitress, properly** | 🔴 | **Very high** — the only route to genuinely new evidence |
| 6 | INAthèque, on site — watch the series | 🔴 | **Very high** — see `05` §3 |
| 7 | Libération archive, incl. the Saturday-index trick | 🟡 | High — tests the column hypothesis |
| 8 | RetroNews sweep | 🟡 | High — period press, reviews |
| 9 | Gault & Millau guide run 1987–99 | 🔴 | High — ratings **and** the missing review text |
| 10 | Hervé This, direct enquiry | 🔴 | High — first-hand, and he may already have published on it |
| 11 | Michelin guide run 1987–99 | 🔴 | Medium — settles the star years |
| 12 | Tourancheau, direct enquiry | 🔴 | Medium-high — eyewitness, no stake in the Philippe story |
| 13 | Buy the 1989 book second-hand | 🟡 | Medium — settles the attribution |
| 14 | L'Express May 1993, in full | 🟡 | Medium — family detail, 1993 standing |
| 15 | Peruvian/society press for clientele | 🟡 | Low-medium — but the only documentary route to that claim |

---

## The questions, listed plainly

**Biographical:** date and place of birth · birth order · full training record · Martinez, yes or no · post-1998 life · is he alive, and where.

**The restaurant:** exact opening date · the star's first and last years · the G&M score and its years · what the food was actually like · was there ever a Peruvian or fusion element on the menu · exact circumstances of the closure.

**Writing:** the 1994 argument in his own words · was there a recurring column, and how many pieces · the 1989 book's true authorship · any writing anywhere else.

**Television:** the other thirteen episodes · exact title orthography · broadcast dates · how the collaboration with This began · is any footage viewable.

**Relationships:** Ducasse · Hervé This beyond the series · the working relationship with Philippe, in his own words · his father Roger's role.

**Clientele:** anything at all, documented.
