# NOTICE

Plutarch — perspective
Copyright (c) 2026 Ariel Lee

This product includes original authored work licensed under the MIT Licence
(see [`LICENSE`](LICENSE)). This notice records what the licence does and does
not cover, and what third-party material the repository relates to.

---

## 1. What the MIT licence covers

The licence covers **only the authored analysis in this repository**:

- `SKILL.md` — the embodiment artifact
- `references/frameworks.md` — the seven operations stated as formal rules
- `references/clusters/*.md` — the mapping of the 78 treatises, with boundary arguments
- `references/episodic.md` — the non-argumentative residue
- `references/provenance.md` — the honesty ledger
- `README.md`, `CHANGELOG.md`, and this notice

It makes **no claim** over Plutarch's works, over any translation or edition of
them, or over the contents of any corpus this repository points at.

## 2. Source text and its status

The underlying works are those of **Plutarch of Chaeronea (c. 46 – c. 120 AD)**,
whose writings are in the **public domain** worldwide by age.

The distillation was performed against an **English translation** of the
*Moralia*, principally the Loeb Classical Library volumes I–XIV. Modern
translations, editions, introductions, notes, apparatus, and digitisations of
public-domain works **may carry their own copyright**, held by their translators,
editors, or publishers. Nothing here grants any right in that material.

## 3. No substantial reproduction

**This repository reproduces no substantial portion of any source text.** It
contains original analysis — rules, mappings, measurements, and boundary
arguments — together with **locators** (`Vol · char-offset`) that point into a
corpus held elsewhere.

Where source wording appears, it is limited to short quotations used for
identification, criticism, and the verification of specific claims, in the
cluster files and in `references/provenance.md` §5. The `.gitignore` is written
to keep source corpora out of version control; they stay on the machine that
runs the distillation.

Nothing this skill generates is a quotation from Plutarch. The package is for
analysis, research, study, and ideation in a documented frame. It is **not** for
forged attribution.

## 4. Companion knowledge base

The corpus is held separately in
**[Plutarch-Thoughts](https://github.com/ariel-lee-1023/Plutarch-Thoughts)**
(`content/PT/`), which is a distinct repository under its own terms. Nothing in
this notice or in `LICENSE` extends to that repository or to the texts within
it, and this repository vendors none of its content.

## 5. Tooling and provenance

Built with **[persona-distiller](https://github.com/ariel-lee-1023/persona-distiller)**.
Measurements were produced with `style_metrics.py` from that toolkit
(stdlib-only). See `references/provenance.md` §7 for reproduction steps.

## 6. Trademarks

No trademark rights are granted by the MIT Licence. "Loeb Classical Library" and
any other names appearing in this repository are used descriptively, to identify
editions, and belong to their respective owners.
