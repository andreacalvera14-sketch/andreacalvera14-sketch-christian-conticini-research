# 08 — Source Map

Every URL in the brief, plus every additional source consulted. **Nothing is silently dropped.**

## Retrieval status key

| Status | Meaning |
|---|---|
| ❌ **BLOCKED-DNS** | Direct fetch failed at DNS resolution. No content retrieved in any format. |
| 🟡 **INDEXED-SUMMARY** | Not opened. Content known only through a search tool that returns a synthesised summary with the source cited. Second-hand. |
| ✅ **RETRIEVED** | Opened and read in original form. **No source in this dossier has this status.** |

## Environment statement

Two independent retrieval mechanisms were tested and both failed for every host in the brief:

1. **`curl` from the shell** → `curl: (6) Could not resolve host: <host>` for all seven hosts tested.
2. **The agent's dedicated page-fetch tool** → `WebFetchBlockedUrlError: failed to lookup address information: No address associated with hostname`.

The only functioning external tool was an **indexed web-search** tool. Its output is a synthesis with citations, not page content. Every 🟡 row below therefore records knowledge *about* a source, not the source.

**Zero files were downloaded. `/dossier/assets/` contains no retrieved binaries.** See `assets/MANIFEST.md`.

---

## A. The eleven primary URLs from the brief

| # | URL | Status | Format saved | Confidence in what we know | Notes |
|---|---|---|---|---|---|
| 1 | `berthomeau.com/search/christian%20conticini/` | ❌ BLOCKED-DNS | none | n/a — no content | Free public blog search. **Trivially retrievable by a human.** |
| 2 | `berthomeau.com/2021/07/le-12-juillet-1994-christian-conticini-dezingue-le-culte-du-produit-sain-authentique-et-naturel-...` | ❌ BLOCKED-DNS / 🟡 | none | **Medium** — existence, date (12 Jul 1994), target, and *Rebonds* placement all consistent across indexing | Berthomeau's own verb « dézingue » is in the URL slug, so is reliable |
| 3 | `gallica.bnf.fr/ark:/12148/bd6t5344993p/f16.item.r=christian%20conticini` | ❌ BLOCKED-DNS | **none** | **Very low** — periodical, date and content all unknown | **The most serious loss in the dossier.** Gallica is fully open with public APIs; this failure is purely environmental |
| 4 | `catalogue.bnf.fr/affinerAut.do?nomAuteur=Conticini,+Christian&index0=AUT3;12114908` | ❌ BLOCKED-DNS | none | **Medium** — the authority ID **12114908** is confirmed from the URL itself | The definitive works list; unread |
| 5 | `agatfilms-exnihilo.com/catalogue/films/toques-a-la-loupe/` | ❌ BLOCKED-DNS / 🟡 | none | **Medium-high** — producer's own catalogue; details corroborated by BnF | Source of the series credits |
| 6 | `catalogue.bnf.fr/ark:/12148/cb444579018` | ❌ BLOCKED-DNS / 🟡 | none | **Medium-high** for the title fragment *"Morue, œuf gras cuit / Philippe Tourancheau réal."* | The `réal.` credit is the key that reframed the whole bibliography |
| 7 | `data.bnf.fr/fr/ark:/12148/cb121149081` | ❌ BLOCKED-DNS / 🟡 | none | **Medium** — record exists; 1989 title and 1997 Hervé This material confirmed present | `.pdf` variant exists but is a rendering of the catalogue page, **not article scans** |
| 8 | `catalogue.bnf.fr/ark:/12148/cb444578192` | ❌ BLOCKED-DNS | none | **Low** — no record-specific content obtained | Likely another *Toques à la loupe* episode, inferred from ARK batch adjacency to #6 |
| 9 | `catalogue.bnf.fr/liste-de-notices.do?arkNotice=ark:/12148/cb450830921` | ❌ BLOCKED-DNS | none | **Low** — nothing obtained | `liste-de-notices` returns a set → possibly the **series-level** record listing all 26 episodes |
| 10 | `liberation.fr/futurs/1998/04/18/savez-vous-manger-les-choux-christian-conticini-detaille-quelques-recettes-de-son-cru_233485/` | ❌ BLOCKED-DNS / 🟡 | none | **Medium** for existence, date, title, byline; **zero** for body text | Also paywalled. Section is *futurs* (science). 18 Apr 1998 was a **Saturday** |
| 11 | `lexpress.fr/informations/la-maison-conticini-de-fils-en-pere_594231.html` | ❌ BLOCKED-DNS / 🟡 | none | **Medium** — May 1993; father **Roger**; Roger's *own separate* Champ-de-Mars bistro (not La Table d'Anvers); "one of the recognised tables of Paris" | Likely paywalled |

**Score: 0 of 11 retrieved. 6 of 11 partially characterised via indexing. 5 of 11 essentially dark (#1, #3, #4, #8, #9).**

---

## B. Additional sources touched via indexed search

| Source | Status | What it contributed | Confidence |
|---|---|---|---|
| `berthomeau.com/archive/2021-07/` | 🟡 | Confirms the 1994 post sits in the July 2021 archive | Medium |
| `liberation.fr/archives/1998/04/18/` | 🟡 | Confirms an archive index page exists for that date | Medium |
| `gazettelabo.fr/archives/publics/1998/31this.htm` | 🟡 | 1998 piece on Hervé This and physical chemistry in cooking — contemporary context for the collaboration | Medium |
| `parisgourmand.com/restaurant-paris/la-table-d-anvers.html` | 🟡 | Restaurant listing; address; successor establishment | Low-medium |
| `fr.gaultmillau.com/.../philippe-conticini` | 🟡 | G&M's own Philippe page; restaurant context; 1991 award | Medium — **about Philippe** |
| `wikiwand.com/fr/articles/Philippe_Conticini` | 🟡 | 1986 founding, brothers, division of labour | Medium — **about Philippe** |
| `grokipedia.com/page/Philippe_Conticini` | 🟡 | Same facts | **Low** — AI-generated encyclopedia, **not independent corroboration** |
| `cuisine.journaldesfemmes.fr/...philippe-conticini...` | 🟡 | Restaurant context; verrines 1994 | Low-medium — **about Philippe** |
| `meetmymentor.fr`, `dedikazio.com`, `mag.guydemarle.com`, `fnac.com` bio | 🟡 | Philippe biography only | Low — **about Philippe** |

### An important caveat on the "independent corroboration" of the star and 17/20

Several 🟡 sources above repeat the 1 Michelin star and 17/20 G&M. **They are not fully independent of one another.** Most are Philippe-focused biography pages, a genre in which facts are copied between sites, and at least one (`grokipedia`) is itself AI-generated. Consistency across such a set is weaker evidence than it looks. **This is why `03` holds those ratings at [PARTIAL] despite their apparent ubiquity.**

---

## C. Sources named in the brief that were never located at all

| Target | Result |
|---|---|
| Christian's *Libération* column, as a **series** | **Two dated pieces identified (1994, 1998). No third. The column's existence remains [UNVERIFIED].** |
| Le Monde, Le Figaro, Le Quotidien de Paris on Conticini or the restaurant | **Nothing located** |
| Gault & Millau guide entry (the text) | **Nothing located** |
| Michelin guide entry | **Nothing located** |
| Thuriès Gastronomie Magazine | **Nothing located** |
| **Any review of La Table d'Anvers, from any source, any year** | **One located on the second pass: the GAYOT notice, praising Christian by name (`03` §2). Still nothing in the French press.** |
| Published evidence of Hôtel Martinez training | **Nothing published. Searches contaminated by Christian Sinicropi. Now attested by family testimony — Chef Duparc, then Chef Christian Willer (`01` §2)** |
| Evidence of an Alain Ducasse friendship | **Nothing** |
| Evidence for fusion / Franco-Peruvian primacy | **Nothing** beyond the 1997 *Ceviche de langoustine* episode title |
| **Any evidence of celebrity or political clientele** | **Nothing. No published source of any kind. See the prompt-echo warning in `07` Tier 4** |
| Any photograph of Christian Conticini | **Nothing** |
| Any first-person interview with Christian | **Nothing** |

---

## D. Manual retrieval instructions, per blocked source

Full detail in `07_open_questions_and_leads.md`. Condensed here so this file stands alone.

### #1, #2 — Berthomeau
Open both URLs in any browser; free, no paywall. Save the 1994 post complete with images — **it may reproduce the Libération text**. Then run `/search/conticini/` as well as `/search/christian%20conticini/` to enumerate all posts. Consider emailing Berthomeau: he has demonstrably engaged with this exact article.

### #3 — Gallica
```
https://gallica.bnf.fr/services/OAIRecord?ark=bd6t5344993p            # identify it
https://gallica.bnf.fr/iiif/ark:/12148/bd6t5344993p/manifest.json     # structure
https://gallica.bnf.fr/RequestDigitalElement?O=bd6t5344993p&E=ALTO&Deb=16   # OCR of f16
https://gallica.bnf.fr/iiif/ark:/12148/bd6t5344993p/f16/full/full/0/native.jpg  # image
https://gallica.bnf.fr/ark:/12148/bd6t5344993p.f16n1.pdf              # PDF
```
Then search *within* the document for every other page mentioning him.

### #4, #6, #7, #8, #9 — BnF
Open each; export the full record. From #4, export the complete attached-works list. Note material type and shelf mark for the audiovisual records. For #7 use the RDF/JSON export for machine-readable works. **If a record renders blank, retry — BnF has acknowledged a cataloguing-migration fault.**

**BnF reproduction request wording** (for material that must be ordered):

> Madame, Monsieur,
>
> Je souhaite obtenir une reproduction numérique des documents suivants, conservés à la Bibliothèque nationale de France :
> — notice ark:/12148/cb444579018 ;
> — notice ark:/12148/cb444578192 ;
> — notice ark:/12148/cb450830921 ;
> — ainsi que l'ensemble des documents rattachés à la notice d'autorité « Conticini, Christian » (identifiant BnF 12114908).
>
> Ces documents concernent la série télévisée « Toques à la loupe » (1997, réal. Philippe Tourancheau, prod. Agat Films & Cie / Ex Nihilo, diffusion La Cinquième), à laquelle a participé le chef Christian Conticini aux côtés d'Hervé This.
>
> Je recherche également le document numérisé Gallica ark:/12148/bd6t5344993p, en particulier la page 16, qui mentionne Christian Conticini : j'aimerais en connaître le titre exact, la date de publication, et obtenir une reproduction de cette page.
>
> Cette demande s'inscrit dans le cadre d'une recherche documentaire à caractère privé et non commercial.
>
> Je vous remercie par avance et vous prie d'agréer, Madame, Monsieur, l'expression de mes salutations distinguées.

### #5 — Agat Films
Open the catalogue page; save synopsis, credits, stills. Then email requesting: full 26-episode list, exact on-screen title spelling, broadcast dates, Christian Conticini's precise credit, surviving press kit.

### #10 — Libération, 18 April 1998
Retrieve via a Libération subscription or the free archive index. **Then exploit the date: 18 April 1998 was a Saturday.** Browse `liberation.fr/archives/YYYY/MM/DD/` for consecutive Saturdays across 1998 to test the recurring-column hypothesis. Fallback: **Libération on microfilm at the BnF**, which is complete for the period.

### #11 — L'Express, May 1993
Retrieve via an L'Express subscription, or consult the printed issue at the BnF. **Determine the exact issue date**, which is not currently known beyond "May 1993."

---

## E. Honest confidence audit

| Claim | Confidence | Rests on |
|---|---|---|
| Christian Conticini is a distinct person, brother of Philippe | **High** | Multiple sources + a distinct BnF authority record |
| Co-founded La Table d'Anvers, 1986, place d'Anvers, Paris 9e | **High** | Multiple consistent sources |
| Christian = savoury; Philippe = pastry | **High** | Stated by every source touching the restaurant |
| BnF authority 12114908 / ark cb121149081 exists | **High** | The ID is in the brief's own URL and matches the ARK |
| *Toques à la loupe*, 1997, 26×13′, Tourancheau, Christian + Hervé This | **Medium-high** | Producer catalogue **plus** independent BnF `réal.` credit |
| The 1997 BnF "works" are TV episodes, not recipes | **Medium-high** | The `réal.` credit; strongly corroborated by the producer catalogue |
| Libération, 12 Jul 1994, *Rebonds*, anti-"natural product" | **Medium** | Berthomeau, via indexing; the verb « dézingue » is his own |
| Libération, 18 Apr 1998, cabbage recipes | **Medium** | URL, date and headline confirmed; **text unseen** |
| 1 Michelin star | **Medium** | Ubiquitous but **not sourced to any guide edition** |
| 17/20 G&M specifically | **Low-medium** | Ubiquitous, unsourced, and **contradicted by the 16/20 on the one guide page located** (`03` §2.1) |
| GAYOT review text, praising Christian's invention | **Medium** | Returned consistently by the index across repeated queries; page itself unread, and its price block post-dates the restaurant |
| Father Roger; L'Express May 1993 | **Medium** | Single indexed source |
| *La Cuisine gourmande des stars*, 1989 | **Medium** for existence; **Low** for attribution | Contested between the brothers |
| Christian's post-1998 life | **None** | No evidence |
| Martinez training (Duparc, then Willer) | **Medium-high** | Direct family testimony; no published corroboration. Consistent with Willer taking the Martinez kitchen in 1985 |
| Christian is the elder brother | **Medium-high** | Direct family testimony; consistent with his holding *chef de cuisine* over Philippe |
| Ducasse friendship | **None** | No evidence |
| Fusion primacy | **None** | No evidence |
| Celebrity/political clientele | **None** | **No published evidence whatsoever** |

---

## F. The one-sentence version

Zero of the eleven primary sources were retrieved across two independent retrieval attempts; the block was then worked around rather than accepted, which yielded a guide review whose subject is Christian himself and upgraded the television finding to a BnF *image animée* classification with Christian credited on conception; family testimony has since settled his birth order and his training under Duparc and Willer at the Martinez; and every remaining gap is closable by a human with a browser, a RetroNews login, and a day at the BnF.
