# BYRSA — read-only fork provenance

This fork is **read-only** for the BYRSA workspace. No code in this repository
is modified; this file is the entire diff.

The BYRSA workspace forks five repositories on the instruction to *"pin the
version, mine one idea each"*. This records the pin and the idea, so a later
session can tell what was borrowed and check it against the source.

| | |
|---|---|
| **Pinned commit** | `edc75b4e8c9162d0679d4d03a1a5837396273734` (`edc75b4`, 2021-04-20) |
| **Idea mined** | **Declarative parameterised strategies.** Sweep a parameter; do not hand-write forty bots. Dominiate expresses a strategy as data rather than code, which is what makes a parameter sweep a first-class experiment instead of forty near-duplicate files. |
| **Where it landed** | `BeliefBot(p)`, `DeferBot(r)`, `SuitBot(s)`, `EnvoyBot(r)` — each takes its parameter in the constructor and exposes it in `.name` so it reaches the result file's provenance block. `byrsa-sim/scenarios/E-03.yaml` sweeps p across 21 values from one line of YAML |
| **Cited in** | `01` §5 |

## Why pinning matters

A borrowed idea that drifts with upstream is an unrecorded dependency. The BYRSA
corpus requires every finding to carry a git SHA and seed range; a technique
borrowed from a moving target would break that chain. This fork is not tracked
for updates — if the idea needs revisiting, it is revisited against **this**
commit.

## What was NOT taken

No rule from any bundled game, ever. BYRSA's rules live in exactly one place:
A2 of the corpus, implemented by `byrsa-sim/byrsa_sim/rules.py`. What is
borrowed here is *methodology* — how to structure a bot roster, how to shape a
report, how to parameterise a strategy — never a mechanic.
