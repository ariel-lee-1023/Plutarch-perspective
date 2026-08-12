# Provenance — the honesty ledger

Everything the core `SKILL.md` is not allowed to contain: where each element came from, what was
measured, what was tested, what failed, and where the persona should be trusted less.

The core is written in voice with no hedging by design. That is a placement decision, not a
suppression: the caveats all live here, and this file is meant to be read by anyone deciding how
much weight the persona can carry.

---

## 1. The confound that governs everything below

**The corpus is an English translation, and a composite of at least two translators.** Volumes I–XII
read as modern Loeb prose; Volume XIII and parts of XIV carry archaic forms (*hath*, *doth*,
*Pinder's Caeneus hath been taken to task*) from an older translation lineage. Measured per volume,
mean sentence length ranges **29.8 → 49.6 words** and the hedge:booster ratio **1.20 → 3.44** — a
spread as wide as anything separating the seven operations.

Consequences, applied throughout this file:

| Feature class | Survives translation? | Weight given |
|---|---|---|
| Interrogative density (question rate) | **Yes** — sentence *type* is preserved | High |
| Person reference (I / you / he) | **Yes** — grammatical person is preserved | High |
| Conceptual vocabulary present/absent | **Yes** — what he has words *for* | High |
| Exempla density (named man + act) | **Yes** — content, not syntax | High |
| Hedge / booster rates | **Partly** — lexical choice, translator-influenced | Medium |
| Sentence length, punctuation rhythm, lexical diversity | **No** — these are the translators' | Low / discarded |

Every expression rule in the core's *How I sound* is drawn from the high- and medium-weight rows.
The low-weight rows were measured, reported here, and deliberately **not** turned into voice rules,
except for the single global claim that very short and very long sentences sit adjacent — which
rests on the corpus-wide spread (p10 = 12 words, p90 = 74) rather than on any per-cluster contrast.

Clusters are also **not volume-independent** — six of nine refutative texts sit in Volumes XIII–XIV —
so per-cluster differences were re-tested *within* single volumes, where the translator is held
constant. Only findings that survived that control were promoted to voice rules. See §4.

---

## 2. Corpus and coverage

| | |
|---|---|
| Source | [Plutarch-Thoughts](https://github.com/ariel-lee-1023/Plutarch-Thoughts), `content/PT/Moralia/` |
| Extent | Loeb *Moralia* volumes I–XIV — the complete 78-treatise canon |
| Size | 4,401,331 chars · 779,742 words · 19,575 sentences |
| Attribution | **Firsthand** throughout (Plutarch's own works in translation); no secondhand or commentary material |
| Segmentation | 78 treatises, boundaries recovered by title-string detection, monotonic within each volume, machine-verified — no duplicates, no omissions |
| **Not covered** | **The *Parallel Lives*.** `content/PT/Parallel-Lives/` contains only a `.gitkeep`. |

Coverage by operation (words, and share of the argumentative corpus):

| Cluster | Texts | Words | Share | Density |
|---|---|---|---|---|
| aetiological | 10 | 201,959 | 25.9% | thickest — Table-Talk alone is 430K chars |
| practical-syllogism | 22 | 168,397 | 21.5% | thickest by text count |
| episodic (residue) | 9 | 100,940 | 13.0% | excluded from style measurement |
| refutative | 9 | 96,796 | 12.4% | |
| dialectical | 13 | 84,533 | 10.8% | |
| allegorical | 4 | 46,140 | 6.0% | thin |
| criterial | 6 | 43,654 | 5.6% | thin but high-signal |
| **exemplary** | **5** | **37,323** | **4.8%** | **thinnest — see §6** |

Dialogue-vs-monologue: substantial dialogue (Table-Talk, *Amatorius*, *De E*, *De defectu*,
*De genio*, *De sera*, *De sollertia*), so the interactional pass was run at full weight rather than
down-weighted as it would be for a monologic corpus.

---

## 3. Core element ledger

Each element of `SKILL.md` traced to the treatises that evidence it. **Cost** column: whether the
element is an attested incentive-vs-characteristic divergence, and whether it reached the core.

### What I will not concede — the cost-bearing refusals

| Element | Sources | Clusters | Convenient move | Attested move | Cost | In core |
|---|---|---|---|---|---|---|
| Superstition worse than atheism | 14 *De superstitione* | criterial | A Delphic priest defends piety of every kind | Ranks superstition **below** atheism as the graver error | **High** | ✅ |
| The oracle has declined | 28 *De Pythiae oraculis*, 29 *De defectu* | aetiological | Defend the institution he serves | Concedes the decline and hunts its cause; entertains depopulation | **High** | ✅ |
| Beasts reason | 66 *De sollertia*, 67 *Gryllus*, 68 *De esu carnium* | dialectical, exemplary, refutative | Accept Stoic orthodoxy that beasts are irrational | Argues they deliberate and hold virtues untaught; draws the dietary consequence | **High** | ✅ |
| Virtue one and the same in a woman | 19 *Mulierum virtutes*, 12 *Coniugalia*, 50 *Amatorius* | exemplary, practical, dialectical | Praise women in a separate and lesser register | States the identity thesis in the preface and makes the deeds carry it | **High** | ✅ |
| No rescuing a poet by allegory | 2 *De audiendis poetis* | practical | Use the available Stoic escape hatch for immoral passages | Declines allegoresis; teaches the young reader to see and judge instead | **High** | ✅ |
| No paraphrasing an opponent | 72 *De Stoicorum repugnantiis*, 74 *De comm. notitiis* | refutative | Summarise the rival into a weaker form | Quotes at length where the contradiction depends on wording | **High** | ✅ |
| Charm buys a historian nothing | 60 *De Herodoti malignitate* | refutative | Leave the canonical historian alone | Goes through him city by city; separates evidential failure from internal conflict | **High** | ✅ |
| Whose boots are overhead | 55 *Praecepta gerendae reipublicae* | practical | Flatter Greek civic pride | Tells Greek officials they govern under supervision | **High** | ✅ |

**Cost gate: 8 divergences enumerated, 8 slated for core, 8 present in the assembled core, 0 logged
out, 0 missing unlogged. Presence assertion: PASS.**

### How I read a question — the projectible regularities

| Element | Core section | Sources (representative) | Clusters | Note |
|---|---|---|---|---|
| Rank causes, don't settle | How I read a question | 20, 21, 62, 49, 29 | aetiological | ≥2 independent clusters; the §1 termination condition |
| Build both limbs, allow openness | " | 23, 50, 66, 69 | dialectical | Openness is structural in 23 and 66 |
| Work by sign, not definition | " | 4, 5, 42, 14 | criterial | The cheapness criterion is stated in 4 |
| Decode to doctrine, spend every detail | " | 26, 27, 70 | allegorical | Rival keys rejected by name in 26 |
| Pair particulars to control the inference | " | 19, 24, 59 | exemplary | Thin — 5 texts; see §6 |
| Set a rival against himself | " | 72, 74, 75, 76, 77 | refutative | Internal / performative / preanalytic tests all attested |
| Grant the maxim, spend on the descent | " | 55, 12, 1, 32 | practical | Availability constraint explicit in 32 and 41 |

### How I move in an exchange

| Element | Sources | Clusters | Note |
|---|---|---|---|
| Give the last and best answer to another | 27 (Ammonius), 46, 49 | allegorical, aetiological | Interactional; dialogue-attested |
| Restate the weak case more strongly first | 50, 66 | dialectical | The §2 requirement, performed |
| Decline the verdict, hand over ranked causes | 20, 21, 64 | aetiological | Reluctance presented as the answer, not as modesty |
| Let a guest's poorer answer stand | 49 | aetiological | Single-cluster — thinner than the rest of this section |

---

## 4. Measured expression features

Aggregate over the 69 argumentative texts (episodic excluded):

```
sentence length   mean 39.8 · median 33 · stdev 30.5 · p10 12 · p90 74
hedges/1k 5.43    boosters/1k 3.12    hedge:booster 1.74
person ref        first 20.6%  second 7.5%  third 71.9%
lexical diversity MATTR-500 0.496
top content       one, said, man, men, things, upon, himself, many, time, reason
absent            work, problem, idea, system, important, social, political
```

### 4a. Re-measurement (second pass), and how it reconciles

The corpus was re-sliced and re-measured for the `voice.md` build at Plutarch-Thoughts revision
**`7df2e10`** ("optimize content formatting for mobile reading", 2026-08-03), which reflowed
paragraphs after the first pass was run. The 78 treatise offsets recorded in `clusters/` still land
on their title strings and were reused unchanged; the segmentation is therefore identical.
Sentence-boundary detection is not, because reflow changes where line breaks fall:

| | first pass | second pass | reconciles as |
|---|---|---|---|
| words (69 argumentative) | 779,742 *(all 78)* | 678,810 *(69 only)* | different denominators, not a discrepancy |
| sentence length, mean | 39.8 | 41.5 | reflow merged some split sentences |
| hedges/1k · boosters/1k | 5.43 · 3.12 | 5.62 · 3.34 | same ordering, ±6% |
| person ref, 1st/2nd/3rd | 20.6 / 7.5 / 71.9 | 22.3 / 7.7 / 70.1 | same ordering |
| per-cluster figures | — | reproduce §4's cluster contrasts to within rounding | **the modulation findings replicate** |

The second-pass numbers are the ones `voice.md` carries, because they are the ones a reader can
re-derive from the current corpus. **Nothing in §4's table below changed direction**, which is the
material point: the findings promoted to voice rules survived a re-run against a re-formatted corpus.

Supplementary counts not produced by `style_metrics.py` — question share as a percentage of
sentences, alternative-opener rate (`Or is it / Or is he / Or was it / Or rather / Or because` per
10k words), and named-person density (capitalised tokens, non-sentence-initial, minus a function-word
stoplist) — were computed with a stdlib script over the same slices. The name-density figure is a
**proxy**, not a count of exempla: it catches place and deity names as well as persons, and it is
reported here as a comparative measure only.

### 4b. New findings from the second pass

| Finding | Evidence | Within-volume control | Status |
|---|---|---|---|
| Refutation keeps its questions; decoding suppresses them | ref 14.5% of sentences vs allegorical 1.6% | **Vol XIII, one translator: 72 → 13.3%, 74 → 17.6% vs 70 → 1.2%, 71 → 2.9%** | **Strongest expression evidence in the distillation.** Sharpens a claim the core already made |
| The *Or is it…* chain is an *Aetia* signature, not a cluster-wide one | *Aetia Romana* 37.5/10k; next-highest text in Vol IV 7.5; *De primo frigido* 0.0 | Vol IV holds translator constant | **Qualifies** the cause-hunting voice rule — recorded in `clusters/aetiological.md` |
| Essays effectively never end on a summary | **1 of 69** ends with a summary marker (*in sum / to conclude / in short, then*) | translation-robust (discourse structure, not lexis) | **New voice rule** in `voice.md` |
| Addressee named in the opening | 28 of 69 name the addressee within the first ~600 chars | translation-robust | **New voice rule**; corroborates the §7 address constraint |
| Second person peaks in *diagnosis*, not counsel | criterial 11.6% vs practical 9.5% | Vol VII and Vol I both hold | **Refines** the existing second-person finding |
| Consolation to his own household strips the exempla | *Consolatio ad uxorem* ~8 names/1k, the corpus minimum, against *De exilio* 63 and the corpus mean ~34 | Vol VII, one translator, both texts | **New register rule** in `voice.md`; single-text on the low side, so held as a register note rather than a core rule |
| Externalising the canvass collapses the interrogative rate | short school pieces 16–37% questions vs long judged dialogues 2.8% | Vol VI (30, 36, 37 short) and Vol XII (66 long) | **New modulation rule** in `clusters/dialectical.md` |

None of these was promoted into the core `SKILL.md`; the core was not reopened in this pass except
for its loading block. They live in `voice.md` and the cluster modules, which is where the expressive
system belongs under the 20% style cap.

The **absent** row is the highest-value single finding here, and it is translation-robust: he has no
abstract-systemic vocabulary at all. That negative fingerprint became a core voice rule.

### Modulation, and which patterns survived the within-volume control

| Pattern | Raw cluster contrast | Survived control? | In core |
|---|---|---|---|
| Questions densest in cause-hunting, near-absent in decoding | aet 6.02/1k vs allegorical 0.69/1k; extremes t62 17.7, t20 17.6 | **Yes** — strongest and most robust finding | ✅ |
| Second person peaks in counsel, collapses in refutation and deed-marshalling | pra 9.5% / cri 11.6% vs ref 5.6% / exe 8.8%; Vol VI clean: pra 11.6 & dia 11.5 vs ref 1.2 & exe 1.0 | **Yes** — Vol VI holds translator constant | ✅ |
| Flat assertion roughly doubles when discriminating look-alikes | cri boosters 5.59/1k vs corpus 3.12; Vol I cri 5.95 vs pra 4.22; Vol VII cri 5.46 vs pra 4.04, aet 3.01 | **Yes** in 2 of 3 testable volumes (Vol II flat) | ✅ |
| First person steady everywhere except deed-marshalling | aet 26.4% / pra 23.2% / ref 20.2% vs exe 12.3% | **Yes** | ✅ |
| Third-person dominance from exempla density | 71.9% corpus-wide | **Yes** | ✅ |
| Sentence length varies by operation | pra 47.4 vs epi 31.4 | **No** — direction reverses between volumes (Vol VI: exe longest; Vol XII: exe shortest) | ❌ discarded |
| Em-dash / parenthetical peak in refutation | ref 2.36 / 3.11 vs exe 1.06 / 0.36 | **No** — tracks Volumes XIII–XIV, i.e. the translator | ❌ discarded |

---

## 5. Fidelity results

### Cost gate — **PASS** (run pre-assembly and re-verified post-assembly)
8 of 8 high-signal divergences present in the core. Nothing logged out. This is the check that most
often fails silently and leaves a persona articulate but generic; it holds here by construction.

### Voice purity gate — **PASS**
Body checked mechanically against the ban list (`based on`, `seems to`, `tends to`, `may have`,
`the author`, `according to`, `the corpus`, …). No banned construction in the voice sections. Meta
is confined to the closing host-agent block. Body ≈ 3,600 tokens against a 5,000 budget.

### Style-match test — **PARTIAL / NOT PASSED**

Three samples generated under the core's expression rules (a cause-hunt, a contested diagnosis, a
refutation) and measured against the corresponding cluster originals. Three rounds were run, with
the expression rules revised between rounds — the loop `fidelity-tests.md` prescribes.

| Round | Change made to the rules | Mean abs. delta |
|---|---|---|
| 1 | — (initial rules) | 62% |
| 2 | Long sentences specified as *very* long; "qualifiers drop away" corrected to "flat strokes are laid **over** continuing hedging"; person rules corrected | 62% |
| 3 | **Exempla density added as an explicit rule** (2–3 named instances per page) | **43%** |

Round 3 residuals against cluster originals:

| | question/1k | hedge/1k | booster/1k | 1st % | 3rd % | sentence len |
|---|---|---|---|---|---|---|
| cause-hunt | +33% | +95% | +144% | +63% | −15% | **−1%** |
| diagnosis | +64% | −51% | +55% | **+6%** | +12% | −45% |
| refutation | +40% | −55% | −55% | +48% | **−4%** | −32% |

**What passed:** the question-rate ordering across the three registers reproduces exactly
(cause-hunt > refutation > diagnosis), and the exempla rule corrected person-reference — the
diagnosis sample went from 51.4% first-person (against 23.0% actual) to 24.5%.

**What did not:** absolute hedge and booster rates remain far off, three of four modulation
orderings do not reproduce, and generated sentences run 30–45% shorter than the originals outside
the cause-hunt register.

**Why the loop was stopped at three rounds rather than continued:** the residual gap sits almost
entirely in the feature classes §1 identifies as *translator artifacts* — sentence length,
subordination depth, and lexical hedge/booster choice. Further iteration would tune generated prose
toward the cadence of a particular 20th-century translator rather than toward Plutarch. The
translation-robust features (question density and its ordering, person reference, exempla density,
absent vocabulary) are the ones that converged, and they are the ones the core encodes.

**Read this as:** the persona reliably reproduces *what kind of sentence* he writes and *who is in
it*; it does not reproduce the period cadence of the Loeb prose, and should not be expected to.

### Style-match test, second pass (core + `voice.md`) — **NOT PASSED, but diagnosed**

The Stage 5 style-match test measures the *pair* — core expression rules plus `voice.md` — because
that pair is the sustained-prose configuration. `voice.md` did not exist when the first pass ran, so
the test was re-run against it. Three fresh samples on topics absent from the corpus (why voices drop
beside a corpse; telling gratitude from discharged obligation; against valuing a man by his
usefulness), ~600 words each.

| round | change | mean abs. delta vs cluster means |
|---|---|---|
| 1 | — (`voice.md` as first written) | 60% |
| 2 | longer sentences; exempla restored outside the cause-hunt; first person raised; second person cut in diagnosis | **50%** |

Still worse than the first pass's 43%, and the reason turned out to be a **fault in the comparator,
not only in the prose**. Re-scoring round 2 against single-text comparators of the same literary form
gave 49% for the refutation with person-reference matching to within 10% — while the cause-hunt
scored badly against *both* the cluster mean (too impersonal) and *Aetia Romana* (far too personal),
because the sample sits between two things that should never have been averaged together.

**The finding, and it is the most useful thing this pass produced:**

| axis | first-person range | question share range |
|---|---|---|
| **literary form** (query / treatise / dialogue / letter) | **3.2% → 30.2%** | **6.8% → 41.0%** |
| operation (the seven clusters) | 12.3% → 26.4% | 1.6% → 14.8% |

Form dominates. A cluster mean averages a bare antiquarian query (first person 3.2%, questions 41%
of sentences) with a staged dialogue (30.2%, 7.5%) and calls the result "the cause-hunting register".
It is not a register; it is a blend of two that never co-occur. This is very likely why the first
pass also stalled — at 43%, with the same three-of-four modulation orderings failing to reproduce.

Acted on rather than merely logged: `voice.md` now carries a **form table** as the primary anchor,
the operation table demoted to a modifier, and single-text anchors for the three commonest tasks.
The loop was stopped at two rounds because further iteration would tune token counts (`never`,
`must`, `rather`, `may` are what move hedge and booster rates at 600 words) rather than prose, and
because 600-word samples cannot stably estimate rates the originals compute over 5k–100k words.

**Read this as:** the persona reproduces *what kind of sentence* he writes, *who is in it*, and the
ordering of question density across registers; it does not hit absolute lexical rates, and the
measurement instrument is too noisy at generation length to say whether that is the persona's fault
or the test's. Anyone re-running this should compare against a single named text, not a cluster.

### Projection check — **RUN, BUT NOT BLINDED. Do not read as a fidelity score.**

Eight treatises whose content had not been read during distillation (located by title-string only)
were used as a masked set, with predictions committed in writing before the texts were opened, plus
one structural probe. Scored 2 / 1 / 0.

| Probe | Predicted | Outcome | Score |
|---|---|---|---|
| 41 *De vitioso pudore* — is compliancy cured by resolve? | No; the maxim is unavailable at the moment of the ask | Confirmed — Creon "expressed a maxim for others to use, but succumbed to pressure himself" | 2 |
| 43 *De se ipsum laudando* — is self-praise permissible? | Yes, occasion by occasion, incl. when wronged | Confirmed — "even more permissible for a statesman when wronged" | 2 |
| 53 *Ad principem ineruditum* — source of legitimacy? | Reason within the ruler, via a divine-image relation | Right stance; the image relation runs ruler↔God, not law↔reason as predicted | 1 |
| 57 *De vitando aere alieno* — borrowing to relieve poverty? | No exception; sell instead; attacks the debtor's self-deception | Confirmed — "ashamed to accept a price, but not ashamed to pay interest on what is their own" | 2 |
| 34 *De fraterno amore* — should the abler brother defer? | Yes, yield precedence voluntarily | Confirmed (Polydeuces, the deferred candidature); the "costs little" qualifier was wrong | 2 |
| 39 *De curiositate* — cured by argument? | No; averting practice and redirected appetite | Appetite-misdirection framing confirmed; therapy-by-practice not evidenced in retrieved passages | 1 |
| 47 *De exilio* — is exile an evil? | Not in itself; opinion makes it so; redescription | Confirmed — "wholly and entirely a figment of unfounded opinion" | 2 |
| 42 *De invidia et odio* — can one envy a bad man? | No; hatred takes the vicious, envy the fortunate | Confirmed — "to attract envy all that is required is apparent prosperity" | 2 |
| P9 — does he usually settle on one cause? | No; ranked and left open | Direction supported (366 question marks, 98 explicit alternative-openers in *Aetia Romana*); verdict rate not cleanly measured | 1 |

**15 / 18 = 0.83.** This number is reported for completeness and should be **discounted heavily**.
The operator holds prior knowledge of Plutarch from outside this corpus and cannot self-blind, so
the masking is partial: it withheld the session's reading, not the operator's background. Treat 0.83
as an upper bound and as an internal-consistency check, not as evidence the regularities generalize.
A valid projection score requires a second party who has not read Plutarch to run the predictions
from `SKILL.md` alone. **That test has not been run.**

---

## 6. Where to trust this persona less

1. **Anything requiring the biographer.** The *Lives* are absent. Comparative judgment of characters
   — the operation most readers associate with Plutarch — rests on 5 texts and 4.8% of the corpus.
   This is the single largest gap, and the fix is a fold-in, not a rewrite.
2. **Prose cadence.** Per the style test, the persona does not reproduce Loeb sentence rhythm, and
   the corpus cannot teach it to, because that rhythm is the translators'.
3. **Generalization is unverified.** See the projection caveat immediately above.
4. **Single-cluster elements.** "Let a guest's poorer answer stand" rests on Table-Talk alone; it is
   attested but not corroborated across independent clusters, unlike everything else in the core.
5. **The two contested mappings.** *De esu carnium* (filed refutative) and the
   *De animae procreatione* pair (filed allegorical) are the assignments most likely to be wrong;
   both are argued in their cluster files' boundary notes.
6. **Anything outside the corpus.** The frame is time-independent; the facts are not. Specific
   factual claims beyond the *Moralia* are outside what this distillation can support.
7. **`voice.md`'s numbers, at short length.** The measured baseline is sound over the whole corpus and
   reproduces across two independent runs. It is *not* a reliable target for a passage of a few
   hundred words, where a handful of tokens moves a per-1k rate by half. Use the form table and the
   single-text anchors; treat the aggregate as orientation.
8. **The register table's operation rows.** They mix literary forms and are therefore softer than
   they look. The form rows are the hard ones. This is stated in `voice.md` itself, but it is the
   likeliest place a reader will over-trust a number.
9. **The name-density figures.** A capitalised-token proxy, not a count of exempla. It catches
   Delphi and Isis alongside Lycurgus. Comparisons between texts are meaningful; the absolute figure
   is not.

### What this second pass changed, and what it did not

Changed: `references/voice.md` written (new); the seven `clusters/*.md` deepened from classification
tables to worked modules carrying attested specimens and per-cluster register data; `SKILL.md`'s
loading block extended to route to `voice.md`; this file extended with §4a, §4b, and the second-pass
style-match result.

**Not changed: the core `SKILL.md`'s voice sections, its refusals, and its operative moves, and the
cluster *assignments*.** No treatise moved between clusters, no cluster was added or removed, and the
78-text mapping is byte-identical in its verdicts. The cost gate and the voice-purity gate were not
re-run because the material they govern was not reopened.

## 7. Third pass — the cluster modules sized to a computed budget

The second pass turned the seven `clusters/*.md` files from classification tables into worked
modules, but sized them by hand. This pass sized them with `scripts/cluster_budget.py` from
persona-distiller and extended each to the number, distilling the additional material from the same
corpus at the same revision (`7df2e10`). The 78 treatise offsets were re-parsed out of the cluster
tables and re-sliced by the §7 procedure below; all 78 slices open on their title strings, so the
segmentation is byte-identical to both earlier passes.

### Inputs to the formula, and how they were counted

`words_firsthand` = 779,742 (all 78 treatises); `n_siblings` = 6 throughout, since every cluster gets
a module. The two class counts follow `scoring.md`'s counting table, with one stated adaptation:
`frameworks.md` has no cluster column, because each of its seven sections *is* a cluster, so
`n_apparatus` was read as the named machinery of that section — object type, the procedure's named
constraints, the termination condition, plus any named construct whose home is the cluster's own
module. **Failure modes were deliberately excluded from the count**; they are the operation's failure
conditions rather than constructs, and including them pushed three clusters to the `n_apparatus` cap
and raised a spurious RECUT flag.

| cluster | app | mov | apl | frg | words | supply = budget | realised | Δ |
|---|---|---|---|---|---|---|---|---|
| aetiological | 8 | 9 | 7 | 24 | 201,959 | 3,819 | 3,940 | +3.2% |
| practical-syllogism | 8 | 10 | 8 | 24 | 168,397 | 3,976 | 4,022 | +1.2% |
| refutative | 9 | 9 | 7 | 20 | 96,796 | 3,726 | 3,700 | −0.7% |
| dialectical | 8 | 9 | 6 | 20 | 84,533 | 3,542 | 3,681 | +3.9% |
| criterial | 10 | 7 | 6 | 16 | 43,654 | 3,385 | 3,488 | +3.0% |
| allegorical | 7 | 7 | 5 | 16 | 46,140 | 3,032 | 3,073 | +1.4% |
| exemplary | 7 | 7 | 5 | 14 | 37,323 | 2,963 | 3,049 | +2.9% |

No FLOOR flag (every cluster earned its module) and no RECUT flag (`n_apparatus` and `n_moves` both
stayed under 12 everywhere, so no cluster is carrying two registers). Realised sizes are `cl100k_base`
counts, all within the script's own stated calibration error of 3.8% mean / 6.0% max. Starting sizes
were 2,309–3,868 tokens; the pass added **5,687 tokens** across the seven, and the package's
`clusters/` total went 19,266 → 24,953.

**Runtime load, which is the figure that matters rather than package size** — modules load one at a
time, two on a close secondary ranking:

```
loaded_worst_case = core (4,000) + 2 × max module (4,022) + voice.md (4,970) + frameworks.md (3,058)
                  = 20,072 tokens
```

### What the added material is, and where it came from

Each module was extended with attested specimens from its own members that earlier passes had listed
but never worked. Nothing was imported from outside the cluster, and no cluster assignment changed.

| cluster | texts newly worked |
|---|---|
| refutative | 73 (the fiction-licence baseline for the preanalytic test), 75 and 76 (the quotation rule stated as a rule of engagement; the reviling and delegated-anger constraints; the charge turned back on Colotes via Democritus) |
| criterial | 41 (the continuum case), 5 (the self-directed case and the endpoint-criterion reduction), 7 (the mark drawn from scarcity) |
| dialectical | 50 (cross-cut advocacy), 23 (symmetric accusations; the priority argument), 69 (the canvass run on a text), 45 (disambiguation as the bounding instrument) |
| allegorical | 70 / 71 (rival keys refused on *capacity* rather than piety; the piety constraint relocated into the doctrine) |
| exemplary | 59 (the shared rubric; decorum of assignment; the two-audience test) |
| aetiological | 62 (each candidate must bring its own checkable phenomenon), 28 (the datum conceded at its most damaging) |
| practical-syllogism | 6 (the address constraint fitted to one reader's shelf) |

### Three findings that qualify earlier verdicts rather than confirming them

1. **71 is partly report, not performance.** Its opening sections are third-person *about* the
   treatise (*the treatise… reports*, *he asserts*, *he says that Posidonius*), which is the
   strongest case anyone will make for demoting it to `episodic.md`. The verdict stands because the
   body abandons that frame and decodes directly — but §6's flag on the *De animae procreatione*
   pair is now sharper, not softer, and the qualification is recorded in the module itself.
2. **59 is reported speech throughout**, so what survives is the skeleton of the comparison and not
   its prose. It should not be used as a register sample for `exemplary.md`, and the module now says
   so. This slightly weakens the cluster's already-thinnest register figures, which rest on 5 texts.
3. **"Let a guest's poorer answer stand" gained a second text, not a second cluster.** 28's guides
   fall silent and are covered rather than corrected, exactly as at table in 49. Both sit in
   `aetiological`, so the ≥2-independent-clusters bar is still unmet and §6's caveat 4 stands
   unchanged.

**Not changed by this pass:** the core `SKILL.md` (untouched), `voice.md`, `frameworks.md`,
`episodic.md`, the cluster assignments, the 78-text mapping, and every fidelity result in §5. The
cost gate and voice-purity gate were not re-run because the material they govern was not reopened.
The style-match caveat in §6 caveat 2 applies to the new prose exactly as it does to the old.

## 8. Reproducing this

Boundary detection, slicing, and metrics were run from the corpus with stdlib-only scripts
(`style_metrics.py` from persona-distiller). Intermediate artifacts — the sliced corpus, per-file
metrics, and the committed predictions — were kept outside version control by design; this
repository holds no substantial portion of the source text. Re-running requires a local checkout of
Plutarch-Thoughts and reproduces the treatise offsets recorded in `clusters/`.

**Second-pass procedure**, which is the one to follow:

1. Clone Plutarch-Thoughts and check out the revision named in `voice.md`'s baseline block
   (`7df2e10`) or later.
2. Parse the `Vol · offset` column out of every table in `clusters/*.md` and `episodic.md` — 78 rows,
   no duplicates. Group by volume, sort by offset, and slice each treatise from its own offset to the
   next offset in the same volume, the last running to end-of-file. Verify by checking that each
   slice opens on its title string.
3. Run `style_metrics.py` over the 69 argumentative slices, then per cluster, then per form group
   (the form groups are listed in `voice.md`), then per individual text for the anchors.
4. Supplementary counts — question share as a percentage of sentences, alternative-opener rate,
   named-person proxy — are plain regex counts over the same slices; the definitions are in §4a.

The offsets are the only thing in this repository that binds it to the corpus, and they are what
makes the whole measurement chain reproducible without reproducing the text.
