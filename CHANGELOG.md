# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- **The seven cluster modules extended to a computed budget.** They had been sized by hand, which is
  how a package ships at a fraction of the depth its own spec asked for without anything catching it.
  Each is now sized with persona-distiller's `scripts/cluster_budget.py` — from the constructs, moves,
  entry-situations and retained evidence routed to it, plus a fence per sibling module and a damped
  corpus-mass term — and written to that number. Budgets 2,963–3,976; realised sizes land within
  −0.7% / +3.9%, inside the script's own calibration error. No cluster fell below the 1,800 floor and
  none saturated the caps, so every operation keeps its module and none is carrying two registers.
  The `clusters/` package went 19,266 → 24,953 tokens; worst-case runtime load is 20,072.
- **The specimens that filled the space, all from members earlier passes had listed but never
  worked.** *Stoicos absurdiora poetis dicere*'s fiction-licence baseline — measure the doctrine
  against what we let a poet make up, and the ship with A PROSPEROUS VOYAGE on her hull that founders
  anyway. The quotation rule stated outright at the head of *Non posse suaviter vivi*, and *Adversus
  Colotem* naming the violation it does not cover: an opponent can quote accurately and still cheat,
  by removing what made the words follow. *De vitioso pudore* as the continuum case, where identical
  conduct is separated by whether the man is grieved or pleased at his own fault. *De profectibus*'
  reduction of the all-or-nothing account — a criterion that can only fire at the endpoint is not a
  criterion. *Amatorius*' cross-cut advocacy, where the inveterate lover is assigned the case against
  love. *De fortuna Romanorum* giving each limb a standing accusation so that winning is a defence
  and not a prize. *Platonicae quaestiones* running the *Is it because… Or has Plato figuratively…*
  chain on a text. *De animae procreatione* refusing a rival key on capacity rather than piety.
  *Comparatio Aristophanis et Menandri*'s two-audience test, set up before either poet is measured.
  *Quaestiones naturales* raising the bar in the physical branch — a candidate with no phenomenon
  behind it does not get listed. *De Pythiae oraculis* conceding the badness of the god's own verse
  before hunting a cause.
- **`references/voice.md` — the second standing module, and the one the package was missing.**
  `frameworks.md` said what he thinks with; nothing said how he sounds at length. The core's *How I
  sound* is capped at roughly a fifth of the artifact by design — enough to be a fingerprint, not
  enough to write a page — so the rest of the expressive system now has a home: favoured and
  **avoided** constructions as rules to self, modulation rules keyed trigger → shift, a register
  range, the lexical fingerprint, attested opening and closing moves, the measured baseline, and six
  anti-drift pairs. Every number in it comes from an actual `style_metrics.py` run over the 69
  argumentative treatises; nothing is estimated.
- **The literary-form axis.** Measuring generated prose against `voice.md` exposed a fault in how the
  corpus had been characterised: expression variance is driven harder by **form** — bare antiquarian
  query, monologic treatise, staged dialogue, letter of address — than by the seven operations. First
  person spans 3.2% → 30.2% across forms against 12.3% → 26.4% across operations; question share
  spans 6.8% → 41.0% against 1.6% → 14.8%. An operation-level average therefore blends registers that
  never co-occur: the cause-hunting cluster's high first-person figure belongs to the dialogues it
  contains, not to the *Aetia*, which are almost authorless. `voice.md` now leads with the form
  table, demotes the operation table to a modifier, and carries single-text anchors so a short
  passage is compared against one named treatise rather than an average.
- **Worked specimens in all seven cluster files.** Each module previously stopped at a table of
  texts and its boundary arguments — a correct mapping with nothing in it to reason *from*. Each now
  carries the operation running end to end on named material: the four-candidate chain of the first
  *Aetia Romana* question with the ranking explained; *De defectu*'s depopulation argument and why
  the cause that explains the pattern of silence outranks the ones that explain silence; the eight
  probes of *De invidia et odio* laid out side by side; the two rival keys *De Iside* rejects by name
  and the sentence that does it; *Mulierum virtutes*' preface, where the juxtaposition rule is stated
  before it is used; the judicial apparatus of the staged debates and the umpire who declines to
  vote; the axiom at the head of *De Stoicorum repugnantiis* and the three consistency tests worked
  against it; the training schedule in *De curiositate* and the restraint of the letter to his wife.
- **Per-cluster register data.** Each cluster file now ends with what that operation is measured to
  sound like — question share, hedge and booster rates, person reference, exempla density — with the
  within-volume control where one exists. The strongest single piece of expression evidence in the
  distillation surfaced here: inside Volume XIII, one translator throughout, the two decoding texts
  run 1.2% and 2.9% interrogative against the two refutations at 13.3% and 17.6%.
- **Knowledge-base priority retrieval rule.** Host agents must first search the companion knowledge base https://github.com/ariel-lee-1023/Plutarch-Thoughts (`content/PT/`) before answering. Matching content is treated as authoritative and must be integrated; absence of a match must never break character or be admitted in meta-language. Use is limited to analysis, research, and reasoning; not for fabricating attribution. Specific factual coverage is bounded by the corpus; updated or external facts must be retrieved by the host agent first, then digested through the persona’s operations.
- Explicit pairing note in `README.md`: this repository = analytical skill / perspective; Plutarch-Thoughts = knowledge base.
- **`NOTICE.md`** — the rights notice the MIT licence does not itself carry: what the licence covers file by file, the public-domain status of Plutarch against the separate copyright in modern translations and editions, the no-substantial-reproduction commitment and the locators-not-text design that upholds it, the separateness of the Plutarch-Thoughts corpus, tooling attribution, and the absence of any trademark grant.

### Changed

- **`SKILL.md`'s loading block routes to `voice.md`** before any sustained prose, and to the cluster
  files for worked instances *and* register. Nothing else in the core was reopened: the refusals, the
  operative moves, the voice sections, and all 78 cluster assignments are unchanged.
- **`references/provenance.md` gained §7**, the third-pass record: the budget inputs and how each was
  counted (including the one stated adaptation — `frameworks.md` has no cluster column, and failure
  modes are excluded from `n_apparatus` because counting them raised a spurious re-cut flag), the
  supply/realised table, the runtime-load line, and three findings that *qualify* earlier verdicts
  rather than confirming them: the *Epitome* is partly report and not performance, which sharpens
  rather than softens the flag on that filing; the *Aristophanes/Menander* comparison survives only
  in reported speech and must not be used as a register sample; and "let a guest's poorer answer
  stand" gained a second text but not a second cluster, so its caveat stands. §7 *Reproducing this*
  renumbered to §8.
- **`references/provenance.md` extended** with §4a (the re-measurement at corpus revision `7df2e10`
  and how it reconciles with the first pass — same directions, ±6% on rates), §4b (seven new
  findings with their controls and their status), the second-pass style-match result, four further
  trust caveats, and a reproduction procedure specific enough to re-derive every number from the
  offsets this repository stores.
- **Style-match test re-run against the core + `voice.md` pair** and reported as **not passed but
  diagnosed** — 60% → 50% mean deviation across two rounds, then re-scored against single-text
  comparators, which is what exposed the form axis above. The loop was stopped deliberately: at
  600-word samples the per-1k rates are moved by a handful of tokens, so further iteration would tune
  word counts rather than prose.
- **Repository layout documented in full.** The tree in `README.md` previously showed only `SKILL.md` and `references/`; it now covers the whole repository, including `CHANGELOG.md`, `LICENSE`, `NOTICE.md`, `README.md`, and `.gitignore`.
- The `README.md` licence section now points at `NOTICE.md` for the full rights scope.
- Expanded the “Loading depth (host-agent note)” section in `SKILL.md` to enforce the knowledge-base search as the highest-priority operation and to separate frame from facts.
- Corresponding documentation added under a new “Knowledge-base priority & factual cutoff” section in `README.md`.

### Planned

- **A blinded projection test.** The projection check in `references/provenance.md` §5 was run but
  not blinded, and its score is explicitly not offered as a fidelity number. A valid test needs a
  second party predicting from `SKILL.md` alone.
- **Fold-in of the *Parallel Lives*.** The source corpus carries only the *Moralia*, which leaves the
  frame without the biographer and leaves operation 5 (exemplary / comparative reasoning) resting on
  5 texts. Folding in the *Lives* would re-weight that operation substantially and would be an
  incremental re-curation, not a rewrite.

## [1.1.0] — 2026-07-28

Expression habits distilled and measured, not just thought patterns; the honesty ledger added.

### Added

- **`references/provenance.md`** — the honesty ledger the pipeline specifies. Traces every core
  element to its source treatises and clusters, records the measured expression features, reports
  all fidelity results with their caveats, and lists where the persona should be trusted less.
- **Measured expression features.** `style_metrics.py` was run over the whole corpus, over each of
  the eight clusters, over each of the fourteen volumes, and per treatise, using a slicing of all 78
  texts at the detected boundaries.
- **A translator control.** The corpus is a composite English translation — per-volume mean sentence
  length ranges 29.8–49.6 words, a spread as wide as anything separating the operations, and the
  clusters are not volume-independent. Per-cluster contrasts were therefore re-tested *within*
  single volumes, and only findings that survived became voice rules. Sentence rhythm and
  punctuation were measured and **discarded** as translator artifacts.

### Changed

- **`SKILL.md` — *How I sound* rewritten and roughly doubled**, from impressionistic description to
  measured rules carrying their modulation: the interrogative as the mode of address to a datum and
  where it stops; second person rising in counsel and collapsing in refutation; first person steady
  everywhere except deed-marshalling; flat assertion doubling when look-alikes are separated while
  hedging continues underneath; exempla density at two or three named instances per page; and the
  absence of any abstract-systemic vocabulary, which is the strongest translation-robust finding in
  the corpus.
- Body grew to ≈3,900 tokens, still well inside the 5,000 budget and still front-loaded.

### Fixed

- Three defects in the expression rules, each found by a failing style-match round and corrected
  before the next: long sentences were under-specified; "the qualifiers drop away" overstated the
  effect and produced samples with zero hedging against an actual rate of 6.26/1k; and the missing
  exempla-density rule had left generated prose at 51% first-person reference against an actual 23%.

## [1.0.0] — 2026-07-27

First release. The complete 78-treatise *Moralia* canon mapped to seven cognitive operations, plus
the embodiment artifact that states those operations in voice.

### Added

- **`SKILL.md`** — the core embodiment artifact. States the seven operations as first-person
  operative moves so that stances are predictable from them, and carries eight cost-bearing refusals
  in priority position: superstition worse than atheism (held while serving Apollo), the oracle's
  decline conceded rather than defended, beasts reason and the table therefore wants a defence,
  virtue one and the same in a woman, no rescuing a poet by allegory, no paraphrasing an opponent
  where the wording carries the contradiction, Herodotus' charm buying him no indulgence, and Greeks
  told whose boots are over their heads. Body ~2,700 tokens against a 5,000 budget, front-loaded so
  the refusals survive compaction.
- **`references/frameworks.md`** — the seven operations as formal rules, each given as object, move,
  termination condition, and failure modes, followed by five combination rules governing texts that
  run more than one. Contains no treatise name and no locator.
- **`references/clusters/`** — seven files, one per operation, holding the instance mappings:
  `aetiological.md` (10 texts), `dialectical.md` (13), `criterial.md` (6), `allegorical.md` (4),
  `exemplary.md` (5), `refutative.md` (9), `practical-syllogism.md` (22).
- **`references/episodic.md`** — the 9 catalog, reference, and compilation texts that run no
  operation. Recorded as a verdict rather than a leftover: a text that reports cannot be wrong in the
  way any of the seven operations makes available, and admitting such texts would dilute every
  pillar that received one.
- **Boundary notes in every cluster file**, arguing the contested assignments and naming the weakest
  fits rather than concealing them — the split of the *fortune-or-virtue* pair across operations 2
  and 5, the retention of *Mulierum virtutes* in a pillar despite its resemblance to the anecdote
  collections, *De facie in orbe lunae* as cause-hunting despite heavy anti-Stoic polemic, and
  *De esu carnium* flagged as the likeliest place the mapping is wrong.
- **`README.md`**, **`LICENSE`** (MIT), **`.gitignore`**, and this changelog.

### Method

- **Assignment rule.** The governing operation is the one that fixes what would count as the text
  having *failed*. This replaces subject matter and surface form as the sorting criterion, and it is
  what decides the contested cases — a disjunctive title does not make a text dialectical, and an
  anecdote collection with a stated thesis is not a collection.
- **Boundary detection.** The source Markdown has no heading structure, since PDF conversion
  flattened treatise titles inline. All 78 boundaries were recovered by title-string detection and
  required to increase monotonically within each volume. Eight titles use wording that differs from
  the Loeb standard in this composite translation and were resolved individually.
- **Verification.** The mapping was machine-checked as a strict partition of the canon — 78 assigned,
  no duplicates, no omissions — with every locator re-checked against the detected boundaries, and
  `frameworks.md` checked to contain no treatise name or volume reference.

### Known limitations

- Scope is the *Moralia* alone; see **Unreleased → Planned**.
- Operation 5 rests on 5 texts and is the thinnest pillar in the scheme.
- `references/episodic.md` excludes two texts whose authenticity is independently doubted
  (*Parallela minora*, *Placita philosophorum*). The residue verdict does not depend on that doubt,
  and would stand if both were genuine.

[Unreleased]: https://github.com/ariel-lee-1023/Plutarch-perspective/compare/v1.1.0...HEAD
[1.1.0]: https://github.com/ariel-lee-1023/Plutarch-perspective/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/ariel-lee-1023/Plutarch-perspective/releases/tag/v1.0.0
