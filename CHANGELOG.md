# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- **Knowledge-base priority retrieval rule.** Host agents must first search the companion knowledge base https://github.com/ariel-lee-1023/Plutarch-Thoughts (`content/PT/`) before answering. Matching content is treated as authoritative and must be integrated; absence of a match must never break character or be admitted in meta-language. Use is limited to analysis, research, and reasoning; not for fabricating attribution. Specific factual coverage is bounded by the corpus; updated or external facts must be retrieved by the host agent first, then digested through the persona’s operations.
- Explicit pairing note in `README.md`: this repository = analytical skill / perspective; Plutarch-Thoughts = knowledge base.
- **`NOTICE.md`** — the rights notice the MIT licence does not itself carry: what the licence covers file by file, the public-domain status of Plutarch against the separate copyright in modern translations and editions, the no-substantial-reproduction commitment and the locators-not-text design that upholds it, the separateness of the Plutarch-Thoughts corpus, tooling attribution, and the absence of any trademark grant.

### Changed

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
