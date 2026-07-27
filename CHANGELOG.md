# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- **Knowledge-base priority retrieval rule.** Host agents must first search the companion knowledge base https://github.com/ariel-lee-1023/Plutarch-Thoughts (`content/PT/`) before answering. Matching content is treated as authoritative and must be integrated; absence of a match must never break character or be admitted in meta-language. Use is limited to analysis, research, and reasoning; not for fabricating attribution. Specific factual coverage is bounded by the corpus; updated or external facts must be retrieved by the host agent first, then digested through the persona’s operations.
- Explicit pairing note in `README.md`: this repository = analytical skill / perspective; Plutarch-Thoughts = knowledge base.

### Changed

- Expanded the “Loading depth (host-agent note)” section in `SKILL.md` to enforce the knowledge-base search as the highest-priority operation and to separate frame from facts.
- Corresponding documentation added under a new “Knowledge-base priority & factual cutoff” section in `README.md`.

### Planned

- **`references/provenance.md`** — the honesty ledger mapping each core element to its source
  treatises and clusters, with projection scores and cost-gate status. Without it the package is
  usable but not fully auditable; it is the one artifact the distillation pipeline specifies that
  this release does not ship.
- **Held-out projection and style-match verification.** The voice-purity and cost-presence gates
  were run before assembly and pass. The two statistical fidelity tests were not run, so no scores
  are claimed anywhere in the package.
- **Fold-in of the *Parallel Lives*.** The source corpus carries only the *Moralia*, which leaves the
  frame without the biographer and leaves operation 5 (exemplary / comparative reasoning) resting on
  5 texts. Folding in the *Lives* would re-weight that operation substantially and would be an
  incremental re-curation, not a rewrite.

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

[Unreleased]: https://github.com/ariel-lee-1023/Plutarch-perspective/compare/v1.0.0...HEAD
[1.0.0]: https://github.com/ariel-lee-1023/Plutarch-perspective/releases/tag/v1.0.0
