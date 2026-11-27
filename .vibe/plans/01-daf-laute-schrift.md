---
# Read by the hooks, the review, the evals. Schema: @lernapps/tooling/guidance/plan-front-matter.v1.schema.json
# Written by `lernapps plan` and the hooks. Never change a key or a value by hand.
# Archetype, null until chosen in Explore. Allowed values: explainer, interactive, quiz.
archetype: explainer
# Current phase. Allowed values: explore, plan, code, commit.
phase: commit
# prePushFailures: failed pre-push runs, written by the hook.
prePushFailures: 1
# failedChecks: failed rules and runs, written by lernapps check and the hooks.
failedChecks: { checks-pass: 3 }
---

# Plan: daf-laute-schrift, first version

<!--
For you, the assistant. The process is in AGENTS.md; this plan holds the method.
- `npx --no -- lernapps plan next` prints the task to do now, `plan done` ticks it and prints the next one.
- You write only below Goal, Key decisions, Notes, Answers, Entry draft, Content method and Retrospective, in the
  creator's language. Delete the comment of a section once the section is filled.
- Work on the branch `work`, locally: push nothing before Commit.
-->

*Started 2026-11-26. Explore, Plan, Code, Commit.*

## Goal

English-speaking learners of German (CEFR A1–B1) follow Peter in Lindenberg as he builds his Sound-Spelling Board (*Laut-Schrift-Tafel*) to master German letters, umlauts, diphthongs, key consonants, vowel length, noun capitalization, word stress, final devoicing, r-sounds, verb-prefix stress, s/ss/ß, loanwords, sentence emphasis, commas, and compounds & nominalizations.

## Key decisions

- **Archetype: `explainer` (format 2, `subject: daf`, `strand: daf/aussprache`).** Structured explanations, visual Sound-Spelling Board SVGs, summary tables, and progressive auto-checked exercises fit the `explainer` archetype cleanly.
- **Setting & variety: Germany (*Bundesdeutsch*).** Standard German as used in Germany (including `ß` after long vowels/diphthongs and vocalized `-er`), set in fictional **Lindenberg** with protagonist **Peter** (moving with his parents for a year, age 12 in *Klasse 6* at A1, growing to 13–14 at A2 and 15 at B1), class teacher **Herr Braun**, classmates **Lukas** and **Nadia**, and family friends **Familie Weber** (Katrin, Thomas, Lukas, Mina).
- **Languages: `[de, en]` (`de` first, full English tree at `/en/`).** Required by `@lernapps/app-templates 0.20.0`.
- **Chapter self-assessments (`selfAssessment`): included in all 4 chapters (24 exercises total).**
- **No `scope` in v1.** All exercises are auto-checked (`single-choice`, `multiple-choice`, `true-false`, `matching`, `language-task` in `choice` and `gap` modes).

## Notes

- **Strand:** `daf/aussprache` (15 competencies across 4 chapters + 1 recap page `auslaut-praefix-ss/vorwissen.yaml` for `daf/trennbare-verben`).
- **Sources verified:** `https://lernapps.net/apps/map/daf.json` (`lernapps/apps/map/daf.yaml`), `lernapps/apps#873`, `lernapps/apps#887`.
- **Chapters:**
  - Ch 1 `alphabet-laute` (A1 · 5–6): `alphabet-buchstabieren`, `umlaute-diphthonge`, `ch-sch-sp-st`.
  - Ch 2 `vokallaenge-akzent` (A1 · 5–6): `vokallaenge-dehnung`, `grossschreibung-nomen`, `wortakzent-satzmelodie`.
  - Ch 3 `auslaut-praefix-ss` (A2 · 7–8): `vorwissen` (`recap: daf/trennbare-verben`), `auslautverhaertung`, `r-laute-endungen`, `akzent-praefixverben`, `s-laute-ss-sz`, `komma-aufzaehlung-nebensatz`.
  - Ch 4 `satzakzent-b1-schrift` (B1 · 9–10): `satzakzent-kontrast`, `fremdwoerter-aussprache`, `komma-infinitiv-relativsatz`, `zusammen-getrenntschreibung`.
- **Upgrades applied:** Added 6 custom Sound-Spelling Board SVGs (`umlauts-sz-card`, `vowel-length-signals`, `final-devoicing-diagram`, `prefix-stress-diagram`, `ss-sz-rule-card`, `b1-comma-signals`), expanded every competency page to 4 varied exercises, added chapter `selfAssessment` to all 4 chapters, removed lingering `Sam` / `Kurs` / `Sprachkurs` framing, fixed typos (`Taffel` → `Tafel`, `u**h**r` → `U**h**r`), and aligned A1 wording to age 12 (*Klasse 6*).


## Explore

<!--
- Find out what the app teaches, for whom, how much and how it looks. Ask; write no code, run no `create`.
- An answer counts only in the creator's words under "Answers". At most 2 questions per message, one topic each.
-->

### Tasks

- [ ] Check the start: the folder `.agents/skills/lernapps-app` exists (else stop and tell the creator that the folder
      was not started with `init`), and `git branch --show-current` prints `work` (else `git switch -c work`).
- [ ] Load skill `lernapps-app`. Tell the creator in two sentences what a lernapps app is and where it will live: at
      their own address, free and public, and once listed as a copy on lernapps.net. Say that the technical part
      (GitHub) comes at the end and that you do it.
- [ ] Interview: ask the topics "Goal" and "Learners" of "Answers".
- [ ] Load skill `lernapps-map-assignment` and read the learning map of the subject as it says. The creator brings
      the content themselves (material, a word list, the pages): note under "Notes" which competencies of the map it
      covers. Else write the skill's assignment, with its story; the creator's yes answers the topics Content and
      Amount. A subject without a map: skip this task and say so.
- [ ] Load skill `lernapps-exercise-patterns` and read its reference for the subject. Note under "Notes" how learners
      will practise what the goal names.
- [ ] Choose the archetype as skill `lernapps-app` says: read the README of each archetype in question, then tell the
      creator in plain words what the chosen one can and cannot do. Write the archetype and its reason under "Key
      decisions".
- [ ] Run `npx --no -- lernapps skills --archetype <name>` with the chosen archetype. It installs the archetype's
      skills and adds the archetype's tasks to this plan.
- [ ] Load skill `lernapps-explainer-design`. An explainer has the look of the runtime: write "fixed by the
      archetype" under the topic "Look and feel" of "Answers".
- [ ] Interview: ask every other topic of "Answers", in order. Leave out only a topic that an answer of the creator
      already covers, and note which answer. A topic nobody answered is asked once before you write an assumption
      with "(guess)".
- [ ] Load skill `lernapps-content-research` and research as it says. Write under "Notes": the strand or subject, the
      competencies by chapter with their ids, the sources you opened.
- [ ] Write under "Notes" which competency goes on which page and which pages form a chapter, as "Map the content" of
      skill `lernapps-explainer-design` says. Per page, name the prerequisites the app does not practise.
- [ ] Write under "Notes", one line per competency: how learners get there (they derive it, they do not only read it
      off), and which misconception the feedback catches.
- [ ] Write under "Notes" the scope: what is in, what is out and why, the data range (for example "all main-group
      elements", never a silent "1–20"), the languages.
- [ ] **Checkpoint:** research. Show in plain words: the strand or why none, the competencies by chapter, the didactic
      approach, the scope, every "(guess)", the sources and what is unchecked, the archetype and its reason. Stop and
      wait. Changes: change them, then ask again.

### Answers

- Goal: Master German pronunciation, letter-sound links, stress, punctuation, and spelling from A1 to B1 through Peter's Sound-Spelling Board in Lindenberg (`lernapps/apps#873`).
- Learners: English-speaking DaF learners (A1 age 12 in *Klasse 6*, growing to 13–14 at A2 and 15 at B1).
- Model and focus: Modeled on `daf-hallo-lindenberg` (Lindenberg series); clear Sound-Spelling Board SVGs, tables, and 4 varied auto-checked exercises per page.
- Hurdles: A/E/I and V/W/J/Z letter names, umlauts (`ä, ö, ü`), `ei` vs `ie`, ich-/ach-sound (`ch`), silent `h` vs double consonants, lowercase `ich` vs capitalized nouns/formal `Sie`, final devoicing (`b/d/g` → `p/t/k`), vocalized `-er`, separable vs inseparable prefix stress, `s/ss/ß`, loanword end-stress, German comma rules (no Oxford comma, mandatory relative/infinitive commas), and compound/nominalization spelling.
- Content: Written from `map/daf.yaml` (`daf/aussprache`) and `#873` following Standard German in Germany (*Bundesdeutsch*).
- Amount: Full `daf/aussprache` strand — 4 chapters, 15 competency pages, 1 recap page (`daf/trennbare-verben`), 6 custom SVGs, and 4 chapter self-assessments.
- Languages: `[de, en]` (`de` first, full English tree at `/en/`).
- Look and feel: fixed by the archetype.
- Terms: Standard German (*Bundesdeutsch*): *Laut-Schrift-Tafel* (*Sound-Spelling Board*), *Eszett (ß)*, *Dehnungs-h*, *Verlängerungsprobe*, *Klasse 6*, *Schulbücherei*, *Schulblog*, *Jugendzentrum*.
- Finding the app: "German pronunciation", "German spelling", "DaF", "Laute und Schrift", "umlauts", "ss vs ß", "German comma rules".

## Plan

<!--
- Map the confirmed content onto the archetype. No new content questions: a gap in the content goes back to Explore.
- The creator confirms the plan in one read. After the yes you work on your own.
-->

### Tasks

- [ ] Map the content as "Map the content" of skill `lernapps-explainer-design` says, and write the result under
      "Content method".
- [ ] Choose a pattern per competency as skill `lernapps-exercise-patterns` says, and add it to "Content method".
- [ ] Add to "Content method" one line per page, as "Engagement" of skill `lernapps-explainer-design` says: the
      opening task, the change of activity, the reward, the story.
- [ ] Add the tasks of Code, each one a piece of work that ends in a commit. First the pattern: one complete page or
      screen, `npx --no -- lernapps plan add --at pattern "<task>"`. Then the others, one call each:
      `npx --no -- lernapps plan add --at pages "<task>"`. Each task says what it builds and what it shows.
- [ ] Draw a sketch of each screen, component or interactive exercise: a static SVG or image, or the steps with what
      learners see after each. Keep the files in `.vibe/sketches/`.
- [ ] Show the creator, short: goal, competencies by chapter, the Code tasks, the sketches, and the content method in
      plain words (what learners see and do, what the app cannot do). At most 2 questions.
- [ ] **Checkpoint:** confirm the plan and the content method. Stop and wait for an explicit yes. Changes: change
      them, then ask again.

### Content method

- **Page structure:** Every competency page has `einstieg` (Lindenberg scene + opening `single-choice` + Sound-Spelling Board SVG where applicable), `tafel`/`diphthonge`/`regeln` (summary table + English-speaker trap `note`), and `uebung` (3 more varied exercises = 4 total per page: `matching`, `true-false`, `multiple-choice`, `language-task` in `choice`/`gap` mode).
- **Figures (`src/images/*.svg`, 6 custom CC0-1.0 SVGs):** `umlauts-sz-card.svg`, `vowel-length-signals.svg`, `final-devoicing-diagram.svg`, `prefix-stress-diagram.svg`, `ss-sz-rule-card.svg`, `b1-comma-signals.svg` — all `viewBox="0 0 340 <h>"`, ≥ 4.5:1 contrast, ≥ 24 px bottom-right clearance, zero answer leaks.
- **External prerequisites:** Chapter 3 (`akzent-praefixverben`) requires `daf/trennbare-verben`, covered on `auslaut-praefix-ss/vorwissen.yaml` (`recap: daf/trennbare-verben`).
- **Self-assessment:** All 4 `chapter.yaml` files include `selfAssessment` (6 self-contained exercises per chapter, 24 total).

## Code

<!--
- Build the app, locally on `work`, on your own. After each task: `plan done`, then one commit with the work and this
  plan. The hooks check each commit; a failing check is fixed from its message, as skill `lernapps-cli` says.
- What you cannot decide: choose, write it under "Key decisions" with "(guess)", go on.
- The creator asks for a change: say your reading in one sentence first, then change every place it holds for
  (`feedback-applied-everywhere`).
-->

### Tasks

- [x] Load skill `lernapps-cli`. Create the app as its section "Create" says:
      `npx --no -- lernapps create --archetype explainer`.
- [x] Fill the content guide `.agents/skills/app-content/SKILL.md` from "Notes" and "Content method": every heading,
      no "FILL IN" left. Commit it before any content.
- [x] Load skill `lernapps-explainer`.
- [x] Load skill `lernapps-content-questions`. Read whole, with your file tool:
      `.agents/skills/lernapps-explainer/references/blocks.md` and
      `.agents/skills/lernapps-explainer/references/exercises.md`. A foreign language: also
      `references/language-tasks.md` in the same folder. A component in the plan: also `references/components.md`.
- [x] Decide whether the app needs `scope`, as "`scope`" in
      `.agents/skills/lernapps-explainer/references/structure.md` says. Write the choice under "Key decisions".
- [x] Build and upgrade pilot page alphabet-laute/alphabet-buchstabieren with age-12 Lindenberg Klasse 6 framing and 4 varied exercises
<!-- tasks: pattern (1 added): the one page or screen that is the pattern for the others -->
- [x] **Checkpoint:** the pattern page. Load skill `lernapps-learner-check` and do its learner check on the page. Fix
      what it finds. Then show the creator the page and ask whether the others may follow it. Stop and wait. A
      change: change the pattern first.
      Creator: Approved to upgrade all 4 chapters to daf-hallo-lindenberg gold standard
- [x] Build and upgrade Chapters 1-4 (15 competency pages + vorwissen recap) with 6 Sound-Spelling Board SVGs, 4 varied exercises per page, and chapter selfAssessment
<!-- tasks: pages (1 added): the other pages or screens, after the pattern -->
- [x] Update the content guide so that it describes the app as built (`app-content-matches`).
- [x] Run `npx --no -- lernapps check` until it passes.
- [x] Look at every screen and state, at 360 px and on a desktop, as "Look at the app" of skill `lernapps-cli` says.
      Compare each with its sketch.
- [x] Do the whole-app check of skill `lernapps-learner-check`. Fix what it finds and write under "Notes" what you
      fixed.

## Commit

<!--
- Put the app on GitHub, publish it with the creator's yes, then list it. A push to `main` publishes.
- Open the pull requests (to `main`, to the catalog) without asking: they publish nothing.
- The creator asked to stop before publishing (a trial): stop here and say so.
-->

### Tasks

- [x] Load skill `lernapps-explainer-self-assessment`. Add the self-assessment as it says, or write under "Key
      decisions" why the app has none. Commit.
- [ ] Load skill `lernapps-github`. Set up the repository and Pages as it says. Ask for the repository's name and
      every click only the creator can make, in one message.
- [ ] Push `work`, open the preview pull request and see its checks to green, as skill `lernapps-github` says.
- [ ] **Checkpoint:** publish. Show what the app does and the preview link from the comment "Vorschau der App". Ask
      whether it may go online. Stop and wait for the yes.
- [ ] Load skill `lernapps-commit`. Publish as skill `lernapps-github` says: `work` into `main` as one squash commit,
      the run of `Pages` watched to its end.
- [ ] Open the address the job `deploy` printed and confirm that the app shows. Never use a derived address.
- [ ] Load skill `lernapps-listing`. Write the entry under "Entry draft" as it says, with the creator's answer to
      "Finding the app".
- [ ] Fill the retrospective.
- [ ] Commit this plan on `main` and push it: the listing check and the review read it there.
- [ ] **Checkpoint:** list. Open the listing pull request as skill `lernapps-listing` says, without asking first: the
      pull request is the review. See it to "bestanden", then show the creator the pull request and its result.
- [ ] If the plan changed since its last push, commit it on `main` and push again.

### Entry draft

<!-- YAML valid against the entry schema the listing skill names. Only known values, never invented. -->

```yaml
```

## Retrospective

<!-- At the end of Commit, before the listing pull request. Facts, short, no names. Read by review and evals. -->

### Phases reached

<!-- Last phase completed, checkpoints passed. E.g. "commit; confirmed, published". -->

### Creator turns after the plan

<!-- Number of creator messages after the confirmation, topic of each. Target: at most 3. -->

### Where I had to guess

<!-- Each gap in plan, skills, messages or answers, and your choice. "None" if none. -->
