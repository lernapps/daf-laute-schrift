---
name: app-content
description: Use for any content work in this app - researching, writing, extending, correcting or reviewing its competencies, chapters, pages, rounds, questions, exercises, figures, terms or sources. This app's own content decisions; they take precedence over the generic lernapps content skills. Load it before you change any content.
---

# Content guide of this app

## Curriculum

- **Subject & level:** German as a Foreign Language (`subject: daf`), strand `daf/aussprache`, spanning CEFR **A1** (learning map band `5-6`, Chapters 1–2), **A2** (`7-8`, Chapter 3), and **B1** (`9-10`, Chapter 4).
- **Orientation:** Learning map `https://lernapps.net/apps/map/daf.json` (canonical source `lernapps/apps/map/daf.yaml`, based on ZfA/KMK *Rahmenplan DaF*, Goethe-Institut / ÖSD / telc A1–B1, and BAMF) and build brief `lernapps/apps#873` (part of overview epic `lernapps/apps#887`).
- **Standard variety:** Standard German as used in Germany (*Bundesdeutsch*) only — including `ß` after long vowels and diphthongs (*Straße, Fußball, draußen*) and standard vocalized `-er` endings.
- **Languages:** `languages: [de, en]` (`de` first per `@lernapps/app-templates 0.20.0`, full English UI tree at `/en/`).

## Competencies

### Chapter 1: `alphabet-laute` — Alphabet, Umlauts and Key Consonants (A1 · 5–6)
1. `alphabet-buchstabieren` (*I can pronounce the German alphabet and spell out names and words clearly.*) → `src/alphabet-laute/alphabet-buchstabieren.yaml` (`buchstaben-e-i`, `buchstaben-zuordnen`, `alphabet-regeln-check`, `adresse-buchstabieren`)
2. `umlaute-diphthonge` (*I can pronounce and spell German umlauts (ä, ö, ü) and diphthongs (ei, eu/äu, au) accurately.*) → `src/alphabet-laute/umlaute-diphthonge.yaml` (`umlaut-lippen`, `ei-ie-regeln`, `diphthong-klang-zuordnen`, `diphthong-schreiben`)
3. `ch-sch-sp-st` (*I can pronounce the ich- and ach-sounds (ch), sch, initial sp/st, and z/tz reliably.*) → `src/alphabet-laute/ch-sch-sp-st.yaml` (`ch-einstieg`, `ach-laut-finden`, `konsonanten-klang`, `konsonanten-luecken`)

### Chapter 2: `vokallaenge-akzent` — Vowel Length, Word Stress and Capitalization (A1 · 5–6)
4. `vokallaenge-dehnung` (*I can hear, pronounce, and recognize spelling cues for long vowels (ie, silent h) and short vowels (double consonants).*) → `src/vokallaenge-akzent/vokallaenge-dehnung.yaml` (`stummes-h-erkennen`, `minimalpaare-laenge`, `vokallaenge-regeln-check`, `vokallaenge-luecken`)
5. `grossschreibung-nomen` (*I can capitalize sentence beginnings, all German nouns, and the formal pronoun Sie.*) → `src/vokallaenge-akzent/grossschreibung-nomen.yaml` (`ich-klein-regel`, `nomen-gross-schreiben`, `sie-vs-sie`, `nomen-tippen`)
6. `wortakzent-satzmelodie` (*I can stress the main syllable of German words and use falling or rising intonation in statements and questions.*) → `src/vokallaenge-akzent/wortakzent-satzmelodie.yaml` (`kompositum-akzent`, `satzmelodie-zuordnen`, `melodie-regeln-check`, `erste-silbe-betont`)

### Chapter 3: `auslaut-praefix-ss` — Devoicing, Prefix Stress, ss/ß and Basic Commas (A2 · 7–8)
- Recap page: `src/auslaut-praefix-ss/vorwissen.yaml` (`recap: daf/trennbare-verben` — *Separable prefix verbs*, `recap-trennbare-verben`).
7. `auslautverhaertung` (*I can pronounce final b, d, g as p, t, k (e.g. Tag, Kind, gelb) and still spell them correctly.*) → `src/auslaut-praefix-ss/auslautverhaertung.yaml` (`auslaut-klang-erkennen`, `verlaengerungsprobe-schreiben`, `auslaut-zuordnen`, `auslaut-tippen`)
8. `r-laute-endungen` (*I can pronounce German r-sounds and reduced unstressed endings (-er, -en, -el) naturally.*) → `src/auslaut-praefix-ss/r-laute-endungen.yaml` (`vokalisiertes-r-erkennen`, `endungen-natuerlich`, `r-regeln-check`, `vokalisiertes-er-finden`)
9. `akzent-praefixverben` (*I can stress separable verb prefixes (aufstehen, einkaufen) and leave inseparable prefixes (verstehen, beginnen) unstressed.*) → `src/auslaut-praefix-ss/akzent-praefixverben.yaml` (`uebersetzen-akzent`, `betonte-praefixe-finden`, `praefix-typ-zuordnen`, `praefix-satz-wahl`)
10. `s-laute-ss-sz` (*I can decide whether to write s, ss, or ß based on vowel length and voicing.*) → `src/auslaut-praefix-ss/s-laute-ss-sz.yaml` (`dass-vs-das`, `ss-oder-sz-waehlen`, `s-regeln-check`, `ss-sz-tippen`)
11. `komma-aufzaehlung-nebensatz` (*I can place commas in lists and before subordinate clauses introduced by weil, dass, wenn, or als.*) → `src/auslaut-praefix-ss/komma-aufzaehlung-nebensatz.yaml` (`komma-weil-und`, `komma-pflicht-erkennen`, `komma-regeln-a2-check`, `komma-setzen-a2`)

### Chapter 4: `satzakzent-b1-schrift` — Sentence Emphasis, Loanwords and B1 Spelling (B1 · 9–10)
12. `satzakzent-kontrast` (*I can shift sentence stress to highlight new information or express contrast in conversation.*) → `src/satzakzent-b1-schrift/satzakzent-kontrast.yaml` (`kontrast-korrektur`, `frage-fokus-zuordnen`, `satzakzent-regeln-check`, `kontrast-podcast`)
13. `fremdwoerter-aussprache` (*I can pronounce and stress common international loanwords in German (e.g. -tion, -ie, -ieren, -tät).*) → `src/satzakzent-b1-schrift/fremdwoerter-aussprache.yaml` (`tion-aussprache`, `fremdwoerter-akzent-sortieren`, `fremdwoerter-regeln-check`, `fremdwoerter-endungen`)
14. `komma-infinitiv-relativsatz` (*I can set commas accurately around relative clauses and infinitive clauses with um/ohne/statt … zu.*) → `src/satzakzent-b1-schrift/komma-infinitiv-relativsatz.yaml` (`eingeschobener-relativsatz`, `infinitiv-komma-pflicht`, `b1-komma-regeln-check`, `b1-komma-setzen`)
15. `zusammen-getrenntschreibung` (*I can write German compounds as single words and capitalize nominalized verbs and adjectives (das Lesen, alles Gute).*) → `src/satzakzent-b1-schrift/zusammen-getrenntschreibung.yaml` (`kompositum-richtig`, `nominalisierung-gross`, `zusammen-getrennt-zuordnen`, `nominalisierung-tippen`)

## Content structure

- **Story world (fixed across all pages):** **Peter**, an English-speaking student who moves to **Lindenberg** (central Germany, *Bundesdeutsch*) with his parents for a year and joins **Klasse 6** (age 12 at A1, growing to 13–14 at A2 and 15 at B1), with class teacher **Herr Braun**, classmates **Lukas** and **Nadia**, and family friends **Familie Weber** (Katrin, Thomas, Lukas, Mina). Recurring visual artifact: **Peter's Sound-Spelling Board** (*Peters Laut-Schrift-Tafel*).
- **Page flow (1 competency per page, max 350 reading words, max 4 consecutive text blocks):**
  1. `einstieg` (Opening): 1–2 sentence Lindenberg school or everyday scene + an immediate, approachable `single-choice` opening task + Sound-Spelling Board SVG figure where applicable.
  2. `tafel` / `diphthonge` / `regeln` (Reference): Compact summary table + one focused `note` highlighting the top English-speaker trap.
  3. `uebung` (Practice): 3 more varied exercises (4 total per competency page), progressing from recognition to active application (`matching`, `true-false`, `multiple-choice`, `language-task` in `choice` or `gap` mode).
- **Chapter self-assessment:** Each `chapter.yaml` defines `selfAssessment` with 6 self-contained exercises (2 pages of 3 exercises per chapter, 24 total across all 4 chapters).

## Terminology

- **Address to learners:** Informal *you* in English (`en`) and informal *du* in German (`de`) throughout.
- **Standard German in Germany (*Bundesdeutsch*) used:** *Brötchen*, *Fahrrad*, *Eszett (ß)*, *Dehnungs-h*, *Verlängerungsprobe*, *Schulbücherei*, *Schulblog*, *Jugendzentrum*.
- **Age-appropriate plain language:** At A1 (age 12, *Klasse 6*), explain sound concepts in plain everyday words (*long/stretched* vs. *short/snappy*, *front/back of the mouth*, *two vowels blending into one sound*) instead of unexplained linguistics jargon (*tense/lax*, *articulated*).
- **Avoided:** "host family / Gastfamilie", "exchange year", "Sprachkurs / language course", and Austrian/Swiss spelling variants (e.g. *Fussball* instead of *Fußball*).

## Exercise patterns

- **Pattern 1 — Situation opening (`single-choice`):** Short Lindenberg scene testing a classic English-speaker sound/spelling trap (e.g. `alphabet-buchstabieren`, `buchstaben-e-i`). Every option has a rule-based `info`.
- **Pattern 2 — Sound-to-spelling pairing (`matching`):** Match German letters, words, stress patterns, or sentence melodies to their rule/sound (e.g. `vokallaenge-dehnung`, `minimalpaare-laenge`).
- **Pattern 3 — Rule verification (`true-false` and `multiple-choice`):** Distinguish real German pronunciation/punctuation rules from English interference (e.g. `komma-aufzaehlung-nebensatz`, `komma-pflicht-erkennen`).
- **Pattern 4 — Targeted spelling choice (`language-task`, `mode: choice`):** `languages: { source: en, target: de }`, plain English `source`, German `[gap]` targets with diagnostic distractors (e.g. `s-laute-ss-sz`, `ss-oder-sz-waehlen`).
- **Pattern 5 — Active spelling production (`language-task`, `mode: gap`):** Learners type German words with `form: { case: hint | strict, punctuation: ok }` and rule-based `mistakes` catching predictable English-speaker errors (e.g. `auslautverhaertung`, `auslaut-tippen`).
- Every competency page has **4 varied exercises** (≤ 2 guessable choices, ≥ 2 active tasks); exercise combinations vary across pages (`explainer-interaction`, `explainer-page-variety`).

## Figures

- **Peter's Sound-Spelling Board SVGs (`src/images/*.svg`, 6 custom SVGs):**
  1. `umlauts-sz-card.svg` (`alphabet-laute/umlaute-diphthonge`) — visual card for `ä, ö, ü, ß` mouth tips.
  2. `vowel-length-signals.svg` (`vokallaenge-akzent/vokallaenge-dehnung`) — long (`ie`, silent `h`, double vowel) vs. short (double consonant, `ck`, `tz`) chart.
  3. `final-devoicing-diagram.svg` (`auslaut-praefix-ss/auslautverhaertung`) — `b→[p]`, `d→[t]`, `g→[k]` and extension test diagram.
  4. `prefix-stress-diagram.svg` (`auslaut-praefix-ss/akzent-praefixverben`) — separable prefix stress vs. inseparable stem stress diagram.
  5. `ss-sz-rule-card.svg` (`auslaut-praefix-ss/s-laute-ss-sz`) — decision card for `s` vs. `ss` vs. `ß`.
  6. `b1-comma-signals.svg` (`satzakzent-b1-schrift/komma-infinitiv-relativsatz`) — B1 comma brackets for embedded relative clauses and infinitive clauses.
- **Conventions:** Self-drawn inline SVGs, `viewBox="0 0 340 <h>"` (clean at 360 px), `source: { de: "Eigene Zeichnung", en: "Own drawing" }`, `licence: CC0-1.0`, ≥ 4.5:1 contrast (`#f8fafc` card, `#0f172a` slate text, `#dbeafe`/`#1e3a8a`, `#fef3c7`/`#78350f`, `#dcfce7`/`#14532d`, `#ffe4e6`/`#9f1239`), ≥ 24 px clear space at bottom-right for the runtime's `© CC0-1.0` badge, and never leaking exercise answers (`explainer-figure-hides-answer`).

## Sources

- `https://lernapps.net/apps/map/daf.json` (canonical `lernapps/apps/map/daf.yaml`, strand `daf/aussprache`) — verified.
- `lernapps/apps#887` (DaF explainer overview) and `lernapps/apps#873` (build brief) — verified.
- No private creator material is committed.

## Adding a chapter or round

1. Check `https://lernapps.net/apps/map/daf.json` for competency ids and `requires`.
2. Create `src/<chapter-id>/chapter.yaml` and one YAML file per competency (plus one compact `recap` page first if any external prerequisite is needed).
3. Register `<chapter-id>` in `src/app.yaml` (`chapters`).
4. Follow the 4-exercise pattern and Sound-Spelling Board SVG conventions above, add `selfAssessment` to `chapter.yaml`, and update this content guide.
5. Run `npx vp check --fix`, `npx vp build`, and `npx --no -- lernapps check`, then commit on `work`.

## Rules learned from mistakes

- Protagonist name must always be **Peter** (never "Sam" — removed lingering `Sam` examples from `s-laute-ss-sz` and `satzakzent-kontrast`).
- Keep Peter's premise consistent across A1–B1: he moves to Lindenberg **with his parents** and attends **Klasse 6** (age 12 at A1, growing to 13–14 at A2 and 15 at B1) — never use "host family", "Sprachkurs / language course", or adult registration framing.
- Avoid inline backticks in YAML prose; use bold (`**...**`) or italics (`*...*`) instead.
- Leave at least 24 px of empty space at the bottom-right of every `src/images/*.svg` so the runtime's `© CC0-1.0` badge never overlaps text at 360 px.
- Reference figures with `image: images/<file>.svg` (relative to `src/`, not `../images/`).
