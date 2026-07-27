# Plutarch — perspective

A **perspective skill**: Plutarch of Chaeronea's *Moralia* distilled into a reusable thinking frame
that an agent can load and reason *in*, rather than a summary of what he thought.

The distinctive claim of this package is architectural. Plutarch's 78 essays are not sorted by
subject — ethics here, religion there, physics somewhere else — but by the **cognitive operation**
each one runs. Seven operations account for 69 of the 78; the remaining 9 report rather than reason
and are held separately, because forcing them into a pillar would empty the pillars of meaning.

```
SKILL.md                       the embodiment artifact — the operations in his voice
references/
├── frameworks.md              the same seven operations as formal rules
├── clusters/                  the 78 texts, mapped, one file per operation
│   ├── aetiological.md            10   cause-hunting
│   ├── dialectical.md             13   aporia
│   ├── criterial.md                6   differential diagnosis
│   ├── allegorical.md              4   symbolic decoding
│   ├── exemplary.md                5   comparative reasoning
│   ├── refutative.md               9   consistency-testing
│   └── practical-syllogism.md     22   maxim-to-case
└── episodic.md                     9   the non-argumentative residue
```

## The seven operations

Each is defined in [`references/frameworks.md`](references/frameworks.md) by its **object** (what
invites it), **move** (the procedure), **termination condition** (what counts as finished), and
**failure modes**. The termination conditions carry most of the weight — they differ sharply, and
they are what makes the scheme decidable rather than impressionistic.

| # | Operation | Finishes when… |
|---|---|---|
| 1 | Aetiological / antiquarian cause-hunting | the candidate causes are **ranked** — not when one is proved |
| 2 | Dialectical problem-posing (aporia) | both limbs stand at full strength; **staying open is a finished answer** |
| 3 | Criterial / differential diagnosis | the marks yield a test usable **before** the injury |
| 4 | Allegorical / symbolic decoding | the doctrine stands without the myth **and** the myth's details are all spent |
| 5 | Exemplary / comparative reasoning | particulars a hostile reader would grant carry a judgment trimmed to their width |
| 6 | Refutative / consistency-testing | the rival must **drop one of two things he asserts** |
| 7 | Practical syllogism (maxim-to-case) | the addressee could act differently tomorrow without further deliberation |

## Why the split between `SKILL.md` and `references/`

They describe the same seven operations from opposite sides, and neither does the other's job.

- **`SKILL.md`** states them as first-person operative moves, so they *predict stances*. It is
  written in voice front to back, with no hedging, provenance, or meta language — that is deliberate,
  since disclaimers pull a reader out of a voice and destroy identification.
- **`references/frameworks.md`** states them as rules, so they *classify reasoning*. It names no
  treatise and carries no locator; instances live in `clusters/` and nowhere else.

Load `SKILL.md` to think as him. Load `frameworks.md` to judge whether a piece of reasoning — his or
anyone's — is doing what it claims.

## Using it

Point an agent at `SKILL.md`. Its closing block tells the host when to pull deeper modules: a single
cluster file for worked instances of one move, `frameworks.md` when the task is to classify rather
than perform, `episodic.md` only to check whether a text falls outside the scheme.

Each cluster file carries **boundary notes** arguing the contested assignments — why the
*fortune-or-virtue* pair is split across two operations, why *Mulierum virtutes* is not filed with
the anecdote collections it resembles, why *De facie in orbe lunae* is cause-hunting rather than
refutation despite the polemic in it. Those notes are the honest part of the mapping; read them
before relying on any single assignment.

## Corpus and locators

Distilled from [Plutarch-Thoughts](https://github.com/ariel-lee-1023/Plutarch-Thoughts) —
Loeb *Moralia* volumes I–XIV, the complete 78-treatise canon.

The corpus Markdown has no heading structure (PDF conversion flattened titles inline), so treatise
boundaries were recovered by title-string detection and required to increase monotonically within
each volume. Locators in the cluster files read `Vol · char-offset` and point at the title string
where each treatise begins in `content/PT/Moralia/MORALIA-Volume_<N>.md`. All 78 were verified:
no duplicates, no omissions, no locator mismatches.

## Scope and limits

- **The *Moralia* only.** The *Parallel Lives* were not in the corpus, so the frame carries none of
  the biographer — the register most readers associate with Plutarch. Adding the *Lives* would be a
  fold-in, not a rewrite, and would weight operation 5 far more heavily than 5 texts.
- **No `provenance.md` yet.** The ledger mapping each core element to its sources with fidelity
  scores is not written. Voice-purity and cost-presence gates were run and pass; held-out projection
  and style-match tests were not.
- **A thinking tool, not a ventriloquist.** This is for analysis, study, and ideation in a documented
  frame. It is not for forged attribution, and nothing it generates is a quotation.

## Provenance and rights

Plutarch (c. 46–120 AD) is in the public domain. Modern translations, editions, and PDF sources may
carry their own copyright.

**This repository reproduces no substantial portion of any source text.** It contains original
analysis — rules, mappings, and boundary arguments — plus locators pointing into a corpus held
elsewhere. The `.gitignore` is written to keep it that way; source corpora stay on the machine that
runs the distillation.

Built with [persona-distiller](https://github.com/ariel-lee-1023/persona-distiller).

## Licence

[MIT](LICENSE) © 2026 Ariel Lee. Covers the authored analysis in this repository; it makes no claim
over Plutarch's works or over any translation.
